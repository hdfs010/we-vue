<template>
  <header class="wv-header" :class="{ 'is-fixed': fixed }">
    <div class="left">
      <slot name="left"></slot>
    </div>
    <h1 class="wv-header-page__title" v-text="title"></h1>
    <div class="wv-header-button">
      <slot name="right"></slot>
    </div>
  </header>
</template>

<script type="text/babel">
export default {
  name: 'wv-header',

  props: {
    title: String,
    skin: {
      type: String,
      default: 'ios'
    },
    fixed: {
      type: Boolean,
      default: true
    }
  }
}
</script>

<style scoped lang="scss">
  .wv-header {
    display: block;
    overflow: hidden;
    background-color: black;
    width: 100%;
    color: white;

    &.is-fixed {
      position: fixed;
      left: 0;
      top: 0;
    }
  }
</style>
