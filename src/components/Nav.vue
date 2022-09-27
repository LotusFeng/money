<template>
  <div class="nav">
    <router-link to="/money">
      <svg>
        <use xlink:herf="#Momey"/>
      </svg>
      记账
    </router-link>
    |
    <router-link to="/labels">标签</router-link>
    |
    <router-link to="/statistics">统计</router-link>
  </div>
</template>

<script lang="ts">
import x from '@/assets/icons/Money.svg';

console.log(x);

export default {
  name: 'Nav'
};
</script>

<style lang="scss" scoped>

</style>