<template>
  <Header />
  <Intro />
  <Technology />
  <Plan />
  <Info />
  <Price />
  <Start />
  <Footer />
</template>

<script>
import Header from "@/components/Header";
import Intro from "@/components/Intro";
import Technology from "@/components/Technology";
import Plan from "@/components/Plan";
import Info from "@/components/Info";
import Price from "@/components/Price";
import Start from "@/components/Start";
import Footer from "@/components/Footer";

export default {
  components: {
    Header,
    Intro,
    Technology,
    Plan,
    Info,
    Price,
    Start,
    Footer,
  },
};
</script>

<style lang="scss">
$black: #22253b;
$orange: #f15525;
$blue: #38bff2;

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  list-style: none;
  text-decoration: none;
  h1,
  h2,
  h3,
  h4,
  h5,
  h6 {
    font-size: 16px;
    font-weight: 400;
  }

  color: $black;
}
a {
  color: $black;
}
@font-face {
  font-family: "GilroyLight";
  src: url("./fonts/Gilroy-Light.eot");
  src: url("./fonts/Gilroy-Light.eot?#iefix") format("embedded-opentype"),
    url("./fonts/Gilroy-Light.woff") format("woff"),
    url("./fonts/Gilroy-Light.ttf") format("truetype");
  font-style: normal;
  font-weight: 300;
}
@font-face {
  font-family: "GilroyRegular";
  src: url("./fonts/Gilroy-Regular.eot");
  src: url("./fonts/Gilroy-Regular.eot?#iefix") format("embedded-opentype"),
    url("./fonts/Gilroy-Regular.woff") format("woff"),
    url("./fonts/Gilroy-Regular.ttf") format("truetype");
  font-style: normal;
  font-weight: 400;
}
@font-face {
  font-family: "GilroyMedium";
  src: url("./fonts/Gilroy-Medium.eot");
  src: url("./fonts/Gilroy-Medium.eot?#iefix") format("embedded-opentype"),
    url("./fonts/Gilroy-Medium.woff") format("woff"),
    url("./fonts/Gilroy-Medium.ttf") format("truetype");
  font-style: normal;
  font-weight: 600;
}
@font-face {
  font-family: "GilroyBold";
  src: url("./fonts/Gilroy-Bold.eot");
  src: url("./fonts/Gilroy-Bold.eot?#iefix") format("embedded-opentype"),
    url("./fonts/Gilroy-Bold.woff") format("woff"),
    url("./fonts/Gilroy-Bold.ttf") format("truetype");
  font-style: normal;
  font-weight: 900;
}

#app {
  font-family: "GilroyRegular";
  display: flex;
  flex-direction: column;
  height: 100%;
  width: 100%;
}
.container {
  max-width: 1160px;
  margin: 0 auto;
}

html,
body {
  width: 100%;
  height: 100%;
  background: #f9f8fd;
}

.title {
  line-height: 46px;
  font-size: 46px;
}
@media (max-width: 767.98px) {
  .title {
    font-size: 34px;
  }
}
</style>