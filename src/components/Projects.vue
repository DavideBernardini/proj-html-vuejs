<template>
    <section id="projects" class="projects">
        <div class="wrapper">
            <h5 class="pb-4">
                WE DO MORE FOR EVERYONE
            </h5>
            <h2 class="mb-5">
                Action &
                <span>Projects</span>
            </h2>
            <ul class="my-3">
                <li class="mx-4 active">
                    ALL
                </li>
                <li class="mx-4"
                v-for="(project, index) in companyProjects"
                :key="index">
                    {{project.category}}
                </li>
            </ul>
            <!-- cards -->
            <div class="container-fluid">
                <div class="row row-cols-3">
                    <!-- card -->
                    <ProjectCard class="col pointer"
                    v-for="(project, index) in companyProjects"
                    :key="index"
                    :project="project"/>
                    <!-- /card -->
                </div>
            </div>
            <!-- /cards -->
        </div>
    </section>
</template>

<script>
import ProjectCard from '../components/ProjectCard.vue';

export default {
    name: 'Projects',
    components: {
        ProjectCard
    },
    props: ['companyProjects']
}
</script>

<style lang="scss">
@import '../assets/style/variables.scss';
@import '../assets/style/mixins.scss';

.projects {
    @include align-center;
    height: 81.25rem;
    color: $textColorPrimary;
    text-align: center;
    h5 {
        font-weight: bold;
        font-size: .875rem;
        color: $mainColor;
    }
    h2 {
        @include heading-style;
        font-size: 3.125rem;
        span {
            padding: .5rem .9375rem;
        }
    }
    ul {
        @include inline-block-list;
        li {
            text-transform: uppercase;
            color: $textColorSecondary;
            cursor: pointer;
        }
        li.active {
            padding: .3125rem .375rem;
            border-radius: .1875rem;
            background-color: $mainColorTransparent;
        }
    }
    .col {
        background-color: #fff;
        width: calc(100% / 3 - 1.25rem);
        margin-top: 1.875rem;
        padding: 0;
        border-radius: .625rem;
        overflow: hidden;
        position: relative;
        img {
            border-radius: .625rem;
            filter: brightness(50%) blur(.03125rem);
        }
        .text {
            position: absolute;
            left: 50%;
            transform: translate(-50%);
            width: 90%;
            bottom: 10%;
            text-align: center;
            h4 {
                color: $textColorSecondarySuperLight;
            }
            p {
                display: none;
                font-size: 1.0625rem;
                color: $textColorSecondaryLighter;
            }
        }
        .fa-arrow-right {
            font-size: 30px;
            color: $textColorSecondarySuperLight;
            position: absolute;
            top: 35px;
            right: 40px;
            display: none;
        }
    }
    .col:hover p, .col:hover .fa-arrow-right {
        display: block;
    }
    .col:nth-child(2), .col:nth-child(5) {
        margin-left: 1.875rem;
        margin-right: 1.875rem;
    }
}
</style>