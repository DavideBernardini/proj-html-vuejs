<template>
    <div>
        <div class="icons mb-1">
            <img :src="require(`../assets/images/svgs/${service.icon}`)" :alt="`icon for ${service.icon}`">
            <a href="#">
                <i class="fas fa-arrow-right"></i>
            </a>
        </div>
        <h4 class="fw-bold py-4">
            {{service.name}}
        </h4>
        <p>
            {{service.info}}
        </p>
    </div>
</template>

<script>


export default {
    name: 'ServiceCard',
    props: ['service']
}
</script>

<style scoped lang="scss">

</style>