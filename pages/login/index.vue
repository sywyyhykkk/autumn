<template>
<div class="container">
    <div class="login-box">    
        <input type="username" placeholder="Username"/>    
        <input type="password" placeholder="Password"/>    
    </div>
    <div class="button">
        <button @click="login">Login</button>  
        <button @click="login">Register</button>  
    </div>
</div>
</template>

<script>
export default {}
</script>

<style scoped>
.container {
    background-color: #f3eac2;
    width: 100%;
    height: 800px;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    border:3px solid #000
}
input{
    border-width: 0px;
    border-style: inset
}
.login-box {
    display: flex;
    flex-direction: column;
    gap: 20px;
    margin-bottom: 10px;
}
button{
    cursor: pointer;
    margin-top: 25px;
    background-color: white;
    border-radius: 3px;
    width: 140px;
    height: 40px;
    border: 1px solid #9ad3bc;
    color: #9ad3bc;
    cursor: pointer;
    outline: aliceblue;
    }
button:hover {
    background-color: #9ad3bc;
    color: white;
}
</style>
