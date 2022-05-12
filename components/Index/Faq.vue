<template>
  <section class="faq">
    <div class="container">
      <h2>Frequently Asked Questions</h2>
      <div class="faq-items">
        <div class="faq-title">
          <div @click="question" class="faq-question">Some question about the product?</div>
          <div class="faq-answer">Lorem ipsum dolor sit amet consectetur adipisicing elit. Labore, facilis</div>
        </div>
        <div class="faq-title">
          <div @click="question" class="faq-question">Some question about the product?</div>
          <div class="faq-answer">Lorem ipsum dolor sit amet consectetur adipisicing elit. Labore, facilis</div>
        </div>
        <div class="faq-title">
          <div @click="question" class="faq-question">Some question about the product?</div>
          <div class="faq-answer">Lorem ipsum dolor sit amet consectetur adipisicing elit. Labore, facilis</div>
        </div>
        <div class="faq-title">
          <div @click="question" class="faq-question">Some question about the product?</div>
          <div class="faq-answer">Lorem ipsum dolor sit amet consectetur adipisicing elit. Labore, facilis</div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  methods: {
    question(e) {
      e.target.parentNode.classList.toggle('active');
    },
  }
}
</script>


<style lang="scss" scoped>
.faq{
  text-align: center;
  margin-bottom: 30px;
  @media(min-width:768px){
    margin-bottom: 160px;
  }
  h2{
    font-weight: 700;
    font-size: 36px;
    line-height: 1.2;
    color: #151515;
    margin-bottom: 70px;
  }
  &-items{
    max-width: 900px;
    width: 100%;
    margin: 0 auto;
  }
  &-title{
    padding: 10px 0;
    text-align: left;
    border-bottom: 1px solid #5EB6EA;
    position: relative;
    cursor: pointer;
    &:not(:last-child){
      margin-bottom: 40px;
    }
    &::before{
      content: url('@/assets/img/arrow-faq.svg');
      display: block;
      position: absolute;
      width: 20px;
      height: 10px;
      right: 0;
      top: 20%;
    }
    &::after{
      content: url('@/assets/img/arrow-faq.svg');
      display: block;
      position: absolute;
      width: 20px;
      height: 10px;
      right: 0;
      top: 20%;
      transform: translate(0, -50%) rotate(-180deg);
    }
  }
  &-question, &-answer{
    font-weight: 400;
    font-size: 18px;
    line-height: 1.2;
    color: #495764;
    padding-left: 0;
    @media(min-width:576px){
      font-size: 24px;
    }
    @media(min-width:992px){
      padding-left: 100px;
    }
  }
  &-title:after{
    display: none;
  }
  &-title.active:after{
    display: block;
  }
  &-title.active:before{
    display: none;
  }
  &-title.active &-answer {
    max-height: 1000px;
    padding: 30px 15px 30px 0;
    @media(min-width:992px){
      padding: 30px 15px 30px 100px;
    }
  }
  &-title &-answer {
    color: #0C426D;
    font-size: 18px;
    line-height: 1.2;
    width: 100%;
    max-height: 0px;
    overflow: hidden;
    transition: .5s ease;
    @media(min-width:576px){
      font-size: 20px;
    }
  }
}
</style>