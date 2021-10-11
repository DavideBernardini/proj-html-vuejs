<template>
    <section id="home" class="home d-flex">
        <div class="content m-auto">
            <h2>Ready <span>Team</span></h2>
            <p class="pt-4">
                No matter what your company needs, we will be ready to assist you in the best possible wat.
            </p>
            <div class="buttons mt-5 pt-2">
                <a href="#" class="btn_full me-4">
                        GET IN TOUCH
                </a>
                <a href="#" class="btn_empty">
                        READ MORE
                </a>
            </div>
        </div>
        <div class="pills">
            <div class="pill"></div>
            <div class="pill full"></div>
            <div class="pill"></div>
        </div>
    </section>
</template>

<script>
export default {
    name: 'Home'
}
</script>

<style scoped lang="scss">
@import '../assets/style/variables.scss';
@import '../assets/style/mixins.scss';

.home {
    height: 850px;
    margin-top: -100px;
    background-image: url('../assets/images/bg-parallax.png');
    background-position: center;
    position: relative;
    .content {
        width: 500px;
        text-align: center;
        h2 {
            font-size: 70px;
            font-weight: bolder;
            color: $textColorPrimary;
            span {
                color: $mainColor;
                background-color: $mainColorTransparent;
                padding: 10px 20px;
                border-radius: 5px;
            }
        }
        p {
            color: $textColorSecondary;
        }
    }
    .pills {
        position: absolute;
        top: 50%;
        transform: translateY(-50%);
    }
}
</style>