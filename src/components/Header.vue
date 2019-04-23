<template>
    <div class="header">
        <div class="header__border header__top"></div>
        <div class="header__inner">Пакеты услуг<br>Сервисы<br>Акции и бонусы</div>
        <div class="header__border header__bottom">
            <p class="header__bottom__text header__bottom__text--left">Листайте<br>вниз</p>
            <img class="header__bottom__img" src="~images/scroll.png">
            <p class="header__bottom__text header__bottom__text--right">Крутите<br>колесико мыши</p>
        </div>
    </div>
</template>

<script>
export default {
  name: 'Header'
}
</script>
<style lang="scss" scoped>
.header {
  background-color: #ffffff;
  margin: 0 auto;
  width: 1024px;
  height: 542px;
  background-image: url('~images/header.png');
    &__border {
        display: inline-block;
        position: relative;
        width: 316px;
        border-left: 3px solid #fff;
        border-right: 3px solid #fff;
    }
    &__top {
        top: 87px;
        height: 33px;
        border-top: 3px solid #fff;
    }
    &__bottom {
        display: flex;
        margin: 0 auto;
        justify-content: center;
        top: 115px;
        height: 104px;
        border-bottom: 3px solid #fff;
        &__text {
            display: inline-block;
            position: relative;
            color: #fff;
            font-style: italic;
            font-family: Open Sans,sans-serif;
            font-size: 14px;
            &--left {
                text-align: right;
            }
            &--right {
                left: 35px;
                top: 18px;
                text-align: left;
            }
        }
        &__img {
            height: 74px;
            position: relative;
            height: 70px;
            left: 20px;
        }
    }
    &__inner{
        text-transform: uppercase;
        position: relative;
        top: 100px;
        color:#fff;
        font-weight: bold;
        font-size: 30px;
        letter-spacing: 2px;
        line-height: 45px;
    }
  }
</style>
