<template>
    <main>
        <Home :sections="sections"/>
        <Services :serviceList="serviceList"/>
        <About :companyValues="companyValues"/>
    </main>
</template>

<script>
import Home from '../components/Home.vue';
import Services from '../components/Services.vue';
import About from '../components/About.vue'

export default {
    name: 'Main',
    components: {
        Home,
        Services,
        About
    },
    props: ['sections', 'serviceList', 'companyValues']
}
</script>

<style scoped lang="scss">

</style>