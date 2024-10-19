<template>
  <!-- without slider -->
  <div class="w-12/12">
    <nav-bar />
    <landing-page />
    <div class="gridCenter">
      <div class="container">
      <view-resume />
      <projects />
      <tech-stacks />
      <my-journey />
      <some-more />
      </div>
    </div>
    <lets-work/>
  </div>
</template>

<script>
import AOS from 'aos';
import 'aos/dist/aos.css';

export default {
  mounted() {
    AOS.init(
      {
      offset: 200,
      duration: 1000,
      easing: 'ease-in-out',
      // delay: 100,
    }
    );
  },
};
</script>



<style>
@import url('https://fonts.googleapis.com/css2?family=Montserrat:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200&display=swap');
  p, h2, i, button, ul {
    font-family: 'Montserrat', sans-serif;
  }
</style>