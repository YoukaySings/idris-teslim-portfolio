<template>
    <div class="h-screen w-12/12 bg-black text-white/30 border-none" data-aos="fade-up">     
        <img src="https://images.unsplash.com/photo-1497005367839-6e852de72767?q=80&w=1467&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D" class="w-full h-screen">
    
        <div class="absolute top-0 left-0 bg-black/90 inset-0 text-white/80 text-lg">
            <!-- <p class=""> -->
                  <!-- Chat Bubble -->
                  <div class="absolute top-[30%] right-4 md:right-10 max-w-xs p-4 bg-purple-700 text-white font-bold text-[20px] rounded-lg shadow-md animate-heartbeat">
                    <!-- Chat Bubble Content -->
                    <h4>
                        Hello! I develop reusable code and create functional websites designed to deliver effective, user-friendly and solution-oriented experiences.
                    </h4>
              
                    <!-- Tail of the Chat Bubble -->
                    <div class="absolute bottom-0 right-4 w-4 h-4 bg-purple-700 transform rotate-45 translate-y-1/2"></div>
                  </div>

                  <h2 class="absolute bottom-0 left-0 text-[100px] md:text-[200px] text-white/30 leading-none font-black">idris teslim</h2>
        </div>
        <!-- <div class="relative w-full h-screen"> -->
        <!-- </div>     -->
    </div>
</template>

<style scoped>
/* Define the keyframes for the heartbeat animation */
@keyframes heartbeat {
  0%, 100% {
    transform: scale(1);
  }
  20% {
    transform: scale(1.1);
  }
  40% {
    transform: scale(0.9);
  }
  60% {
    transform: scale(1.1);
  }
  80% {
    transform: scale(0.95);
  }
}

/* Tailwind custom animation class for heartbeat */
.animate-heartbeat {
  animation: heartbeat 1.5s ease-in-out infinite;
}
</style>