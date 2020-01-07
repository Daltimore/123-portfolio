<template>
  <div class="slide-container">
    <div class="d-flex justify-content-between skills-section">
      <swiper :options="swiperOption">
        <swiper-slide>
          <div class="one-skill">
            <h2>Ai</h2>
          </div>
        </swiper-slide>
        <swiper-slide>
          <div class="one-skill">
            <h2>Ae</h2>
          </div>
        </swiper-slide>
        <swiper-slide>
          <div class="one-skill">
            <h2>Xd</h2>
          </div>
        </swiper-slide>
        <swiper-slide>
          <div class="one-skill">
            <h2>Pr</h2>
          </div>
        </swiper-slide>
      </swiper>
    </div>
  </div>
</template>

<script>
export default {
  data () {
    return {
      swiperOption: {
        slidesPerView: 2,
        loop: true,
      }
    }
  }
}
</script>

<style scoped>

.slide-container {
  margin-left: -8rem;
}

</style>