<template>
    <section id="results" class="results">
        
        <!-- top -->
        <div class="top">
            <div class="wrapper">
                <h5 class="pb-4 fw-bold">
                    WHAT ARE WE DOING
                </h5>
                <h2 class="text-white">
                    <span class="text-white p-2">Results</span>
                    in numbers
                </h2>
                <!-- results list -->
                <ul>
                    <li class="fw-bold"
                    v-for="(res, index) in results"
                    :key="index">
                        <div class="number pb-2">
                            {{res.number}}
                        </div>
                        {{res.stat}}
                    </li>
                </ul>
                <!-- results list -->
            </div>
        </div>
        <!-- /top -->
        <!-- bottom -->
        <div class="bottom">
            <div class="wrapper h-100">
                <!-- technologies logo -->
                <ul class="w-100">
                    <li v-for="(tech, index) in technologiesLogo"
                    :key="index">
                        <img :src="require(`../assets/images/${tech.logo}.png`)" :alt="`logo of ${tech.name}`">
                    </li>
                    <li>
                        <img :src="require(`../assets/images/${technologiesLogo[0].logo}.png`)" :alt="`logo of ${technologiesLogo[0].name}`">
                    </li>
                </ul>
            </div>
        </div>
        <!-- /bottom -->
    </section>
</template>

<script>
export default {
    name: 'Results',
    props: ['results', 'technologiesLogo']
}
</script>

<style lang="scss" scoped>
@import '../assets/style/mixins.scss';
@import '../assets/style/variables.scss';

.results {
    height: 54.375rem;
    background-color: $bgDark;
    text-align: center;
    .top {
        height: 70%;
        background-image: url('../assets/images/bg-7.jpg');
        background-size: cover;
        @include align-center;
        h5 {
            color: $mainColorLighter;
            font-size: .875rem;
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
            @include space-between;
            margin-top: 7.5rem;
            width: 100%;
            color: $textColorSecondarySuperLight;
            font-size: 1.25rem;
            text-transform: capitalize;
            .number {
                color: $mainColorLighter;
                font-size: 2.8125rem;
            }
        }
    }
    .bottom {
        height: 30%;
        .wrapper {
            @include align-center;
        }
        ul {
            @include inline-block-list;
            @include space-between;
            img {
                height: 1.875rem;
                filter: brightness(300%);
            }
        }
        
    }
}
</style>