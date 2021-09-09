<template>
  <h4>Reaction time - {{ result }} ms</h4>
  <p class="rank">{{ rank }}</p>
</template>

<script>
export default {
  props: ["result"],
  data() {
    return {
      rank: null,
    };
  },

  mounted() {
    if (this.result < 250) {
      this.rank = "Ninja Fingers";
    } else if (this.result < 400) {
      this.rank = "Rapid Reflexes";
    } else {
      this.rank = "Snail Pace";
    }
  },
};
</script>

<style>
.rank {
  font-size: 1.4rem;
  color: #0faf87;
  font-weight: bold;
}
</style>
