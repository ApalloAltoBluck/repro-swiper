<script>
  // Import Swiper Svelte components
  import { Swiper, SwiperSlide } from 'swiper/svelte';
  import { EffectCube, Navigation } from "swiper";
  import "swiper/css/effect-cube";
  // Import Swiper styles
  import 'swiper/css';
</script>

<main class="w-screen">
   <Swiper
    spaceBetween={50}
    slidesPerView={3}
    on:slideChange={() => console.log('slide change')}
      effect={"cube"}
    class="w-screen swiperCustom"
    on:swiper={(e) => console.log(e.detail[0])}
    modules={[EffectCube ]}
  >
    <SwiperSlide><div class="h-screen w-full bg-pink-300" /></SwiperSlide>
    <SwiperSlide><div class="h-screen w-full bg-pink-200" /></SwiperSlide>
    <SwiperSlide><div class="h-screen w-full bg-pink-300" /></SwiperSlide>
    <SwiperSlide><div class="h-screen w-full bg-pink-300" /></SwiperSlide>
  </Swiper>
</main>

<style>
:root {
  background: #ff3f3f;
}
.swiperCustom {
  left: 0px;
}
  .h-screen {
    height:100vh;
  }
    .w-screen {
    width:100vw;
  }
  .bg-pink-300 {
    background: #f12fff;
  }
  .w-full {
    width:100%;
  }
    .bg-pink-200 {
    background: #f12fdf;
  }
</style>