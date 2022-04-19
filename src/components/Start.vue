<template>
  <div class="start__wrapper">
    <div class="container">
      <div class="start__content">
        <div class="start__text-wrapper">
          <div class="start__img">
            <img src="../img/start/start_img.png" alt="Img" title="Img" />
          </div>
          <div class="start__text">
            Все блоки проходятся строго по порядку. Пропустить какой-то блок или
            начать обучение с середины нельзя, даже если вы считаете, что уже
            знаете какую-то часть материала. Только так мы можем гарантировать,
            что вы получите все знания, предусмотренные учебной программой.
          </div>
        </div>
        <main-button>Начать обучение</main-button>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style lang='scss' scope>
.start__wrapper {
  margin-bottom: 67px;
}
.start__content {
  display: flex;
  gap: 25px;
  justify-content: center;
  padding: 65px 51px;
  background: #eaf2f5;
  border-radius: 30px;

  .main_button {
    max-width: 311px;
    width: 100%;
    max-height: 70px;
    letter-spacing: -0.03em;
    font-size: 20px;
  }
}
.start__text-wrapper {
  display: flex;
  justify-content: center;
  gap: 25px;
}
.start__img {
  flex: 0 1 91px;
}
.start__text {
  flex: 0 1 600px;
  font-size: 17px;
  line-height: 22px;
}
@media (max-width: 1023.98px) {
  .start__content {
    flex-wrap: wrap;
  }
}
@media (max-width: 767.98px) {
  .start__text-wrapper {
    flex-wrap: wrap;
    gap: 17px;
    font-size: 12px;
    line-height: 22px;
    text-align: center;
  }
  .start__content {
    padding: 38px 24px;
    gap: 17px;

    .main__button {
      font-size: 15px;
      line-height: 96.69%;
    }
  }
}
</style>