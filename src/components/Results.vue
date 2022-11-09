<template>
  <p>Reaction Time: {{ score }} ms</p>
  <p>Rank : {{ rank }}</p>
</template>

<script>
export default {
  props: ["score"],
  data() {
    return {
      rank: null,
    };
  },
  mounted() {
    if (this.score < 250) {
      this.rank = "Damn Fast";
    } else if (this.score < 400) {
      this.rank = "Good but not Fast";
    } else {
      this.rank = "slow";
    }
  },
};
</script>

<style>
</style>