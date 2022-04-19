<template>
  <div class="intro__wrapper">
    <div class="container">
      <div class="intro__content">
        <div class="intro__left">
          <div class="header__title title">
            Школа <span>{</span> программирования <span>}</span> для тех, кому
            нужны реальные навыки, а не просто сертификат
          </div>
          <div class="header__text">
            Пройдите тестирование, чтобы получить доступ к бесплатным вводным
            урокам
          </div>
          <main-button>Пройти тестирование</main-button>
        </div>
        <div class="intro__right">
          <img src="@/img/intro/intro_img.png" alt="Image" title="Image" />
        </div>
      </div>
    </div>
    <div class="arrow_bottom__wrapper">
      <div class="arrow_bottom">
        <svg
          width="16"
          height="15"
          viewBox="0 0 16 15"
          fill="none"
          xmlns="http://www.w3.org/2000/svg"
        >
          <path
            d="M9 1C9 0.447715 8.55228 -2.41411e-08 8 0C7.44772 2.41411e-08 7 0.447715 7 1L9 1ZM7.29289 14.7071C7.68342 15.0976 8.31658 15.0976 8.70711 14.7071L15.0711 8.34315C15.4616 7.95262 15.4616 7.31946 15.0711 6.92893C14.6805 6.53841 14.0474 6.53841 13.6569 6.92893L8 12.5858L2.34315 6.92893C1.95262 6.53841 1.31946 6.53841 0.928932 6.92893C0.538408 7.31946 0.538408 7.95262 0.928933 8.34315L7.29289 14.7071ZM7 1L7 14L9 14L9 1L7 1Z"
            fill="#22253B"
          />
        </svg>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style lang='scss' scope>
.intro__wrapper {
  position: relative;
  width: 100%;
  padding: 130px 0 116px 0;
  background: url("../img/main/background_photo.png") no-repeat center;
  background-size: cover;
}
.intro__content {
  display: flex;
  justify-content: space-between;
}
.intro__left {
  padding: 3px 0 40px 0;
  flex: 0 1 645px;
}
.header__title {
  font-family: "GilroyMedium";
  margin-bottom: 45px;

  span {
    color: #f15525;
  }
}
.header__text {
  margin-bottom: 19px;
  line-height: 23px;
  max-width: 365px;
  width: 100%;
}
.arrow_bottom__wrapper {
  position: relative;
  z-index: 5;
  display: flex;
  align-items: center;
  justify-content: center;
  position: absolute;
  padding: 23px;
  bottom: 5px;
  left: calc(50% - 43.5px);
}
.intro__right{
  img{
    width: 100%;
    height: 100%;
    object-fit: contain;
  }
}
.arrow_bottom{
  background: #fff;
  padding: 12px;
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  cursor: pointer;
}
@media (max-width: 1050px) {
  .intro__content{
    flex-direction: column;
    align-items: center;
  }
  .intro__left{
    flex: 1 1 100%;
    padding: 0 10px;
    display: flex;
    flex-direction: column;
    align-items: center;
    margin-bottom: 63px;
  }
}
@media (max-width: 1023.98px) {
  .header__content {
    gap: 30px;
  }
  .header__menu-list {
    gap: 20px;
  }
}

</style>