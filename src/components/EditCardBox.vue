<template>
    <div>
        <label for="name" class="label">name: </label>
        <input type="text" class="input">
        <label for="description" class="label">description: </label>
        <input type="text" class="input">

        <button class="btn">update</button>
        <button class="btn">delete</button>
    </div>
</template>

<style scoped>
    .label{
        margin: 5px;
        color: white;
        font-weight: bold;
    }
    .input{
        margin: 10px 20px;
        height: 30px;
        border-radius: 10px;
        border-style: none;
        box-shadow: grey 0 0 5px;
        text-align: center;
        font-family: Avenir, Helvetica, Arial, sans-serif;
        -webkit-font-smoothing: antialiased;
        -moz-osx-font-smoothing: grayscale;
    }
    .btn{
        margin: 5px;
        width: 80px;
        height: 30px;
        background-color: white;
        border-radius: 10px;
        border-style: none;
        color: grey;
        font-family: Avenir, Helvetica, Arial, sans-serif;
        -webkit-font-smoothing: antialiased;
        -moz-osx-font-smoothing: grayscale;
        font-size: 15px;
        font-weight: bold;
    }
    .btn:hover{
        background-color: whitesmoke;
        cursor: pointer;
    }
    .btn:active{
        background-color: lightgray;
    }
</style>