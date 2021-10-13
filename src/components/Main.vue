<template>
    <main>
        <Home :sections="sections"/>
        <Services :serviceList="serviceList"/>
        <About :companyValues="companyValues"/>
        <Projects :companyProjects="companyProjects"/>
    </main>
</template>

<script>
import Home from '../components/Home.vue';
import Services from '../components/Services.vue';
import About from '../components/About.vue'
import Projects from '../components/Projects.vue'

export default {
    name: 'Main',
    components: {
        Home,
        Services,
        About,
        Projects
    },
    props: ['sections', 'serviceList', 'companyValues', 'companyProjects']
}
</script>

<style scoped lang="scss">

</style>