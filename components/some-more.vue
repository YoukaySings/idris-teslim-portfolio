<template>
   <div class="my-[100px] w-full h-auto">
      <div class="w-full h-auto flex flex-col justify-center items-center content-center gap-10">
         <!-- section card -->
        <div class="gridCenter">
            <div class="section-card">
                <h2 class="header" data-aos="fade-right">Some more...</h2>
                <p data-aos="fade-left">I create beautiful websites your users will love - building web content and functions that unlock business potential and increase business profit margin by 30%</p>
            </div>
            <div class="section-card-img bg-gray-300">
               <div class="w-full">
               <div class="w-full h-[500px] md:h-[300px] bg-style bg-[url('https://images.unsplash.com/photo-1483058712412-4245e9b90334?q=80&w=1470&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D')] rounded-md">
                  <div v-if="iframeSrc" class="w-full h-full transition-opacity duration-500 ease-in opacity-100">
                      <iframe :src="iframeSrc" class="w-full h-full"></iframe>
                  </div>
               </div>
           </div>
            </div>
        </div>
        <!-- section card -->

            <div class="w-full grid grid-cols-2 gap-6 uppercase">
            <!-- Calculator -->
            <div>
               <!-- <div class="w-full h-[120px] md:h-[200px] bg-gray-300 rounded-md mb-2"> -->
               <!-- </div> -->
               <a href="#" @click.prevent="openWindow('https://sunnyside-landing-page-seven-fawn.vercel.app/')" class="font-bold text-[12px] hover:text-blue-500 hover:underline">SunnySide Landing Page</a>
               <p>HTML, CSS, JS</p>
            </div>

            <!-- Calculator -->
            <div>
               <!-- <div class="w-full h-[120px] md:h-[200px] bg-gray-300 rounded-md mb-2"> -->
               <!-- </div> -->
               <a href="#" @click.prevent="openWindow('https://calculator-theta-liart.vercel.app/')" class="font-bold text-[12px] hover:text-blue-500 hover:underline">Calculator</a>
               <p>HTML, CSS, JS</p>
            </div>

            <!-- Calculator -->
            <div>
               <!-- <div class="w-full h-[120px] md:h-[200px] bg-gray-300 rounded-md mb-2"> -->
               <!-- </div> -->
               <a href="#" @click.prevent="openWindow('https://to-do-list-chi-ebon.vercel.app/')" class="font-bold text-[12px] hover:text-blue-500 hover:underline">To-Do List</a>
               <p>HTML, CSS, JS</p>
            </div>

            <!-- Calculator -->
            <div>
               <!-- <div class="w-full h-[120px] md:h-[200px] bg-gray-300 rounded-md mb-2"> -->
               <!-- </div> -->
               <a href="#" @click.prevent="openWindow('https://login-sign-up-page-three.vercel.app/')" class="font-bold text-[12px] hover:text-blue-500 hover:underline">Simple Sign in & Sign up page</a>
               <p>Vue.js, Tailwind CSS</p>
            </div>
            
            </div>
      </div>
   </div>
</template>

<script>
export default {
  data() {
    return {
      iframeSrc: ''  // Holds the URL of the webpage to display
    };
  },
  methods: {
    openWindow(url) {
      this.iframeSrc = url;  // Set the iframe source to the clicked URL
    }
  }
};
</script>