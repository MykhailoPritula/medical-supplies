<template>
  <section class="masks">
    <div class="container">
      <div class="masks-title">
        <h2>Masks</h2>
        <span>Short description</span>
      </div>
      <div class="masks-item">
        <div class="masks-left">
          <h3>Disposable Mask</h3>
          <img src="@/assets/img/disposable-mask.png">
          <ul>
            <li>• FDA CE Approved</li>
            <li>• 3ply</li>
            <li>• Non-Woven Filtration Layer</li>
            <li>• Dust Particle Protection</li>
            <li>• Soft And Comfortable</li>
          </ul>
          <span>$ 0.60 - 0.51</span>
        </div>
        <div class="masks-right">
          <h3>Disposable Mask 2.0</h3>
          <img src="@/assets/img/disposable-mask2.png">
          <ul>
            <li>• CE Approved</li>
            <li>• 3ply</li>
            <li>• Non-Woven Filtration Layer</li>
            <li>• Dust Particle Protection</li>
            <li>• Soft And Comfortable</li>
          </ul>
          <span>$ 0.46</span>
        </div>
        <!-- <div class="product" v-for="item in products">
          <h3>{{ item.title }}</h3>
          <img :src="item.png">
          <ul>
            <li v-for="itemList in item.list" v-html="itemList"></li>
          </ul>
          <span>{{ item.price }}</span>
        </div> -->
      </div>
      <div class="masks-item">
        <div class="masks-left">
          <h3>KN95 FFP2 Mask</h3>
          <img src="@/assets/img/ffp-mask.png">
          <ul>
            <li>• FDA CE Approved</li>
            <li>• 3ply</li>
            <li>• Non-Woven Filtration Layer</li>
            <li>• Dust Particle Protection</li>
            <li>• Soft And Comfortable</li>
          </ul>
          <span>$ 2.40 - 1.80</span>
        </div>
        <div class="masks-none"></div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  // data(){
  //   return{
  //     products: [
  //       {
  //         title: `Disposable Mask`,
  //         png: require('@/assets/img/disposable-mask.png'),
  //         list: [`• FDA CE Approved`, `• 3ply`, `• Non-Woven Filtration Layer`, `• Dust Particle Protection`, `• Soft And Comfortable`],
  //         price: `$ 0.60 - 0.51`
  //       },
  //       {
  //         title: `Disposable Mask 2.0`,
  //         png: require('@/assets/img/disposable-mask2.png'),
  //         list: [`• CE Approved`, `• 3ply`, `• Non-Woven Filtration Layer`, `• Dust Particle Protection`, `• Soft And Comfortable`],
  //         price: `$ 0.46`
  //       },
  //       {
  //         title: `KN95 FFP2 Mask`,
  //         png: require('@/assets/img/ffp-mask.png'),
  //         list: [`• FDA CE Approved`, `• 3ply`, `• Non-Woven Filtration Layer`, `• Dust Particle Protection`, `• Soft And Comfortable`],
  //         price: `$ 2.40 - 1.80`
  //       }
  //     ]
  //   }
  // }
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
    margin-bottom: 80px;
    h2{
      font-weight: 500;
      font-size: 64px;
    }
    span{
      font-weight: 300;
      font-size: 18px;
    }
  }
  &-item{
    @media(min-width:992px){
      display: flex;
      justify-content: space-between;
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
  &-left, &-right{
    position: relative;
    width: 100%;
      margin-bottom: 65px;
  }
  @media(min-width:992px){
    &-left, &-right{
      flex: 1 50%;
      width: 100%;
      max-width: 470px;
    }
  }
}
</style>
