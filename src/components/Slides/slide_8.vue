<template>
    <div class="slide">
        <div class="slide__title">Акция «Тест-драйв»</div>
        <p class="text">Специальное предложение для новых клиентов:</p>
        <div class="slide__grayback">
            <div class="iconTextBox">
                <div class="iconTextBox__left">
                    <img class="iconTextBox__left__img" src="~images/bullet.png">
                    <div class="iconTextBox__left__number">1</div>
                    </div>
                <div class="iconTextBox__right">
                <div>Клиент выбирает пакет услуг из участвующих<br>в акции и подключает его</div>
                </div>
            </div>
        </div>
        <div class="slide__grayback">
            <div class="iconTextBox">
                <div class="iconTextBox__left">
                    <img class="iconTextBox__left__img" src="~images/bullet.png">
                    <div class="iconTextBox__left__number">2</div>
                    </div>
                <div class="iconTextBox__right">
                <div>Платит 1 руб. за пользование в месяц открытия</div>
                </div>
            </div>
        </div>
        <div class="slide__grayback">
            <div class="iconTextBox">
                <div class="iconTextBox__left">
                    <img class="iconTextBox__left__img" src="~images/bullet.png">
                    <div class="iconTextBox__left__number">3</div>
                    </div>
                <div class="iconTextBox__right">
                <div>Еще 2 полных месяца оплачивает вцбранный<br>пакет услуг та же, по 1 руб./мес</div>
                </div>
            </div>
        </div>
    </div>
</template>
<script>
export default {
  name: 'slide8'
}
</script>
<style lang="scss" scoped>
.slide {
    &__title {
        font-weight: bold;
        font-size: 36px;
        line-height: 36px;
        color: #52626e;
        text-align: center;
        padding: 45px 0 45px 0;
    }
    &__grayback {
        background-color: #f0f0f8;
        width: 1024px;
        position: relative;
        right: 100px;
        display: flex;
        flex-direction: column;
        align-items: center;
    }
    .big-text {
        font-size: 20px;
        margin-bottom: 22px;
        font-weight: 600;
        padding-left: 10px;
    }
     .text {
        margin: 0 0 35px;
        font-size: 18px;
        line-height: 24px;
    }
      .iconTextBox {
        display: flex;
        align-items: center;
        flex-wrap: row nowrap;
        margin: 16px 50px;
        background-color: #ffffff;
        box-shadow: 0 3px 19px 1px rgba(214,213,228,.6);
        border-radius: 5px;
        &__left {
            padding: 25px;
            &__img {
                position: relative;
                top: 10px;
            }
            &__number {
                position: relative;
                bottom: 18px;
                color: #ffffff;
                font-weight: 600;
            }
        }
        &__right {
            padding-right: 30px;
            width: 420px;
            font-size: 16px;
            text-align: left;
            line-height: 23px;
        }
    }
}
</style>
