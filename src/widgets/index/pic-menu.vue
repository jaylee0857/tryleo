<template>
  <!-- <header>{{ t("button.cancel") }}點擊菜單</header> -->
  <ul class="picMenu space-x-20">
    <li
      v-for="(item, index) in picMenu"
      :key="index"
      class="photo"
      :class="['btn' + index]"
      :style="{ background: item.background }"
    >
      <div class="picMenu_T">{{ item.title }}</div>
    </li>
  </ul>
</template>

<script setup>
import { ref } from "vue";
// import { useRoute, useRouter } from "vue-router";
// import { useI18n } from "@/hooks/use-i18n";
import { getImageUrl } from "@/unit/getImageUrl";

// const { t } = useI18n();
const picMenu = ref([
  {
    title: "摸彩活動",
    background: `url('${getImageUrl(
      "index/pic_project4.jpg"
    )}') no-repeat center -0`,
  },
  {
    title: "酷映直播",
    background: `url('${getImageUrl(
      "index/coolin_CN.gif"
    )}') no-repeat center -0`,
  },
  {
    title: "西甲合作夥伴",
    background: `url('${getImageUrl(
      "index/pic_project4.jpg"
    )}') no-repeat center -0`,
  },
  {
    title: "免費影城",
    background: `url('${getImageUrl(
      "index/pic_project4.jpg"
    )}') no-repeat center -0`,
  },
]);
</script>
<style scoped lang="scss">
.picMenu {
  display: flex;
  justify-content: center;
  min-width: 1000px;
  margin-top: 30px;
  .photo {
    display: flex;
    align-items: flex-end;
    width: 233px;
    height: 180px;
    border-radius: 5px;
    cursor: pointer;
    &:hover .picMenu_T {
      font-size: 17px;
      padding: 15px 0;
    }
    .picMenu_T {
      background-color: rgba(0, 0, 0, 0.6);
      width: 100%;
      text-align: center;
      color: #fff;
      font-size: 16px;
      line-height: 35px;
      letter-spacing: 2px;
      z-index: 1;
      transition: all ease 0.3s;
      border-radius: 0 0 5px 5px;
    }
  }
  .btn0:hover {
    .picMenu_T {
      color: #ffa7da;
    }
  }
  .btn1:hover {
    .picMenu_T {
      color: #5df6ff;
    }
  }
  .btn2:hover {
    .picMenu_T {
      color: #bf92ff;
    }
  }
  .btn3:hover {
    .picMenu_T {
      color: #fff200;
    }
  }
}
</style>
