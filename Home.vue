<template>
    <Header/>
    <h2>List of Restaurants</h2>
    <table border=1>
            <td>ID</td>
            <td>NAME</td>
            <td>ADDRESS</td>
            <td>CONTACT</td>

        <tr v-for="item in restaurants" :key="item.id">
            <td>{{item.id}}</td>
            <td>{{item.name}}</td>
            <td>{{item.address}}</td>
            <td>{{item.contact}}</td>

        </tr>
    </table>
</template>

<script>
import Header from './Header.vue'
// import json from './json/rest_mgmt.json'
export default {
    name:'Home',

    data(){
        return{
            name:'',
            restaurants:[
                {'id':1,'name':"kfc",'address':"hyderabad","contact":"124578"},
                {'id':2,'name':"dominos",'address':"suncity","contact":"124"},
                {'id':3,'name':"pizza hut",'address':"toli chowki","contact":"369852"}
            ]
        }
    },

    components:{
       Header
   } 
//     mounted()
// {
//     let newuser=localStorage.getItem('user-info');
//     if (!newuser)
//     {
//         this.$router.push({name:"SignUp"})
//     }
// }
}
</script>

