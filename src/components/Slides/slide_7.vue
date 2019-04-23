<template>
    <div class="slide">
        <div class="slide__title">Основные характеристики<br>услуги информирования</div>
        <div class="slide__double-box">
            <div class="slide__double-box__leftside">
                <p class="big-text">Особенности услуги<br>информирования:</p>
                <p class="icon-text--first text">Доступна только для счетов, открытых<br>в рублях РФ.</p>
                <p class="icon-text--second text">Если Клиент открывает расчетный счет<br>и впервые подключает услугу<br>СМС-информирования, ему<br> предоставляется <strong>бесплатное<br>пользование услугой на два месяца:</strong><br>месяц, когда услуга была подключена,<br>и полный календарный месяц,<br>следующий за ним.</p>
                <p class="icon-text--third text">Если Клиент самостоятельно<br>подключает СМС-информирование<br>через СББОЛ, <strong>плата будет взиматься<br>с первого месяца подключения.</strong><br>При этом плата за неполный месяц<br>взимается как за полный.</p>
                <p class="icon-text--last text">Подключить и отключить услугу<br>возможно через СББОЛ или в любом<br>отделении, обслуживающем ЮЛ.</p>
            </div>
            <div class="slide__double-box__rightside">
                <div class="graybox graybox--bags">
                    <div class="graybox__image"></div>
                </div>
            </div>
        </div>
    </div>
</template>
<script>
export default {
  name: 'slide1'
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
    &__double-box {
        display: flex;
        &__leftside {
            width: 457px;
            font-family: 'GothamPro';
            font-weight: 400;
            line-height: 20px;
            text-align: left;
            font-size: 16px;
            line-height: 24px;
            &__text {
                margin-bottom: 30px;
            }
        }
        &--rightside {
            width: 457px;
        }
    }
        .icon-text {
            position: relative;
            left: 50px;
            width: 380px;
            &--man {
                position: relative;
                left: 40px;
                &:before {
                content: '';
                position: absolute;
                left: -60px;
                top: -5px;
                width: 52px;
                height: 52px;
                background-image: url('~images/man-icon.png');
            }
        }
            &--first {
                position: relative;
                left: 40px;
                &:before {
                content: '';
                position: absolute;
                left: -60px;
                top: -5px;
                width: 52px;
                height: 52px;
                background-image: url('~images/icon-rub.png');
            }
        }
         &--second {
                position: relative;
                left: 40px;
                &:before {
                content: '';
                position: absolute;
                left: -60px;
                top: -5px;
                width: 52px;
                height: 52px;
                background-image: url('~images/icon-second.png');
            }
        }
         &--third {
                position: relative;
                left: 40px;
                &:before {
                content: '';
                position: absolute;
                left: -60px;
                top: -5px;
                width: 52px;
                height: 52px;
                background-image: url('~images/icon-third.png');
            }
        }
         &--last {
                position: relative;
                left: 40px;
                &:before {
                content: '';
                position: absolute;
                left: -60px;
                top: -5px;
                width: 52px;
                height: 52px;
                background-image: url('~images/icon-last.png');
            }
        }
    }
    .graybox {
            background-color: #f0f0f8;
            position: relative;
            &--bags {
                width: 385px;
                height: 600px;
                left: 100px;
                top: 30px;
            }
            &__image {
                position: relative;
                top: 30px;
                right: 65px;
                width: 358px;
                height: 490px;
                background-image: url('~images/phone.png');
                box-shadow: 0 3px 20px 0 rgba(213,213,227,.8);
            }
        }
    .big-text {
        font-size: 20px;
        margin-bottom: 22px;
        font-weight: 600;
        padding-left: 10px;
    }
     .text {
        margin: 27px 20px;
    }
}
</style>
