<template>
    <div class="slide">
        <div class="slide__title">E-invoicing. Тарифы</div>
        <p class="slide__subtitle">E-invoicing — это сервис электронного документооборота.<br>Существует два тарифа подключения</p>
        <div class="slide__container">
            <div class="circlebox">
                <div class="circlebox__circle circlebox__circle--pink">
                    <img class="pic" src="~images/main-tarif.png" alt="Основной тариф">
                    <p>Основной<br>тариф</p>
                </div>
                <p class="big-text">Бесплатный</p>
                <p class="text">Возможности:</p>
                <ul>
                    <li class="text circlebox__list circlebox__list--pink">Обмен документами в электронном<br>виде со Сбербанком</li>
                    <li class="text circlebox__list circlebox__list--pink">Получение документов от любях<br>контрагентов</li>
                    <li class="text circlebox__list circlebox__list--pink">Удаленный выпуск и использование<br>квалифицированной электронной<br>подписи (КЭП)</li>
                    </ul>
            </div>
            <div class="circlebox">
                <div class="circlebox__circle circlebox__circle--green">
                    <img class="pic pic--green" src="~images/extra-tarif.png" alt="Дополнительный тариф">
                    <p>Дополнительный<br>тариф</p>
                </div>
                <p class="big-text">295 руб. с НДС в месяц</p>
                <p class="text">Возможности:</p>
                <ul>
                    <li class="text circlebox__list circlebox__list--green">Обмен документами в неограниченном<br>количестве с любыми контрагентами</li>
                    <li class="text circlebox__list circlebox__list--green">Удаленный выпуск и использование КЭП</li>
                    <li class="text circlebox__list circlebox__list--green">В подарок при подключении - сервис<br>сдачи отчетности в государственные<br>органы</li>
                    </ul>
            </div>
        </div>
    </div>
</template>
<script>
export default {
  name: 'slide3'
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
     &__subtitle {
    font-size: 18px;
    }
        &__container {
            display: flex;
            flex-wrap: row;
            justify-content: space-between
        }
    .circlebox {
        width: 372px;
        &__circle {
            font-weight: 600;
            width: 283px;
            height: 283px;
            margin: 0 auto;
            display: flex;
            flex-flow: column;
            justify-content: center;
            color: #ffff;
            font-size: 20px;
            &--pink {
            background-image: url('~images/pink-circle.png');
            }
             &--green{
            background-image: url('~images/green-circle.png');
            }
        }
        &__list {
            text-align: left;
            position: relative;
            list-style-type: none;
            &--pink {
                &:before {
                    content: '';
                    position: absolute;
                    left: -30px;
                    top: 5px;
                    width: 23px;
                    height: 17px;
                    background-image: url('~images/orange-paragraph.png');
                }
            }
             &--green {
                &:before {
                    content: '';
                    position: absolute;
                    left: -30px;
                    top: 5px;
                    width: 23px;
                    height: 17px;
                    background-image: url('~images/green-paragraph.png');
                }
            }
        }
    }
    .pic {
        width: 91px;
        height: 57px;
        position: relative;
        left: 90px;
        bottom: 10px;
        &--green {
            width: 96px;
            height: 70px;
        }
    }
     .big-text {
        font-size: 20px;
        margin-bottom: 22px;
        font-weight: 600;
    }
     .text {
        font-family: 'GothamPro';
        font-weight: 400;
        margin-bottom: 22px;
        line-height: 24px;
     }
}
  </style>
