<template>
    <section id="about" class="about">
        <div class="container-fluid h-100">
            <div class="row h-100">
                <!-- left -->
                <div class="col-6 h-100 left">
                    <!-- content left -->
                    <div class="content me-5">
                        <h5 class="fw-bold pb-4">
                            OUR BUISNESS AREA
                        </h5>
                        <h2>
                            <span>The</span>
                            Company
                        </h2>
                        <p class="py-4">
                            For 12 years we have been providing audit and warranty, financial advice, taxes and related services to selected clients.
                        </p>
                        <!-- value cards -->
                        <div class="container-fluid p-0">
                            <div class="row row-cols-2">
                                <div class="col my-3"
                                v-for="(value, index) in companyValues"
                                :key="index">
                                    <h4 class="fw-bold pb-3">
                                        <i class="pe-1"
                                        :class="value.icon"></i>
                                        {{value.title}}
                                    </h4>
                                    <p>
                                        {{value.info}}
                                    </p>
                                </div>
                            </div>
                        </div>
                        <!-- /value cards -->
                        <!-- buttons -->
                        <div class="buttons mt-5 pt-2">
                            <a href="#support" class="btn_full me-4">
                                    GET IN TOUCH
                            </a>
                            <a href="#about" class="btn_empty">
                                    READ MORE
                            </a>
                        </div>
                        <!-- /buttons -->
                    </div>
                    <!-- /content left -->
                </div>
                <!-- /left -->
                <!-- right -->
                <div class="col-6 h-100 right">
                    <img class="h-100 w-100" src="../assets/images/about-4.jpg" alt="tizio incravattato">
                </div>
                <!-- /right -->
            </div>
        </div>
        <!-- bullets decoration -->
        <img class="bullets top" src="../assets/images/svgs/svg-0.svg" alt="bullets decoration">
        <img class="bullets" src="../assets/images/svgs/svg-0.svg" alt="bullets decoration">
    </section>
</template>

<script>
export default {
    name: 'About',
    props: ['companyValues']
}
</script>

<style lang="scss" scoped>
@import '../assets/style/variables.scss';
@import '../assets/style/mixins.scss';

.about {
    height: 55rem;
    color: $textColorSecondaryLighter;
    position: relative;
    .container-fluid {
        .col-6 {
            padding: 0;
        }
        .left {
            background-color: $bgDark;
            @include align-center;
            justify-content: end;
            .content {
                width: 70%;
                h5 {
                    font-size: .875rem;
                    color: $mainColorLighter;
                }
                h2 {
                    @include heading-style;
                    font-size: 3.125rem;
                    color: #fff;
                    span {
                        padding: .5rem .9375rem;
                        color: #fff;
                    }
                }
                .col {
                    h4 {
                        color: $textColorSecondarySuperLight;
                        i {
                            color: $mainColorLighter;
                        }
                    }
                }
            }
            .btn_empty {
                color: #fff;
            }
        }
        .right {
            img {
                object-fit: cover;
            }
        }
    }
    .bullets {
        position: absolute;
        top: 100%;
        left: 50%;
        transform: translate(-50%, -27.5%);
        height: 5.625rem;
        filter: invert(40%) sepia(61%) saturate(858%) hue-rotate(136deg) brightness(86%) contrast(98%);
        opacity: 0.5;
    }
    .bullets.top {
        top: 0;
    }
}

</style>