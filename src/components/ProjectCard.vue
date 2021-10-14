<template>
    <div>
        <img class="w-100" 
        :src="require(`../assets/images/${project.image}`)" :alt="`image for ${project.title}`">
        <div class="text">
            <h4 class="fw-bold">
                {{project.title}}
            </h4>
            <p>
                {{project.paragraph}}
            </p>
        </div>
        <i class="fas fa-arrow-right"></i>
    </div>
</template>

<script>
export default {
    name: 'ProjectCard',
    props: ['project']
}
</script>

<style scoped lang="scss">

</style>