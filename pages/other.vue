<template>
  <section class="others">
    <div class="container">
      <div class="others-title">
        <h2>Other</h2>
        <h3>Short description</h3>
      </div>
      <div class="others-row">
        <div class="others-item" v-for="product in products">
          <div class="others-top">
            <h3>{{ product.title }}</h3>
            <img :src="product.img">
          </div>
          <div class="others-bottom">
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
          title: 'Alcohol wipes',
          img: require('@/assets/img/wipes.png'),
          list: ['20*15cm', '50pcs/bag', '32bags/cartons', '25*13*7cm, 11kg'],
          price: '$ 1.70'
        },
        {
          title: 'TOILET PAPER',
          img: require('@/assets/img/paper.png'),
          list: ['70g/roll 3 layers'],
          price: '$ 0.29'
        }
      ]
    }
  }
}
</script>

<style lang="scss" scoped>
.others{
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