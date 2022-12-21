<template>
  <div>
  <Hero/>
  <LargeCardDisplay
      v-for="largeCard in largeCardInfo"
      :key="largeCard.id"
      :largeCard="largeCard"
    />
    <SmallCardDisplay
    v-for="smallCard in smallCardSections"
    :key="smallCard.id"
    :smallCard="smallCard"
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
 