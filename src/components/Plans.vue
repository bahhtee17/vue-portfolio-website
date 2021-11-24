<template>
  <div class="container">
<button @click="change = !change">Animation</button>
<transition name="scale"
enter-active-class="animate__animated animate__tada" leave-active-class="animate__animated animate__bounceOutRight">
    <div v-if="change" class="first-time">

     </div>
</transition>



     <div class="monthly">

     </div>

     <div class="yearly">

     </div>
  </div>
</template>

<script>
import 'animate.css';
export default {
    data(){
        return{
            change: true
        }
    }

}
</script>

<style scoped>



  .container{
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
      .container{
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



