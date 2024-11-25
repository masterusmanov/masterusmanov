<template>
    <div class="main h-[70px] grid items-center font-sans bg-white">
       <div class="container mx-auto flex items-center justify-between xl:px-[10px] 2xl:px-0">
            <div class="flex items-center gap-4 px-[10px] md:px-0">
                <p class="logo text-[20px] font-[600] bg-[#A53DFF] px-3 py-2 text-white rounded-full">EU</p>
                <p class="hidden md:block font-[700] text-[22px]">Elyor Usmanov</p>
            </div>
            <div class="hidden w-[50%] lg:flex justify-between items-center font-bold text-gray-600">
                <a href="#">Home</a>
                <a href="#about_me">About</a>
                <a href="#">Skills</a>
                <a href="#">Portfolio</a>
                <a href="#">Services</a>
                <a href="#">Blog</a>
                <a href="https://t.me/masterusmanov" class="bg-[#A53DFF] text-white px-5 py-2 rounded-md">Contact</a>
            </div>
            <div class="w-[150px] md:w-[15%] flex items-center justify-between lg:hidden">
                <a href="https://t.me/masterusmanov" class="bg-[#A53DFF] text-white px-5 py-2 rounded-md">Contact</a>
                <Menubar class=""/>
            </div>
           
       </div>
    </div>
</template>

<script setup>

</script>

<style  scoped>
    .main{
        box-shadow: 10px 0 10px gray;
    }
    .logo{
        text-shadow: 1px 1px 4px black;
    }
</style>