<template>
  <footer>
    <div class="top">
      <div class="topBox">
        <div class="left">
          <img src="@/assets/logo.svg" alt="logo" />
          <div class="support">
            <div>
              <h5>8 800 841-95-95</h5>
              <span>Служба поддержки</span>
            </div>
            <div>
              <h5>support@sport.ru</h5>
              <span>Служба поддержки</span>
            </div>
          </div>
        </div>
        <div class="right">
          <menu>
            <li>Вакансии</li>
            <li>Блог</li>
            <li>Акции</li>
          </menu>
          <standart-btn
            :style="{ width: '188px', color: '#1551E5' }"
            text="Предложить идею"
          />
        </div>
      </div>
    </div>
    <div class="midle">
      <div class="midleBox">
        <div class="list">
          <span>Женщинам</span>
          <ul>
            <li>Одежда</li>
            <li>Обувь</li>
            <li>Аксессуары</li>
            <li>Белье</li>
            <li>Bra fitting</li>
          </ul>
        </div>
        <div class="list">
          <span>Мужчинам</span>
          <ul>
            <li>Одежда</li>
            <li>Обувь</li>
            <li>Аксессуары</li>
            <li>Белье</li>
          </ul>
        </div>
        <div class="list">
          <span>Детям</span>
          <ul>
            <li>Одежда</li>
            <li>Обувь</li>
            <li>Аксессуары</li>
            <li>Белье</li>
            <li>Игрушки</li>
            <li>Малыши</li>
          </ul>
        </div>
        <div class="list">
          <span>Виды спорта</span>
          <ul>
            <li>Велоспорт</li>
            <li>Туризм</li>
            <li>Тренажеры и фитнес</li>
            <li>Командные виды спорта</li>
            <li>Самокаты</li>
          </ul>
        </div>
      </div>
    </div>
    <div class="bottom">
      <div class="bottomBox">
        <div class="bottomFirst">
          <ul>
            <li>
              <img src="@/assets/file.svg" alt="file icon" />
              <span>PDF презентация</span>
            </li>
            <li>
              <img src="@/assets/video.svg" alt="video icon" />
              <span>Видео инструкция </span>
            </li>
            <li>
              <img src="@/assets/info.svg" alt="info icon" />
              <span>FAQ</span>
            </li>
            <li>
              <img src="@/assets/YouTube.svg" alt="youtube icon" />
              <span style="color: #1551e5">Мы на YouTube</span>
            </li>
            <li>
              <span>Политика конфиденциальности </span>
            </li>
            <li>
              <span>Лицензионное соглашение</span>
            </li>
          </ul>
        </div>
        <div class="bottomSecond">
          <p>
            Настоящая Политика обработки персональных данных разработана в
            соответствии с Конституцией Российской Федерации, Трудовым кодексом
            Российской Федерации, Гражданским кодексом Российской Федерации,
            Федеральным законом от 27 июля 2006 года 149-ФЗ "Об информации,
            информационных технологиях и о защите информации"
          </p>
        </div>
        <div class="bottomThird">
          <img src="@/assets/logo-grey.svg" alt="logo" />
          <h6>Разработка платформы</h6>
        </div>
      </div>
    </div>
  </footer>
</template>

<script setup>
import StandartBtn from "@/components/StandartBtn.vue";
</script>

<style lang="scss" scoped>
footer {
  max-width: 1600px;
  margin: 0 auto;
  .top {
    width: 100%;
    border-top: 1px solid #e2e4f0;
    height: 155px;
    display: flex;
    align-items: center;
    .topBox {
      width: 100%;
      height: 59px;
      display: flex;
      align-items: center;
      justify-content: space-between;
      .left {
        display: flex;
        gap: 56px;
        img {
          width: 205px;
        }
        .support {
          display: flex;
          gap: 48px;
          div {
            display: flex;
            flex-direction: column;
            justify-content: space-between;
            height: 43px;
            h5 {
              font-size: 16px;
              font-family: "GothamPro-Bold", sans-serif;
            }
            span {
              font-size: 12px;
              color: #77829e;
              font-family: "GothamPro-Medium", sans-serif;
            }
          }
        }
      }
      .right {
        display: flex;
        gap: 32px;
        menu {
          display: flex;
          align-items: center;
          gap: 32px;
          li {
            font-family: "GothamPro-Bold", sans-serif;
          }
        }
      }
    }
  }
  .midle {
    width: 100%;
    border-top: 1px solid #e2e4f0;
    height: 320px;
    display: flex;
    align-items: center;
    .midleBox {
      display: flex;
      width: 100%;
      justify-content: space-between;
      .list {
        width: 370px;
        span {
          font-family: "GothamPro-Bold", sans-serif;
          font-size: 16px;
        }
        ul {
          margin-top: 24px;
          font-size: 14px;
          color: #050d23;
          display: flex;
          flex-direction: column;
          gap: 15px;
        }
      }
    }
  }
  .bottom {
    width: 100%;
    border-top: 1px solid #e2e4f0;
    height: 248px;
    .bottomBox {
      height: 200px;
      width: 100%;
      display: flex;
      flex-direction: column;
      justify-content: start;
      .bottomFirst {
        ul {
          margin-top: 48px;
          display: flex;
          justify-content: center;
          gap: 28px;
          li {
            display: flex;
            align-items: center;
            gap: 8px;
            color: #828ead;
            font-size: 12px;
          }
        }
      }
      .bottomSecond {
        font-size: 12px;
        color: #828ead;
        text-align: center;
        margin-top: 40px;
      }
      .bottomThird {
        margin-top: 47px;
        width: 100%;
        display: flex;
        justify-content: center;
        align-items: center;
        gap: 24px;
        h6 {
          font-family: "GothamPro-Bold", sans-serif;
          font-size: 14px;
          color: #8f9bb3;
        }
      }
    }
  }
}
</style>