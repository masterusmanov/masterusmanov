<template>
    <div>
        <div clas></div>
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
               <div class="flex items-center justify-around mt-[142px]">
                    <div v-for="el of experience" :key="el.id" class="bg-[#F5EBFE] px-[12px] py-[17px] w-[220px]">
                        <p class="text-[38px] font-bold text-center">{{el.title}}</p>
                        <p class="text-gray-500 text-center">{{el.desc}}</p>
                    </div>
               </div>
            </div>
            <div class="w-1/2 block">
                <img src="../assets/images/2.png" alt="My picture" class="w-[70%] rounded-xl mx-auto">
            </div>
        </div>
        <div id="about_me" class="container mx-auto flex items-center justify-between shadow-xl pt-[70px] px-[112px] relative top-40 bg-white">
            <div class="w-1/2">
                <img src="../assets/images/22.png" alt="My picture" class="w-[70%] object-contain rounded-full object-center">
                <div class="flex items-center justify-around w-[50%] text-[32px] text-[#A53DFF] bg-white rounded-lg shadow-lg py-[12px] px-24px relative top-[-72px] left-16">
                    <a href="#"><i class='bx bxl-telegram hover:bg-[#A53DFF] hover:text-white py-[12px] px-[12px] rounded-lg'></i></a>
                    <a href="#"><i class='bx bxl-linkedin hover:bg-[#A53DFF] hover:text-white py-[12px] px-[12px] rounded-lg' ></i></a>
                    <a href="#"><i class='bx bxl-github hover:bg-[#A53DFF] hover:text-white py-[12px] px-[12px] rounded-lg' ></i></a>
                </div>
            </div>
            <div class="w-1/2">
                <h2 class="text-[38px] font-[700] my-[32px]">I'm full-stack developer</h2>
                <p class="text-justify text-gray-600">I have extensive knowledge and experience in the field of web application development. I love creating end-to-end interactive, modern, and user-centric websites. My main expertise lies in building full-stack web applications using Node.js, Vue.js, and React.js technologies.
                    I use the latest technologies for my work and adhere to modern approaches and best practices. I strive to fully understand my clients' needs and help them achieve their goals.
                    I also have a strong understanding of universal design principles to enhance the accessibility of web pages, mobile apps, and other digital products in terms of hearing, vision, and usability.
                    I constantly update my programming and web design knowledge, and also consider important issues such as security, privacy, and data protection. <br><br>
                    I am always eager to learn new technologies and improve my skills. I enjoy working closely with clients, understanding their objectives, and proposing the best solutions.
                    If you need full-stack developer services or web design assistance, I'm ready to offer you excellent solutions. I recommend you get in touch with me!</p>
                <div class="flex items-center gap-36 my-[32px]">
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