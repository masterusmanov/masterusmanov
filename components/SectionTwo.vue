<template>
    <div class="bg-[#F0F1F3] xl:pt-[200px] xl:pb-[100px] 2xl:pt-[248px] 2xl:pb-[140px]">
        <div class="container mx-auto flex items-center justify-between xl:px-[10px] 2xl:px-0">
            <div class="w-[45%] py-[160px]">
                <h2 class="text-[38px] font-[700]">Work process</h2>
                <p class="text-gray-500 text-justify mt-[24px]">Comprehensive web development services encompassing both frontend and backend development, database management, API integration, security implementation, responsive design, SEO optimization, server configuration, and monitoring. Delivering high-performance software solutions using cutting-edge technologies (Vue or React, Node.js) and robust databases (PostgreSQL, MySQL, MongoDB) tailored to meet client specifications. Ensuring quality assurance throughout each project phase, including rigorous testing, bug fixing, and system optimization. <br><br> Additionally, offering services for legacy system modernization, feature enhancement, and ongoing technical support to ensure optimal performance and user satisfaction."</p>
            </div>
            <div class="w-1/2 flex items-center justify-around ">
                <div class="grid gap-[24px]">
                    <div v-for="card in firstRowCards" :key="card.id" class="xl:w-[300px] xl:h-[350px] 2xl:w-[350px]  2xl:h-[300px] bg-white rounded-lg shadow-lg p-6 hover:shadow-xl transition-shadow duration-300">
                        <i :class="[card.icon, 'text-4xl text-[#A53DFF] border border-[#A53DFF] p-[20px] rounded-lg hover:bg-[#A53DFF] hover:text-white  mb-4']"></i>
                        <h3 class="text-xl font-bold mb-3">{{ card.title }}</h3>
                        <p class="text-gray-600 text-justify text-[14px]">{{ card.desc }}</p>
                    </div>
                </div>
                <div class="grid gap-[24px] mt-[48px]">
                    <div v-for="card in secondRowCards" :key="card.id" class="xl:w-[300px] xl:h-[350px] 2xl:w-[350px] 2xl:h-[300px] bg-white rounded-lg shadow-lg p-6 hover:shadow-xl transition-shadow duration-300">
                        <i :class="[card.icon, 'text-4xl text-[#A53DFF] border border-[#A53DFF] p-[20px] rounded-lg hover:bg-[#A53DFF] hover:text-white  mb-4']"></i>
                        <h3 class="text-xl font-bold mb-3">{{ card.title }}</h3>
                        <p class="text-gray-600 text-justify text-[14px]">{{ card.desc }}</p>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script setup>
    import { computed } from 'vue'

    const card = [
        {
            id: 1,
            icon: 'bx bx-notepad',
            title: 'Research',
            desc: 'As a full-stack developer and researcher, I am deeply passionate about exploring new technologies and their practical applications in web development.'
        },
        {
            id: 2,
            icon: 'bx bx-pencil',
            title: 'Design',
            desc: " I believe in the perfect blend of aesthetics and functionality. My design philosophy centers on creating intuitive, user-centric solutions that not only look stunning but also serve their purpose effectively."
        },
        {
            id: 3,
            icon: 'bx bx-line-chart',
            title: 'Analyze',
            desc: 'As a full-stack developer with strong analytical skills, I specialize in transforming complex data into actionable insights. My analytical approach combines technical expertise with strategic thinking to deliver optimal solutions.'
        },
         {
            id: 4,
            icon: 'bx bx-rocket',
            title: 'Launch',
            desc: 'As a seasoned full-stack developer, I follow a systematic and comprehensive approach to project launches. My methodology ensures smooth deployment and successful project implementation.'
        }
    ]

    const firstRowCards = computed(() => card.slice(0, 2))
    const secondRowCards = computed(() => card.slice(2, 4))
</script>

<style lang="scss" scoped>

</style>