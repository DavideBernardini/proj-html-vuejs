<template>
    <header>
        <div class="wrapper">
            <!-- left -->
            <div class="header_left">
                <i class="fas fa-clock pe-1"></i>
                Open hours: Mon - Sat - 9:00 - 18:00
            </div>
            <!-- /left -->
            <!-- right -->
            <div class="header_right">
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
    </header>
</template>

<script>
export default {
    name: 'Header'
}
</script>

<style scoped lang="scss">
@import '../assets/style/variables.scss';
@import '../assets/style/mixins.scss';

header {
    .wrapper {
        @include align-center-between;
        height: 100%;
        ul {
            @include inline-block-list;
        }
    }
    height: 3.125rem;
    background-color: $textColorPrimary;
    color: rgb(192, 195, 208);
}
</style>