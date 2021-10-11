<template>
    <header>
        <!-- header top -->
        <div class="header_top">
            <div class="wrapper">
                <!-- left -->
                <div class="header_top_left">
                    <i class="fas fa-clock pe-1"></i>
                    Open hours: Mon - Sat - 9:00 - 18:00
                </div>
                <!-- /left -->
                <!-- right -->
                <div class="header_top_right">
                    <ul>
                        <li class="pe-4">
                            <i class="fas fa-phone pe-1"></i>
                            +1 (305) 1234-5678
                        </li>
                        <li>
                            <i class="fas fa-envelope"></i>
                            hello@example.com
                        </li>
                        <li class="px-4">
                            <a href="#">
                                <i class="fab fa-facebook-f"></i>
                            </a>
                        </li>
                        <li class="pe-4">
                            <a href="#">
                                <i class="fab fa-linkedin-in"></i>
                            </a>
                        </li>
                        <li>
                            <a href="#">
                                <i class="fab fa-twitter"></i>
                            </a>
                        </li>
                    </ul>
                </div>
                <!-- /right -->
            </div>
        </div>
        <!-- /header top -->
        <!-- nav -->
        <nav>
            <div class="wrapper">
                <!-- left -->
                <div class="nav_left">
                    <div class="logo">
                        <span>NEXT</span>GEN
                    </div>
                </div>
                <!-- /left -->
                <!-- right -->
                <div class="nav_right">
                    <ul>
                        <li class="px-3"
                        v-for="(section, index) in sections"
                        :key="index">
                            <a :href="`#${section}`">{{section}}</a>
                        </li>
                    </ul>
                    <a href="#" class="btn_full ms-3">
                        GET IN TOUCH
                    </a>
                </div>
                <!-- /right -->
            </div>
        </nav>
        <!-- /nav -->
    </header>
</template>

<script>
export default {
    name: 'Header',
    props: ['sections']
}
</script>

<style scoped lang="scss">
@import '../assets/style/variables.scss';
@import '../assets/style/mixins.scss';

header {
    .header_top {
        height: 3.125rem;
        background-color: $textColorPrimary;
        color: rgb(192, 195, 208);
    }
    .wrapper {
        @include align-center-between;
        height: 100%;
        ul {
            @include inline-block-list;
        }
    }
    nav {
        height: 5.3125rem;
        .logo {
            color: $textColorPrimary;
            @include logo-style;
            font-size: 1.25rem;
        }
        li {
            text-transform: uppercase;
        }
    }
}
</style>