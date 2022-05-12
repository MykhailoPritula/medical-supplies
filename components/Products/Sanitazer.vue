<template>
  <section class="sanitizers">
    <div class="container">
      <div class="sanitizers-title">
        <h2>Sanitizers</h2>
        <span>Short description</span>
      </div>
      <div class="sanitizers-item">
        <div class="sanitizers-left">
          <h3>Sanitizer 100ml</h3>
          <img src="@/assets/img/sanitizer-100.png">
          <ul>
            <li>• Instant Hand Sanitizer </li>
            <li>• 100ml Travel Size</li>
            <li>• Kills 99.99% Of Germs</li>
            <li>• Wash Free</li>
            <li>• 75% Ethyl Alcohol</li>
          </ul>
          <span>$ 0.95</span>
        </div>
        <div class="sanitizers-right">
          <h3>Sanitizer 250ml</h3>
          <img src="@/assets/img/sanitizer-250.png">
          <ul>
            <li>• Instant Hand Sanitizer</li>
            <li>• 100ml Travel Size</li>
            <li>• Kills 99.99% Of Germs</li>
            <li>• Wash Free</li>
            <li>• 75% Ethyl Alcohol</li>
          </ul>
          <span>$ 0.00</span>
        </div>
      </div>
      <div class="sanitizers-item">
        <div class="sanitizers-left">
          <h3>Sanitizer 500ml</h3>
          <img src="@/assets/img/sanitizer-500.png">
          <ul>
            <li>• Instant Hand Sanitizer </li>
            <li>• 100ml Travel Size</li>
            <li>• Kills 99.99% Of Germs</li>
            <li>• Wash Free</li>
            <li>• 75% Ethyl Alcohol</li>
          </ul>
          <span>$ 3.40</span>
        </div>
        <div class="sanitizers-right">
          <h3>Hand Sanitiser Altapharma</h3>
          <img src="@/assets/img/hand-sanitizer.png">
          <ul>
            <li>1pc for 200ml water</li>
            <li>10pcs / bag</li>
          </ul>
          <span>$ 0.19</span>
        </div>
      </div>
    </div>
  </section>
</template>

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
