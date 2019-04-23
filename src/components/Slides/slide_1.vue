<template>
    <div class="slide">
        <div class="slide__title">Пакеты услуг</div>
        <div class="slide__double-box">
            <div class="slide__double-box__leftside">
                <p class="slide__double-box__leftside__text">Сбербанк предлагает новым клиентам ряд выгодных<br>пакетов услуг и удобных сервисом для бизнеса.</p>
                <p class="slide__double-box__leftside__text">Почему следует предлагать подключение именно пакетов услуг?</p>
                <p class="icon-text--man"><strong>Индивидуальный подход для любого бизнеса.</strong><br>Клиент самостоятельно может пройти<br>опросник на сайте и понять, какой пакет услуг<br>будет выгоден именно ему - начинающему<br>бизнесмену, Клиенту с сезонным бизнесом,<br>Клиенту с множеством операций на счету<br>в месяц и т.п.</p>
                <p class="icon-text--money"><strong>Услуги в пакетах стоят дешевле</strong></p>
                <div class="greenbox">
                    <p>Актуальные пакеты услуг по РКО<br>можно найти на сайте Банка</p>
                    <a href="https://www.sberbank.ru/ru/s_m_business/open-accounts" target="_blank"><img class="arrow" src='~images/arrow.png' alt="arrow"></a>
                    </div>
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
            &--money {
                position: relative;
                left: 40px;
                &:before {
                content: '';
                position: absolute;
                left: -60px;
                top: -5px;
                width: 52px;
                height: 52px;
                background-image: url('~images/money-icon.png');
            }
        }
    }
    .graybox {
            background-color: #f0f0f8;
            position: relative;
            &--bags {
                width: 385px;
                height: 507px;
                left: 100px;
            }
            &__image {
                position: relative;
                top: 60px;
                right: 30px;
                width: 319px;
                height: 360px;
                background-image: url('~images/bags.jpg');
                box-shadow: 0 3px 20px 0 rgba(213,213,227,.8);
            }
        }
    .greenbox {
        display: flex;
        flex-wrap: row wrap;
        font-size: 18px;
        margin-top: 60px;
        border-radius: 5px;
        border: 2px solid #b2dadd;
        text-decoration: underline;
        padding: 0 25px;
    }
    .arrow {
        position: relative;
        left: 25px;
        top: 12px;
        width: 52px;
        height: 52px;
    }
}
</style>
