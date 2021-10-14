<template>
    <section id="support" class="support">
        <div class="wrapper">
            <div class="container-fluid">
                <div class="row">
                    <!-- left -->
                    <div class="col-8 pe-5 pt-2">
                        <h5 class="fw-bold pb-4">
                            SEND A MESSAGE 
                        </h5>
                        <h2>
                            Get in 
                            <span>Touch</span>
                        </h2>
                        <p class="py-4">
                            We will respond to your message as soon as possible.
                        </p>
                        <!-- form -->
                        <form>
                            <div class="container-fluid px-0">
                                <!-- name and email -->
                                <div class="row pb-3">
                                    <div class="col pe-2">
                                        <input class="w-100 px-3" type="text" placeholder="Name">
                                    </div>
                                    <div class="col ps-2">
                                        <input class="w-100 px-3" type="email" placeholder="Email">
                                    </div>
                                </div>
                                <!-- /name and email -->
                                <!-- number and info -->
                                <div class="row pb-3">
                                    <div class="col pe-2">
                                        <input class="w-100 px-3" type="number" placeholder="Phone">
                                    </div>
                                    <div class="col ps-2">
                                        <select class="w-100 px-3">
                                            <option value="" disabled selected>
                                                More Info
                                            </option>
                                        </select>
                                    </div>
                                </div>
                                <!-- /number and info -->
                                <!-- textarea -->
                                <textarea class="w-100 p-3" placeholder="Message"></textarea>
                                <!-- /textarea -->
                                <button type="submit" class="btn_full mt-5">
                                    SEND
                                </button>
                            </div>
                        </form>
                        <!-- /form -->
                    </div>
                    <!-- /left -->
                    <!-- right -->
                    <div class="col-4">
                        <h4 class="fw-bold">Example Inc.</h4>
                        <p class="py-3">
                            Lorem ipsum dolor sit amet consectetur adipiscing elit.
                        </p>
                        <p class="pb-2">
                            Praesent diam lacus, dapibus sed imperdiet consecutor.
                        </p>
                        <!-- contacts -->
                        <ul class="contacts">
                            <li class="py-3"
                            v-for="(contact, index) in contacts"
                            :key="index">
                                <div class="circle me-2">
                                    <i :class="contact.icon"></i>
                                </div>
                                {{contact.info}}
                            </li>
                        </ul>
                        <!-- /contacts --> 
                        <div class="pointer btn_empty d-inline-block mt-3">VIEW MAP</div>                       
                    </div>
                    <!-- /right -->
                </div>
            </div>
        </div>
    </section>
</template>

<script>

export default {
    name: 'Support',
    props: ['contacts']
}
</script>

<style scoped lang="scss">
@import '../assets/style/variables.scss';
@import '../assets/style/mixins.scss';

.support {
    height: 53.125rem;
    @include align-center;
    color: $textColorSecondary;
    // left
    .col-8 {
        h5 {
            font-size: .875rem;
            color: $mainColorLighter;
        }
        h2 {
            @include heading-style;
            font-size: 3.125rem;
            span {
                padding: .5rem .9375rem;
            }
        }
        form {
            input, select, textarea {
                border: none;
                background-color: $bgColorForm;
                height: 3.125rem;
                border-radius: .3125rem;
            }
            input:focus-visible, select:focus-visible, textarea:focus-visible {
                outline-color: $mainColor;
            }
            // input number apparence
            input::-webkit-outer-spin-button,
            input::-webkit-inner-spin-button {
                -webkit-appearance: none;
                margin: 0;
            }
            input[type=number] {
                -moz-appearance: textfield;
            }
            select {
                // delete arrow select
                -moz-appearance:none; /* Firefox */
                -webkit-appearance:none; /* Safari and Chrome */
                appearance:none;
                background-image: url("../assets/images/svgs/caret-down-svgrepo-com.svg");
                background-size: 10%;
                background-repeat: no-repeat;
                background-position-x: 100%;
                background-position-y: 50%;
                color: $textColorSecondary;
            }
            textarea {
                resize: none;
                height: 9.375rem;
            }
            button {
                border: none;
            }
        }
    }
    // right
    .col-4 {
        h4 {
            font-size: 1.75;
            color: $textColorPrimary;
        }
        .contacts {
            @include list-style-none;
            color: $mainColor;
            font-size: 1.1875rem;
            .circle {
                display: inline-block;
                background-color: $mainColorTransparent;
                height: 3.125rem;
                width: 3.125rem;
                border-radius: 50%;
                line-height: 3.125rem;
                text-align: center;
                font-size: 1.5rem;
            }
        }
    } 
}
</style>