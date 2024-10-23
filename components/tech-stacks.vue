<template>
    <div class="h-auto gridCenter mb-[100px] md:mb-[140px]">
        <!-- section card -->
        <div class="gridCenter mb-10">
            <div class="section-card">
                <h2 class="header" data-aos="fade-right">Tech Stacks...</h2>
                <p data-aos="fade-left">"At the heart of any powerful digital product lies a carefully tech stack - 
                    a blend of cutting-edge languages, frameworks, and tools that bring an idea to life"</p>
            </div>             
            <div class="section-card-img bg-[url('https://images.unsplash.com/photo-1498050108023-c5249f4df085?q=80&w=1472&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D')]"></div>
        </div>
        <!-- section card -->
        <div class="h-full flex flex-col justify-between gap-4">
            <div class="card">
                <p data-aos="fade-right">html, css, javascript, vue.js, store, nuxt, vuex, tailwindcss, bootstrap, vuetify, git &amp; github, gitlab</p>
                <h2 class="circle relative flex items-end" data-aos="fade-left">web development</h2>
            </div>
            <br>
            <div class="card">
                <p data-aos="fade-right">dialogue flows &amp; prototyping, UX Writing, user research, user interviews, wireframing, figma, figjam, adobe xd, webflow, sketch, agile ux design</p>
                <h2 class="circle relative flex items-end" data-aos="fade-left">ui/ux design</h2>
            </div>
            <br>
            <div class="card">
                <p data-aos="fade-right">Problem solving and Time management, Prototyping & Wireframing, Information architecture, User research, UX Writing, Visual design, Detail oriented, Visual design elements, Productivity, Adequate delivery, Great communication skills</p>
                <h2 class="circle relative flex items-end" data-aos="fade-left">Skills</h2>
            </div>
            <br>
            <div class="card">
                <p data-aos="fade-right">Html, Css, Javascript, Vue.js, Vue 2, Vue 3, Vuex, Nuxt 2, Nuxt 3, Vuetify, Tailwind css, Bootstrap, Composition API, REST API.</p>
                <h2 class="circle relative flex items-end" data-aos="fade-left">Languages</h2>
            </div>
            <br>
        </div>
    </div>
</template>

<style scoped>

.circle::after {
  content: '';
  display: block;
  width: 10px; /* Adjust size of the circle */
  height: 10px;
  background-color: #0f0905; /* Tailwind's gray-600 color */
  border-radius: 50%; /* Fully round */
  position: absolute;
  left: -6px; /* Center it relative to the border */
  bottom: -10px; /* Position it at the bottom of the div */
}

img{
    width: 50px;
    height: 50px;
}

p{
    font-size: 16px;
    font-weight: 300;
    width: 90%;
    line-height: 26px;
    word-break: break-all;
}

@media (min-width: 768px) {
    img {
        width: 100px;
        height: 100px;
    }
}

@media (max-width: 768px) {
    p {
        width: 100%;
        font-size: 16px;
    }
}
</style>