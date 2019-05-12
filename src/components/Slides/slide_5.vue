<template>
    <div class="slide">
        <div class="slide__title">Как подключить e-invoicing</div>
        <p class="slide__subtitle">Подключить e-invoicing легко.</p>
          <div class="pictureTextBox">
            <div class="pictureTextBox__left pictureTextBox__left--main"></div>
            <div class="pictureTextBox__right">
                <div class="strong-text">Основной тариф</div>
                <ul>
                        <li v-for="(item, index) in greenList" :key="index" class="green-li"><div v-html="item"></div></li>
                    </ul>
            </div>
          </div>
            <div class="pictureTextBox">
            <div class="pictureTextBox__left pictureTextBox__left--extra"></div>
            <div class="pictureTextBox__right">
                <div class="strong-text">Дополнительный тариф</div>
                <ul>
                    <li v-for="(item, index) in orangeList" :key="index" class="orange-li"><div v-html="item"></div></li>
                </ul>
                <p class="text">При желании прекратить пользоваться сервисом Клиент может перейти на основной тариф</p>
            </div>
        </div>
    </div>
</template>
<script>
export default {
  name: 'slide5',
  data () {
    return {
      greenList: [
        'Подключается всем клиентам Банка с момента<br>подключения к «Сбербанк Бизнес Онлайн» (СББОЛ)',
        'Клиенту необходимо принять условия тарифа, после<br>чего тариф активируется т можно осуществлять работу в сервисе'
      ],
      orangeList: [
        'Подключается в СББОЛ',
        'Клиенту необходимо принять условия дополнительного тарифа',
        'Сразу после активации можно осуществлять работу в сервисе',
        'После подключения к тарифу будет ежемесячно списываться стоимость пользования сервисом. Списание происходит в конце месяца на безакцептной основе'
      ]
    }
  }
}
</script>
<style lang="scss" scoped>
.slide {
    font-family: GothamPro;
    font-weight: 400;
    &__subtitle {
    font-size: 18px;
    }
    &__title {
        font-weight: bold;
        font-size: 36px;
        line-height: 36px;
        color: #52626e;
        text-align: center;
        padding: 45px 0 35px 0;
    }
     .pictureTextBox {
        display: flex;
        flex-wrap: row nowrap;
        justify-content: space-between;
        margin-top: 30px;
        width: 100%;
        box-shadow: 0 3px 19px 1px rgba(214,213,228,.6);
        border-radius: 5px;
        &__left {
            width: 237px;
            &--main {
            height: 259px;
            background-image: url('~images/main-tarif-man.png');
            }
            &--extra {
                height: 446px;
                background-image: url('~images/extra-tarif-man.png');
            }
        }
        &__right {
            margin-top: 34px;
            padding-right: 60px;
            width: 500px;
            text-align: left;
            line-height: 23px;
        }
    }
     .strong-text {
        margin-bottom: 22px;
        font-weight: 600;
        font-size: 20px;
    }
     .green-li {
        list-style-type: none;
        position: relative;
        padding-bottom: 24px;
        &:before {
            content: '';
            position: absolute;
            left: -30px;
            top: 7px;
            width: 10px;
            height: 10px;
            background-color: #c7f4e7;
            border-radius: 50%;
        }
    }
    .orange-li {
        list-style-type: none;
        position: relative;
        padding-bottom: 24px;
        &:before {
            content: '';
            position: absolute;
            left: -30px;
            top: 7px;
            width: 10px;
            height: 10px;
            background-color: #ffe3d3;
            border-radius: 50%;
        }
    }
    .text {
        margin: 0;
        position: relative;
        bottom: 30px;
    }
}
</style>
