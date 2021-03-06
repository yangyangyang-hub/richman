<template>
  <div id="app">
    <big-item></big-item>
  </div>
</template>

<script>
import BigItem from './components/bigItem'
export default {
  name: 'App',
  components: {
    BigItem
  }
}
</script>

<style lang="less" scoped>
@import './assets/css/normalize.css';
@import './assets/css/smallItem.css';
@import './assets/css/middleItem.css';
@import './assets/css/bigItem.css';

</style>>
