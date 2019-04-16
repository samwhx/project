<template>
  <div>
    <img src="../assets/Main.png" />
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';

@Component
export default class BackgroundBlueLeft extends Vue {
}
</script>

<style scoped lang="scss">
img {
  padding: 0;
  display: block;
  margin: 0 0;
  height: 98vh;
  max-height: 100%;
  min-width: 100%;
}
</style>
