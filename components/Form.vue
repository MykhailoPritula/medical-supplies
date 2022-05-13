<template>
  <section class="form" v-if="form">
    <div class="container">
      <form @submit="submitForm" method="GET">
        <div class="row">
          <div class="field">
            <label for="first_name">First Name</label>
            <input id="first_name" required type="text" v-model="first_name"/>
          </div>
          <div class="field">
            <label for="last_name">Last Name</label>
            <input id="last_name" required type="text" v-model="last_name"/>
          </div>
        </div>
        <div>
          <div class="field">
            <label for="email">Email</label>
            <input id="email" required type="email" v-model="email"/>
          </div>
        </div>
        <div>
          <div class="field">
            <label for="phone">Phone Number</label>
            <input id="phone" required type="tel" v-model="phone"/>
          </div>
        </div>
        <div>
          <div class="field">
            <label for="message">Message</label>
            <textarea id="message" required rows="3" v-model="message"></textarea>
          </div>
        </div>
        <input class="button" type="submit" value="Submit">
      </form>
    </div>
  </section>
</template>
<script>
export default {
  data() {
    return {
      first_name: null,
      last_name: null,
      email: null,
      phone: null,
      message: null,
      form: true
    }
  },
  methods: {
    submitForm(e) {
      e.preventDefault()
      this.form = false
    }
  }
}
</script>
<style lang="scss" scoped>
.form{
  background: #5EB6EA;
  width: 100%;
  margin: 10px auto;
  padding: 20px;
  @media(min-width:992px){
    width: 50%;
  }
  .field {
    display: flex;
    flex-direction: column;
    margin-bottom: 15px;
    input {
      width: 100%;
      padding: 10px;
      height: 30px;
      border: 1px solid #fff;
      border-radius: 5px;
      font-size: 20px;
      line-height: 1.2;
      color: #5EB6EA;
    }
    textarea{
      width: 100%;
      padding: 10px;
      height: auto;
      border: 1px solid #fff;
      border-radius: 5px;
      font-size: 14px;
      line-height: 1.2;
      color: #5EB6EA;
      resize: none;
    }
    label {
      margin-bottom: 10px;
      color: rgb(250, 243, 243);
      font-size: 20px;
      font-weight: 400;
      font-family: sans-serif;
    }
  }
  .button{
    background: linear-gradient(92.66deg, #1A76DC 0%, #2485af 100.68%);
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
  }
}
</style>
