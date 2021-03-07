<template>
  <div id="big">
    <div class="border">
      <img
        src="../assets/img/coin.png"
        alt=""
        class="coin"
        :style="{
          top: coinT + 'rem',
          left: coinL + 'rem',
          width: coinH + 'rem',
          height: coinH + 'rem',
        }"
      />

      <img
        src="../assets/img/man.png"
        alt=""
        class="man"
        :style="{
          top: manT + 'rem',
          left: manL + 'rem',
          width: manH + 'rem',
          height: manH + 'rem',
        }"
      />
    </div>
  </div>
</template>

<script>
export default {
  name: "big",
  data() {
    return {
      manT: 30,
      manH: 5,
      manL: 0,

      coinH: 3,
      coinL: 0,
      coinT: 0,
      coinRealT: 0,

      differT: 0,
      differL: 0,
      s: true,
    };
  },
  mounted() {
    this.moveDown();
    window.onkeydown = e => {
        console.log(1);
    }
  },
  methods: {
    keydown() {

    },
    produceCoin(n) {
        this.coinT = 1;
        this.s = true
        this.coinL = Math.floor(Math.random()*39+0);

    },
    moveDown() {
      const that = this;
      that.timeDown = setInterval(function () {
        that.coinT += 0.1;
        that.countDistance(that);
      }, 1000);
    },
    countDistance(that) {
      this.differT = this.manT - this.coinT;
      if (this.differT < 0 ) {
          if(this.s) {
              console.log();
              alert("d的一份")
              this.s = false
              this.produceCoin(this.differT)
          }

        
        
        
      }
    },
  },
};
</script>

<style lang="less" scoped>
#big {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  color: blue;
  height: 40rem;
  width: 40rem;
  .border {
    position: absolute;
    height: 38rem;
    width: 40rem;
    border: 1px solid black;
    // overflow: hidden;
      .man {
    position: absolute;
  }
  .coin {
    position: absolute;
  }
  }

}
</style>
