<template>
    <div class="wrapper place-items-center" data-aos="fade-up">
        
        <div class="w-full grid gap-3">
        <div>
           <h2 class="header">LuxeTimes - Personal Entertainment Blog</h2>
        </div>

        <div>
            <h2 class="font-light">
               Front-End Developer (2023)
            </h2>
        </div>
        </div>

        <div class="project-img bg-[url('/luxetimes.png')]">
            <div class="projectBtn-group group">
                <div class="projectBtn-wrapper">
                    <button @click="openModal" class="projectBtn mt-5 items-center inline-flex">Read more</button>
                </div>
            </div>
        </div>

        <!-- Modal Pop-up (fades in and out) -->
      <Transition name="nested" :duration="1000">
        <div
          v-if="showModal"
          class="outer pop-up-outer"
          @click.self="closeModal"
        >
          <div class="inner pop-up-inner">
            <div class="bg-gray-300 w-full h-3/5 gridCenter"></div>
            <h2 class="header mb-4 mt-6">LuxeTimes</h2>
            <p class="text-gray-700 mb-6">
                LuxeTimes a fully responsive and visually captivating Luxury & Entertainment Blog using Vue.js and TailwindCSS. This blog is designed to cater to high-end audiences with a focus on luxury lifestyles, entertainment, and exclusive events, blending performance and aesthetic appeal for an engaging user experience.
            </p>

            <h2 class="sub-header mt-6 mb-4">Objectives</h2>
            <p>
                <b>1.Deliver a Premium User Experience: </b>Create a sleek and intuitive interface that reflects the exclusivity and sophistication of the luxury and entertainment industry.
                <br><br>
                <b>2.Responsive Design: </b>Ensure seamless functionality across all devices, from mobile to desktop, providing users with a smooth, consistent experience regardless of screen size.
                <br> <br>
                <b>3.Improve Content Accessibility: </b>Implement an efficient content management structure for easy updates and navigation, ensuring users can access content quickly and effortlessly.
                <br> <br>
                <b>4.Engage Users with Interactivity: </b>Enhance user engagement through interactive features, including hover effects, animations, and a dynamic content search system.
                <br> <br>
            </p>

            <h2 class="sub-header mt-6 mb-4">Key Features</h2>
            <p>
                <b>1.Dynamic Content Management: </b>Used Vue.js to develop a modular architecture for flexible, reusable components that facilitate seamless content updates.
                <br><br>
                <b>2.Responsive Design: </b>Leveraged TailwindCSS to create a responsive layout that delivers a polished and consistent experience on all devices.
                <br> <br>
                <b>3.Interactive Elements: </b>Integrated smooth transitions and animations to engage users, providing a more immersive experience.
                <br> <br>
                <b>4.Search and Filter Functionality: </b>Implemented a custom search and filter system for users to easily navigate and find specific blog posts by category or keyword.
                <br> <br>
                <b>4.Optimized Performance: </b>Ensured fast load times and smooth performance through the efficient state management capabilities of Vue.js.
                <br> <br>
            </p>

            <h2 class="sub-header mt-6 mb-4">Technologies</h2>
            <p>Figma, Vue.js, Nuxt, Tailwind css, Git and GitLab.</p>
          </div>
        </div>
      </Transition>
      </div>
</template>


<script>
  export default {
    data() {
      return {
        showModal: false,
      };
    },
    methods: {
      openModal() {
        this.showModal = true;
      },
      closeModal() {
        this.showModal = false;
      },
    },
  };
  </script>
  
  <style>
    .nested-enter-active, .nested-leave-active {
    	transition: all 1s ease-in-out;
    }
    /* delay leave of parent element */
    .nested-leave-active {
      transition-delay: 0.5s;
    }
    
    .nested-enter-from,
    .nested-leave-to {
      transform: translateY(30px);
      opacity: 0;
    }
    
    /* we can also transition nested elements using nested selectors */
    .nested-enter-active .inner,
    .nested-leave-active .inner { 
      transition: all 0.5s ease-in-out;
    }
    /* delay enter of nested element */
    .nested-enter-active .inner {
    	transition-delay: 0.5s;
    }
    
    .nested-enter-from .inner,
    .nested-leave-to .inner {
      transform: translateX(30px);
      /*
      	Hack around a Chrome 96 bug in handling nested opacity transitions.
        This is not needed in other browsers or Chrome 99+ where the bug
        has been fixed.
      */
      opacity: 0.001;
    }
  </style>
  