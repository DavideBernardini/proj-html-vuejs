<template>
    <nav>
        <div class="wrapper h-100 px-1">
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
                    v-for="(section, index) in sections.slice(0, 5)"
                    :key="index">
                        <a class="py-3"
                        :href="`#${section}`">{{section}}</a>
                    </li>
                </ul>
                <a href="#support" class="btn_full ms-3">
                    GET IN TOUCH
                </a>
            </div>
            <!-- /right -->
        </div>
    </nav>
</template>

<script>

export default {
    name: 'Navbar',
    props: ['sections']
}
</script>

<style scoped lang="scss">
@import '../assets/style/variables.scss';
@import '../assets/style/mixins.scss';

nav {
    height: 5.3125rem;
    .wrapper {
        @include align-center-between;
        ul {
            @include inline-block-list;
        }
        .logo {
            color: $textColorPrimary;
            @include logo-style;
            font-size: 1.25rem;
        }
        li {
            text-transform: uppercase;
        }
        li:hover a {
            border-bottom: 3px solid $mainColor;
            margin-bottom: -3px;
        }
    }
}
</style>