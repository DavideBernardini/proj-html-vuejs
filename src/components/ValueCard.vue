<template>
    <div>
        <h4 class="fw-bold pb-3">
            <i class="pe-1"
            :class="value.icon"></i>
            {{value.title}}
        </h4>
        <p>
            {{value.info}}
        </p>
    </div>
</template>

<script>
export default {
    name: 'ValueCard',
    props: ['value']
}
</script>

<style scoped lang="scss">

</style>