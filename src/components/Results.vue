<template>
  <p> Your time is: {{ score }} ms.</p>
</template>

<script>
export default {
 props: ['score']
}
</script>

<style>
  p {
    font-weight: bold;
  }
</style>