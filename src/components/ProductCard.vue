<template>
  <div class="product-card">
    <div class="img-box">
      <img
        class="img-main"
        src="@/assets/sneakers/main-sneakers.png"
        alt="sneakers"
      />
      <div class="carousel">
        <button class="btn-left">
          <img src="@/assets/arrow-left.svg" alt="arrow left" />
        </button>
        <ul>
          <img v-for="(img, i) in images" :src="img" :key="i" />
        </ul>
        <button class="btn-right">
          <img src="@/assets/arrow-right.svg" alt="arrow right" />
        </button>
      </div>
    </div>
    <div class="product-info">
      <div class="top-info">
        <div class="bay-info">
          <span class="no-sale">166 534.00 цена без скидки</span>
          <div class="price">
            <h1>122 566 ₽</h1>
            <div class="sale">-15%</div>
          </div>
          <div class="wholesale-settings">
            <div class="value">
              <span>12 штук в уп.</span>
            </div>
            <CheckBox style="margin-left: 16px" />
            <span class="order-descr">Заказ упаковкой</span>
          </div>
          <div class="line-horizontal"></div>
          <div class="order-info">
            <div>
              <h6>Завтра</h6>
              <p>Доставка</p>
            </div>
            <div>
              <h6>7 шт.</h6>
              <p>Тарасовка</p>
            </div>
            <div>
              <h6>7 шт.</h6>
              <p>Тарасовка</p>
            </div>
          </div>
          <div class="order-btns">
            <StandartBtn
              :icon="TrolleyIcon"
              :style="{
                width: '284px',
                height: '56px',
                background: '#1551E5',
                color: 'white',
                'justify-content': 'center',
                gap: '14px',
              }"
              text="В корзину"
            />
            <StandartBtn
              :icon="LikeIcon"
              :style="{
                width: '72px',
                height: '56px',
                background: '#F2F6FF',
              }"
            />
          </div>
        </div>
        <div class="line-vertical"></div>
        <div class="characteristics">
          <h4>Характеристики</h4>
          <div class="characteristics-box">
            <div class="column">
              <div class="item">
                <h6>ELC00696</h6>
                <p>Код поставщика</p>
              </div>
              <div class="item">
                <h6>ELC00696</h6>
                <p>Код РАЭК</p>
              </div>
              <div class="item">
                <h6>Electric used</h6>
                <p>Бренд</p>
              </div>
              <div class="item">
                <h6>ELC0200000696</h6>
                <p>Код производителя</p>
              </div>
            </div>
            <div class="column">
              <div class="item">
                <h6>ELC0200000696</h6>
                <p>Артикул</p>
              </div>
              <div class="item">
                <h6>ELC00696</h6>
                <p>Код ЕТМ</p>
              </div>
              <div class="item">
                <h6>ELC00696</h6>
                <p>Серия</p>
              </div>
            </div>
          </div>
        </div>
      </div>
      <div class="description">
        <h3>Описание товара</h3>
        <p>
          Создание приверженного покупателя специфицирует неопровержимый
          комплексный анализ ситуации. CTR существенно индуцирует из ряда вон
          выходящий SWOT-анализ. Воздействие на потребителя определяет
          возрастающий интеграл по поверхности, что известно даже школьникам.
          Отсюда естественно следует, что коммуникация уравновешивает косвенный
          фактор коммуникации. Поле направлений естественно допускает
          экспериментальный скачок функции, таким образом сбылась мечта идиота -
          утверждение полностью доказано. Арифметическая прогрессия притягивает
          линейно зависимый пул лояльных изданий.
        </p>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref } from "vue";
import CheckBox from "@/components/CheckBox.vue";
import StandartBtn from "@/components/StandartBtn.vue";
import TrolleyIcon from "@/assets/trolley-white.svg";
import LikeIcon from "@/assets/heart-blue.svg";

const images = ref([
  "/test-snickers/assets/sneakers/1.png",
  "/test-snickers/assets/sneakers/2.png",
  "/test-snickers/assets/sneakers/3.png",
  "/test-snickers/assets/sneakers/4.png",
]); //особенности gh-pages
</script>

<style lang="scss" scoped>
.product-card {
  margin-top: 32px;
  width: 100%;
  display: flex;
  .img-box {
    .carousel {
      margin-top: 24px;
      display: flex;
      button {
        width: 38px;
        height: 64px;
        border-radius: 8px;
        display: flex;
        align-items: center;
        justify-content: center;
        background: #f2f6ff;
      }
      ul {
        display: flex;
        gap: 12px;
        width: 300px;
        margin: 0 12px;
        overflow: scroll;
        &::-webkit-scrollbar {
          display: none;
        }
      }
    }
  }

  .product-info {
    margin-left: 48px;
    display: flex;
    flex-direction: column;

    .top-info {
      display: flex;
      .no-sale {
        font-size: 14px;
        color: #ff3d71;
      }
      .price {
        margin-top: 20px;
        display: flex;
        align-items: center;
        h1 {
          font-size: 32px;
        }
        .sale {
          margin-left: 16px;
          width: 53px;
          height: 22px;
          background: #ff3d71;
          border-radius: 4px;
          display: flex;
          align-items: center;
          justify-content: center;
          color: white;
          font-size: 16px;
        }
      }
      .wholesale-settings {
        margin-top: 28px;
        display: flex;
        align-items: center;
        .value {
          width: 111px;
          height: 26px;
          background: #f2f5f9;
          border-radius: 8px;
          color: #828ead;
          font-size: 14px;
          display: flex;
          align-items: center;
          justify-content: center;
        }
        .order-descr {
          margin-left: 12px;
          font-size: 14px;
          color: #071435;
        }
      }
      .line-horizontal {
        margin-top: 28px;
        width: 372px;
        border-bottom: 1px solid #e2e4f0;
      }
      .order-info {
        margin-top: 30px;
        display: flex;
        gap: 16px;
        div {
          width: 113px;
          h6 {
            color: #071435;
            font-size: 14px;
          }
          p {
            margin-top: 10px;
            color: #828ead;
            font-size: 12px;
            font-family: "GothamPro-Medium", sans-serif;
            font-weight: 400;
          }
        }
      }
      .order-btns {
        margin-top: 30px;
        display: flex;
        gap: 16px;
      }
      .line-vertical {
        margin-left: 48px;
        height: 312px;
        border-left: 1px solid #e2e4f0;
      }
      .characteristics {
        margin-left: 48px;
        h4 {
          font-size: 20px;
          font-family: "GothamPro-Medium", sans-serif;
          font-weight: 500;
        }
        .characteristics-box {
          margin-top: 32px;
          display: flex;
          gap: 32px;
          .column {
            width: 302px;
            display: flex;
            flex-direction: column;
            gap: 24px;
            .item {
              h6 {
                font-size: 13px;
              }
              p {
                margin-top: 18px;
                color: #828ead;
                font-size: 12px;
              }
            }
          }
        }
      }
    }

    .description {
      margin-top: 48px;
      h3 {
        font-size: 24px;
      }
      p {
        margin-top: 24px;
        font-size: 18px;
        font-family: "Gotham-Medium", sans-serif;
        line-height: 28px;
      }
    }
  }
}
</style>