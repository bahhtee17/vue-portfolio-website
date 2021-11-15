<template>
  <div id="app">
    <div id="nav">
      <router-link class="home" to="/">Home</router-link>
      <router-link class="about" to="/about">About</router-link>
    </div>
    <router-view/>
  </div>
</template>

<style>
body{
  padding: 0;
  margin: 0;
}

#app #nav{
  font-family: Roboto;
 background-color: #A6998A;
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

@media only screen and (max-width: 600px){
  .home{
    font-size: 3vw;
  }

  .about{
    font-size: 3vw;
  }
}




</style>
