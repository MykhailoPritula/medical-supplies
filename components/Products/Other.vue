<template>
  <section class="others">
    <div class="container">
      <div class="others-title">
        <h2>Other</h2>
        <span>Short description</span>
      </div>
      <div class="others-item">
        <div class="others-left">
          <h3>Alcohol wipes</h3>
          <img src="@/assets/img/wipes.png">
          <ul>
            <li>20*15cm</li>
            <li>50pcs/bag</li>
            <li>32bags/cartons</li>
            <li>25*13*7cm, 11kg</li>
          </ul>
          <span>$ 1.70</span>
        </div>
        <div class="others-right">
          <h3>TOILET PAPER</h3>
          <img src="@/assets/img/paper.png">
          <ul>
            <li>70g/roll 3 layers</li>
          </ul>
          <span>$ 0.29</span>
        </div>
      </div>
    </div>
  </section>
</template>

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
