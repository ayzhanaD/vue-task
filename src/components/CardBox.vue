<template>
    <div class='card'>
        <h4>{{itemName}}</h4>
        <p>{{itemDesc}}</p>
        <img 
            :src="itemImage" 
            alt="image" 
            class="image"
        >
        <button 
            id="show-edit-card" 
            @click="showEditCard = true" 
            class="edit-btn btn"
        >edit</button>
    </div>

    <div class="edit-cards">
        <EditCardBox 
        v-show='showEditCard' 
        class='edit-card'
        ></EditcardBox>

        <button 
        v-show='showEditCard' 
        @click="showEditCard = false" 
        class="close-btn"
        >x</button>
    </div>
</template>

<script>
import EditCardBox from '../components/EditCardBox.vue';

export default {
    props:{
        itemImage: String,
        itemName: String,
        itemDesc: String
    },
    components:{
        EditCardBox
    },
    data() {
        return{
            showEditCard: false,
        }
    }
}
</script>

<style scoped>
    .card{
        margin: 20px;
        padding: 20px;
        width: 200px;
        height: auto;
        display: flex;
        flex-direction: column;
        align-items: center;    
        box-shadow: grey 0 0 10px;
        border-radius: 10px;
    }
    .image{
        width: 50%;
        height: 50%;
    }
    .edit-cards{
        display: flex;
        flex-direction: row;
        justify-content: center;
        flex-wrap: wrap;
    }
    .edit-card{
        margin: 10px;
        padding: 20px;
        display: flex;
        width: 200px;
        height: auto;
        flex-direction: column;
        align-items: center;    
        box-shadow: grey 0 0 10px;
        border-radius: 10px;
        background-color: #a3a3a3;
    }
    .close-btn{
        width: 30px;
        height: 30px;
        color: white;
        background-color: grey;
        border-radius: 10px;
        border-style: none;
        text-align: center;
        font-family: Avenir, Helvetica, Arial, sans-serif;
        -webkit-font-smoothing: antialiased;
        -moz-osx-font-smoothing: grayscale;
        font-size: 20px;
        font-weight: bold;
    }
    .close-btn:hover{
        background-color: dimgray;
        cursor: pointer;
    }
    .close-btn:active{
        background-color: lightgrey;
    }
    .edit-btn{
        width: 80px;
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
    .btn:hover{
        background-color: dimgrey;
        cursor: pointer;
    }
    .btn:active{
        background-color: darkgray;
    }
</style>