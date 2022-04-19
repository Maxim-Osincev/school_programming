<template>
  <header>
    <div class="header__wrapper">
      <div class="container">
        <div class="header__content">
          <div class="header__logo">
            <a href="/">
              <img
                src="../img/header/header_logo.png"
                alt="Logo"
                title="Logo"
              />
            </a>
          </div>
          <nav class="header__menu">
            <ul class="header__menu-list">
              <li class="header__menu-item">
                <a href="#">Чему вы научитесь</a>
              </li>
              <li class="header__menu-item">
                <a href="#">Процесс обучения</a>
              </li>
              <li class="header__menu-item"><a href="#">Стоимость</a></li>
              <li class="header__menu-item"><a href="#">Контакты</a></li>
            </ul>
          </nav>
          <div class="header__buttons">
            <button @click.prevent="" class="header__register header__button">
              Регистрация
            </button>
            <button @click.prevent="" class="header__auth header__button">
              Войти
            </button>
          </div>
          <div @click="showMenuMobile" class="header__burger_menu"></div>
          <div @click="hideMenu" class="header__burger_menu-wrapper">
            <div @click.stop="" class="header__burger_menu-list">
              <div @click="hideMenu" class="header__burger_menu-item">
                Чему вы научитесь
              </div>
              <div @click="hideMenu" class="header__burger_menu-item">
                Процесс обучения
              </div>
              <div @click="hideMenu" class="header__burger_menu-item">
                Стоимость
              </div>
              <div @click="hideMenu" class="header__burger_menu-item">
                Контакты
              </div>
              <div @click="hideMenu" class="header__burger_menu-item">
                Регистрация
              </div>
              <div class="header__burger_menu-btn">
                <button
                  @click="hideMenu"
                  @click.prevent=""
                  class="header__auth header__button"
                >
                  Войти
                </button>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </header>
</template>

<script>
export default {
  methods: {
    showMenuMobile(event) {
      event.target.classList.toggle("hidden");
      document
        .querySelector(".header__burger_menu-wrapper")
        .classList.toggle("visible");
    },
    hideMenu() {
      document.querySelector('.header__burger_menu').classList.remove("hidden");
      document
        .querySelector(".header__burger_menu-wrapper")
        .classList.remove("visible");
    },
  },
};
</script>

<style lang='scss' scope>
.header__wrapper {
  position: fixed;
  z-index: 10;
  top: 12px;
  width: 100%;
}
.header__content {
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 16px 21px;
  backdrop-filter: blur(15px);
  border-radius: 75px;
  font-size: 13px;
  gap: 73px;

  background: #fff;
}
.header__menu {
  flex: 1 1 auto;
}
.header__menu-list {
  display: flex;
  gap: 41px;
}
.header__menu-item {
  a {
    transition: all 0.2s ease;

    &:hover {
      color: #f15525;
      transition: all 0.2s ease;
    }
  }
}
.header__buttons {
  display: flex;
  gap: 15px;
}
.header__register {
  transition: all 0.2s ease;

  &:hover {
    color: #f15525;
    transition: all 0.2s ease;
  }
}
.header__auth {
  transition: all 0.2s ease;

  &:hover {
    background: #f15525;
    transition: all 0.2s ease;
  }
}
.header__button {
  font-size: 13px;
  background: transparent;
  border: none;
  cursor: pointer;
}
.header__auth {
  font-family: "GilroyMedium";
  background: #38bff2;
  border-radius: 34px;
  padding: 9px 19px;
  color: #fff;
}
.header__burger_menu {
  display: none;
  z-index: 5;
  transition: all 0.2s ease;
}
.header__burger_menu.hidden {
  background: transparent;
  transition: all 0.2s ease;

  &:before {
    transform: translate(0, 6px) rotate(45deg);
    background: #bcbcbc;
    transition: all 0.2s ease;
  }
  &:after {
    transform: translate(0, -6px) rotate(-45deg);
    background: #bcbcbc;
    transition: all 0.2s ease;
  }
}
.header__burger_menu-wrapper {
  display: none;
  z-index: 1;
  position: absolute;
  top: 0;
  right: 0;
  height: calc(100vh + 12px);
  width: 100vw;
  padding: 14px 10px;
  overflow: hidden;
  background: rgb(0, 0, 0, 0.5);
  transform: translate(0, -12px);
}
.header__burger_menu-list {
  padding: 53px 34px 34px 34px;
  background: #fff;
  border-radius: 20px;
  height: 95vh;
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  font-weight: 500;
  font-size: 20px;
  gap: 15px;
  max-width: 256px;
}
.header__burger_menu-btn{
  flex: 1 1 auto;
   max-width: 132px;
  width: 100%;
  display: flex;
  align-items: end;

  .header__auth,
  .header__button{
    width: 100%;
  }
}
.header__burger_menu-wrapper.visible {
  display: flex;
  justify-content: end;
}
@media (max-width: 1023.98px) {
  .header__menu,
  .header__register {
    display: none;
  }
  .header__burger_menu {
    position: relative;
    display: block;
    height: 2px;
    background: #f15525;
    width: 17px;
    border-radius: 21px;
    transition: all 0.2s ease;

    &:before {
      content: "";
      height: 2px;
      background: #f15525;
      width: 17px;
      position: absolute;
      top: -6px;
      border-radius: 21px;
      transition: all 0.2s ease;
    }
    &:after {
      content: "";
      height: 2px;
      background: #f15525;
      width: 17px;
      position: absolute;
      top: 6px;
      border-radius: 21px;
      transition: all 0.2s ease;
    }
  }
}
</style>