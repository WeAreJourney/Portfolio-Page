<template>
  <div class="main">
    <header>
      <div class="title">
        <h1>Contact</h1>
      </div>
    </header>
    <b-container>
      <b-row class="justify-content-center" @submit.prevent="onSubmit">
        <b-form class="col-md-6 col-sm-12">
          <p>{{ msg }}</p>
          <b-form-group label-for="name">
            <b-form-input id="name" 
                          type="text" 
                          placeholder="Name" 
                          v-model="name">
            </b-form-input>              
          </b-form-group>
          <b-form-group label-for="email">
            <b-form-input id="email" 
                          type="email" 
                          placeholder="Email" 
                          v-model="email">
            </b-form-input>              
          </b-form-group>
          <b-form-group label-for="phone">
            <b-form-input id="phone" 
                          type="tel" 
                          placeholder="Phone" 
                          v-model="phone">
            </b-form-input>              
          </b-form-group>
          <b-form-group label-for="Do No Fill This Out" class="hide">
            <b-form-input id="text" 
                          placeholder="Leave this one blank"
                          type="text" 
                          v-model="hide">
            </b-form-input>
          </b-form-group>
          <b-form-textarea id="messageText" 
                            placeholder="Message" 
                            :rows="3" 
                            :max-rows="6" 
                            v-model="messageBody">
          </b-form-textarea>
          <div class="send-btn">
            <b-button type="submit" variant="primary">Send</b-button>
          </div>
        </b-form>
      </b-row>
    </b-container>
    
  </div> 
</template>

<script>
import axios from 'axios'

export default {
  /* eslint-disable */
  name: 'contact',
  data () {
    return {
      name: '',
      email: '',
      phone: '',
      hide: '',
      messageBody: '',
      form: {
        name: '',
        email: '',
        phone: '',
        hide: '',
        messageBody: ''
      },
      msg: ''
    }
  },
  methods: {
    onSubmit (e) {
      this.form.name = this.name
      this.form.email = this.email
      this.form.phone = this.phone
      this.form.hide = this.hide
      this.form.messageBody = this.messageBody
      axios.post('http://localhost:5000/', this.form)
        .then((response) => {
          console.log(response)
          this.msg = response.data
          setTimeout(() => { this.msg = '' }, 5000)
        })
        .catch((error) => {
          console.log(error)
          this.msg = 'This is embarassing.  Something seems to have gone wrong. :('
        })
        this.onReset()
    },
    onReset () {
      this.name = ''
      this.email = ''
      this.phone = ''
      this.hide = ''
      this.messageBody = ''
    }
  }
}
</script>

<style scoped> 
  header {
    width: 100%;
    height: 200px;
    background-color: #f5f8fa; 
    padding-bottom: 10px;
    margin-bottom: 20px;
    border-bottom: 1px solid rgba(0, 0, 0, 0.125);
  }

  .title {
    width: 50%;
    margin: 0 auto;
    padding-top: 40px;
    text-align: center;
  }

  .title > h1 {
    color: #3A4145;
    font-family: montserrat, sans-serif;
    text-transform: uppercase;
    letter-spacing: 0.2rem;
    font-weight: 900;
  }

  button {
    width: 540px;
  }
  
  .send-btn {
    padding-top: 15px;
    display: flex;
    align-items: flex-start;
  }

  .hide {
    display: none !important;
  }

  @media (max-width: 500px) {
    .title {
      width: 100%;
    }

    .title > h1 {
      font-size: 1.5rem;
    }

    header {
      height: 150px;
    }
  }

</style>