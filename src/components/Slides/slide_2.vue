<template>
    <div class="slide">
        <div class="slide__title">Описание продуктов и сервисов</div>
        <p class="slide__subtitle">При подключении РКО расскажите Клиенту о продуктах и сервисах<br> Cбербанка, которые помогут вести бизнес быстро и просто.
        </p>
        <div class="slide__buttons">
            <div
                :class="['white-button', activeCard === 0 ? 'active' : '' ]"
                v-on:click="setActiveCard(0)"
             >
             «Сбербанк Бизнес Онлайн»</div>
            <div
                :class="['white-button', activeCard === 1 ? 'active' : '' ]"
                v-on:click="setActiveCard(1)"
             >
             E-invoicing</div>
            <div
            :class="['white-button', activeCard === 2 ? 'active' : '' ]"
            v-on:click="setActiveCard(2)"
            >Информирование</div>
            <div
            :class="['white-button', activeCard === 3 ? 'active' : '' ]"
            v-on:click="setActiveCard(3)"
            >Самоинкассация</div>
            <div
            :class="['white-button', activeCard === 4 ? 'active' : '' ]"
            v-on:click="setActiveCard(4)"
            >Бизнес-карта</div>
        </div>
            <div class="pictureTextBox">
            <div :class="'pictureTextBox__left pictureTextBox__left--' + this.allCards[this.currentElem].name"></div>
            <div class="pictureTextBox__right">
                <div class="big-text"> {{ this.allCards[this.currentElem].title }}</div>
                <div class="strong-text">Описание</div>
                <div class="text"><div v-html="this.allCards[this.currentElem].opisanie">{{ this.allCards[this.currentElem].opisanie }}</div></div>
                <div class="strong-text">Кому пригодится</div>
                <div class="text"><div v-html="this.allCards[this.currentElem].komu">{{ this.allCards[this.currentElem].komu }}</div></div>
                <div class="strong-text">Стоимость при подключении с РКО</div>
                <div class="text"><div v-html="this.allCards[this.currentElem].stoimost">{{ this.allCards[this.currentElem].stoimost }}</div></div>
            </div>
        </div>
    </div>
</template>
<script>
export default {
  name: 'slide2',
  data () {
    return {
      currentElem: 0,
      activeCard: 'businessOnline',
      allCards: [
        {
          name: 'businessOnline',
          title: '«Сбербанк Бизнес Онлайн»',
          opisanie: 'Интернет-банк, дает возможность управления<br>продуктами Банка без посещения офиса</div>',
          komu: 'Всем клиентам, кто ценит время и мобильность.',
          stoimost: 'Бесплатно.'
        }, {
          name: 'invoicing',
          title: 'E-invoicing',
          opisanie: 'Комплекс услуг по электронному документообороту:<br>электронная отчетность и т. п. Обмен документами<br>с Банком, налоговой инспекцией, контрагентами',
          komu: 'Клиентам, которые пользуются НДС-услугами и получают от Банка счета-фактуры (они отправляются только по e-invoicing)',
          stoimost: 'Бесплатно.<br>Есть платные опции.'
        }, {
          name: 'info',
          title: 'Информирование об операциях',
          opisanie: 'Услуга, при которой Клиент получает информацию<br>о поступлении и/или списании денежных средст<br>с расчетного счета в виде:<br><ul><li class="green-li">СМС на мобильный телефон</li><li class="green-li">Push-уведомлений на мобильный телефон</li><li class="green-li">Уведомлений на e-mail</li></ul>',
          komu: 'Клиентам, которым важен постоянный контроль сумм<br>на счетах',
          stoimost: 'Согласно тарифам ТБ. В некоторых пакетах<br>предоставляется бесплатно.'
        }, {
          name: 'samoinkassacia',
          title: 'Самоинкассация',
          opisanie: 'Это самостоятельное внесение денежных средств на<br>расчетный счет через устройства самообслуживания<br>Сбербанка',
          komu: 'Клиентам, которым удобнее самостоятельно класть<br>выручку на счет без очередей и в любое время'
        }, {
          name: 'businesscard',
          title: 'Бизнес-карта',
          opisanie: 'Это банковская карта, открывающая Клиенту<br>круглосуточный доступ к средствам на расчетном<br>счете организации',
          komu: 'Клиентам, которым приходится часто оплачивать<br>расходы компании. И тем, кто часто совершает<br>командировки',
          stoimost: 'Согласно тарифам ТБ. В некоторых пакетах<br>предоставляется бесплатно'
        }
      ]
    }
  },
  methods: {
    setActiveCard (val) {
      this.currentElem = val
      this.activeCard = this.allCards[this.currentElem].name
    }
  },
  mounted () {
    console.log(this.allCards[this.currentElem].name)
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
        padding: 45px 0 45px 0;
    }
    &__buttons {
        display: flex;
        justify-content: center;
        flex-flow: row wrap;
    }
    .white-button {
        display: flex;
        justify-content: center;
        align-items: center;
        margin: 10px 17px;
        color: #009aa4;
        line-height: 18px;
        font-weight: 700;
        border: 2px solid #009aa4;
        border-radius: 27px;
        height: 53px;
        padding: 0 30px;
        box-sizing: border-box;
        cursor: pointer;
        &:hover {
            background-image: linear-gradient(0deg,#39d3b1,#00b7b0 50%,#009aa4);
            box-shadow: 0 15px 28.5px 1.5px rgba(81,229,222,.2);
            border: none;
            color: #ffff;
            border: 2px solid transparent;
        }
    }
    .active {
        background-image: linear-gradient(0deg,#39d3b1,#00b7b0 50%,#009aa4);
        box-shadow: 0 15px 28.5px 1.5px rgba(81,229,222,.2);
        border: none;
        color: #ffff;
        border: 2px solid transparent;
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
            width: 251px;
            height: 594px;
            &--big {
                width: 274px;
            }
            &--businessOnline {
            background-image: url('~images/business-online.png');
            }
             &--invoicing {
            background-image: url('~images/einvoicing.png');
            }
            &--info {
            background-image: url('~images/information.png');
            }
            &--samoinkassacia{
            background-image: url('~images/samoinkassacia.png');
            }
            &--businesscard {
               background-image: url('~images/business-card.png');
            }
        }
        &__right {
            margin-top: 34px;
            width: 500px;
            text-align: left;
            line-height: 23px;
        }
    }
    .text {
        font-family: 'GothamPro';
        font-weight: 400;
        margin-bottom: 22px;
        line-height: 24px;
    }
    .big-text {
        font-size: 20px;
        margin-bottom: 22px;
        font-weight: 600;
    }
    .strong-text {
        margin-bottom: 22px;
        font-weight: 600;
    }
    .green-li {
        list-style-type: none;
        position: relative;
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
}
</style>
