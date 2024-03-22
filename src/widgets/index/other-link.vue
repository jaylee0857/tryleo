<template>
  <div class="otherLink">
    <a href="" class="btn" v-for="(btn, index) in btns" :key="index">
      <div
        class="icon"
        :style="{ 'background-position': btn.img_position }"
      ></div>
      {{ btn.title }}</a
    >
  </div>
</template>

<script setup>
import { ref } from "vue";
// import { useRoute, useRouter } from "vue-router";
const btns = ref([
  {
    title: "客 服",
    img_position: "9px -50px",
  },
  {
    title: "幫助中心",
    img_position: "-51px -53px",
  },
  {
    title: "活動花絮",
    img_position: "-117px -53px",
  },
  {
    title: "投訴箱",
    img_position: "-240px -46px",
  },
]);
</script>
<style scoped lang="scss">
.otherLink {
  display: flex;
  justify-content: space-between;
  width: 700px;
  margin: 27px auto 0 auto;
  .btn {
    display: flex;
    align-items: center;
    color: #666;
    letter-spacing: 2px;
    font-size: 16px;
    transition: 0.4s;
    &:hover {
      transform: translateY(-10px);
      cursor: pointer;
    }
    .icon {
      margin-right: 10px;
      background: url("/src/assets/images/layout/right-bar/icon_group.png")
        no-repeat;
      width: 55px;
      height: 55px;
    }
  }
}
</style>
