<template>
 <div class="container">

    <div class="img-container">
        <img class="image" src="../assets/images/section_03.jpg"/>
    </div>

    <div class="text">
       <h3 class="header">Static Line Parachuting </h3>
       <p> They say that the first solo parachute jump is always the one you remember the most. There is no chance of you forgetting this opportunity. This splendid package puts you on a two day tuition course at the end of which you will make a solo parachute jump. The first day you'll do both theoretical and practical sessions on a range of subjects – safety regulation, sky diving techniques, steering, landing and many others in order to prepare you for the jump ahead. On the second day you'll be taken up to 3000ft, the aeroplane door will be opened and you will launch yourself into the void. The static line will release the parachute and you will drift slowly to earth, admiring the beautiful view and the complete tranquillity as you do so.</p>
    </div>


 </div>

</template>

<script>
export default {

}
</script>

<style scoped>
.container{
    display: flex;
    width: 100%;
    font-size: 60%;
     height: 30vw;

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
    .container{
        height: 110vw;
        display: inline-flex;
        flex-direction: column;
    }

    .img-container .image{
        width: 100%;
    }
}
</style>