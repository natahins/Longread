<template>
    <div class="longread-container">
        <slide1/>
        <slide2/>
        <slide3/>
        <slide4/>
        <slide5/>
        <slide6/>
        <slide7/>
        <slide8/>
    </div>
</template>
<script>
import slide1 from './components/Slides/slide_1.vue'
import slide2 from './components/Slides/slide_2.vue'
import slide3 from './components/Slides/slide_3.vue'
import slide4 from './components/Slides/slide_4.vue'
import slide5 from './components/Slides/slide_5.vue'
import slide6 from './components/Slides/slide_6.vue'
import slide7 from './components/Slides/slide_7.vue'
import slide8 from './components/Slides/slide_8.vue'

export default {
  name: 'Longread',
  components: {
    slide1,
    slide2,
    slide3,
    slide4,
    slide5,
    slide6,
    slide7,
    slide8
  }
}
</script>
<style>
.longread-container {
    background-color: #ffffff;
    margin: 0 100px;
    font-family: GothamPro;
    font-weight: 400;
}
</style>
