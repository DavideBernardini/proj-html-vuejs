<template>
    <section id="services" class="services">
        <div class="wrapper">
            <h5 class="pb-4">
                OUR BUISNESS AREA
            </h5>
            <h2>
                Excellence in
                <span>Services</span>
            </h2>
            <div class="options_info mt-5">
                <p>
                We are leaders in providing consultancy services with a set of cutting edge technologies and a team of experienced and renowned professionals. These are some options that you can hire.
                </p>
                <a href="#" class="btn_full">
                    SEE ALL
                </a>
            </div>
            <!-- cards -->
            <div class="container-fluid">
                <div class="row row-cols-3">
                    <div class="col"
                    v-for="(service, index) in serviceList"
                    :key="index">
                        <div class="icons mb-1">
                            <img :src="require(`../assets/images/svgs/${service.icon}`)" :alt="`icon for ${service.icon}`">
                            <a href="#">
                                <i class="fas fa-arrow-right"></i>
                            </a>
                        </div>
                        <h4 class="fw-bold py-4">
                            {{service.name}}
                        </h4>
                        <p>
                            {{service.info}}
                        </p>
                    </div>
                </div>
            </div>
            <!-- /cards -->
        </div>
        <!-- bullets decoration -->
        <img class="bullets" src="../assets/images/svgs/svg-0.svg" alt="bullets decoration">
    </section>
</template>

<script>
export default {
    name: 'Services',
    props: ['serviceList']
}
</script>

<style scoped lang="scss">
@import '../assets/style/variables.scss';
@import '../assets/style/mixins.scss';

.services {
    @include align-center;
    background-color: $bgColor;
    height: 68.125rem;
    color: $textColorSecondary;
    position: relative;
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
    .options_info {
        @include align-center-between;
        p {
            width: 80%;
        }
        a {
            align-self: baseline;
        }
    }
    .col {
        background-color: #fff;
        width: calc(100% / 3 - 1.25rem);
        margin-top: 1.875rem;
        padding: 2.8125rem;
        border-radius: .9375rem;
        .icons {
            @include space-between;
            img {
                height: 2.8125rem;
                filter: invert(35%) sepia(80%) saturate(4880%) hue-rotate(164deg) brightness(89%) contrast(96%);
            }
            i {
                font-size: 1.5625rem;
                color: $mainColorTransparentDark;
            }
        }
        h4 {
            color: $textColorPrimary;
        }
    }
    .col:nth-child(2), .col:nth-child(5) {
        margin-left: 1.875rem;
        margin-right: 1.875rem;
    }
    .bullets {
        position: absolute;
        top: 100%;
        left: 50%;
        transform: translate(-50%, -27.5%);
        height: 3.75rem;
        filter: invert(40%) sepia(61%) saturate(858%) hue-rotate(136deg) brightness(86%) contrast(98%);
        opacity: 0.5;
    }
}
</style>