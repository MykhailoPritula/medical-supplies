<template>
  <main class="layout layout-default">
    <Header />
    <Nuxt />
    <Footer />
  </main>
</template>
<script>
export default {
  head() {
    return {
      title: 'Medical Supplies',
      meta: [
        {
          hid: 'description',
          name: 'description',
          content: 'description text',
        },
        {
          hid: 'keywords',
          name: 'keywords',
          content: 'keywords, words',
        },
        {
          hid: 'theme-color',
          name: 'theme-color',
          content: '#ffffff',
        },
      ]
    }
  }
}
</script>
<style lang="scss">
.layout-default{
  @import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@300;400;500;600;700&display=swap');
  *{
    font-family: 'Montserrat', sans-serif;
  }
  .container {
    width: 100%;
    padding-left: 10px;
    padding-right: 10px;
    margin-left: auto;
    margin-right: auto;
    position: relative;
    z-index: 2;
    @media (min-width: 768px) {
      max-width: 768px;
    }
    @media (min-width: 992px) {
      max-width: 992px;
    }
    @media (min-width: 1200px) {
      max-width: 1200px;
      padding-left: 0;
      padding-right: 0;
    }
  }
}
</style>