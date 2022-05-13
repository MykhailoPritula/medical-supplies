<template>
  <section class="products">
    <div class="container">
      <h1>Medical Personal Protective Equipment</h1>
      <div class="subtitle">We deliver at the right time at the right price to the right place</div>
      
      <div class="products-item">
        <div class="products-left">
          <h3>Masks</h3>
          <p>Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book.</p>
          <button><nuxt-link to="/masks">Check availability</nuxt-link></button>
        </div>
        <div class="products-right">
          <img src="@/assets/img/mask.png">
        </div>
      </div>

      <div class="products-item">
        <div class="products-left">
          <h3>Protection</h3>
          <p>Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it</p>
          <button><nuxt-link to="/protection">Check availability</nuxt-link></button>
        </div>
        <div class="products-right">
          <img src="@/assets/img/protection.png">
        </div>
      </div>

      <div class="products-item">
        <div class="products-left">
          <h3>Sanitizer</h3>
          <p>Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book.</p>
          <button><nuxt-link to="/sanitizer">Check availability</nuxt-link></button>
        </div>
        <div class="products-right">
          <img src="@/assets/img/sanitizer.png">
        </div>
      </div>

      <div class="products-item">
        <div class="products-left">
          <h3>Tests</h3>
          <p>Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it</p>
          <button><nuxt-link to="/test">Check availability</nuxt-link></button>
        </div>
        <div class="products-right">
          <img src="@/assets/img/tests.png">
        </div>
      </div>

      <div class="products-item">
        <div class="products-left">
          <h3>Dispensers</h3>
          <p>Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book.</p>
          <button><nuxt-link to="/dispenser">Check availability</nuxt-link></button>
        </div>
        <div class="products-right">
          <img src="@/assets/img/dispensers.png">
        </div>
      </div>

      <div class="products-item">
        <div class="products-left">
          <h3>Other</h3>
          <p>Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it </p>
          <button><nuxt-link to="/other">Check availability</nuxt-link></button>
        </div>
        <div class="products-right">
          <img src="@/assets/img/other.png">
        </div>
      </div>

    </div>
  </section>
</template>

<script>
export default {
}
</script>

<style lang="scss" scoped>
.products{
  padding: 0 0 30px;
  @media(min-width:768px){
    padding: 0 0 100px;
  }
  h1{
    text-align: center;
    font-weight: 500;
    font-size: 30px;
    line-height: 1.2;
    color: #000;
    margin-bottom: 20px;
    @media(min-width:768px){
      font-size: 48px;
    }
  }
  .subtitle{
    font-weight: 300;
    font-size: 18px;
    line-height: 1.2;
    color: #000;
    text-align: center;
    margin-bottom: 30px;
    @media(min-width:768px){
      margin-bottom: 180px;
    }
  }
  &-item{
    @media(min-width:768px){
      display: flex;
      align-items: center;
      &:nth-child(even){
        .products-left{
          order: 2;
          h3{
            margin-bottom: 55px;
          }
          p{
            margin-bottom: 45px;
          }
        }
      }
    }
    &:not(:last-child){
      margin-bottom: 40px;
      @media(min-width:768px){
        margin-bottom: 80px;
      }
    }
  }
  @media(min-width:768px){
    &-left, &-right{
      flex: 1 50%;
      width: 50%;
    }
  }
  img{
    display: block;
    margin: 0 auto;
  }
  &-left{
    padding: 0 60px;
    @media(max-width:767px){
      text-align: center;
      margin-bottom: 30px;
    }
    h3{
      font-weight: 700;
      font-size: 36px;
      line-height: 1.2;
      color: #000;
      margin-bottom: 25px;
    }
    p{
      font-weight: 400;
      font-size: 14px;
      line-height: 1.6;
      color: #495764;
      margin-bottom: 20px;
    }
    button{
      background: linear-gradient(92.66deg, #1A76DC 0%, #3CB9EE 100.68%);
      border-radius: 6px;
      color: #fff;
      font-weight: 400;
      font-size: 18px;
      line-height: 1.2;
      padding: 15px 20px;
      border: none;
      transition: .7s;
      margin-bottom: 20px;
      text-decoration: none;
      &:hover{
        transform: scale(1.1);
        transition: .7s;
      }
      @media(min-width:768px){
        margin-bottom: 0;
      }
      a{
        color: #fff;
        text-decoration: none;
      }
    }
  }
}
</style>