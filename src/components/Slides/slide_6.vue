<template>
    <div class="slide">
        <div class="slide__title">Информирование об операциях<br>о банковскому счету</div>
        <p class="slide__subtitle">Клиент может самостоятельно настроить:</p>
          <div class="iconTextBox">
            <div class="iconTextBox__left"><img src="~images/icon-notification.png"></div>
            <div class="iconTextBox__right">
                <div class="strong-text">Куда именно будут поступать информирования</div>
                <ul>
                        <li class="green-li">СМС - на телефон</li>
                        <li class="green-li">Push-уведомления - на телефон</li>
                        <li class="green-li">Письма - на e-mail</li>
                    </ul>
            </div>
          </div>
            <div class="iconTextBox">
            <div class="iconTextBox__left"><img src="~images/icon-score.png"></div>
            <div class="iconTextBox__right">
                <div class="strong-text">Счета для уведомлений</div>
                <p class="text">Если в СББОЛ несколько счетов, услуга автоматически действует по всем счетам</p>
            </div>
          </div>
           <div class="iconTextBox">
            <div class="iconTextBox__left"><img src="~images/icon-sum.png"></div>
            <div class="iconTextBox__right">
                <div class="strong-text">Пороговые суммы</div>
                <p class="text">Так Клиенту не придется получать информацию по мелким суммам, которые ему неинтересны</p>
            </div>
          </div>
    </div>
</template>
<script>
export default {
  name: 'slide5'
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
     .iconTextBox {
        display: flex;
        flex-wrap: row nowrap;
        margin: 30px 50px;
        box-shadow: 0 3px 19px 1px rgba(214,213,228,.6);
        border-radius: 5px;
        &__left {
            padding: 25px;
        }
        &__right {
            margin-top: 16px;
            padding-right: 30px;
            width: 500px;
            text-align: left;
            line-height: 23px;
        }
    }
     .strong-text {
        margin-bottom: 7px;
        font-weight: 600;
    }
     .green-li {
        list-style-type: none;
        position: relative;
        padding-bottom: 10px;
        &:before {
            content: '';
            position: absolute;
            left: -30px;
            top: 7px;
            width: 10px;
            height: 10px;
            background-color: #66b5bc;
            border-radius: 50%;
        }
    }
    .text {
        margin: 0 0 20px;
    }
}
</style>
