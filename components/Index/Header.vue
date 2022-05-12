<template>
  <header class="header">
    <div class="container">
      <img class="header-logo" src="@/assets/img/logo.svg">
      <ul ref="nav" class="header-nav">
        <li @click.prevent="changeTab(0)"><a href="#">Home</a></li>
        <li><a href="#">Shop</a></li>
        <li><a href="#">Contacts</a></li>
      </ul>
      <div class="header-search">
        <img src="@/assets/img/search.svg">
        <span>Search for Products</span>
      </div>
      <button class="header-btn" @click.prevent="toggleMenu">
        <span></span>
        <span></span>
        <span></span>
        <svg width="26" height="24" viewBox="0 0 26 24" fill="none" xmlns="http://www.w3.org/2000/svg"><path d="M2 2L13 12.25M13 12.25L24 22.5M13 12.25L24 2M13 12.25L2 22.5" stroke="#3068BB" stroke-width="3"/></svg>
      </button>
    </div>
  </header>
</template>
<script>
export default {
  methods: {
    toggleMenu(e){
      this.$refs.nav.classList.toggle('active')
      e.target.classList.toggle('active')
    },
    changeTab(index){
      this.$store.state.index = index
    }
  }
}
</script>
<style lang="scss" scoped>
.header{
  margin-bottom: 30px;
  @media(min-width:992px){
    margin-bottom: 0;
    padding: 60px 0 120px;
  }
  .container{
    position: relative;
    @media(min-width:992px){
      display: flex;
      justify-content: space-between;
      align-items: center;
    }
  }
  &-nav{
    display: flex;
    max-width: 450px;
    width: 100%;
    justify-content: space-between;
    @media(max-width:991px){
      max-height: 0px;
      transition: 1s ease;
      overflow: hidden;
      &.active{
        padding-top: 15px;
        padding-bottom: 15px;
        max-height: 1000px;
        max-width: 100%;
        @media(min-width:576px){
          padding-top: 30px;
          padding-bottom: 30px;
        }
      }
    }
    a{
      font-weight: 500;
      font-size: 18px;
      color: #1A76DC;
      text-decoration: none;
      border: 1px solid transparent;
      border-radius: 15px;
      padding: 10px;
      &:hover{
        border: 1px solid #7EAFE6;
        transition: .7s;
      }
    }
  }
  &-search{
    @media(max-width:991px){
      text-align: center;
    }
    img{
      cursor: pointer;
    }
    span{
      font-weight: 500;
      font-size: 12px;
      color: #7EAFE6;
      padding-left: 15px;
    }
  }
  &-btn{
    position: absolute;
    padding: 10px 0;
    background: none;
    border: none;
    right: 10px;
    top: 6px;
    display: block;
    border: 1px solid transparent;
    border-radius: 15px;
    transition: .5s ease;
    width: 40px;
    @media(min-width:992px){
      display: none;
    }
    *{
      pointer-events: none;
    }
    span{
      height: 3px;
      background: #3068BB;
      display: block;
      transition: opacity .5s ease;
      &:not(:first-child){
        margin-top: 5px;
      }
    }
    svg{
      opacity: 0;
      position: absolute;
      left: 50%;
      top: 50%;
      transform: translate(-50%, -50%);
      transition: opacity .5s ease;
    }
    &.active{
      span{
        opacity: 0;
      }
      svg{
        opacity: 1;
      }
    }
  }
}
</style>