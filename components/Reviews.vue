<template>
    <div>
        <h3>Customer Reviews</h3>
        <div v-if="!$fetchState.pending">
            <ReviewCard
                v-for="reviewer in reviewers.results"
                :key="reviewer.login.uuid"
                :review="reviewer"
            />
        </div>
        <div v-else>
            Loading.....
        </div>
    </div>
</template>

<script>
function sleep(ms) {
  return new Promise(resolve => setTimeout(resolve, ms));
}

    export default {
        data(){
            return {
                reviewers: []
            }
        },
        async fetch() {
                await sleep(5000).then(async () => {
                    this.reviewers = await fetch('https://randomuser.me/api/?results=5').then((res) => res.json())
                })

        }
    }
</script>

<style lang="scss" scoped>

</style>