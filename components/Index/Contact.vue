<template>
  <section class="contact">
    <div class="container">
      <div class="contact-box">
        <h2>Have A Question?</h2>
        <button>Contact Us</button>
        <a href="www.supplies.bcommerce.global">www.supplies.bcommerce.global</a>
      </div>
    </div>
  </section>
</template>

<style lang="scss" scoped>
.contact{
  margin-bottom: 30px;
  @media(min-width:768px){
    margin-bottom: 250px;
  }
  &-box{
    max-width: 340px;
    width: 100%;
    margin: 0 auto;
    text-align: center;
    h2{
      font-weight: 700;
      font-size: 36px;
      line-height: 1.2;
      padding-bottom: 55px; 
    }
    button{
      width: 205px;
      height: 45px;
      padding: 10px;
      margin-bottom: 45px;
      border: 1px solid #1A76DC;
      border-radius: 10px;
      background: none;
      color: #1A76DC;
      font-weight: 400;
      font-size: 18px;
      line-height: 1.2;
      transition: .7s;
      &:hover{
        transform: scale(1.1);
        transition: .7s;
        background: #1A76DC;
        color: #fff;
      }
    }
    a{
      text-decoration: none;
      font-weight: 400;
      font-size: 18px;
      color: #1A76DC;
    }
  }
}
</style>