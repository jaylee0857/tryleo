<template>
  <div>
    <swiper
      :modules="modules"
      :slides-per-view="1"
      :space-between="0"
      @swiper="onSwiper"
      @slideChange="onSlideChange"
      :lazy="true"
      :pagination="{
        clickable: true,
      }"
      :autoplay="{
        delay: 2500,
        disableOnInteraction: false,
      }"
      :effect="'fade'"
    >
      <swiper-slide v-for="(item, i) in banners" :key="i"
        ><div :style="{ background: item.imgUrl }" class="bannerImg"></div
      ></swiper-slide>
    </swiper>
  </div>
</template>

<script setup>
import { ref } from "vue";
// import { useRoute, useRouter } from "vue-router";
// import { useI18n } from "@/hooks/use-i18n";
import { Swiper, SwiperSlide } from "swiper/vue";
import { Pagination, Autoplay, EffectFade } from "swiper";
import "swiper/css";
import "swiper/css/effect-fade";
import "swiper/css/pagination";
// const { t } = useI18n();
const banners = ref([
  {
    imgUrl:
      "url(https://pic.yvumd.com/pic2/ts777/13_PC_TW.jpg) no-repeat center",
  },
  {
    imgUrl:
      "url(https://pic.yvumd.com/pic2/ts777/10_PC_TW.jpg) no-repeat center",
  },
  {
    imgUrl:
      "url(https://pic.yvumd.com/pic2/ts777/Traditional-Chinese.jpg) no-repeat center",
  },
  {
    imgUrl: "url(https://pic.yvumd.com/pic2/USDT_PC_TW.jpg) no-repeat center",
  },
  {
    imgUrl:
      "url(https://pic.yvumd.com/pic2/ts777/13_PC_TW.jpg) no-repeat center",
  },
  {
    imgUrl:
      "url(https://pic.yvumd.com/pic2/ts777/13_PC_TW.jpg) no-repeat center",
  },
  {
    imgUrl:
      "url(https://pic.yvumd.com/pic2/ts777/10_PC_TW.jpg) no-repeat center",
  },
  {
    imgUrl:
      "url(https://pic.yvumd.com/pic2/ts777/Traditional-Chinese.jpg) no-repeat center",
  },
]);
const onSwiper = (swiper) => {
  console.log(swiper);
  const bullets = document.querySelectorAll(".swiper-pagination-bullet");

  bullets.forEach((bullet) => {
    bullet.addEventListener("mouseover", function () {
      this.click();
    });
  });
};
const onSlideChange = () => {
  console.log("slide change");
};
const modules = [Pagination, Autoplay, EffectFade];
</script>
<style scoped>
.bannerImg {
  height: 450px;
}
.swiper::v-deep .swiper-pagination .swiper-pagination-bullet-active {
  background: rgb(255, 255, 255);
}
</style>
