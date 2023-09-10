<template>
    <section class="pb-4">
        <h2 class="text-3xl text-center my-4">Featured Collection</h2>
        <div class="container grid grid-cols-2 py-8 gap-4">
            <div class="relative flex justify-end items-center after:absolute after:w-full after:h-full after:border after:border-black after:-right-1/4 after:top-8">
                <div class="img-bg">
                    <NuxtImg class="opacity-70"
                        src="https://images.unsplash.com/photo-1528740561666-dc2479dc08ab?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxzZWFyY2h8Mnx8Y2xlYW5pbmd8ZW58MHwxfDB8fHww&auto=format&fit=crop&w=800&q=60"
                        alt="" />
                </div>
                <div class="absolute z-10 rounded-md shadow-lg bg-white p-16 flex flex-col items-center gap-4">
                    <div class="aspect-square cursor-pointer overflow-hidden w-60">
                        <img class="w-full h-full duration-700 object-cover transition-transform hover:scale-110" src="https://images.unsplash.com/photo-1528740561666-dc2479dc08ab?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxzZWFyY2h8Mnx8Y2xlYW5pbmd8ZW58MHwxfDB8fHww&auto=format&fit=crop&w=800&q=60" alt="">
                    </div>
                    <h3 class="text-2xl">Reinigungsmittel</h3>
                    <button class="button">Check</button>
                </div>
            </div>
            <div class="flex items-center relative z-20">
                <Swiper :spaceBetween="30" :autoplay="{
                    delay: 3000,
                    disableOnInteraction: false,
                }" :modules="[SwiperAutoplay, SwiperEffectFade, SwiperPagination]" :slides-per-view="3" :loop="true">
                    <SwiperSlide v-for="(slide, index) in prods" :key="index">
                        <div class="slide pb-8">
                            <div class="flex relative flex-col z-20 pb-2 shadow-lg bg-white rounded-md cursor-pointer after:absolute after:w-full after:h-full after:border after:z-10 after:border-black after:-right-2 after:top-2">
                                <img class="aspect-square object-cover" :src="slide.img" alt="">
                                <h4 class="text-lg px-2 text-center">{{ slide.title }}</h4>
                                <p class="text-center">{{ slide.price }}</p>
                            </div>
                        </div>
                    </SwiperSlide>
                </Swiper>
            </div>
        </div>
    </section>
</template>

<script setup>

const prods = [
    {
        title: "test",
        img: "https://images.unsplash.com/photo-1550963295-019d8a8a61c5?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxzZWFyY2h8OHx8Y2xlYW5pbmd8ZW58MHwxfDB8fHww&auto=format&fit=crop&w=800&q=60",
        price: 13.99
    },
    {
        title: "test",
        img: "https://images.unsplash.com/photo-1550963295-019d8a8a61c5?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxzZWFyY2h8OHx8Y2xlYW5pbmd8ZW58MHwxfDB8fHww&auto=format&fit=crop&w=800&q=60",
        price: 13.99
    },
    {
        title: "test",
        img: "https://images.unsplash.com/photo-1550963295-019d8a8a61c5?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxzZWFyY2h8OHx8Y2xlYW5pbmd8ZW58MHwxfDB8fHww&auto=format&fit=crop&w=800&q=60",
        price: 13.99
    },
    {
        title: "test",
        img: "https://images.unsplash.com/photo-1550963295-019d8a8a61c5?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxzZWFyY2h8OHx8Y2xlYW5pbmd8ZW58MHwxfDB8fHww&auto=format&fit=crop&w=800&q=60",
        price: 13.99
    },
    {
        title: "test",
        img: "https://images.unsplash.com/photo-1550963295-019d8a8a61c5?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxzZWFyY2h8OHx8Y2xlYW5pbmd8ZW58MHwxfDB8fHww&auto=format&fit=crop&w=800&q=60",
        price: 13.99
    },
    {
        title: "test",
        img: "https://images.unsplash.com/photo-1550963295-019d8a8a61c5?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxzZWFyY2h8OHx8Y2xlYW5pbmd8ZW58MHwxfDB8fHww&auto=format&fit=crop&w=800&q=60",
        price: 13.99
    },
]

</script>

<style scoped>
.container {
    height: 100vh;
}

.img-bg,
.img-bg img {
    width: 110%;
}
</style>