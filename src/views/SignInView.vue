<template>
  <div class="home">
      <h1>Sign In</h1>
  </div>
  <form class="form">

    <input 
      type="email" 
      name="email"
      class="input"
      placeholder="email.."
      v-model="state.email"
    >

    <input 
      type="password" 
      name="password"
      class="input"
      placeholder="password.."
      v-model="state.password"
    >

    <button 
      type="submit" 
      class="submit-btn"
      @click="submitForm"
    >submit</button>
  </form>
</template>

<script>
import useValidate from '@vuelidate/core'
import { required } from '@vuelidate/validators'
import { reactive, computed } from 'vue'

export default {
  setup() {
    const state = reactive({
      email: '',
      password: ''
    })

    const rules = computed(() => {
      return {
        email: { required },
        password: { required }
      }
    })

    const  v$ = useValidate(rules, state);

    return{
      state,
      v$
    }
  },
  methods: {
    submitForm(){
      this.v$.$validate();
      if(!this.v$.$error){
        alert('form submitted successfully!');
      }else{
        alert('form submition failed.');
      }
   
    }
  }
}
</script>

<style scoped>
  .form{
    margin: auto;
    width: 20%;
    display: flex;
    flex-direction: column;
  }
  .input{
    margin: 20px;
    height: 30px;
    border-radius: 10px;
    border-style: none;
    box-shadow: grey 0 0 5px;
    text-align: center;
    font-family: Avenir, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
  }
  .submit-btn{
    margin: auto;
    margin-top: 20px;
    width: 100px;
    height: 30px;
    color: white;
    background-color: grey;
    border-radius: 10px;
    border-style: none;
    font-family: Avenir, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    font-size: 15px;
    font-weight: bold;
  }
</style>