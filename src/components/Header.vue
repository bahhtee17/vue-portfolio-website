<template>
  <header class="container">
    <div class="header">
       <h1>Skyjump</h1>
    </div>

    <div class="sub-header">
        <h3>Feel gravity in your skin</h3>
    </div>

    <div class="btn">
        <button>Buy now</button>
    </div>
  </header>
</template>

<script>

export default {

}
</script>

<style scoped>



  .container{
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
 }

 .sub-header h3{
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
     .container{
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


