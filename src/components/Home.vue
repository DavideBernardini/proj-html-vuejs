<template>
    <section id="home" class="home d-flex flex-column">
        <!-- nav -->
        <Navbar :sections="sections"/>
        <!-- /nav -->
        <!-- content center -->
        <div class="content m-auto">
            <h2>
                Ready 
                <span>
                    Team
                </span>
            </h2>
            <p class="pt-4">
                No matter what your company needs, we will be ready to assist you in the best possible wat.
            </p>
            <div class="buttons mt-5 pt-2">
                <a href="#support" class="btn_full me-4">
                        GET IN TOUCH
                </a>
                <a href="#about" class="btn_empty">
                        READ MORE
                </a>
            </div>
        </div>
        <!-- /content center -->
        <!-- navigation pills -->
        <div class="pills">
            <div class="pill"></div>
            <div class="pill my-2 active"></div>
            <div class="pill"></div>
        <!-- /navigation pills -->
        </div>
    </section>
</template>

<script>
import Navbar from '../components/Navbar.vue'

export default {
    name: 'Home',
    components: {
        Navbar
    },
    props: ['sections']
}
</script>

<style scoped lang="scss">
@import '../assets/style/variables.scss';
@import '../assets/style/mixins.scss';

.home {
    height: 53.125rem;
    background-image: url('../assets/images/bg-parallax.png');
    background-color: lightgray;
    background-position: center;
    position: relative;
    .content {
        width: 31.25rem;
        text-align: center;
        @include center-absolute;
        h2 {
            @include heading-style;
            font-size: 4.375rem;
            span {
                padding: .625rem 1.25rem;
            }
        }
        p {
            color: $textColorSecondary;
        }
    }
    .pills {
        position: absolute;
        top: 50%;
        right: 1.875rem;
        transform: translateY(-50%);
        .pill {
            height: 2.5rem;
            width: .625rem;
            border: .0625rem solid $mainColor;
            border-radius: .625rem;
        }
        .pill.active {
            background-color: $mainColor;
        }
    }
    
}
</style>