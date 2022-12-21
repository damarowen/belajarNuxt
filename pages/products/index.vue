<template>
    <div class="container">
        <LargeCardDisplay
            v-for="largeCard in largeCardInfo.slice(0,1)"
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

<script>
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

<style scoped>

</style>