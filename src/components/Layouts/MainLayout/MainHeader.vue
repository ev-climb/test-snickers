<template>
  <header>
    <div class="top">
      <img src="@/assets/logo.svg" alt="logo" class="logo" />
      <StandartBtn
        :icon="burgerIcon"
        text="Меню"
        color="white"
        background="#1551e5"
        width="127px"
      />
      <div class="topBox">
        <div class="inputBox">
          <input type="text" placeholder="Название запроса" />
          <img src="@/assets/close.svg" />
          <img src="@/assets/search.svg" />
        </div>
        <div class="iconBox">
          <img src="@/assets/bell.svg" />
        </div>
        <div class="line-vertical"></div>
        <div class="iconBox">
          <img src="@/assets/heart.svg" />
        </div>
        <StandartBtn
          :icon="trolleyIcon"
          background="#F2F6FF"
          text="144 235Р"
          color="#1551E5"
          width="148px"
        />
      </div>
      <div class="user">
        <img src="@/assets/avatar.png" alt="avatar" />
        <span>Ермаков Е.</span>
        <img src="@/assets/arrow.svg" alt="arrow" />
      </div>
    </div>
    <div class="line-gorisont"></div>
    <div class="bottom">
      <menu>
        <li>Мои заказы</li>
        <li>Сотрудники</li>
        <li>Шаблоны заказов</li>
        <li>Обращения</li>
      </menu>
      <div class="secondMenu">
        <StandartBtn
          :icon="messageIcon"
          :style="{
            background: '#F2F6FF',
            color: '#1551E5',
            width: '159px',
            height: '32px',
            padding: '0 12px',
            'border-radius': '4px',
            'font-family': 'GothamPro-Medium, sans-serif',
          }"
          text="Ваш менеджер"
        />
        <div>
          <img src="@/assets/percent.svg" alt="" />
          <a>Акции</a>
        </div>
        <a>Блог</a>
      </div>
    </div>
    <div class="line-gorisont"></div>
  </header>
</template>

<script setup>
import StandartBtn from "@/components/StandartBtn.vue";
import burgerIcon from "@/assets/burger.svg";
import trolleyIcon from "@/assets/trolley.svg";
import messageIcon from "@/assets/message.svg";
</script>

<style lang="scss" scoped>
header {
  width: 100%;
  height: 136px;
  .top {
    margin: 0 auto;
    max-width: 1600px;
    height: 80px;
    display: flex;
    align-items: center;
    justify-content: space-between;
    gap: 24px;
    .logo {
      width: 144px;
    }
    .topBox {
      display: flex;
      .inputBox {
        position: relative;
        width: 732px;
        height: 48px;
        display: flex;
        align-items: center;
        padding-right: 12px;
        input {
          position: absolute;
          width: 728px;
          height: 100%;
          border: 1px solid #e1e5eb;
          border-radius: 8px;
          padding-left: 16px;
          &::placeholder {
            font-family: "GothamPro-Medium", sans-serif;
            color: #050d23;
          }
        }
        img {
          position: absolute;
          right: 12px;
          &:first-of-type {
            right: 48px;
          }
        }
      }
      .iconBox {
        width: 80px;
        display: flex;
        align-items: center;
        justify-content: center;
      }
      .line-vertical {
        height: 48px;
        border-left: 1px solid #e2e4f0;
      }
    }
    .user {
      width: 169px;
      height: 32px;
      display: flex;
      align-items: center;
      justify-content: space-between;
    }
  }
  .line-gorisont {
    border-top: 1px solid #e2e4f0;
  }
  .bottom {
    max-width: 1600px;
    margin: 0 auto;
    height: 56px;
    display: flex;
    align-items: center;
    justify-content: space-between;
    gap: 16px;
    menu {
      display: flex;
      justify-content: start;
      gap: 24px;
      font-size: 14px;
      width: 1230px;
    }
    .secondMenu {
      display: flex;
      align-items: center;
      color: #1551e5;
      font-size: 14px;
      gap: 24px;
      a {
        color: #1551e5;
        cursor: pointer;
      }
      div {
        display: flex;
        align-items: center;
        gap: 16px;
        cursor: pointer;
      }
    }
  }
}
</style>