<template>
    <div class="my-[100px]">
        <div class="container mx-auto">
            <h1 class="text-[42px] font-[700] text-center">Portfolio</h1>
            <p class="text-gray-500 px-[10px] md:px-0 text-center lg:w-[70%] mx-auto mt-[24px]">A diverse collection of successfully implemented projects across various industries, including corporate websites, e-commerce platforms, educational portals, and mobile applications. Each project is equipped with modern technologies, high-level security measures, and user-friendly interfaces. The portfolio reflects the technical complexity of projects, design solutions, and the level of meeting client requirements. All projects are created based on responsive design principles, ensuring perfect functionality across different devices. Our work demonstrates expertise in creating scalable, secure, and efficient digital solutions that drive business growth and user engagement.</p>
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6 md:justify-around items-center my-[70px] px-[20px] md:px-0 xl:px-[10px] 2xl:px-0">
                <div v-for="el of portfolio" :key="el.id" class="w-[100%] shadow-xl rounded-xl">
                    <img :src="el.img" alt="picture" class="rounded-t-xl">
                    <div class="p-[24px]">
                        <p class="text-[14px] text-gray-500">{{ el.title.toLocaleUpperCase() }}</p>
                        <h2 class="my-[12px] font-bold text-[24px] lg:text-[20px] xl:text-[24px]">{{ el.title1 }}</h2>
                        <p class="text-gray-500 lg:text-[14px] xl:text-[16px] ">{{ el.desc.slice(0, 40) }}...</p>
                        <button class="text-[#A53DFF] border border-[#A53DFF] rounded-md py-[12px] px-[24px] mt-[32px] hover:bg-[#A53DFF] hover:text-white font-bold">Case Study →</button>
                    </div>
                </div>
            </div>
                <button class="text-white rounded-md py-[12px] px-[24px] mt-[32px] bg-[#A53DFF] font-bold flex mx-auto">More project</button>
        </div>
    </div>
</template>

<script setup>
   import portfolio from '../files/portfolio.json'   
   
</script>

<style lang="scss" scoped>

</style>