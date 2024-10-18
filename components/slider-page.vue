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









<!-- <template>
  <div class="md:flex md:justify-center md:items-center w-12/12 container">
    <swiper autoplay :pagination="true" :modules="modules" >
        <swiper-slide><page-one/></swiper-slide>
        <swiper-slide><page-two/></swiper-slide>
        <swiper-slide><page-three/></swiper-slide>
        <swiper-slide><page-four/></swiper-slide>
        <swiper-slide><page-five/></swiper-slide>
        <swiper-slide><page-six/></swiper-slide>
    </swiper>
  </div>
</template> -->

<!-- <script>
export default {
  components: {
      Swiper,
      SwiperSlide,
    },
    
    setup() {
      return {
        modules: [Pagination, Autoplay],
      };
    },
};

  // Import Swiper Vue.js components
  import { Swiper, SwiperSlide } from 'swiper/vue';

  // Import Swiper styles
  import 'swiper/css';

  import 'swiper/css/pagination';

  // import required modules
  import { Pagination, Autoplay } from 'swiper';
</script> -->