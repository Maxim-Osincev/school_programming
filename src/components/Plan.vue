<template>
  <header>
    <div class="plan__wrapper">
      <div class="container">
        <div class="plan__content">
          <div class="plan__title title">Как происходит обучение на YtYt?</div>
          <div class="plan__second_title">
            Обучение должно быть комфортным. Поэтому мы разработали собственную
            платформу для обучения программированию. На ней вы можете не только
            изучать теорию, но и запускать готовые примеры и даже писать свой
            собственный код.
          </div>
          <div class="plan__video"></div>
          <div class="plan__list">
            <div class="plan__item">
              <div class="plan__item-number">01</div>
              <div class="plan__item-title">
                Весь материал разбит на небольшие уроки
              </div>
              <div class="plan__item-text">
                Теория и практика подаются маленькими порциями. Так вам будет
                легче усваивать новые знания.
              </div>
            </div>
            <div class="plan__item">
              <div class="plan__item-number">02</div>
              <div class="plan__item-title">Обучение через практику</div>
              <div class="plan__item-text">
                Всё, что вы узнали, вы тут же начинаете применять на практике.
                Вы сразу видите результаты своего труда.
              </div>
            </div>
            <div class="plan__item">
              <div class="plan__item-number">03</div>
              <div class="plan__item-title">Нет ограничений по времени</div>
              <div class="plan__item-text">
                Можно совмещать учёбу с работой и другими делами. Не нужно
                выпрашивать академический отпуск, если пришлось сделать перерыв.
              </div>
            </div>
          </div>
          <div class="plan__start">
            <main-button>Начать обучение</main-button>
            <div class="plan__start-text">
              Попробуйте, первые уроки бесплатны, но нужно пройти тестирование
            </div>
          </div>
        </div>
      </div>
    </div>
  </header>
</template>

<script>
export default {};
</script>

<style lang='scss' scope>
.plan__wrapper {
  padding: 65px 0 90px 0;
}
.plan__content {
  display: flex;
  flex-direction: column;
  align-items: center;
}
.plan__title {
  font-family: "Gilroy SemiBold";
  text-align: center;
  margin-bottom: 26px;
}
.plan__second_title {
  max-width: 642px;
  line-height: 20px;
  margin-bottom: 28px;
}
.plan__video {
  margin-bottom: 30px;
}
.plan__list {
  background: #ffffff;
  box-shadow: 0px 81px 120px -77px rgba(34, 37, 59, 0.04);
  border-radius: 40px;
  display: flex;
  padding: 45px 0;
  margin-bottom: 26px;
}
.plan__item {
  display: flex;
  flex-direction: column;
  padding: 0 50px;
  border-left: 1px solid #eaf2f5;

  &:first-child {
    border-left: none;
  }
}
.plan__item-number {
  font-size: 77px;
  line-height: 30px;
  margin-bottom: 30px;
  color: #38bff2;
}
.plan__item-title {
  flex: 1 1 auto;
  font-weight: 600;
  font-size: 22px;
  line-height: 30px;
  margin-bottom: 20px;
}
.plan__item-text {
  line-height: 23px;
}
@media (max-width: 1023.98px) {
  .plan__wrapper {
    padding: 65px 10px 90px 10px;
  }
  .plan__list {
    padding: 0;
  }
  .plan__list {
    flex-direction: column;
  }
  .plan__item {
    margin: 0 20px 0 20px;
    border-left: none;
    border-bottom: 1px solid #eaf2f5;
    padding: 46px 0 39px 0;

    &:last-child {
      border-bottom: none;
    }
  }
  .plan__item-number {
    font-weight: 700;
    font-size: 50px;
    margin-bottom: 15px;
  }
  .plan__item-title {
    font-size: 20px;
    margin-bottom: 14px;
    line-height: 19px;
  }
  .plan__item-text {
    font-size: 12px;
    line-height: 14px;
  }
}
.plan__start {
  display: flex;
  align-items: center;
  gap: 24px;
  background: #ffffff;
  border-radius: 110px;
  padding: 12px 14px;

  .main_button {
    font-size: 16px;
    max-width: 249px;
    width: 100%;
  }
}
.plan__start-text {
  font-size: 15px;
  line-height: 18px;
  font-weight: 600;
}
@media (max-width: 550px) {
  .plan__start{
    flex-direction: column;
    padding: 11px 25px 22px 25px;
    gap: 12px;
  }
  .plan__start-text{
    text-align: center;
  }
}
</style>