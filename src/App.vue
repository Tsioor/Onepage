<template>
    <div id="app">
        <Header />
        <Hero />
        <About />
        <Services />
        <Works />
        <Footer />
    </div>
</template>

<script>
import Header from './components/Header'
import Footer from './components/Footer'
import Hero from './components/Hero'
import About from './components/About.vue'
import Services from './components/Services.vue'
import Works from './components/Works.vue'

export default {
    name: 'App',
    components: {
        Header, 
        Footer,
        Hero,
        About,
        Services,
        Works,
    }
}
</script>

<style lang="scss">
#app {
    display: flex;
    flex-direction: column;
    min-height: 100vh;
}
</style>
