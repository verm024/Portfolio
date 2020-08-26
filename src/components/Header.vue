<template>
    <div class="header container">
        <v-row class="align-center">
            <v-col class="col-12 col-md-6">
                <span class="header-text-hello">Hello, I am</span>
                <br>
                <span class="header-text-name">Muhammad Naufal</span>
                <br>
                <span class="header-text-job">Web Developer</span>
            </v-col>
            <v-col class="col-12 col-md-6 header-photo-container">
                <img src="@/assets/header-photo.png" class="header-photo" alt="">
            </v-col>
        </v-row>
    </div>
</template>

<script>
export default {
    name: "Header"
}
</script>

<style>
    .header{
        height: calc(100vh - 64px);
        padding-top: 0 !important;
        padding-bottom: 0 !important;
    }

    .header .row{
        height: 100%;
    }

    .header-text-hello{
        color: #FFD082 !important;
        font-family: 'Open Sans', sans-serif;
        font-weight: 300;
        font-size: 22px;
    }

    .header-text-name{
        color: white !important;
        font-family: 'PT Serif', serif;
        font-weight: 700;
        font-size: 44px;
        letter-spacing: 3px;
    }

    .header-text-job{
        color: white !important;
        font-family: 'Open Sans', sans-serif;
        font-weight: 300;
        font-size: 18px;
    }

    .header-photo{
        height: calc(100vh - 64px);
        margin-bottom: -12px;
    }

    .header-photo-container{
        overflow: hidden;
        padding-top: 0 !important;
        padding-bottom: 0 !important;
        height: calc(100vh - 64px);
        text-align: right;
    }
</style>