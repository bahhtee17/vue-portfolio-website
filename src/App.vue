<template>
  <div id="app">
    <div id="nav">
      <router-link class="home" to="/">Home</router-link>
      <router-link class="about" to="/about">About</router-link>
    </div>
    <router-view/>
  </div>
</template>

<script>

export default {

  data(){
    return{

    }
  },

  mounted(){


  }
}
</script>

<style scoped>
body{
  padding: 0;
  margin: 0;

}



#app #nav{



  font-family: Roboto;
 background: linear-gradient(to right, rgb(118, 118, 245), rgb(42, 97, 199));
  height: 50px;
  display: flex;
  justify-content: space-around;
  align-items: center;
  ;
  padding-left:3%;
  text-decoration: none;
}

.home{

  text-decoration: none;
  font-size: 2vw;
  color:white
}

.home:hover{
color: #ffffcd;
}

.about{
  font-size: 2vw;
  text-decoration: none;
  color:white
}

.about:hover{
  color: #ffffcd;
}

@media only screen and (max-width: 800px){
  .home{
    font-size: 3vw;
  }

  .about{
    font-size: 3vw;
  }
}




</style>
