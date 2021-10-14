<template>
    <footer>
        <!-- top -->
        <div class="top">
            <div class="wrapper">
                <div class="container-fluid">
                    <div class="row row-cols-4">
                        <div class="col info">
                            <div class="logo py-3">
                                <span class="me-1">NEXT</span>GEN
                            </div>
                            <p class="py-3">
                                A functional HTML Template for Corporate & Buisness.
                            </p>
                            <ul class="contacts">
                                <li class="pb-4"
                                v-for="(contact, index) in contacts"
                                :key="index">
                                    <i :class="contact.icon"></i>
                                    {{contact.info}}
                                </li>
                            </ul>
                            <a href="#support" class="btn_empty mt-2">
                                GET IN TOUCH
                            </a>
                        </div>
                        <LinksFooter class="col"
                        v-for="(group, index) in footerLinks"
                        :key="index"
                        :group="group"/>
                    </div>
                </div>
            </div>
        </div>
        <!-- /top -->
        <!-- bottom -->
        <div class="bottom">
            <div class="wrapper">
                <p>
                    Enjoy the low price. We are tracking any intention of piracy.
                </p>
                <p>
                    @ 2020 NEXTGEN is Proudly Powered by <span>Codings</span>.
                </p>
            </div>
            <a href="#header" class="to_top">
                <i class="fas fa-arrow-up"></i>
            </a>
            
        </div>
        <!-- /bottom -->
    </footer>
</template>

<script>
import LinksFooter from '../components/LinksFooter';

export default {
    name: 'Footer',
    components: {
        LinksFooter
    },
    props: [
        'footerLinks',
        'contacts'
    ]
}
</script>

<style lang="scss">
@import '../assets/style/variables.scss';
@import '../assets/style/mixins.scss';

footer {
    .top {
        height: 620px;
        background-color: $bgDark;
        @include align-center;
        .row {
            @include space-between;
            .col {
                width: calc(100% / 4 - 1.25rem);
                border-radius: .625rem;
                color: $textColorSecondaryLighter;
            }
            .col.info {
                .logo {
                    @include logo-style;
                    font-size: 24px;
                    color: $textColorSecondarySuperLight;
                }
                p {
                    font-size: 17px;
                }
                .contacts {
                    @include list-style-none;
                    font-size: 17px;
                }
                a {
                    color: $textColorSecondarySuperLight;
                }
            }
            .col.links {
                padding: 50px 44px;
                background-color: rgb(42, 42, 47, 0.2);
                h4 {
                    color: $textColorSecondarySuperLight;
                    font-weight: bold;
                    font-size: 25px;
                    margin-bottom: 30px;
                }
                ul {
                    @include list-style-none;
                    li {
                        margin-top: 10px;
                        margin-bottom: 10px;
                        a {
                            font-size: 17px;
                            span {
                                vertical-align: middle;
                            }
                            i {
                                font-size: 25px;
                                vertical-align: middle;
                            }
                        }
                    }
                }
            }
        }
    }
    .bottom {
        background-color: $bgDarker;
        height: 90px;
        color: $textColorSecondaryLighter;
        @include align-center;
        position: relative;
        .wrapper {
            @include space-between;
            p {
                margin: 0;
                span {
                    color: $mainColor;
                }
            }
        }
        .to_top {
            display: inline-block;
            background-color: rgb(42, 42, 47, 0.4);
            height: 3.125rem;
            width: 3.125rem;
            border-radius: 50%;
            line-height: 3.125rem;
            text-align: center;
            font-size: 1.5rem;
            color: $bgDark;
            position: absolute;
            right: 25px;
            top: 50%;
            transform: translateY(-50%);
        }
    }
}
</style>