<template>
    <div class="wrapper place-items-center" data-aos="fade-up">
        <div class="w-full grid gap-3">
        <div>
           <h2 class="header">TAAS - Tax Automation and Administration Solution System (Imo State)</h2>
        </div>

        <div>
            <h2 class="font-light">
               Front-End Developer and UI/UX Designer (2022)
            </h2>
        </div>
        </div>

        <div class="project-img bg-[url('/taas.png')]">
            <div class="projectBtn-group group">
                <div class="projectBtn-wrapper">
                    <NuxtLink to="taas-page"><button class="projectBtn mt-5 items-center inline-flex">Read more</button></NuxtLink>
                </div>
            </div>
        </div>
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
  