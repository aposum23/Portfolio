<template>
  <div class="carousel-comp">
    <!--
    <svg>
      <path d="M30,0 5,100, 30,200" stroke="#fff" stroke-width="3" fill="none"/>
    </svg>
    -->
    <div class="carousel-cards">
      <div class="carousel-card" v-for="elem in skills" :key="elem.id">
        <img :src="require(`@/assets/${elem.image}`)"/>
        <h3>{{elem.skill}}</h3>
      </div>
    </div>
    <!--
    <svg>
      <path d="M20,0 45,100, 20,200" stroke="#fff" stroke-width="3" fill="none"/>
    </svg>
    -->
  </div>
</template>

<script>
export default {
  name: 'CarouselComp',
  data () {
    return {
      skills: [{ id: 1, skill: 'HTML5', image: 'html.svg' }, { id: 2, skill: 'CSS3', image: 'css.svg' }, { id: 3, skill: 'JavaScript', image: 'js.svg' }, { id: 4, skill: 'Vue 2-3', image: 'vue.svg' }, { id: 5, skill: 'SCSS/SASS', image: 'sass.svg' }, { id: 6, skill: 'Git', image: 'git.svg' }, { id: 7, skill: 'Axios.js', image: 'axios.svg' }, { id: 8, skill: 'Docker', image: 'docker.svg' }, { id: 9, skill: 'Bootstrap 4-5', image: 'bootstrap.svg' }]
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
svg {
  height: 200px;
  width: 50px;
  display: inline-flex;
  margin: 0px 20px;
}

.carousel-comp {
  margin-top: 50px;
  text-align: center;
}
.carousel-cards {
  overflow: hidden;
  display: inline-flex;
  width: 750px;
}

@keyframes carousel-anim {
  0%{
    left: 0;
  }
  15%{
    left: 0;
  }
  30%{
    left: -750px;
  }
  45%{
    left: -750px;
  }
  60%{
    left: -1500px;
  }
  75%{
    left: -1500px;
  }
  100%{
    left: 0;
  }
}

.carousel-card {
  text-align: center;
  width: 250px;
  height: 300px;
  animation: carousel-anim 10s ease;
  animation-iteration-count: infinite;
  position:relative;

  & h3 {
    margin: 20px 0px 0px 0px;
    width: 250px;
  }

  & img {
    width: 200px;
    height: 200px;
  }
}
</style>
