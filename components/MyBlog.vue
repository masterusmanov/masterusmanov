<template>
    <div class=" container mx-auto relative my-[70px]">
        <div class="slides-container flex snap-x snap-mandatory overflow-hidden overflow-x-auto space-x-6 rounded scroll-smooth before:w-[45vw] before:shrink-0 after:w-[45vw] after:shrink-0 md:before:w-0 md:after:w-0" ref="slidesContainer">
            <div v-for="el of blog" :key="el.id" class="w-[325px] h-[400px] mx-auto rounded-[16px] border md:w-[350px] lg:w-[325px] xl:w-[400px] 2xl:w-[490px] xl:h-[450px] 2xl:h-[500px] slide aspect-square  flex-shrink-0 snap-center overflow-hidden">
                <img :src="el.img" alt="Blog" class="w-full h-[40%] xl:h-[50%] 2xl:h-[60%] object-cover">
                <div class=" grid items-center gap-4 p-4">
                    <p class="text-gray-500">{{el.date.toLocaleUpperCase()}}</p>
                    <h2 class="text-[18px] font-[700]">{{el.title.toUpperCase()}}</h2>
                    <p class="text-gray-500 text-[14px] text-justify h-[90px] xl:h-[70px] 2xl:h-[50px]">{{el.desc.slice(0, 200)}}</p>
                    <a :href="el.link" class="text-end text-[#A53DFF]">Details</a>
                </div>
            </div>
        </div>
       <div class="flex justify-end items-center gap-4 md:gap-0 mt-[32px] md:mt-[56px] xl:mt-[48px]">
        <div class="md:w-[10%] lg:w-[10%] xl:w-[8%] 2xl:w-[6%] flex items-center gap-[20px] mr-[30px]">
            <div class=" top-0 -left-4 h-full items-center">
                <button @click="prevSlide" role="button" class="prev px-2 py-2 rounded-full text-[#A53DFF] border border-[#A53DFF] hover:bg-[#A53DFF] hover:text-white group" aria-label="prev"><svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-5 h-5 group-active:-translate-x-2 transition-all duration-200 ease-linear">
                        <path stroke-linecap="round" stroke-linejoin="round" d="M15.75 19.5L8.25 12l7.5-7.5" />
                    </svg>
                </button>
            </div>
            <div class=" top-0 -right-4 h-full items-center">
                <button @click="nextSlide" role="button" class="next px-2 py-2 rounded-full text-[#A53DFF] border border-[#A53DFF] hover:bg-[#A53DFF] hover:text-white group" aria-label="next"><svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-5 h-5 group-active:translate-x-2 transition-all duration-200 ease-linear">
                        <path stroke-linecap="round" stroke-linejoin="round" d="M8.25 4.5l7.5 7.5-7.5 7.5" />
                    </svg>
                </button>
            </div>
        </div>
       </div>
    </div>
</template>

<script setup>
    import { ref, computed, onMounted, onBeforeUnmount } from 'vue';
    import blog from "../files/blog.json"
    const slidesContainer = ref(null); // Ref to the slides container element

    const slideWidth = computed(() => {
    if (!slidesContainer.value) return 0;
    return slidesContainer.value.querySelector('.slide').clientWidth;
    });

    const scrollLeft = (amount) => {
    if (!slidesContainer.value) return;
    slidesContainer.value.scrollLeft += amount;
    };

    const nextSlide = () => scrollLeft(slideWidth.value);
    const prevSlide = () => scrollLeft(-slideWidth.value);

    const onSlideChange = (event) => {
    // Handle slide change event (optional)
    };

    onMounted(() => {
        slidesContainer.value.addEventListener('scroll', onSlideChange);
    });

    onBeforeUnmount(() => {
        slidesContainer.value.removeEventListener('scroll', onSlideChange);
    });
</script>


<style lang="scss" scoped>
    .slides-container {
        -ms-overflow-style: none; /* Internet Explorer 10+ */
        scrollbar-width: none; /* Firefox */
    }
    .slides-container::-webkit-scrollbar {
        display: none; /* Safari and Chrome */
    }

</style>