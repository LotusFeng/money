<template>
  <div class="wrapper" ref="wrapper"></div>
</template>

<script lang="ts">
import * as echarts from 'echarts';
import {Component, Prop, Vue} from 'vue-property-decorator';

@Component
export default class Chart extends Vue {
  @Prop() options?: any;

  mounted() {
    if (this.options === undefined) {
      return console.error('option为空');
    }
    const chart = echarts.init(this.$refs.wrapper as HTMLDivElement);
    chart.setOption(this.options);
  }
}
</script>

<style scoped lang="scss">
.wrapper {
  height: 400px;
}
</style>