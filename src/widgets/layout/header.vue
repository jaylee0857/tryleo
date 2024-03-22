<template>
  <header>
    <div class="headerIn">
      <div class="btn_setFavor">
        <div class="divPrompt">加入最愛</div>
      </div>
      <div id="divNotLogined" class="headIn_R space-x-24">
        <input class="btn_register" type="button" value="免費註冊" />
        <input
          id="txtUser"
          class="signIn_ID uppercase"
          type="text"
          placeholder="帳號 / 手機號碼"
          maxlength="11"
        />
        <div class="passwordBox">
          <input
            id="txtPassword"
            class="signIn_PW"
            type="password"
            autocomplete="off"
            placeholder="密碼"
          />
          <div class="btn_questionMark">
            <div class="divPrompt">忘記密碼</div>
          </div>
        </div>
        <input class="btn_signIn" type="button" value="登入" />
      </div>
    </div>
  </header>
</template>

<script setup>
// import { computed } from "vue";
// import { useRoute, useRouter } from "vue-router";
</script>
