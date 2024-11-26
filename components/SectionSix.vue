<template>
    <div class="bg-gray-500 py-[100px]">
        <div id="service" class="container mx-auto">
             <h2 class="text-[38px] font-[700] text-center">Happy Clients</h2>
            <p class="w-[90%] md:w-[70%] mx-auto mt-[24px] text-center">By combining our technical expertise, industry knowledge, and client-centric mindset, we are able to consistently deliver projects that exceed expectations and foster long-term, mutually beneficial relationships. Our clients know they can count on us to be reliable, responsive, and dedicated partners in their success.</p>
        </div>
        <div>
            <Client/>
        </div>
        <div class="container mx-auto text-white">
            <div class="bg-white text-black py-[88px] rounded-md md:p-[88px] grid grid-cols-1 lg:grid-cols-2 justify-between relative top-40">
                <div class="w-[100%] ">
                    <h2 class="text-center lg:text-left text-[32px] font-[700]">Let’s discuss your Project</h2>
                    <p class="lg:w-[90%] xl:w-[100%] text-center lg:text-left text-gray-500 mt-[24px] px-[10px] md:px-0">I'd welcome the opportunity to discuss how my skills in modern web technologies, API integration, and user experience design could benefit your upcoming initiatives. </p>      
                    <div>
                        <div v-for="el of address" :key="el.id" class="flex items-center gap-[10px] my-[12px] p-[24px] w-[90%] md:w-[80%] xl:w-[70%] hover:shadow-xl hover:border-l-4 hover:border-[#A53DFF] ">
                            <i :class="el.icon" class=" w-[50px] text-center text-[24px] bg-[#F5EBFF] hover:bg-[#A53DFF] hover:text-white rounded-lg py-[10px] px-[10px]"></i>
                            <div>
                                <p class="text-gray-500 text-[14px]">{{el.titul}}</p>
                                <p class="font-[500] text-[16px]">{{el.title}}</p>
                            </div>
                        </div>
                    </div>
                    <div class="mx-[20px] md:mx-0 flex items-center justify-around w-[50%] text-[32px] text-[#A53DFF] bg-white rounded-lg shadow-lg py-[12px] px-24px mt-[24px]">
                        <a href="#"><i class='bx bxl-telegram hover:bg-[#A53DFF] hover:text-white py-[12px] px-[12px] rounded-lg'></i></a>
                        <a href="#"><i class='bx bxl-linkedin hover:bg-[#A53DFF] hover:text-white py-[12px] px-[12px] rounded-lg' ></i></a>
                        <a href="#"><i class='bx bxl-github hover:bg-[#A53DFF] hover:text-white py-[12px] px-[12px] rounded-lg' ></i></a>
                    </div>
                </div>
                <div class=" mt-[48px] lg:mt-0 ">
                    <form action="" class="grid gap-[70px] mx-auto w-[80%]">
                        <h2 class="text-center lg:text-left text-[32px] font-[700]">Are there any questions?</h2>
                        <input type="text" name="name" id="name" placeholder="Full name *" class=" outline-none border-b border-gray-500 text-[20px] p-[10px]">
                        <input type="tel" name="phone" id="phone" placeholder="Your phone number *" class="outline-none border-b border-gray-500 text-[20px] p-[10px]">
                        <input type="submit" value="Submit" class="bg-[#A53DFF] text-white rounded-md font-[700] text-[20px] w-[150px] py-[10px]">
                    </form>
                </div>
            </div>
        </div>
    </div>
</template>

<script setup>
    const address = [
        {
            id: 1,
            icon: 'fa-solid fa-location-dot',
            titul: 'Address:',
            title: 'Toshkent, Mirzo Ulugbek, Namangan, Uchkurgan 160900'
        },
        {
            id: 2,
            icon: 'bx bx-mail-send',
            titul: 'My Email:',
            title: 'elyor.usmanov87@mail.ru, elyor.usmanov22@gmail.com'
        },
        {
            id: 3,
            icon: 'bx bx-phone-call',
            titul: 'Call Me Now',
            title: '+998972179900'
        }
    ]
</script>

<style lang="scss" scoped>

</style>