<template>
  <section class="protections">
    <div class="container">
      <div class="protections-title">
        <h2>Protection</h2>
        <span>Short description</span>
      </div>
      <div class="protections-item">
        <div class="protections-left">
          <h3>DISPOSABLE MEDICAL-GRADE BODY SUIT</h3>
          <img src="@/assets/img/medical-body.png">
          <ul>
            <li>• Full Seamed Seal</li>
            <li>• Protects Against Hazardous</li>
            <li>• Air Particles</li>
            <li>• Anti-Static</li>
            <li>• Manufactured in accordance</li>
            <li>With EN 14126:2003/AC:2004 Standard</li>
          </ul>
          <span>$ 22.00</span>
        </div>
        <div class="protections-right">
          <h3>PROTECTIVE COVERALL</h3>
          <img src="@/assets/img/protective.png">
          <ul>
            <li>• Protects Against Hazardous Air Particles</li>
            <li>• Anti-Static</li>
            <li>• Two-Way Zipper</li>
            <li>• Manufactured in accordance</li>
            <li>With EN ISO 13688:2013 Standard</li>
          </ul>
          <span>$ 19.30</span>
        </div>
      </div>
      <div class="protections-item">
        <div class="protections-left">
          <h3>FACE SHIELD</h3>
          <img src="@/assets/img/face-shield.png">
          <ul>
            <li>• Visor Made From PET Material</li>
            <li>• Anti-Fog Coating</li>
            <li>• Elastic Band Fram</li>
            <li>• Disposable</li>
          </ul>
          <span>$ 0.86</span>
        </div>
        <div class="protections-right">
          <h3>PROTECTIVE GOGGLES</h3>
          <img src="@/assets/img/goggles.png">
          <ul>
            <li>• Fits Over Glasses</li>
            <li>• Anti-Fog Coating</li>
            <li>• Made From TPE Material</li>
            <li>• Lightweight</li>
          </ul>
          <span>$ 0.00</span>
        </div>
      </div>
    </div>
  </section>
</template>

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
