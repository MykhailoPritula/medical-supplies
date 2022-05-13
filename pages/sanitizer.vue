<template>
  <section class="sanitizers">
    <div class="container">
      <div class="sanitizers-title">
        <h2>Sanitizers</h2>
        <h3>Short description</h3>
      </div>
      <div class="sanitizers-row">
        <div class="sanitizers-item" v-for="product in products">
          <div class="sanitizers-top">
            <h3>{{ product.title }}</h3>
            <img :src="product.img">
          </div>
          <div class="sanitizers-bottom">
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
          title: 'Sanitizer 100ml',
          img: require('@/assets/img/sanitizer-100.png'),
          list: ['Instant Hand Sanitizer ', '100ml Travel Size', 'ills 99.99% Of Germs', 'Wash Free', '75% Ethyl Alcohol'],
          price: '$ 0.95'
        },
        {
          title: 'Sanitizer 250ml',
          img: require('@/assets/img/sanitizer-250.png'),
          list: ['Instant Hand Sanitizer ', '100ml Travel Size', 'ills 99.99% Of Germs', 'Wash Free', '75% Ethyl Alcohol'],
          price: '$ 0.00'
        },
        {
          title: 'Sanitizer 500ml',
          img: require('@/assets/img/sanitizer-500.png'),
          list: ['Instant Hand Sanitizer ', '100ml Travel Size', 'ills 99.99% Of Germs', 'Wash Free', '75% Ethyl Alcohol'],
          price: '$ 3.40'
        },
        {
          title: 'Hand Sanitiser Altapharma',
          img: require('@/assets/img/hand-sanitizer.png'),
          list: ['1pc for 200ml water', '10pcs / bag'],
          price: '$ 0.19'
        }
      ]
    }
  }
}
</script>

<style lang="scss" scoped>
.sanitizers{
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
