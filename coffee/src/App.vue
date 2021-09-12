<script setup>
import CoinDetails from './components/CoinDetails.vue'
import SiteHeader from './components/SiteHeader.vue'
import coinData from './shared/data';
import { ref } from 'vue'
const data = ref(coinData);
</script>

<template>
  <SiteHeader></SiteHeader>
  <main>
    <div class="py-3 border-bottom border-top" id="pay-by-cryptocurrency">
      <div class="container d-flex flex-wrap justify-content-center">
        <a href="#pay-by-cryptocurrency" class="d-flex align-items-center text-dark text-decoration-none">
          <span class="fs-4 d-flex align-items-center"><i class="fab fa-bitcoin fs-1 mx-3"></i> Cryptocurrency</span>
        </a>
      </div>
    </div>
    <!-- <div class="px-3  mt-3">
      <form class="form-inline">
        <div class="input-group">
          <div class="input-group-prepend">
            <span class="input-group-text" id="basic-addon1">@</span>
          </div>
          <input class="form-control mr-sm-2" type="search" placeholder="Start typing.." aria-label="Search">
        </div>
      </form>
    </div> -->
    <div class="container-fluid">
      <div class="row ms-1 pt-3">
        <div
          class="col-sm-12 col-md-6 col-lg-4 col-xl-3 px-0"
          v-for="(coin, index) in data"
          :key="coin.code"
          :data-index="index"
        >
          <CoinDetails :coinInfo="coin" />
        </div>
      </div>
    </div>
  </main>
</template>

<style>
#app {
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
.container {
  max-width: 960px;
}
.flex-equal > * {
  flex: 1;
}
@media (min-width: 768px) {
  .flex-md-equal > * {
    flex: 1;
  }
}
.bg-ada {
  background: #0a38a6;
}
.bg-dogecoin {
  background: #e1b303;
}
</style>
