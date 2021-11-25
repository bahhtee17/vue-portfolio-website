<template>
 <div class="container2">

    <div class="img-container">
        <img class="image" src="../assets/images/section_02.jpg"/>
    </div>

    <div class="text">
       <h3 class="header">INDOOR SKYDIVING IS REAL FLYING</h3>
       <p> Experience the sensation of flying in our state-of-the-art vertical wind tunnels. Safe for all ages, experience levels and abilities, indoor sky diving at iFLY is a family-friendly activity perfect for kid’s birthday parties, corporate events, team building, and more.</p>
    </div>


 </div>

</template>

<script>

import { ScrollTrigger } from "gsap/ScrollTrigger";
import { gsap } from "gsap";
export default {

mounted(){
 gsap.registerPlugin(ScrollTrigger);

 gsap.set('.container2', {
     opacity: 0,
     x: 700,
 })

 gsap.to('.container2', {
     opacity: 1,
     x: 0,
     duration: 3,
     ease: "power2.out",
     scrollTrigger: {
         trigger: '.container2',
         start: 'top 90%',
         end: 'top 20%',
         scrub: true,
         markers: true,

     }
 })

}
}
</script>

<style scoped>
.container2{
    display: flex;
    width: 100%;
    font-size: 60%;
     height: 30vw;
     flex-direction: row-reverse;
    justify-content: center;
    color: black;




}

.text .header{
    font-size: 3em;
    font-family: Roboto;
    color:#b66358;
    line-height: 1em;
    font-weight: 100;
}

.text p{
color:rgb(44, 78, 78)
}


 .img-container .image{
  height: 90%;
  background-size: cover;
}

.text{
    text-align: center;
    padding: 0% 3% 0% 3%;
    height: 90%;
    letter-spacing: 0.1em;
    line-height: 1.5em;
    background-color: aliceblue;
}

@media only screen and (max-width: 800px){
    .container2{
        height: 110vw;
        display: inline-flex;
        flex-direction: column;
    }

    .img-container .image{
        width: 100%;
    }
}
</style>