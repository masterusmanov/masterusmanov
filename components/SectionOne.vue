<template>
    <div>
        <div clas></div>
        <div id="home" class="container mx-auto md:flex items-center justify-center md:gap-[70px] 2xl:gap-[136px] my-[70px] md:my-[126px] xl:px-[10px] 2xl:px-0">
            <div class="md:w-[70%] lg:w-1/2">
               <div class="px-[10px]">
                    <h1 class="text-[38px] lg:text-[48px] font-bold">Hello, I’m <br>Elyor Usmanov</h1>
                    <p class="text-[20px] text-justify text-gray-500 my-[24px]">My speciality is Full-stack software developer
                        (Backend and Frontend). I am very fond of
                        in this field. In the future, I want to be the
                        professional Full-stack software engineer,
                        and to reach my target, I am ready to go through
                        any troubles and learn new technologies.
                    </p>
                    <button class="px-[24px] py-[12px] bg-[#A53DFF] text-[18px] text-white font-[700] rounded-md">Contact</button>
               </div>
               <div class="flex items-center justify-between xl:gap-2 px-[10px] 2xl:justify-around my-[50px] md:my-0 md:mt-[50px] xl:mt-[80px] 2xl:mt-[142px]">
                    <div v-for="el of experience" :key="el.id" class="bg-[#F5EBFE] px-[10px] md:px-0 lg:px-[12px] 2xl:px-[12px] 2xl:py-[17px] xl:w-[180px] 2xl:w-[220px]">
                        <p class="xl:text-[32px] 2xl:text-[38px] font-bold text-center">{{el.title}}</p>
                        <p class="text-gray-500 text-center text-[14px] md:text-[16px] xl:text-[14px]">{{el.desc}}</p>
                    </div>
               </div>
            </div>
            <div class="md:w-[60%] lg:w-1/2">
                <img src="../assets/images/2.png" alt="My picture" class=" w-[90%] md:w-[100%] lg:w-[70%] rounded-xl mx-auto">
            </div>
        </div>
        <div id="about_me" class="container mx-auto xl:w-[95%] 2xl:w-[100%] bg-white md:flex items-center justify-between shadow-xl xl:px-[112px] lg:relative lg:top-14 xl:top-24 rounded-md">
            <div class="hidden lg:grid w-1/2">
                <img src="../assets/images/22.png" alt="My picture" class=" lg:w-[80%] 2xl:w-[70%] object-contain rounded-full object-center mx-auto xl:mx-0">
                <div class="flex items-center justify-around w-[50%] text-[32px] text-[#A53DFF] bg-white rounded-lg shadow-lg py-[12px] px-24px relative lg:top-[-80px] lg:left-[125px] xl:top-[-72px] xl:left-16">
                    <a href="#"><i class='bx bxl-telegram hover:bg-[#A53DFF] hover:text-white py-[12px] px-[12px] rounded-lg'></i></a>
                    <a href="#"><i class='bx bxl-linkedin hover:bg-[#A53DFF] hover:text-white py-[12px] px-[12px] rounded-lg' ></i></a>
                    <a href="#"><i class='bx bxl-github hover:bg-[#A53DFF] hover:text-white py-[12px] px-[12px] rounded-lg' ></i></a>
                </div>
            </div>
            <div class="px-[10px] md:px-[20px] lg:px-0 lg:w-[45%] xl:w-1/2">
                <h2 class="text-[38px] font-[700] lg:my-[32px]">I'm full-stack developer</h2>
                <p class="text-justify text-gray-600 md:mt-[30px] lg:mt-0 lg:px-[25px] xl:px-0">I have extensive knowledge and experience in the field of web application development. I love creating end-to-end interactive, modern, and user-centric websites. My main expertise lies in building full-stack web applications using Node.js, Vue.js, and React.js technologies.
                    I use the latest technologies for my work and adhere to modern approaches and best practices. I strive to fully understand my clients' needs and help them achieve their goals.
                    I also have a strong understanding of universal design principles to enhance the accessibility of web pages, mobile apps, and other digital products in terms of hearing, vision, and usability.
                    I constantly update my programming and web design knowledge, and also consider important issues such as security, privacy, and data protection. <br><br>
                    I am always eager to learn new technologies and improve my skills. I enjoy working closely with clients, understanding their objectives, and proposing the best solutions.
                    If you need full-stack developer services or web design assistance, I'm ready to offer you excellent solutions. I recommend you get in touch with me!</p>
                <div class="flex items-center py-[30px] lg:py-[30px] gap-2 md:gap-14 xl:gap-36  xl:my-[50px] 2xl:my-[32px]">
                    <a href="#" class="px-[24px] py-[12px] text-[#A53DFF] border border-[#A53DFF] rounded-lg font-[700] hover:bg-[#A53DFF] hover:text-white">My projects</a>    
                    <a href="#" download class="px-[24px] py-[12px] text-[#A53DFF] border border-[#A53DFF] rounded-lg font-[700] hover:bg-[#A53DFF] hover:text-white"><i class='bx bx-download mr-4 text-[20px]' ></i>Download CV</a>
                </div>
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