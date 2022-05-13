<template>
  <section class="tests">
    <div class="container">
      <div class="tests-title">
        <h2>Sanitizers</h2>
        <h3>Short description</h3>
      </div>
      <div class="tests-row">
        <div class="tests-item" v-for="product in products">
          <div class="tests-top">
            <h3>{{ product.title }}</h3>
            <img :src="product.img">
          </div>
          <div class="tests-bottom">
            <ul>
              <li v-for="item in product.list">{{ item }}</li>
            </ul>
            <span>{{ product.price }}</span>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  data(){
    return{
      products: [
        {
          title: 'CORONA VIRUS (COVID-19) TEST KIT',
          img: require('@/assets/img/corona-test.png'),
          list: ['Novel Coronavirus (SARS - CoV-2) Antibody Detection Kit', 'Colloidal Method', 'IgM Test Card', 'IgG Test Card', 'Test kit Video Link'],
          price: '$ 14.40'
        },
        {
          title: 'INFARED THERMOMETER',
          img: require('@/assets/img/thermometer.png'),
          list: ['Instant Hand Sanitizer ', '100ml Travel Size', 'ills 99.99% Of Germs', 'Wash Free', '75% Ethyl Alcohol'],
          price: '$ 46.00'
        }
      ]
    }
  }
}
</script>

<style lang="scss" scoped>
.tests{
  padding: 0 0 30px;
  @media(min-width:768px){
    padding: 0 0 100px;
  }
  &-title{
    text-align: center;
    line-height: 1.2;
    color: #000;
    margin-bottom: 15px;
    h2{
      font-weight: 500;
      font-size: 64px;
    }
    h3{
      font-weight: 300;
      font-size: 18px;
    }
  }
  &-row{
    @media(min-width:992px){
      display: flex;
      flex-wrap: wrap;
      justify-content: space-between;
    }
  }
  &-item{
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    margin-top: 65px;
    @media(min-width:992px){
      flex: 1 50%;
      width: 50%;
      max-width: calc(50% - 100px);
    }
    h3{
      text-align: center;
      font-weight: 700;
      font-size: 36px;
      line-height: 1.2;
      color: #000;
      margin-bottom: 10px;
    }
    img{
      display: block;
      margin: 0 auto 50px;
    }
    ul{
      font-weight: 400;
      font-size: 14px;
      line-height: 1.2;
      color: #495764;
      list-style-type: disc;
    }
    span{
      font-weight: 500;
      font-size: 24px;
      line-height: 1.2;
      position: absolute;
      bottom: 0;
      right: 0;
    }
  }
  &-top{

  }
  &-bottom{
    position: relative;
  }
}
</style>