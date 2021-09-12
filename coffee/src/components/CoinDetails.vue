<script>
export default {
  props: {
    coinInfo: Object
  },
  computed: {
    getCoinIcon: (props) => { return `assets/coin-icons/${props.coinInfo.code}.svg`; },
    getCoinQrCode: (props) => { return `assets/coin-qr-codes/${props.coinInfo.code}.jpeg`; },
  },
  setup (props) {
    return {
      ...props.coinInfo,
    }
  }
};
</script>

<template>
  <div
    class="me-3 mb-3 pt-3 pt-md-0 px-3 px-md-3 text-center overflow-hidden"
    :class="bgColor + ' ' + (textColor)"
  >
    <div class="my-3 pt-3">
      <div class="coin-icon px-1 py-1 shadow-sm rounded-circle"><img :src="getCoinIcon" /></div>
      <h2 class="display-6 mt-2 text-truncate">{{ name }}</h2>
      <!-- <p class="lead text-break">{{ address }}</p> -->
      <div class="form-group">
        <label for="exampleFormControlTextarea1">Address</label>
        <textarea
          class="form-control"
          :class="textColor"
          rows="2"
          spellcheck="false"
          readonly
          style="background: transparent; border: 0; resize: none;"
          onclick="this.select()"
        >{{ address }}</textarea>
      </div>
    </div>
    <div class="shadow-sm mx-auto qr-code" :class="imgBgColor">
      <img :src="getCoinQrCode" />
    </div>
  </div>
</template>

<style scoped>
.qr-code {
  max-width: 90%;
  border-radius: 21px 21px 0 0;
  overflow: hidden;
}
.qr-code img {
  width: 100%;
  display: block;
  margin: 0 auto;
}
.cut-text { 
  text-overflow: ellipsis;
  overflow: hidden; 
  width: 160px; 
  height: 1.2em; 
  white-space: nowrap;
}
.coin-icon {
  background: #fff;
  display: inline-block;
}
.coin-icon img {
  width: 48px;
  height: 48px;
}
</style>
