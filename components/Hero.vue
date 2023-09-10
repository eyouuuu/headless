<template>
    <section class="relative">
        <Swiper :autoplay="{
            delay: 3000,
        }" :modules="[SwiperAutoplay, SwiperEffectFade, SwiperPagination]" :slides-per-view="1" :loop="true"
            :effect="'fade'" :pagination="{
                clickable: true,
            }">
            <SwiperSlide v-for="(slide, index) in imgs" :key="index">
                <div class="slide flex items-center">
                    <div class="img-bg">
                        <LazyNuxtImg class="opacity-70" :src="slide" />
                    </div>
                    <div class="container text-white z-10" >
                        <h3 class="text-5xl">Biolab {{ index }}</h3>
                        <p class="text-lg">text</p>
                    </div>
                </div>
            </SwiperSlide>
        </Swiper>
    </section>
</template>

<script setup>

const imgs = [
    'https://images.unsplash.com/photo-1563453392212-326f5e854473?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxzZWFyY2h8Mnx8Y2xlYW5pbmd8ZW58MHx8MHx8fDA%3D&auto=format&fit=crop&w=800&q=60',
    'https://images.unsplash.com/photo-1583907659441-addbe699e921?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxzZWFyY2h8MTF8fGNsZWFuaW5nfGVufDB8fDB8fHww&auto=format&fit=crop&w=800&q=60',
    'https://plus.unsplash.com/premium_photo-1679501956116-97589191fafb?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxzZWFyY2h8MTN8fGNsZWFuaW5nfGVufDB8fDB8fHww&auto=format&fit=crop&w=800&q=60'
]

</script>

<style scoped>
.slide {
    min-height: 100vh;
    overflow: hidden;
    position: relative;
}

h3,
p {
    animation: fade-in 3s;
}
</style>