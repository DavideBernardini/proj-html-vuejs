<template>
    <main>
        <Home :sections="sections"/>
        <Services :serviceList="serviceList"/>
        <About :companyValues="companyValues"/>
        <Projects :companyProjects="companyProjects"/>
        <Results :results="results" :technologiesLogo="technologiesLogo"/>
        <Support :contacts="contacts"/>
    </main>
</template>

<script>
import Home from '../components/Home.vue';
import Services from '../components/Services.vue';
import About from '../components/About.vue';
import Projects from '../components/Projects.vue';
import Results from '../components/Results.vue';
import Support from '../components/Support.vue';

export default {
    name: 'Main',
    components: {
        Home,
        Services,
        About,
        Projects,
        Results,
        Support
    },
    props: [
        'sections',
        'serviceList',
        'companyValues',
        'companyProjects',
        'results',
        'technologiesLogo',
        'contacts'
    ]
}
</script>

<style scoped lang="scss">

</style>