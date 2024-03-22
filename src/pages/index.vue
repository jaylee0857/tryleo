<!-- eslint-disable vue/multi-word-component-names -->
<template>
  <MainNav></MainNav>
  <Banner></Banner>
  <PicMenu></PicMenu>
  <OtherLink></OtherLink>
  <Footer></Footer>
  <RightBar></RightBar>
</template>
<script>
import { onMounted } from "vue";
import { useI18n } from "@/hooks/use-i18n";
import MainNav from "@/widgets/layout/main-nav.vue";
import Footer from "@/widgets/layout/footer.vue";
import RightBar from "@/widgets/layout/right-bar.vue";
import Banner from "@/widgets/index/banner.vue";
import OtherLink from "@/widgets/index/other-link.vue";
import PicMenu from "@/widgets/index/pic-menu.vue";

export default {
  layout: "layout-default",
  components: {
    MainNav,
    Footer,
    RightBar,
    Banner,
    OtherLink,
    PicMenu,
  },
  setup() {
    // import storage from "store2";
    const { t } = useI18n();
    onMounted(() => {});
    return {
      t,
    };
  },
};
</script>
