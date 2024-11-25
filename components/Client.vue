<template>
   <div class="gallery-container mt-[50px] md:my-[100px]">
    <div class="gallery">
      <img v-for="(src, index) in images" :key="index" :src="src" alt="" class=" w-[70px]  md:w-[100px]"/>
    </div>
  </div>
</template>

<script setup>
    import bestbux from '../public/images/Clients/bestbux.svg'
    import cosinus from '../public/images/Clients/cosinus.svg'
    import it_school from '../public/images/Clients/IT_school.jpg'
    import barber from '../public/images/Clients/barber.png'

    const images = [
        bestbux,
        it_school,
        cosinus,
        barber,
        bestbux,
        it_school,
        cosinus,
        barber,
        bestbux,
        it_school,
        cosinus,
        barber,
        // Duplicate images to create the seamless scroll effect
        bestbux,
        it_school,
        cosinus,
        barber,
        bestbux,
        it_school,
        cosinus,
        barber,
        bestbux,
        it_school,
        cosinus,
        barber,,
    ];
</script>


<style lang="scss" scoped>
    .gallery-container {
        /* width: 100%; */
        overflow: hidden;
        position: relative;
    }

    .gallery {
        display: flex;
        animation: scroll 25s linear infinite;
        gap: 20px;
        width: max-content;
    }

    .gallery img {
        /* width: 200px; */
        /*height: 100px;*/
        margin-right: 10px;
    }

    @keyframes scroll {
        0% {
            transform: translateX(0);
        }

        100% {
            transform: translateX(-50%);
        }
    }
</style>