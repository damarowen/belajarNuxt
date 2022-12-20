<template>
  <div>
  <Hero/>
  <LargeCardDisplay
      v-for="cardInfo in largeCardInfo"
      :key="cardInfo.id"
      :cardsSection="cardInfo"
    />
    </div>

</template>

<script lang="ts">
import { largeCardSections, smallCardSections } from "@/assets/data.js"
export default {
  data(){
    return {
      largeCardInfo: largeCardSections,
      smallCardSections: smallCardSections
    }
  }
}
</script>
 