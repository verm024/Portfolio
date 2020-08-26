<template>
    <div class="home">
        <div class="header-container">
            <Header/>
        </div>
        <div class="about-container" id="about">
            <About/>
        </div>
    </div>
</template>

<script>
import Header from '@/components/Header.vue'
import About from '@/components/About.vue'

export default {
    components: {
        Header,
        About
    }
}
</script>

<style scoped>
    .header-container{
        background: radial-gradient(50% 50% at 50% 50%, rgba(33, 36, 61, 0.95) 0%, #21243D 100%);
    }

    .about-container{
        background: #21243D;
    }

</style>
