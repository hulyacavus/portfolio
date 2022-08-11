<template>
  <div>
    <h1 class="text-center text-gray-800 dark:text-gray-300 pb-20 text-5xl font-extrabold">
      {{$t('iwork')}}
    </h1>
    <carousel
      :perPageCustom="[[320, 1],[900, 3], [1199, 4]]"
      :mouse-drag="true"
      :autoplay="true"
      :paginationSize="0"
      :loop="true"
      :speed="800"
      :autoplayTimeout="3000"
      :autoplayHoverPause="false"
    >
      <slide v-for="(skill, index) in skills" :key="index">
        <div class="rounded-full flex flex-col items-center justify-center bg-white dark:bg-gray-700 p-8 w-48 h-48 lg:w-52 lg:h-52 mx-6 space-y-6">
          <img class="w-1/2" :src="skill.image" />
          <h1 class="text-base dark:text-gray-300">{{ skill.name }}</h1>
        </div>
      </slide>
    </carousel>
  </div>
</template>


<script>
import { Carousel, Slide } from 'vue-carousel'

export default {
    name:'Skills',
    components: { Carousel, Slide },
    data(){
        return{
            skills: [
                {name: 'Python', image: require("../assets/images/skills/python.png")},
                { name: "JavaScript", image: require("../assets/images/skills/javascript.png")},
                { name: "HTML", image: require("../assets/images/skills/html.png")},
                { name: "CSS", image: require("../assets/images/skills/css.png")},

                { name: "Vue JS", image: require("../assets/images/skills/vue.png")},
                { name: "React JS", image: require("../assets/images/skills/reactjs.png")},
                { name: "Bootstrap", image: require("../assets/images/skills/bootstrap.png")},
                { name: "Tailwind CSS", image: require("../assets/images/skills/tailwind.png")},

                { name: "Git", image: require("../assets/images/skills/git.png")},

            ],
        }
    }
};
</script>
