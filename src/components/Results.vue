<template>
  <p>Your time is: {{ score }} ms.</p>
  <p class="result">{{ rank }}</p>
</template>

<script>
export default {
 props: ['score'],
 data() {
   return {
     rank: null
   }
 },
 mounted() {
   if (this.score < 320) {
     this.rank = "You're blazing fast! \ud83d\ude08"
   } else if (this.score < 450) {
     this.rank = 'Not bad... \ud83d\ude0c'
   } else {
     this.rank = 'You need to train! \ud83d\ude02'
   }
 }
}
</script>

<style>
  p {
    font-weight: bold;
  }

  .result {
    font-size: 24px;
  }
</style>