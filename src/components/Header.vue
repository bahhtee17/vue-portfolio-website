<template>
  <header class="container-header">
    <div class="header">
       <h1 class=" .animate__bounce animate__backInDown ">Skyjump</h1>
    </div>

    <div class="sub-header">
        <h3 class="animate__backInRight">Feel gravity in your skin</h3>
    </div>

    <div class="btn">
        <button class="buy-btn">Buy now</button>
    </div>
  </header>
</template>

<script>

import 'animate.css';
import { gsap } from "gsap";
export default {

mounted(){



    gsap.set('.container-header', {
        scale: 0,
    })
    gsap.to('.container-header', {
        duration: 3,
        ease: "elastic.out(1, 0.3)",
        opacity: 1,
        scale: 1,
    })

    gsap.set('.buy-btn', {
        opacity: 0,
        y: 400
    })

    gsap.to('.buy-btn', {
        opacity: 1,
        y: 0,
        duration: 2,
        ease: "bounce.out"


    })

}

}
</script>

<style scoped>



  .container-header{

      display: flex;
      width: 100%;
      height: 40vw;
      background: linear-gradient(to right, #7297a6bd, #033e8cbb), url(../assets/images/bg-header.jpg);
      background-size: cover;
      justify-content: center;
      flex-direction: column;
      align-items: center;
  }

 .header h1{

     font-family: Roboto;
     color: #C2D2F2;
     height: 2vw;
     font-style: normal;
     font-size: 6vw;
     letter-spacing: 0.2em;
     font-weight: 300;
     text-transform: uppercase;
     animation-duration: 2s;
     animation-delay: 0s;

 }

 .sub-header h3{

     animation-duration: 2s;
     animation-delay: 0s;
     color: #C2D2F2;
     font-family: Roboto;
     font-style: normal;
     font-size: 2vw;
     text-transform: uppercase;
     font-weight: 300;
 }

 .btn button{
      font-family: Roboto;
      font-size: 1.5vw;
     border: none;
     width: 10vw;
     padding: 5px;
     text-transform: uppercase;
     border-radius: 10px;
     background-color: #E6C410;
 }
 .btn button:hover{
     background-color: #f3dc68;
 }

 @media only screen and (max-width: 800px) {
     .container-header{
         height: 100vw;
     }

     .header h1{
         height: 3vw;
         font-size: 10vw;
     }

     .sub-header h3{
         font-size: 3vw;
     }

     .btn button{
         width: 20vw;
         font-size: 3vw;
     }
 }

</style>


