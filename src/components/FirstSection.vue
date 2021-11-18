<template>
 <div class="container">

    <div class="img-container">
        <img class="image" src="../assets/images/section_01.jpg"/>
    </div>

    <div class="text">
       <h3 class="header">Tandem Skydive</h3>
       <p> For the spirited adrenaline junkie, there really is no greater challenge. This tandem skydive is the ultimate test of bravery for all thrill seekers, as you plummet from the plane. After your short briefing you will be kitted up in a jumpsuit ready to board the plane. An anxious 25-minute flight to reach the jump height will give you all the time you need to test your nerves to their limits, before you’re finally ready to take that leap of faith. Once harnessed to your fully qualified tandem partner, there is no going back as you fall through the sky, reaching speeds of 120mph. A truly unique sensation! Once you reach around 5000ft the instructor will deploy the parachute and you’ll float back down to solid ground, completing a memory that will stay with you for the rest of your life.</p>
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