<template>
  <div class="container-plan">


    <div @mouseover="animatedMouseOver('.first-time')" @mouseleave="animatedMouseLeave('.first-time')"  class="first-time">

     </div>


     <div  @mouseover="animatedMouseOver('.monthly')" @mouseleave="animatedMouseLeave('.monthly')" class="monthly">

     </div>

     <div  @mouseover="animatedMouseOver('.yearly')" @mouseleave="animatedMouseLeave('.yearly')" class="yearly">

     </div>
  </div>
</template>

<script>

import { ScrollTrigger } from "gsap/ScrollTrigger";
import { gsap } from "gsap";
export default {
data(){
    return{
      trigger: false
    }
},

methods:{

    animatedMouseOver(className){
         gsap.to(className, {
         opacity:0
      })
    },
   animatedMouseLeave(el){
     gsap.to(el, {
         opacity:1
     })
   }

},



mounted(){
     gsap.registerPlugin(ScrollTrigger);







     gsap.set('.first-time', {
       opacity: 0,
       x: 700,
     })

     gsap.to('.first-time', {
         opacity: 1,
         x: 0,
         duration: 10,
         ease: "back.out(1.7)",
         scrollTrigger:{
             trigger: '.container-plan',
             start: 'top 90%',
             end: 'top 20%',
             markers: true,
             scrub: true,
         }
     })

     gsap.set('.monthly', {
         opacity: 0,
         x: 700
     })

     gsap.to('.monthly', {
         opacity: 1,
         x: 0,
         duration: 11,
         ease: "back.out(1.7)",
         scrollTrigger: {
             trigger: '.container-plan',
             start: 'top 90%',
             end: 'top 20%',
             markers: true,
             scrub: true
         }
     })

     gsap.set('.yearly', {
         opacity: 0,
         x: 700
     })

     gsap.to('.yearly', {
         opacity: 1,
         x: 0,
         duration: 12,
         ease: "back.out(1.7)",
         scrollTrigger: {
             trigger: '.container-plan',
             start: 'top 90%',
             end: 'top 20%',
             markers: true,
             scrub: true
         }
     })
}
}
</script>

<style scoped>



  .container-plan{
      display: flex;
      justify-content: space-around;
      align-items: center;
      background: linear-gradient(to right, #A7A7E0, #99F7D5);
      width: 100%;
      height: 35vw;

  }

  .first-time{
      border-radius: 5%;
      width: 20%;
       box-shadow: 10px 10px 5px #9CA1F7;
      height: 65%;
      background-color: antiquewhite;
  }

  .monthly{
      border-radius: 5%;
      box-shadow: 10px 10px 5px #9CA1F7;
      width: 20%;
      height: 65%;
      background-color: antiquewhite;
  }

  .yearly{
      border-radius: 5%;
      width: 20%;
       box-shadow: 10px 10px 5px #9CA1F7;
      height: 65%;
      background-color: antiquewhite;
  }

  @media only screen and (max-width:800px){
      .container-plan{
          height: 50vw;
          flex-direction: column;
      }

      .first-time{
          height: 30%;
          width: 60%;
           box-shadow: 3px 3px 5px #9CA1F7;
      }

      .monthly{
          height: 30%;
          width: 60%;
           box-shadow: 3px 3px 5px #9CA1F7;
      }

      .yearly{
        height: 30%;
          width: 60%;
           box-shadow: 3px 3px 5px #9CA1F7;
      }
  }
</style>



