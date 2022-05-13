<template>
  <section class="protections">
    <div class="container">
      <div class="protections-item" v-for="item in items">
        <img :src="item.png">
        <p>{{ item.text }}</p>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  data(){
    return{
      items: [
        {
          png: require('@/assets/img/protection-img.png'),
          text: `Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's `
        },
        {
          png: require('@/assets/img/protection-img.png'),
          text: `Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's `
        },
        {
          png: require('@/assets/img/protection-img.png'),
          text: `Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's `
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
    padding: 0 0 140px;
  }
  .container{
    @media(min-width:768px){
      display: flex;
      max-width: 700px;
      width: 100%;
    }
  }
  &-item{
    text-align: center;
    img{
      display: block;
      margin: 0 auto;
      margin-bottom: 45px;
    }
    p{
      font-weight: 400;
      font-size: 14px;
      line-height: 1.6;
      color: #495764;
      padding: 20px;
    }
  }
}
</style>
