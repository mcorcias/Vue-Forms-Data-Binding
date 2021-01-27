<template>
  <form>
      <label>Email:</label>
      <input type="email" required v-model="email">

      <label>Password:</label>
      <input type="password" required v-model="password">

      <label>Role:</label>
      <select v-model="role">
          <option value="developer">Web Developer</option>
          <option value="designer">Web Designer</option>
      </select>

      <div class="terms">
          <input type="checkbox" v-model="terms" required>
          <label>Accept terms and conditions</label>
      </div>


    
        <div class="box">
          <input type="checkbox" value="moshe" v-model="names">
          <label>Moshe</label>
        </div>
        <div class="box">
          <input type="checkbox" value="avraam" v-model="names">
          <label>Avraam</label>
        </div>
        <div class="box">
          <input type="checkbox" value="mario"  v-model="names">
          <label>Mario</label>
        </div>
 

  </form>
  <p>Email:{{email}}</p>
  <p>Paword:{{password}}</p> 
  <p>Role:{{role}}</p>
  <p>Terms accepted: {{terms}}</p>
  <p>Names: {{names}}</p>
</template>

<script>
export default {
    data(){
        return{
            email: '',
            password: '',
            role: 'designer',
            terms: false,
            names:[]
        }
    },
 
}
</script>

<style>
  form {
    max-width: 420px;
    margin: 30px auto;
    background: white;
    text-align: left;
    padding: 40px;
    border-radius: 10px;
  }
  label {
    color: #aaa;
    display: inline-block;
    margin: 25px 0 15px;
    font-size: 0.6em;
    text-transform: uppercase;
    letter-spacing: 1px;
    font-weight: bold;
  }
  input, select {
    display: block;
    padding: 10px 6px;
    width: 100%;
    box-sizing: border-box;
    border: none;
    border-bottom: 1px solid #ddd;
    color: #555;
  }

  input,select:focus{
    outline:0 ;
  }

  .terms,.box{
      display: flex;
      align-items: center;
      justify-content: flex-start;
     

  }
  input[type="checkbox"]{
      position: relative;
      width: 20px;
      top: 5px;  
  }
  


</style>