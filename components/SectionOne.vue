<template>
    <div>
        <div class="container mx-auto flex items-center justify-center gap-[136px] my-[126px]">
            <div class="w-1/2">
               <div>
                    <h1 class="text-[48px] font-bold">Hello, I’m <br>Elyor Usmanov</h1>
                    <p class="text-[20px] text-gray-500 my-[24px]">My speciality is Full-stack software developer
                        (Backend and Frontend). I am very fond of
                        in this field. In the future, I want to be the
                        professional Full-stack software engineer,
                        and to reach my target, I am ready to go through
                        any troubles and learn new technologies.
                    </p>
                    <button class="px-[24px] py-[12px] bg-[#A53DFF] text-[18px] text-white font-[700] rounded-md">Contact</button>
               </div>
               <div class="flex items-center justify-around">
                    <div v-for="el of experience" :key="el.id">
                        <p>{{el.title}}</p>
                        <p>{{el.desc}}</p>
                    </div>
               </div>
            </div>
            <div class="w-1/2">
                <img src="../assets/images/2.jpg" alt="">
            </div>
        </div>
    </div>
</template>

<script setup>
    const experience = [
        {
            title: '1+',
            desc: 'Expreience'
        },
        {
            title: '5+',
            desc: 'Project Completed'
        },
        {
            title: '5+',
            desc: 'Happy Client'
        }
    ]
</script>

<style lang="scss" scoped>

</style>