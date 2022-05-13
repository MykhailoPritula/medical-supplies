<template>
  <section class="protections">
    <div class="container">
      <div class="protections-title">
        <h2>Protection</h2>
        <h3>Short description</h3>
      </div>
      <div class="protections-row">
        <div class="protections-item" v-for="product in products">
          <div class="protections-top">
            <h3>{{ product.title }}</h3>
            <img :src="product.img">
          </div>
          <div class="protections-bottom">
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
          title: 'DISPOSABLE MEDICAL-GRADE BODY SUIT',
          img: require('@/assets/img/medical-body.png'),
          list: ['Full Seamed Seal', 'Protects Against Hazardous', 'Air Particles', 'Anti-Static', 'Manufactured in accordance', 'With EN 14126:2003/AC:2004 Standard'],
          price: '$ 22.00'
        },
        {
          title: 'PROTECTIVE COVERALL',
          img: require('@/assets/img/protective.png'),
          list: ['Protects Against Hazardous Air Particles', 'Anti-Static', 'Two-Way Zipper', 'Manufactured in accordance', 'With EN 14126:2003/AC:2004 Standard'],
          price: '$ 19.30'
        },
        {
          title: 'FACE SHIELD',
          img: require('@/assets/img/face-shield.png'),
          list: ['Visor Made From PET Material', 'Anti-Fog Coating', 'Elastic Band Fram', 'Disposable'],
          price: '$ 0.86'
        },
        {
          title: 'PROTECTIVE GOGGLES',
          img: require('@/assets/img/goggles.png'),
          list: ['Fits Over Glasses', 'Anti-Fog Coating', 'Made From TPE Material','Lightweight'],
          price: '$ 0.00'
        }
      ]
    }
  }
}
</script>

<style lang="scss" scoped>
.protections{
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
