<template>
    <section class="text-white mt-20" id="testimonials" data-aos="zoom-in">
        <h2 class="text-4xl font-bold text-white text-left mb-4 px-4 xl:pl-16">Testimonials</h2>
        <div class="px-4 xl:px-16">
            <Carousel v-bind="settings" :breakpoints="breakpoints">
                <Slide v-for="element in testimonials" :key="element.id">
                    <div class="carousel__item p-4">
                        <div class="w-full mx-auto bg-[#111a3e] shadow-lg border border-[#1f1641] p-5 text-white font-light mb-6">
                            <div class="w-full flex mb-4 items-center">
                                <div class="overflow-hidden rounded-full w-10 h-10 bg-gray-50 border border-gray-200">
                                    <img :src="element.image" alt="testimonial image" loading="lazy">
                                </div>
                                <h6 class="ml-4 font-bold text-sm uppercase text-white">{{ element.fullName }}</h6>
                            </div>
                            <div class="w-full">
                                <p class="text-sm leading-tight">
                                    <span class="text-lg leading-none italic font-bold text-white mr-1">"</span>
                                    {{ element.comment }}
                                    <span class="text-lg leading-none italic font-bold text-white mr-1">"</span>
                                </p>
                            </div>
                        </div>
                    </div>
                </Slide> 
                <template #addons>
                    <Navigation />
                </template>
            </Carousel>
        </div>
    </section>
</template>

<script setup>
import { ref } from 'vue';
import { Carousel, Navigation, Slide } from 'vue3-carousel';
import 'vue3-carousel/dist/carousel.css';

// Carousel settings
const settings = ref({
    itemsToShow: 1,
    snapAlign: "center",
});

// Breakpoints
const breakpoints = ref({
    700: {
        itemsToShow: 2.5,
        snapAlign: 'center',
    },
    1024: {
        itemsToShow: 3,
        snapAlign: 'start',
    },
});

// Real Testimonials
const testimonials = ref([
    {
        id: 1,
        fullName: 'Mohammad Tanweer Salah',
        image: 'src/assets/tanweer.jpeg', 
        comment: 'A very hardworking and enthusiastic team leader, who has been a very valuable asset to the growth and marketing of GeeksGod. She is a very dedicated person at work and an expert in organizing and managing events and other community activities.',
    },
    {
        id: 2,
        fullName: 'Praveen Kumar Purushothaman',
        image: 'src/assets/praveen.jpeg', 
        comment: 'Madhvi’s hands-on approach to collaboration, leadership, proactiveness, and powerful character won her the respect of her peers. She is reliable, forward-thinking, and inspiring. Her marketing and content management expertise make her a great leader.',
    },
    {
        id: 3,
        fullName: 'Nitesh Keswani',
        image: 'src/assets/nitesh.jpeg', 
        comment: 'Madhvi is a great professional to work with. Her work ethic is immaculate, and she always goes the extra mile to find efficient ways to complete tasks. She is an inspiration to the rest of us.',
    },
]);
</script>

<style>
.carousel__prev,
.carousel__next {
    color: white !important;
}
</style>
