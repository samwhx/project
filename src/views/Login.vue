<template>
  <div>
    <b-row>
    <b-col>
      <BackgroundBlueLeft />
    </b-col>
    <b-col>
      <LoginComponent />
    </b-col>
    </b-row>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';
import LoginComponent from '@/components/LoginComponent.vue';
import BackgroundBlueLeft from '@/components/BackgroundBlueLeft.vue';

@Component({
  components: {
    LoginComponent,
    BackgroundBlueLeft,
  },
})
export default class Login extends Vue {}
</script>

<style scoped lang="scss">
</style>
