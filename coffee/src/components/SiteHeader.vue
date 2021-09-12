<script>
export default {
setup () {
  return {
  }
}};
</script>

<template>
  <div class="hero-bg">
    <div class="px-4 pb-5 pt-5 text-center" style="background-color: rgba(255, 255, 255, 0.8);">
      <div class="text-center pb-3" style="font-size: 60px;;"><i class="fas fa-mug-hot text-danger"></i></div>
      <h1 class="display-5 fw-bold">Let's build stuff</h1>
      <div class="col-lg-6 mx-auto pb-3">
        <p class="lead my-4">
          Contribute in helping me build stuff.
          <br />
          Your contribution helps me to run all the cloud servers and get coffee to stay awake and write codes.
        </p>
        <div class="d-grid gap-2 d-sm-flex justify-content-sm-center">
          <a href="#pay-by-cryptocurrency" class="btn btn-primary px-4 gap-3">
            <i class="fab fa-bitcoin fs-1"></i>
            <div class="mt-1">Cryptocurrency</div>
          </a>
          <a href="https://donorbox.org/building-helpful-google-chrome-extensions" target="_blank" class="btn btn-primary px-4">
            <i class="far fa-credit-card fs-1"></i>&nbsp;
            <i class="fab fa-cc-visa fs-1"></i>&nbsp;
            <i class="fab fa-cc-mastercard fs-1"></i>&nbsp;
            <i class="fab fa-cc-paypal fs-1"></i>&nbsp;
            <div class="mt-1">Credit Card / PayPal</div>
          </a>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.hero-bg {
  border: 1px solid white;
  /* background-image: url(assets/bg2.jpeg); */
  background-image: url(/assets/bg1.jpeg);
  background-size: cover;
  /* background-position: center top; */
}
</style>
