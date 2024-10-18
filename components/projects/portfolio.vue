<template>
    <div class="wrapper place-items-center" data-aos="fade-up">
        <div class="w-full grid gap-3">
        <div>
           <h2 class="header">Idris Teslim Portfolio - Personal Website</h2>
        </div>

        <div>
            <h2 class="font-light">
               Front-End Developer (2023)
            </h2>
        </div>
        </div>

        <div class="project-img bg-[url('/portfolio.png')]">
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
            <h2 class="header mb-4 mt-6">Portfolio Website</h2>
            <p class="text-gray-700 mb-6">
              Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla convallis egestas rhoncus.
            </p>
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
  