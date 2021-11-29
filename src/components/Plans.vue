<template>
  <div class="container-plan">


    <div @mouseenter="animatedMouseOver('.first-time')" @mouseout="animatedMouseLeave('.first-time')"  class="first-time">

     </div>


     <div  @mouseenter="animatedMouseOver('.monthly')" @mouseout="animatedMouseLeave('.monthly')" class="monthly">

     </div>

     <div  @mouseenter="animatedMouseOver('.yearly')" @mouseout="animatedMouseLeave('.yearly')" class="yearly">

     </div>


  </div>
</template>

<script>

import Scene from "scenejs";
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
         rotate: 90,
      })
    },
   animatedMouseLeave(el){
     gsap.to(el, {
         rotate: 0,
         duration: 1,
         ease: "back.out(1.7)",
         repeat: 0,
     })
   }

},



mounted(){

     const scene = new Scene({
            '.container-plan': [
                {
                  'background-position': '0 50%'
                },

                {
                    'background-position': '50% 100%'
                }
            ]
        },
        {
            duration: 10,
            easing: Scene.EASE_IN_OUT,
            selector:true,
            direction: 'alternate',
            iterationCount: "infinite",
        }).playCSS();



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
      background-position: 0 50%;
      display: flex;
      justify-content: space-around;
      align-items: center;
      background: linear-gradient(45deg, #A7A7E0, #b8d633, #85d819);
      background-size: 400% 300%;
      width: 100%;
      height: 35vw;

  }

  .first-time{
      border-radius: 5%;
      width: 20%;
       box-shadow: 5px 5px 3px #e3ecba;
      height: 65%;
      background-color: antiquewhite;
  }

  .monthly{
      border-radius: 5%;
      box-shadow: 5px 5px 3px #e3ecba;
      width: 20%;
      height: 65%;
      background-color: antiquewhite;
  }

  .yearly{
      border-radius: 5%;
      width: 20%;
       box-shadow: 5px 5px 3px #e3ecba;
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



