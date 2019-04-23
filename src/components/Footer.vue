<template>
    <div class="footer">
        <div class="footer__content">
        <p>А теперь вернись к Владу и задай<br>ему интересующие тебя вопросы!</p>
        <div class="footer__content__button">Поехали!</div>
        </div>
    </div>
</template>

<script>
export default {
  name: 'Footer'
}
</script>
<style lang="scss" scoped>
.footer {
    background-color: #ffffff;
    margin: 0 auto;
    width: 1024px;
    height: 495px;
    background-image: url('~images/footer.png');
    &__content {
        position: relative;
        position: relative;
        top: 205px;
        left: 30px;
        line-height: 25px;
        &__button {
            position: relative;
            width: 270px;
            height: 5px;
            border-radius: 50px;
            color: white;
            background-image: linear-gradient(0deg,#39d3b1,#00b7b0 50%,#009aa4);
            box-shadow: 1.634px 2.516px 19px 1px rgba(81,229,222,.3);
            transition: box-shadow .2s;
            margin-top: 40px;
            height: 50px;
            display: flex;
            margin: 0 auto;
            justify-content: center;
            align-items: center;
            cursor: pointer;
        }
    }
}
</style>
