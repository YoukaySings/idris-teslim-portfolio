<template>
    <div class="wrapper place-items-center" data-aos="fade-up">
        <div class="w-full grid gap-3">
        <div>
           <h2 class="header">Maxcoach Educational Website</h2>
        </div>

        <div>
            <h2 class="font-light">
               Front-End Developer and UX Writer (2023)
            </h2>
        </div>
        </div>

        <div class="project-img bg-[url('/maxcoach.png')]">
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
            <h2 class="header mt-6 mb-4">Maxcoach Educational/Learning Website</h2>
            <p>
                Maxcoach is an educational and learning platform designed to offer a variety of online courses and training programs. Maxcoach is a Learner-Centric Online Education System Powered by Learn Press plugin and Elementor editor, MaxCoach makes it easier to create rich lesson content, organize courses, manage learners' data and privacy.
                <br><br>
                It provides a user-friendly interface that connects learners with instructors, enabling users to access diverse educational resources, from professional development to personal growth. Maxcoach focuses on delivering high-quality, interactive learning experiences, making education accessible to individuals seeking to enhance their skills or knowledge across various disciplines.
            </p>

            <h2 class="sub-header mt-6 mb-4">Problems to solve</h2>
            <p>
                Maxcoach's existing website was built using React, but the platform had become increasingly difficult to maintain and scale efficiently. Performance issues arose, particularly as new features were added, resulting in slower loading times and a less responsive user experience. The complexity of managing state, reusable components, and animations in React led to development bottlenecks, slowing down feature releases and creating technical debt.
            </p>

            <h2 class="sub-header mt-6 mb-4">Solution</h2>
            <p>The decision to migrate from React to Vue.js was based on the need for a more maintainable, flexible, and efficient framework. Vue.js offered a simpler learning curve, better documentation, and a more organized structure with its single-file components.
                <br><br>
               One of the key improvements was the extensive use of reusable components throughout the application. This modular approach allowed the team to break down the UI into smaller, maintainable parts that could be easily reused across different pages and features. By creating reusable components for elements like navigation bars, buttons, and form inputs, we not only reduced redundancy but also sped up development, making future updates much more efficient.
               <br><br>
               Additionally, Vue’s ecosystem of libraries, such as Vue Router for dynamic routing and Vuetify for UI design, streamlined the process of implementing consistent styling. For animations, I used Vue-Transition-Group and other Vue animation libraries to integrate seamless, performant transitions that elevated the user experience without compromising speed. These tools enabled smoother interactions and visually appealing effects while optimizing load times and responsiveness.
               <br><br>
               Overall, the shift to Vue.js resulted in a more scalable and maintainable website, offering faster performance, better user experience, and simpler ongoing development.
            </p>
            
            <h2 class="sub-header mt-6 mb-4">Participation</h2>
            <div>
                <ol class="list-disc leading-loose list-outside ml-4">
                    <li>Created reusable Nuxt components for the tabs.</li>
                    <li>Developed the  Maxcoach routing system and interfaces</li>
                    <li>Write design contents to create a seamless experience for users.</li>
                    <li>Redesigned and made design adjustments for a responsive and functional interaction across interfaces.</li>
                    <li>Developed mobile responsiveness for the application.</li>
                </ol>
            </div>

            <h2 class="sub-header mt-6 mb-4">Technologies</h2>
            <p>Vue.js, Nuxt 3, Tailwind css, font awesome icon, google fonts, Git and Github</p>

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
  