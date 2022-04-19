<template>
  <div class="info__wrapper">
    <div class="container">
      <div class="info__content">
        <div class="info__row">
          <div class="info__item-image info__item">
            <img src="../img/info/info_item_1.png" alt="Image" title="Image" />
          </div>
          <div class="info__item-content info__item">
            <div class="info__item-title">Помощь и поддержка</div>
            <div class="info__item-text">
              <p>
                Если в процессе обучения возникнут сложности, вы всегда сможете
                задать вопрос своему наставнику.
              </p>
              <p>
                Раз в несколько уроков вы будете получать большое задание,
                которое нужно будет сдавать на проверку код-ревьюеру. Он
                внимательно изучит ваш код, найдет ошибки и поможет вам стать
                лучше.
              </p>
            </div>
          </div>
        </div>
        <div class="info__row">
          <div class="info__item-content info__item">
            <div class="info__item-title">Методика обучения</div>
            <div class="info__item-text">
              <p>
                Весь учебный материал структурирован по принципу «спирального
                обучения». Сначала вы получаете базовые знания, а затем на
                каждом витке спирали углубляетесь в изученные темы, доводя их
                понимание до совершенства. Такой подход упрощает обучение и
                гарантирует, что вы не пропустите ничего важного.
              </p>
            </div>
          </div>
          <div class="info__item-image info__item">
            <img src="../img/info/info_item_2.png" alt="Image" title="Image" />
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style lang='scss' scope>
.info__wrapper {
  background: #ffffff;
  border-radius: 80px;
  padding: 90px 0;
}
.info__content {
  display: flex;
  flex-direction: column;
  gap: 30px;
}
.info__row {
  display: flex;
  justify-content: space-between;
  gap: 30px;
}
.info__item {
  background: #eaf2f5;
  border-radius: 40px;
  display: flex;
  flex-direction: column;
}
.info__item-image {
  padding: 41px 65px;
  max-width: 401px;
  width: 100%;

  img {
    width: 100%;
    height: 100%;
    object-fit: contain;
  }
}
.info__item-content {
  padding: 50px 80px 50px 100px;
  max-width: 730px;
  width: 100%;
}
.info__item-title {
  font-weight: 600;
  font-size: 32px;
  line-height: 30px;
  margin-bottom: 18px;
}
.info__item-text {
  display: flex;
  flex-direction: column;
  gap: 15px;
  line-height: 25px;
}
@media (max-width: 1170px) {
  .info__content {
    padding: 0 10px;
  }
}
@media (max-width: 1023.98px) {
  .info__row {
    flex-direction: column;
    align-items: center;
  }
}
@media (max-width: 768px) {
  .info__item-content {
    padding: 38px 22px;
  }
  .info__item-image {
    padding: 34px 48px;
  }
  .info__item-title {
    font-size: 20px;
    line-height: 19px;
  }
  .info__item-text {
    font-size: 12px;
    line-height: 17px;
  }
}
</style>