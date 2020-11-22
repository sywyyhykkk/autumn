<template>
<div class="container">
    <table class="icon-table">
    <div class="icon-container">
        <img src="../../assets/images/logo.png" alt="logo.png">
        Login
    </div>
    </table>
    <table class="login-table">
    <div class="login-box">    
    <span>
        Username 
    </span>
    <input type="username" placeholder="Username"/>
    <span>    
        Password
    </span>
    <input type="password" placeholder="Password"/>    
    </div>
    <div class="button">
      <button @click="login">Login</button>  
    </div>
    </table>
    <div class="register-box">
     <nuxt-link :to="{ name: 'registration' }">
     Register
     </nuxt-link>
     </div>
</div>
</template>

<script>
export default {}
</script>

<style scoped>
.container {
    width: 100%;
    height: 800px;
    display: flex;
    flex-direction: column;
    align-items: center;
}
.login-table {
    border: 1px solid black;
    flex-direction: column;
    width: 340px;
    height: 344px;
    margin: 0 auto;
    display: flex;
    align-items: center;
}
.icon-container {
    padding-top: 32px;
    padding-bottom: 24px;
    display: flex;
    flex-direction: column;
    text-align: center;
}
.icon-container img {
    width: 70px;
    height: 70px;
}
input {
    border-radius: 3px;
    border-width: 0px;
    border-style: inset;
    height:40px;
    width: 300px;
}
.login-box {
    display: flex;
    flex-direction: column;
    gap: 20px;
}
button {
    cursor: pointer;
    margin-top: 25px;
    background-color: white;
    border-radius: 3px;
    width: 300px;
    height: 36px;
    border: 1px solid #93abd3;
    color: #93abd3;
    cursor: pointer;
    outline: aliceblue;
    }
button:hover {
  background-color: #93abd3;
  color: white;
}
.register-box{
    margin-top: 10px;
    display: flex;
    justify-content: space-between;
}
.login-box span{
    margin-top: 30px;
}
</style>
