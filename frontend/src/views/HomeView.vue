<template>
  <div id="first-block">
    <div class="logo">
      <img src="@/assets/DSD-Modern.png"/>
    </div>
    <div class="present">
      <div class="title">
        <h1>FRONT-END DEVELOPER</h1>
        <h3 class="typed-text text header">Hello, world! I'm Mikhail Duhno and it's my portfolio</h3>
      </div>
      <LightningComp class="lightning"/>
    </div>
  </div>
  <div id="second-block">
    <LightningComp class="second-lightning"/>
    <div class="second-text">
      <h3 class="header">About me</h3>
      <p>I'm 20 years old. I styding in North Caucasus Federal university. Since 2021 I'm styding front-end develop. In this gap of time was made some projects with such technologies as Vue, REST API and so on. My final point is become high level front-end developer</p>
    </div>
  </div>
  <div id="third-block">
    <h3 class="header">My skills</h3>
    <CarouselComp/>
  </div>
</template>

<script>
import LightningComp from '@/components/LIghtningComp.vue'
import CarouselComp from '@/components/CarouselComp.vue'

export default {
  name: 'App',
  components: {
    LightningComp,
    CarouselComp
  }
}
</script>

<style lang="scss">
body {
  background-color: #2C2F36;
  overflow-x:hidden;
}

h1 {
  font-size: 100px;
  width: 10em;
  text-align: left;
  margin: 0px 0px 23px 0px;
}

h3 {
  color: #53A620;
  font-size: 25px;
}

.header {
  width: 25em;
  margin: 23px 0px 0px 0px;
}

.title {
  height: 500px;
  width: 50%;
  margin: 3em 0em 0em 9em;
}

.text{
  position:relative;
  white-space: nowrap;
  width:25em;
  border-right: 4px solid rgba(255,255,255,.75);
  overflow: hidden;
  transform: translateY(-50%);
}

.typed-text {
  animation: typewriter 5s steps(54) 1s normal both, blinkTextCursor 500ms steps(44) infinite normal;
}

@keyframes typewriter{
  from{width: 0;}
  to{width: 25em;}
}

@keyframes blinkTextCursor{
  from{border-right-color: rgba(255,255,255,.75);}
  to{border-right-color: transparent;}
}

.present {
  display:inline-flex;
  padding-bottom: 10em;
}
.logo {
  text-align: right;
  margin-bottom: 200px;
  & img{
    width: 10em;
    margin: 1em;
  };
}

#second-block {
  display:inline-flex;

  .second-lightning {
    margin-left: -5em;
    transform: scale(-1, 1);
  }
}

.second-text {
  width: 20%;
  margin: 4em 15em 0px auto;
  & p {
    font-size: 20px;
    text-align: right;
  };

  & h3 {
    width: 100%;
    text-align: right;
  }
}

#third-block {
  .header {
    margin-left: 5em;
  }
}
</style>
