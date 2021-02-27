<template>
    <footer id="footer" class="footer">
        <div class="container">
            <h2 class="title-section text-white">SAY HELLO</h2>
            <div class="row">
                <div class="col-md-5">
                    <b-tabs content-class="mt-3">
                        <b-tab title="Paris" active>
                            <address>
                                1 rue de Paris  - 75009 Paris<br>
                                +33 9 34 67 89 45
                            </address>
                        </b-tab>
                        <b-tab title="London">
                            <address>
                                64  Guild Street - N21 4HS<br>
                                070 5558 5715
                            </address>
                        </b-tab>
                    </b-tabs>
                    <div class="social">
                        <h3>FOLLOW US</h3>
                        <b-navbar-nav class="navbar-nav-social flex-row">
                            <b-nav-item href="#" class="px-2"><span class="fab fa-twitter"></span></b-nav-item>
                            <b-nav-item href="#" class="px-2"><span class="fab fa-facebook-f"></span></b-nav-item>
                            <b-nav-item href="#" class="px-2"><span class="fab fa-linkedin-in"></span></b-nav-item>
                        </b-navbar-nav>
                    </div>
                </div>
                <div class="col-md-7">
                    <b-form @submit="onSubmit">
                        <b-form-group id="input-group-name">
                            <b-form-input
                                id="input-name"
                                v-model="form.name"
                                placeholder="Name *"
                                required
                            ></b-form-input>
                        </b-form-group>
                        <b-form-group id="input-group-email">
                            <b-form-input
                                id="input-email"
                                v-model="form.email"
                                type="email"
                                placeholder="Email *"
                                required
                            ></b-form-input>
                        </b-form-group>
                        <b-form-group>
                            <b-form-textarea
                                id="textarea-message"
                                v-model="form.message"
                                placeholder="Message *"
                                rows="2"
                                required
                            ></b-form-textarea>
                        </b-form-group>
                        <b-button type="submit" variant="primary">Send</b-button>
                    </b-form>
                </div>
            </div>
        </div>
        <div class="copyright">
            <div class="container">
                <div class="row">
                    <div class="col-auto">
                        Copyright © Tous droits réservés 2018                     
                    </div>
                    <div class="col-auto ml-auto">
                        <a href="#" class="rgpd-link">Conditions générales de vente</a>
                        <a href="#" class="rgpd-link">Politique de confidentialité</a>
                        <a href="#" class="rgpd-link">Mentions légales</a>
                    </div>
                </div>
            </div>
        </div>
    </footer>
</template>

<script>
    export default {
        data() {
            return {
                form: {
                    name: '',
                    email: '',
                    message: ''
                },
            }
        },
        methods: {
            onSubmit(e) {
                e.preventDefault()
                console.log(JSON.stringify(this.form))
            }
        }
    }
</script>

<style lang="scss" scoped>
    .footer {
        background-color: #323232;
        margin-top: auto;
    }
</style>