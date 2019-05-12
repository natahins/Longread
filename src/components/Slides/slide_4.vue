<template>
    <div class="slide">
        <div class="slide__title">E-invoicing. Преимущества</div>
          <div class="slide__double-box">
            <div class="slide__double-box__leftside">
                <p class="strong-text">E-invoicing обладает следующими преимуществами:</p>
                <ul>
                    <li v-for="(item, index) in list"  :key="index" class="green-li"> <div v-html="item"></div> </li>
                </ul>
            </div>
            <div class="slide__double-box__rightside">
                <div class="graybox graybox--comp">
                    <div class="graybox__image"></div>
                </div>
            </div>
        </div>
    </div>
</template>
<script>
export default {
  name: 'slide4',
  data () {
    return {
      list: [
        'Безбумажный защищенный электронный документооборот c Банком и партнерами',
        'Возможность быстро, бесплатно, удаленно получить КЭП для подписания электронных документов',
        'Сокращение трудозатрат на отслеживание доставки документов контрагентам. Доставка осуществляется<br>моментально с информацией о статусе получения документа',
        'Отказ от бумажных архивов: удобство хранения и поиска документов компани',
        'Сокращение расходов на офисную технику и канцтовары при переводе документооборота в электронный вид'
      ]
    }
  }
}
</script>
<style lang="scss" scoped>
.slide {
    font-family: GothamPro;
    font-weight: 400;
    font-size: 16px;
    &__title {
        font-weight: bold;
        font-size: 36px;
        line-height: 36px;
        color: #52626e;
        text-align: center;
        padding: 45px 0 45px 0;
    }
    .strong-text {
        margin-bottom: 22px;
        font-weight: 600;
    }
    &__double-box {
        display: flex;
        &__leftside {
            width: 457px;
            font-family: 'GothamPro';
            font-weight: 400;
            text-align: left;
            line-height: 24px;
        }
        &--rightside {
            width: 457px;
        }
    }
      .graybox {
            background-color: #f0f0f8;
            position: relative;
            &--comp {
                width: 298px;
                height: 465px;
                left: 169px;
            }
            &__image {
                position: relative;
                top: 55px;
                right: 135px;
                width: 435px;
                height: 338px;
                background-image: url('~images/comp.png');
            }
        }
        .green-li {
            list-style-type: none;
            position: relative;
            padding-bottom: 25px;
            line-height: 20px;
            &:before {
                content: '';
                position: absolute;
                left: -30px;
                top: 10px;
                width: 10px;
                height: 10px;
                background-color: #66b5bc;
                border-radius: 50%;
            }
        }
}
  </style>
