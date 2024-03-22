<template>
  <section class="footer">
    <div class="under_list">
      <ul class="footerLink space-x-8">
        <li>關於我們</li>
        <li class="">|</li>
        <li>博彩條款</li>
        <li class="">|</li>
        <li class="">LEO瀏覽器</li>
        <li class="">|</li>
        <li class="text-yellow-300">備用網址</li>
        <li class="">|</li>
        <li class="">客服電話：<span class="text-white">+63276215730</span></li>
      </ul>
      <div class="rightSwitch" @click="togglebGuild">
        <div class="text-white">網站導覽<span>|</span></div>
        <div class="rightArrow" :class="{ active: !isGuildCollapsed }"></div>
      </div>
    </div>
    <div class="btmGuild" :class="{ closed: isGuildCollapsed }">
      <div class="flex justify-center">
        <div class="leftGuidList space-x-24">
          <div class="item" v-for="(item, index) in btmGuild" :key="index">
            <div class="guilList title">
              <div
                class="icon"
                :style="{ 'background-position': item.img_position }"
              ></div>
              {{ item.title }}
            </div>
            <ul class="flex items-center flex-col space-y-6">
              <li v-for="(sub, index) in item.Subproject" :key="index">
                <div class="cursor-pointer">{{ sub.name }}</div>
              </li>
            </ul>
          </div>
        </div>
        <div class="rightMobile">
          <div class="rq_box">
            <div id="qrcode">
              <qrcode-vue value="www.google.com" :size="100" level="H" />
            </div>
          </div>
          <div class="guilList title">
            <div class="icon_btmMobile"></div>
            LEO 手機版
          </div>
          <span>隨時享受 即時投注</span>
        </div>
      </div>
    </div>
    <div>
      <img
        class="brandImg"
        :src="getImageUrl('layout/footer/icon_footerLogo5.png')"
        alt=""
      />
    </div>
  </section>
</template>

<script setup>
// import { computed } from "vue";
// import { useRoute, useRouter } from "vue-router";
import { getImageUrl } from "@/unit/getImageUrl";
import { ref } from "vue";
import QrcodeVue from "qrcode.vue";

const isGuildCollapsed = ref(false);
const btmGuild = ref([
  {
    title: "體育投注",
    img_position: "left -793px",
    Subproject: [
      {
        url: "",
        name: "KU體育",
      },
      {
        url: "",
        name: "JZ體育",
      },
      {
        url: "",
        name: "平博體育",
      },
      {
        url: "",
        name: "熊貓體育",
      },
    ],
  },
  {
    title: "真人遊戲",
    img_position: "-28px -793px",
    Subproject: [
      {
        url: "",
        name: "KU真人",
      },
      {
        url: "",
        name: "歐博真人",
      },
      {
        url: "",
        name: "OG真人",
      },
      {
        url: "",
        name: "DG真人",
      },
      {
        url: "",
        name: "SA真人",
      },
      {
        url: "",
        name: "WM真人",
      },
      {
        url: "",
        name: "HG真人",
      },
      {
        url: "",
        name: "DB真人",
      },
    ],
  },
  {
    title: "電子遊戲",
    img_position: "-56px -793px",
    Subproject: [
      {
        url: "",
        name: "3D電子",
      },
      {
        url: "",
        name: "BNG電子",
      },
      {
        url: "",
        name: "ZEBRA電子",
      },
      {
        url: "",
        name: "RK5電子",
      },
      {
        url: "",
        name: "福星電子",
      },
    ],
  },
  {
    title: "彩球遊戲",
    img_position: "-84px -793px",
    Subproject: [
      {
        url: "",
        name: "KU彩球",
      },
      {
        url: "",
        name: "WG彩球",
      },
    ],
  },
  {
    title: "電競投注",
    img_position: "-222px -792px",
    Subproject: [
      {
        url: "",
        name: "DB電競",
      },
    ],
  },
  {
    title: "捕 魚 機",
    img_position: "-112px -793px",
    Subproject: [
      {
        url: "",
        name: "3D鯊皇傳說",
      },
      {
        url: "",
        name: "ZEBRA三仙捕魚",
      },
      {
        url: "",
        name: "KS捕魚",
      },
      {
        url: "",
        name: "DB捕魚",
      },
    ],
  },
  {
    title: "對戰遊戲",
    img_position: "-168px -793px",
    Subproject: [
      {
        url: "",
        name: "3D對戰",
      },
    ],
  },
  {
    title: "服務幫助",
    img_position: "-140px -793px",
    Subproject: [
      {
        url: "",
        name: "幫助中心",
      },
      {
        url: "",
        name: "關於我們",
      },
      {
        url: "",
        name: "博彩條款",
      },
      {
        url: "",
        name: "活動花絮",
      },
      {
        url: "",
        name: "客服中心",
      },
      {
        url: "",
        name: "投訴箱",
      },
      {
        url: "",
        name: "公告專區",
      },
    ],
  },
]);
const togglebGuild = () => {
  console.log(isGuildCollapsed.value);
  isGuildCollapsed.value = !isGuildCollapsed.value;
};
</script>
