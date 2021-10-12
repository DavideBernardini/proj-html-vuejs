<template>
    <main>
        <Home :sections="sections"/>
        <Services :serviceList="serviceList"/>
    </main>
</template>

<script>
import Home from '../components/Home.vue';
import Services from '../components/Services.vue'

export default {
    name: 'Main',
    components: {
        Home,
        Services
    },
    props: ['sections', 'serviceList']
}
</script>

<style scoped lang="scss">

</style>