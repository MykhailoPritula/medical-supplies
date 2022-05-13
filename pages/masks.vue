<template>
  <section class="masks">
    <div class="container">
      <div class="masks-title">
        <h2>Masks</h2>
        <h3>Short description</h3>
      </div>
      <div class="masks-row">
        <div class="masks-item" v-for="product in products">
          <div class="masks-top">
            <h3>{{ product.title }}</h3>
            <img :src="product.img">
          </div>
          <div class="masks-bottom">
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
          title: 'Disposable Mask',
          img: require('@/assets/img/disposable-mask.png'),
          list: ['FDA CE Approved', '3ply', 'Non-Woven Filtration Layer', 'Dust Particle Protection', 'Soft And Comfortable'],
          price: '$ 0.60 - 0.51'
        },
        {
          title: 'Disposable Mask 2.0',
          img: require('@/assets/img/disposable-mask2.png'),
          list: ['CE Approved', '3ply', 'Non-Woven Filtration Layer', 'Dust Particle Protection', 'Soft And Comfortable'],
          price: '$ 0.46'
        },
        {
          title: 'KN95 FFP2 Mask',
          img: require('@/assets/img/ffp-mask.png'),
          list: ['FDA CE Approved', '3ply', 'Non-Woven Filtration Layer', 'Dust Particle Protection', 'Soft And Comfortable'],
          price: '$ 2.40 - 1.80'
        }
      ]
    }
  }
}
</script>

<style lang="scss" scoped>
.masks{
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
