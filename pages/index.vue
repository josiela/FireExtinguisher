<template>
  <div>
    <Nav/>
    <div class="container">
      <!-- we pull each component in: -->
      <Hero/>
      <!-- So instead of calling them in manually with
      <LargeCardDisplay/>
      we can call it in with a v-for-loop -->
      <LargeCardDisplay
        v-for="cardInfo in largeCardInfo" :key="cardInfo.id"
        :cardSection="cardInfo"
      />
      <SmallCardDisplay
        v-for="cardInfo in smallCardSections" :key="cardInfo.id"
        :cardSection="cardInfo"
      />
    </div>
  </div>
</template>

<script>
//why largeCardSections: in data.js the const in which the data is stored is calles largeCardSections so we're calling that const
  import { largeCardSections, smallCardSections } from '@/assets/data.js';
  export default {
    data() {
      return {
        //associate largeCardInfo with the data-const
        largeCardInfo: largeCardSections,
        smallCardSections
      }
    }
  }
</script>

<style scoped>

</style>