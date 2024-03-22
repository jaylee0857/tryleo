<template>
  <!-- <section>{{ t("button.cancel") }}熱門</section> -->
  <div class="mainNav">
    <div class="mainNav_In">
      <img class="logo" :src="getImageUrl('layout/header/logo_2.svg')" />
      <ul class="navList">
        <li id="divMenuHot">
          <div class="gameBanner">
            <ul class="subList">
              <li id="hot_nbb" class="listContainer">
                <div class="vertical-layout">
                  <div>
                    <img
                      style="
                        width: 135px;
                        max-width: 100%;
                        padding-bottom: 12px;
                      "
                      :src="getImageUrl('layout/header/KUxOSASUNA.png')"
                    />
                    <span class="logo_title">KU體育</span>
                  </div>
                </div>
              </li>
              <li id="hot_ku" class="listContainer">
                <div class="vertical-layout">
                  <div>
                    <img
                      :src="getImageUrl('layout/header/logo_KUCasino.png')"
                    />
                    <span class="logo_title">KU真人</span>
                  </div>
                </div>
              </li>
              <li id="hot_ball" class="listContainer">
                <div class="vertical-layout">
                  <div>
                    <img
                      :src="getImageUrl('layout/header/logo_KUCasino.png')"
                    />
                    <span class="logo_title">KU彩球</span>
                  </div>
                </div>
              </li>
              <li id="hot_3d" class="listContainer">
                <div class="vertical-layout">
                  <div>
                    <img
                      :src="getImageUrl('layout/header/logo_KUCasino.png')"
                    />
                    <span class="logo_title">KU電子</span>
                  </div>
                </div>
              </li>
            </ul>
          </div>
          <p class="hot">
            <img :src="getImageUrl('layout/header/fire30X30_1.gif')" />KU熱門
          </p>
        </li>
        <li id="sportid">
          <div class="gameBanner">
            <ul class="subList">
              <li id="nbb" class="listContainer">
                <div class="vertical-layout">
                  <div class="banner_img"></div>
                  <div>
                    <img
                      style="
                        width: 135px;
                        max-width: 100%;
                        padding-bottom: 12px;
                      "
                      :src="getImageUrl('layout/header/KUxOSASUNA.png')"
                    />
                    <span class="logo_title">KU體育</span>
                  </div>
                </div>
              </li>
              <li id="aBall" class="listContainer">
                <div class="vertical-layout">
                  <div class="banner_img"></div>
                  <div>
                    <img :src="getImageUrl('layout/header/logo_JZ.png')" />
                    <span class="logo_title">JU體育</span>
                  </div>
                </div>
              </li>
              <li id="pin" class="listContainer">
                <div class="vertical-layout">
                  <div class="banner_img"></div>
                  <div>
                    <img :src="getImageUrl('layout/header/logo_PIN.png')" />
                    <span class="logo_title">平博體育</span>
                  </div>
                </div>
              </li>
              <li id="obSport" class="listContainer">
                <div class="vertical-layout">
                  <div class="banner_img"></div>
                  <div>
                    <img :src="getImageUrl('layout/header/logo_OBSport.png')" />
                    <span class="logo_title">熊貓體育</span>
                  </div>
                </div>
              </li>
            </ul>
          </div>
          <p>體育投注</p>
        </li>
        <li id="liveid">
          <div class="gameBanner">
            <ul class="subList">
              <li id="ab" class="listContainer">
                <div class="horizontal-layout">
                  <div class="banner_img">
                    <div class="banner_logo">
                      <img :src="getImageUrl('layout/header/logo_AB.png')" />
                      <span class="logo_title">歐博真人</span>
                    </div>
                  </div>
                </div>
              </li>
              <li id="ku" class="listContainer">
                <div class="horizontal-layout">
                  <div class="banner_img">
                    <div class="banner_logo">
                      <img
                        :src="getImageUrl('layout/header/logo_KUCasino.png')"
                      />
                      <span class="logo_title">KU真人</span>
                    </div>
                  </div>
                </div>
              </li>
              <li id="dg" class="listContainer">
                <div class="horizontal-layout">
                  <div class="banner_img">
                    <div class="banner_logo">
                      <img :src="getImageUrl('layout/header/logo_DG.png')" />
                      <span class="logo_title">DG真人</span>
                    </div>
                  </div>
                </div>
              </li>
              <li id="sa" class="listContainer">
                <div class="horizontal-layout">
                  <div class="banner_img">
                    <div class="banner_logo">
                      <img :src="getImageUrl('layout/header/logo_SA.png')" />
                      <span class="logo_title">SA真人</span>
                    </div>
                  </div>
                </div>
              </li>
              <li id="og" class="listContainer">
                <div class="horizontal-layout">
                  <div class="banner_img">
                    <div class="banner_logo">
                      <img :src="getImageUrl('layout/header/logo_OG.png')" />
                      <span class="logo_title">OG真人</span>
                    </div>
                  </div>
                </div>
              </li>
              <li id="wm" class="listContainer">
                <div class="horizontal-layout">
                  <div class="banner_img">
                    <div class="banner_logo">
                      <img :src="getImageUrl('layout/header/logo_WM.png')" />
                      <span class="logo_title">WM真人</span>
                    </div>
                  </div>
                </div>
              </li>
              <li id="hg" class="listContainer">
                <div class="horizontal-layout">
                  <div class="banner_img">
                    <div class="banner_logo">
                      <img :src="getImageUrl('layout/header/logo_HG.png')" />
                      <span class="logo_title">HG真人</span>
                    </div>
                  </div>
                </div>
              </li>
              <li id="obLive" class="listContainer">
                <div class="horizontal-layout">
                  <div class="banner_img">
                    <div class="banner_logo">
                      <img
                        :src="getImageUrl('layout/header/logo_OBLive.png')"
                      />
                      <span class="logo_title">DB真人</span>
                    </div>
                  </div>
                </div>
              </li>
            </ul>
          </div>
          <p>真人遊戲</p>
        </li>
        <li id="slotid">
          <div class="gameBanner">
            <ul class="subList">
              <li id="ftg" class="listContainer">
                <div class="vertical-layout">
                  <div class="banner_img"></div>
                  <div>
                    <img :src="getImageUrl('layout/header/logo_FTG.png')" />
                    <span class="logo_title">福星電子</span>
                  </div>
                </div>
              </li>
              <li id="bng" class="listContainer">
                <div class="vertical-layout">
                  <div class="banner_img"></div>
                  <div>
                    <img :src="getImageUrl('layout/header/logo_BNG.png')" />
                    <span class="logo_title">BNG電子</span>
                  </div>
                </div>
              </li>
              <li id="aCNF" class="listContainer">
                <div class="vertical-layout">
                  <div class="banner_img"></div>
                  <div>
                    <img
                      :src="getImageUrl('layout/header/logo_KUCasino.png')"
                    />
                    <span class="logo_title">3D電子</span>
                  </div>
                </div>
              </li>
              <li id="ds" class="listContainer">
                <div class="vertical-layout">
                  <div class="banner_img"></div>
                  <div>
                    <img :src="getImageUrl('layout/header/logo_DS.png')" />
                    <span class="logo_title">ZEBRA電子</span>
                  </div>
                </div>
              </li>
              <li id="ps" class="listContainer">
                <div class="vertical-layout">
                  <div class="banner_img"></div>
                  <div>
                    <img :src="getImageUrl('layout/header/logo_PS.png')" />
                    <span class="logo_title">RK5電子</span>
                  </div>
                </div>
              </li>
            </ul>
          </div>
          <p>電子遊戲</p>
        </li>
        <li id="ballid">
          <div class="gameBanner">
            <ul class="subList">
              <li id="wg" class="listContainer">
                <div class="horizontal-layout">
                  <div class="banner_img">
                    <div class="banner_logo">
                      <img :src="getImageUrl('layout/header/logo_WG.png')" />
                      <span class="logo_title">WG彩球</span>
                    </div>
                  </div>
                </div>
              </li>
              <li id="aColor" class="listContainer">
                <div class="horizontal-layout">
                  <div class="banner_img">
                    <div class="banner_logo">
                      <img
                        :src="getImageUrl('layout/header/logo_KU_new.svg')"
                      />
                      <span class="logo_title">KU彩球</span>
                    </div>
                  </div>
                </div>
              </li>
              <li class="listContainer">
                <div class="horizontal-layout not-allowed">
                  <div class="banner_img">
                    <div class="banner_logo">
                      <img
                        :src="getImageUrl('layout/header/logo_noticeLoto.png')"
                      />
                      <span class="logo_title soon">敬請期待</span>
                    </div>
                  </div>
                </div>
              </li>
            </ul>
          </div>
          <p>彩球遊戲</p>
        </li>
        <li id="E-sprotid">
          <div class="gameBanner">
            <ul class="subList">
              <li id="wg" class="listContainer">
                <div class="horizontal-layout">
                  <div class="banner_img">
                    <div class="banner_logo">
                      <img
                        :src="getImageUrl('layout/header/logo_OBEsport.png')"
                      />
                      <span class="logo_title">DB電競</span>
                    </div>
                  </div>
                </div>
              </li>
              <li id="dg" class="listContainer">
                <div class="horizontal-layout not-allowed">
                  <div class="banner_img">
                    <div class="banner_logo">
                      <img
                        :src="getImageUrl('layout/header/logo_noticeLoto.png')"
                      />
                      <span class="logo_title soon">敬請期待</span>
                    </div>
                  </div>
                </div>
              </li>
            </ul>
          </div>
          <p>電競投注</p>
        </li>
        <li id="fishid">
          <div class="gameBanner">
            <ul class="subList">
              <li id="ks" class="listContainer">
                <div class="vertical-layout">
                  <div class="banner_img"></div>
                  <div>
                    <img :src="getImageUrl('layout/header/logo_KS.png')" />
                    <span class="logo_title">KS捕魚</span>
                  </div>
                </div>
              </li>
              <li id="aBall" class="listContainer">
                <div class="vertical-layout">
                  <div class="banner_img"></div>
                  <div>
                    <img :src="getImageUrl('layout/header/logo_DS.png')" />
                    <span class="logo_title">ZEBRA三仙捕魚</span>
                  </div>
                </div>
              </li>
              <li id="pin" class="listContainer">
                <div class="vertical-layout">
                  <div class="banner_img"></div>
                  <div>
                    <img
                      :src="getImageUrl('layout/header/logo_KUCasino.png')"
                    />
                    <span class="logo_title">3D鯊皇傳說</span>
                  </div>
                </div>
              </li>
              <li id="obSport" class="listContainer">
                <div class="vertical-layout">
                  <div class="banner_img"></div>
                  <div>
                    <img :src="getImageUrl('layout/header/logo_OBFish.png')" />
                    <span class="logo_title">DB捕魚</span>
                  </div>
                </div>
              </li>
            </ul>
          </div>
          <p>捕魚機</p>
        </li>
        <li>
          <p>對戰遊戲</p>
        </li>
        <li>
          <p style="color: #ac35de">優惠活動</p>
        </li>
        <li>
          <p id="phone_icon">
            <img :src="getImageUrl('layout/header/icon_phone.svg')" />APP下載
          </p>
        </li>
      </ul>
    </div>
  </div>
</template>

<script setup>
// import { computed } from "vue";
// import { useRoute, useRouter } from "vue-router";
// import { useI18n } from "@/hooks/use-i18n";
import { getImageUrl } from "@/unit/getImageUrl";

// const { t } = useI18n();
</script>
<style scoped lang="scss">
@import url("/src/assets/scss/main-nav.scss");
</style>
