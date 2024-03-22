<template>
  <div class="customerServ" :class="{ active: anchor }">
    <ul>
      <li>
        <div class="icon" style="background-position: 5px 1px"></div>
        <p>在線客服</p>
      </li>
      <li class="relative">
        <div class="icon" style="background-position: -48px 1px"></div>
        <p>Line客服</p>
        <div class="customerServDiv">
          <div class="servDivT">Line客服</div>
          <div class="rightCsArrow"></div>
          <div class="csQrImg">
            <div
              id="csQrCode"
              class="flex justify-center items-center"
              alt="QRcode"
            >
              <qrcode-vue value="www.google.com" :size="85" level="H" />
            </div>
            <span>@leo666</span>
          </div>
        </div>
      </li>
      <li>
        <div class="icon" style="background-position: -95px 1px"></div>
        <p>回電服務</p>
      </li>
      <li>
        <div class="icon" style="background-position: -148px 1px"></div>
        <p>遠端協助</p>
      </li>
    </ul>
  </div>
</template>

<script setup>
import { ref, onMounted, onUnmounted } from "vue";
import QrcodeVue from "qrcode.vue";
// import { useRoute, useRouter } from "vue-router";
// import { useI18n } from "@/hooks/use-i18n";

// const { t } = useI18n();
const anchor = ref(false);

// 创建滚动事件处理函数
const handleScroll = () => {
  // 当滚动高度超过60px时添加类，否则移除类
  anchor.value = window.scrollY > 60;
};

// 在组件挂载时添加滚动事件监听器
onMounted(() => {
  window.addEventListener("scroll", handleScroll);
});

// 在组件卸载时移除滚动事件监听器
onUnmounted(() => {
  window.removeEventListener("scroll", handleScroll);
});
</script>

<style scoped lang="scss">
.customerServ {
  position: absolute;
  top: 100px;
  right: 0;
  width: 80px;
  font-size: 14px;
  z-index: 999;
  &.active {
    position: fixed;
    top: 0;
  }
  ul {
    li {
      display: flex;
      justify-content: center;
      align-items: center;
      flex-direction: column;
      padding: 15px 0;
      background-color: rgba(0, 0, 0, 0.8);
      cursor: pointer;
      color: white;
      transition: all ease 0.3s;
      &:hover {
        background-color: rgba(0, 0, 0, 0.4);
      }
      &:nth-child(2):hover .customerServDiv {
        pointer-events: unset;
        opacity: 1;
        transition: 0.5s;
      }
      .icon {
        width: 50px;
        height: 50px;
        background: url("/src/assets/images/layout/right-bar/icon_group.png")
          no-repeat;
      }
      .customerServDiv {
        position: absolute;
        right: 90px;
        background-color: rgba(255, 255, 255, 0.7);
        top: 0;
        width: 170px;
        text-align: center;
        opacity: 0;
        transition: 0.5s;
        pointer-events: none;
        .servDivT {
          height: 40px;
          line-height: 40px;
          border-bottom: 2px solid #fff;
          font-size: 14px;
          color: #1a7ecc;
          position: relative;
        }
        .rightCsArrow {
          width: 0;
          height: 0;
          border-top: 10px solid transparent;
          border-bottom: 10px solid transparent;
          border-left: 10px solid rgba(255, 255, 255, 0.7);
          position: absolute;
          top: 10px;
          right: -10px;
          z-index: 100;
        }
        .csQrImg {
          padding: 10px 0;
          span {
            color: #000;
          }
        }
      }
    }
  }
}
</style>
