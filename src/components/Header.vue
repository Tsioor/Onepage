<template>
    <header class="header">
        <b-navbar toggleable="lg" class="shadow-sm">
            <b-navbar-brand href="#">
                <img src="../assets/images/logo.png" alt="Onepage" class="img-fluid">
            </b-navbar-brand>
            <b-navbar-toggle target="nav-collapse" class="mr-3"></b-navbar-toggle>
            <b-collapse id="nav-collapse" is-nav>
                <b-navbar-nav class="navbar-nav-left" v-b-scrollspy="80">
                    <b-nav-item href="#about" @click.prevent="scrollIntoView">About</b-nav-item>
                    <b-nav-item href="#services" @click.prevent="scrollIntoView">Services</b-nav-item>
                    <b-nav-item href="#works" @click.prevent="scrollIntoView">Works</b-nav-item>
                    <b-nav-item href="#">Blog</b-nav-item>
                    <b-nav-item href="#footer" @click.prevent="scrollIntoView">Contact</b-nav-item>
                </b-navbar-nav>
    
                <b-navbar-nav class="ml-auto navbar-nav-social">
                    <b-nav-item href="#"><span class="fab fa-twitter"></span></b-nav-item>
                    <b-nav-item href="#"><span class="fab fa-facebook-f"></span></b-nav-item>
                    <b-nav-item href="#"><span class="fab fa-linkedin-in"></span></b-nav-item>
                </b-navbar-nav>
            </b-collapse>
        </b-navbar>
    </header>
</template>

<script>
export default {
    methods: {
      scrollIntoView(e) {
        const href = e.target.getAttribute('href')
        const el = href ? document.querySelector(href) : null
        if (el) {
            window.scrollTo({
                top: el.offsetTop - 80,
                behavior: 'smooth'
            })
        }
      }
    },
}
</script>
