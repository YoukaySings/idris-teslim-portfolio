<template>
    <div class="h-auto py-[100px] grid grid-rows-5 gap-10">
        <!-- section card -->
        <div class="gridCenter">
            <div class="section-card">
                <h2 class="header" data-aos="fade-right">I've worked on...</h2>
                <p data-aos="fade-left">I have experience working on SPAs and collaborating with a large team on large and complex projects</p>
            </div>
            <div class="section-card-img bg-[url('https://img.freepik.com/free-photo/programer-coding-laptop-sitting-down-desk-with-computer-screens-parsing-code-software-agency-software-developer-compiling-algorithms-with-cloud-programers-working-background_482257-43993.jpg?t=st=1729116935~exp=1729120535~hmac=7498b165f9972c6611f52e7ba8f612d5a132c8f60e986c6133140605019a4c2e&w=996')]">
            </div>
        </div>
        <!-- section card -->
           <taas/>
           <maxcoach/>
           <luxetimes-blog/>
           <portfolio/>
    </div>
</template>

<script>
import taas from './projects/taas.vue';
import maxcoach from './projects/maxcoach.vue';
import luxetimesBlog from './projects/luxetimes-blog.vue';
import portfolio from './projects/portfolio.vue';
export default {
    components: {taas, maxcoach, luxetimesBlog, portfolio}
}
</script>
