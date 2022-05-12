<template>
  <section class="dispensers">
    <div class="container">
      <div class="dispensers-title">
        <h2>Dispensers</h2>
        <span>Short description</span>
      </div>
      <div class="dispensers-item">
        <div class="dispensers-left">
          <h3>Hand sanitiser dispenser automatic</h3>
          <img src="@/assets/img/white-dispenser.png">
          <ul>
            <li>200ml</li>
            <li>1.5V Batteries * 4</li>
            <li>Output: Foam</li>
          </ul>
          <span>$ 7.20</span>
        </div>
        <div class="dispensers-right">
          <h3>Hand sanitiser dispenser automatic</h3>
          <img src="@/assets/img/black-dispenser.png">
          <ul>
            <li>350ml</li>
            <li>USB charging 3H for 120 days</li>
            <li>Output: Foam</li>
          </ul>
          <span>$ 13.00</span>
        </div>
      </div>
      <div class="dispensers-item">
        <div class="dispensers-left">
          <h3>Hand sanitiser dispenser automatic</h3>
          <img src="@/assets/img/white-profile-dispenser.png">
          <ul>
            <li>500ml</li>
            <li>1.5V Batteries * 4</li>
            <li>3 options for output</li>
            <li>Saniriser</li>
            <li>Foam</li>
            <li>Spray</li>
          </ul>
          <span>$ 31.20</span>
        </div>
        <div class="dispensers-none">
        </div>
      </div>
    </div>
  </section>
</template>

<style lang="scss" scoped>
.dispensers{
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
