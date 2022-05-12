<template>
  <section class="tests">
    <div class="container">
      <div class="tests-title">
        <h2>Tests</h2>
        <span>Short description</span>
      </div>
      <div class="tests-item">
        <div class="tests-left">
          <h3>CORONA VIRUS (COVID-19) TEST KIT</h3>
          <img src="@/assets/img/corona-test.png">
          <ul>
            <li>• Novel Coronavirus (SARS - CoV-2) Antibody Detection Kit</li>
            <li>• Colloidal Method</li>
            <li>• IgM Test Card</li>
            <li>• IgG Test Card</li>
            <li>• Test kit Video Link</li>
          </ul>
          <span>$ 14.40</span>
        </div>
        <div class="tests-right">
          <h3>INFARED THERMOMETER</h3>
          <img src="@/assets/img/thermometer.png">
          <ul>
            <li>• No Contact</li>
            <li>• Instant Temperature</li>
            <li>• All Ages (Adults, Kids, Infants)</li>
            <li>• High Accuracy ± 0.3°C</li>
            <li>• 1-10cm Read Distance</li>
            <li>• Digital Screen</li>
          </ul>
          <span>$ 46.00</span>
        </div>
      </div>
    </div>
  </section>
</template>

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
