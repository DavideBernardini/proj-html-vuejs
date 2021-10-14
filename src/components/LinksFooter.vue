<template>
    <div class="links">
        <h4>
            {{group.title}}
        </h4>
        <ul>
            <li v-for="(link, index) in group.links"
            :key="index">
                <a :href="group.action">
                    <i class="fas fa-angle-right pe-3"></i>
                    <span>{{link}}</span> 
                </a>
            </li>
        </ul>
    </div>
</template>

<script>

export default {
    name: 'LinksFooter',
    props: ['group']
}
</script>

<style scoped lang="scss">
@import '../assets/style/variables.scss';
@import '../assets/style/mixins.scss';

</style>