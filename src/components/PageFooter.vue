<script>
export default {
    name: 'PageFooter',
    data() {
        return {
            iconArray: [
                'fa-youtube',
                'fa-twitch',
                'fa-facebook-f',
                'fa-discord',
            ],
            quickLinks: [
                'Games',
                'Latest Tournament',
                'Shop',
                'Blog',
                'Contact',
            ],
            helpLinks: [
                'Faqs',
                'Terms & Conditions',
                'Privacy',
            ],
            FollowUsLinks: [
                'Facebook',
                'Twitter',
                'Instagram',
                'Youtube',
                'Github',
            ],
        }
    },
    components: {

    },
    methods: {

    }
}
</script>

<template>
    <footer class="my-0">
        <section class="my-footer-bg-top">
            <div class="container-xl position-relative">
                <div class="border rounded-5 position-absolute">
                    <div class="my-footer-card mx-auto ">
                        <div class="row">
                            <div class="col text-white py-5">
                                <h2>Subscribe Newsletter</h2>
                                <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Odit doloribus magni quia
                                    dolorum.
                                </p>
                            </div>
                            <div class="col-5">
                                <div class="my-input-group py-5">
                                    <input class="text-light rounded-4" type="text" name="" id=""
                                        placeholder="Enter your email">
                                    <span><img src="img/icon/send-icon.png" alt=""></span>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>

                <div class="row text-white pt-5">
                    <div class="col-4">
                        <img id="logo" src="img/logo.png" alt="">
                        <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Atque in sunt, quisquam ullam quos
                            impedit
                            expedita.
                        </p>
                        <div>
                            <span v-for="(icon) in iconArray">
                                <i class="fa-brands me-3 p-3 rounded-5 border border-1 my-icons" :class="icon">
                                </i>
                            </span>
                        </div>
                    </div>
                    <div class="col-2">
                        <h4>Quick Links</h4>
                        <ul>
                            <li v-for="link in quickLinks">
                                <a href="">
                                    {{ link }}
                                </a>
                            </li>
                        </ul>
                    </div>
                    <div class="col-2">
                        <h4>Help</h4>
                        <ul>
                            <li v-for="link in helpLinks">
                                <a href="">
                                    {{ link }}
                                </a>
                            </li>
                        </ul>
                    </div>
                    <div class="col-2">
                        <h4>Follow Us</h4>
                        <ul>
                            <li v-for="link in FollowUsLinks">
                                <a href="">
                                    {{ link }}
                                </a>
                            </li>
                        </ul>
                    </div>
                    <div class="col-2">
                        <h4>Contact</h4>
                        <p class="my-green-text">Location:</p>
                        <p>4 Mayfield, Buckden,
                            <br>
                            PE19 5SZ
                        </p>
                        <p class="my-green-text pt-2">
                            Phone:
                        </p>
                        <p>(302)555-0107</p>
                    </div>
                </div>
            </div>
        </section>
        <section class="my-footer-bg-bottom">
            <p class="text-center text-white py-4">
                Copyright &#169; 2022 <span class="my-green-text">FUTIO</span>. ALL rights reserved.
            </p>
        </section>
    </footer>
</template>

<style lang="scss" scoped>
@use "../scss/variables.scss" as *;

.my-footer-bg-top {
    background-color: $footer-bg-1;
    padding-top: 100px;

    div {
        .position-absolute {
            position: absolute;
            width: 80%;
            bottom: 300px;
            left: 100px;
            border: transparent;
            background-color: $color-4;
        }
    }
}

.my-footer-bg-bottom {
    background-color: $footer-bg-2;
}

.my-footer-card {
    width: 90%;

}

.my-input-group {
    position: relative;

    input {
        width: 90%;
        padding: 15px;
        background-color: #435374;
        border: 1px solid grey;
    }

    span {

        width: 100px;


        img {
            position: absolute;
            background-color: #94CB56;
            top: 50px;
            right: 55px;
            padding: 13px;
            border-radius: 50%;
        }
    }
}

.my-icons:hover {
    background-color: $color-2;
}
</style>