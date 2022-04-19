<template>
  <div class="price__wrapper">
    <div class="container">
      <div class="price__title title">Стоимость обучения</div>
      <div class="price__content">
        <div class="price__row_item">
          <div class="price__item">
            <div class="price__item-img">
              <img
                src="../img/price/price_item_1.png"
                alt="Image"
                title="Image"
              />
            </div>
            <div class="price__item-text">
              Весь курс разбит на несколько блоков. Оплата поэтапная вы платите
              только за тот блок, который сейчас проходите.
            </div>
          </div>
          <div class="price__item">
            <div class="price__item-img">
              <img
                src="../img/price/price_item_2.png"
                alt="Image"
                title="Image"
              />
            </div>
            <div class="price__item-text">
              Любой из блоков вы можете оплатить в рассрочку
            </div>
          </div>
          <div class="price__item">
            <div class="price__item-img">
              <img
                src="../img/price/price_item_3.png"
                alt="Image"
                title="Image"
              />
            </div>
            <div class="price__item-text">
              Если передумаете учиться, то возврат можно оформить в любой
              момент. Возвращаем деньги за 3 рабочих дня.
            </div>
          </div>
        </div>
        <div class="price__table-wrapper">
          <div class="price__table">
            <div class="price__table-row_title">
              <div class="price__table-title price__table-block">Блок</div>
              <div class="price__table-title price__table-price">
                Стоимость (₽)
              </div>
              <div class="price__table-title price__table-time">
                Расчетное время обучения (мес.) *
              </div>
            </div>
            <div class="price__table-row_item">
              <div class="price__table-item price__table-block">
                Введение в программирование
              </div>
              <div class="price__table-item price__table-price">Бесплатно</div>
              <div class="price__table-item price__table-time">0.5</div>
            </div>
            <div class="price__table-row_item">
              <div class="price__table-item price__table-block">
                Основы программирования на Python
              </div>
              <div class="price__table-item price__table-price">9 900</div>
              <div class="price__table-item price__table-time">1</div>
            </div>
            <div class="price__table-row_item">
              <div class="price__table-item price__table-block">
                Python, продвинутый уровень
              </div>
              <div class="price__table-item price__table-price">14 900</div>
              <div class="price__table-item price__table-time">2.5</div>
            </div>
            <div class="price__table-row_item">
              <div class="price__table-item price__table-block">
                Сети + фреймворк Flask
              </div>
              <div class="price__table-item price__table-price">14 900</div>
              <div class="price__table-item price__table-time">2.5</div>
            </div>
            <div class="price__table-row_item">
              <div class="price__table-item price__table-block">
                Базы данных
              </div>
              <div class="price__table-item price__table-price">14 900</div>
              <div class="price__table-item price__table-time">2</div>
            </div>
            <div class="price__table-row_item">
              <div class="price__table-item price__table-block">
                Фреймворк Django
              </div>
              <div class="price__table-item price__table-price">14 900</div>
              <div class="price__table-item price__table-time">2</div>
            </div>
            <div class="price__table-row_item">
              <div class="price__table-item price__table-block">
                Разработка «боевого» проекта
              </div>
              <div class="price__table-item price__table-price">9 900</div>
              <div class="price__table-item price__table-time">1.5</div>
            </div>
            <div class="price__table-row_summ">
              <div class="price__table-summ price__table-block">Итого</div>
              <div class="price__table-summ price__table-price">
                {{ summPrice }}
              </div>
              <div class="price__table-summ price__table-time">
                {{ summTime }}
              </div>
            </div>
          </div>
        </div>
      </div>
      <div class="price__addition">* если занятиям уделяется около 20 часов в неделю</div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      summPrice: 0,
      summTime: 0,
    };
  },
  mounted() {
    Array.from(document.querySelectorAll(".price__table-row_item")).forEach(
      (el, index) => {
        if (index % 2 === 0) {
          el.style.background = "#F3F3F3";
        }
      }
    );

    Array.from(document.querySelectorAll('.price__table-price')).forEach(el => {
      let value = parseInt(el.innerText.split(' ').join(''))
      value ? this.summPrice += value : false
    })

    Array.from(document.querySelectorAll('.price__table-time')).forEach(el => {
      let value = Number(el.innerText.split(' ').join(''))
      value ? this.summTime += value : false
    })
  },
};
</script>

<style lang='scss' scope>
.price__wrapper {
  padding: 90px 0 0 0;
}
.price__content{
  margin: 0 0 25px 0;
}
.price__title {
  font-family: "Gilroy SemiBold";
  text-align: center;
  margin-bottom: 35px;
}
.price__row_item {
  display: flex;
  gap: 69px;
  justify-content: space-between;
  margin-bottom: 41px;
}
.price__item {
  display: flex;
  align-items: center;
  gap: 30px;
  max-width: 33.3%;
}
.price__table-wrapper {
  padding: 36px 40px;
  background: #ffffff;
  border-radius: 30px;
}
.price__table-row_title {
  display: flex;
  justify-content: space-between;
  border-radius: 10px;
  padding: 16px 19px;
  gap: 10px;
  align-items: center;
}
.price__table-title {
  color: #38bff2;
  line-height: 25px;
  font-weight: 700;
}
.price__table-row_item {
  display: flex;
  justify-content: space-between;
  border-radius: 10px;
  padding: 16px 19px;
  gap: 10px;
  align-items: center;
}
.price__table-item {
  font-size: 20px;
  line-height: 25px;
}
.price__table-row_summ {
  display: flex;
  justify-content: space-between;
  border-radius: 10px;
  padding: 16px 19px;
  gap: 10px;
  align-items: center;
}
.price__table-summ {
  font-weight: 700;
  font-size: 24px;
  line-height: 25px;
}
.price__table-block {
  flex: 1 1 518px;
}
.price__table-price {
  flex: 1 1 285px;
}
.price__table-time {
  flex: 1 1 278px;
}
.price__addition{
  line-height: 25px;
  margin: 0 0 33px 53px;
  color: #8E8E8E;
}
@media (max-width: 1160px) {
  .price__content {
    padding: 0 10px;
  }
  .price__row_item {
    gap: 30px;
  }
  .price__item {
    gap: 20px;
  }
}
@media (max-width: 900px) {
  .price__row_item {
    flex-direction: column;
    align-items: center;
  }
  .price__item {
    gap: 30px;
    max-width: 500px;
    width: 100%;
  }
}
@media (max-width: 768px) {
  .price__table-wrapper {
    padding: 36px 10px;
  }
  .price__table-title {
    font-size: 14px;
  }
  .price__table-summ {
    font-size: 19px;
  }
  .price__table-item {
    font-size: 13px;
  }
}
@media (max-width: 600px) {
  .price__table-wrapper {
    overflow: auto;
  }
  .price__table-row_item,
  .price__table-row_title,
  .price__table-row_summ{
    width: 600px;
  }
}
@media (max-width: 425px) {
  .price__row_item {
    flex-direction: column;
    align-items: center;
  }
  .price__item {
    flex-direction: column;
    gap: 10px;
  }
}
</style>