<template>
  <div id="big">
    <table>
      <tr v-for="(item, index) in row" :key="index">
        <td v-for="(item, index) in row" :key="index" class="td"></td>
      </tr>
      <img src="" alt="">
    </table>
  </div>
</template>

<script>
export default {
  data() {
    return {
      row: 20,
      col: 20,
    };
  },
};
</script>

<style lang="less" scoped>
#big {
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    
  table {
    border-collapse: collapse;
    border: 1px solid #aaa;
  }
  .td {
    width: 2rem;
    height: 2rem;
    border: 1px solid black;
    padding: 0;
  }
}
</style>
