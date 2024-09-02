<template>
  <section id="price" class="py-5">
    <div class="container">
      <h2>Exploit this system now! <br>
        Before it gets <span>expensive.</span>
      </h2>
      <div class="text-wrapper">
        <img class="d-none d-md-block" src="~/assets/img/Illustration.png" alt="">
        <p>Cloudflare is aggressively trying to win the marketshare.
          That's why you can get 1 second load speed - dirt cheap.
        </p>
        <h5>But it needs specific type of website to use it. </h5>
        <p>Take advantage of it, with us.. <br>
          Before cloudflare succeeded..
        </p>
        <h6>Or, gives up. ❌</h6>
      </div>
      <div class="price-wrapper">
        <div class="list-wrapper">
          <p class="mb-1">Starts at</p>
          <h1><span>IDR 5.000.000</span> - USD 333</h1>
          <h5>Pay only once - No monthly fees</h5>
          <hr>
          <p>What's Include ?</p>
          <ul>
            <li>Custom Code Website</li>
            <li>1.5 second speed guaranteed</li>
            <li>No monthly fee</li>
            <li>No redesign</li>
          </ul>
          <div class="ctwa">
            <a :href="WhatsAppLink" target="_blank">
              Book A Call
            </a>
          </div>
        </div>
        <div class="list-wrapper d-flex flex-column justify-content-between">
          <div>
            <p class="mb-1">Starts at</p>
            <h1><span>IDR 10.000.000</span> - USD 629</h1>
            <h5>Pay only once - No monthly fees</h5>
            <hr>
            <p>What's Include ?</p>
            <ul>
              <li>All above</li>
              <li>Custom boutique design</li>
            </ul>
          </div>
          <div class="ctwa">
            <a :href="WhatsAppLink" target="_blank">
              Book A Call
            </a>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      phoneNumber: '6285172111145',
      message: "I'd like to inquire about the opportunity to optimize my site"
    }
  },
  computed: {
    WhatsAppLink() {
      return `https://wa.me/${this.phoneNumber}?text=${encodeURIComponent(this.message)}`
    }
  },
}
</script>

<style scoped></style>
