<template>
    <section id="about" class="about">
        <div class="container-fluid h-100">
            <div class="row h-100">
                <!-- left -->
                <div class="col-6 h-100 left">
                    <!-- content left -->
                    <div class="content me-5">
                        <h5 class="pb-4">
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
                                    <h4 class="pb-3">
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
                            <a href="#" class="btn_full me-4">
                                    GET IN TOUCH
                            </a>
                            <a href="#" class="btn_empty">
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
                    font-weight: bold;
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
                        color: #fff;
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
}

</style>