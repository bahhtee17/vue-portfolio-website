<template>
  <div class="home">
    <div class="header">
       <Header/>
    </div>

    <div class="firstSection">
      <FirstSection />
    </div>

    <div class="secondSection">
      <SecondSection/>
    </div>

    <div class="thirdSection">
       <ThirdSection />
    </div>

    <div class="plans">
      <Plans />
    </div>
  </div>

</template>

<script>

import Header from '../components/Header.vue'
import FirstSection from '../components/FirstSection.vue'
import SecondSection from '../components/SecondSection.vue'
import ThirdSection from '../components/ThirdSection.vue'
import Plans from '../components/Plans.vue'
export default {
  name: 'Home',
  components: {
    Header,
    FirstSection,
    SecondSection,
    ThirdSection,
    Plans
  }
}
</script>


<style scoped>
 .header{
  margin-bottom: 5%;
 }




 @media only screen and (max-width: 800px){
  .firstSection{
    margin-bottom: 5%;
  }
 }

</style>