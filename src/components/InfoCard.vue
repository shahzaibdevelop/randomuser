<template>
    <div class="main" >
        <div class="card">
            <img :src="image" >
            <!-- This : is the shordhand for v-bind which binds id's attribute in sync
                 in this case image dynamic image variable  -->
        <div class="text">
            <!-- <input type="text" v-model="name"> 
                V model synced the input tag with name used in h1 below so
                when user typed something in input tag it will display in h1 tag 
            -->
            
            <!-- <h1 v-if="name.length == 6">Name : {{ name }}</h1> 
                    Use V-if for some conditions to show an element
            --> 
            <h1>Name : {{ name }}</h1>
            <h1>Gender : {{gender}}</h1>
            <h1>Email : {{email}}</h1>
        </div>
            <button v-on:click="getUser()">Change User</button>
            <!-- v-on adds an event listener in the tag  -->

        </div>
    </div>
</template>

<script>
    export default{
        name:'InfoCard',
        // props:{
        //     name:String,
        //     gender:String,
        //     email:String,
        // },
        
        data(){
  
  return {
    name: 'name',
    gender: 'Male',
    email: 'email',
    image:'../assets/logo.svg'
  }
},
methods: {
    async getUser() {
            const res= await fetch('https://randomuser.me/api')
            const {results} = await res.json()
        this.name=results[0].name.first,
    // this.gender= capitalizeFirstLetter(str),
    this.email=results[0].email,
    this.image=results[0].picture.large

    function capitalizeFirstLetter(str) {
  return str.charAt(0).toUpperCase() + str.slice(1);
}
      }
  },
  created(){
    this.getUser();
  }
        
    }
</script>

<style scoped>
*{
    color: black;
}
.text{
    display: flex;
    flex-direction: column;
    gap: 10px;
    margin: 0px 20px ;
    flex-wrap: wrap;
}
.main{
    display: flex;
    justify-content: center;
    align-items: center;
    margin-top: 100px;
}
.card{
    width: 300px;
    height: 420px;
    background-color: #a3dab9 ;
    display: flex;
    gap: 20px;
    flex-direction: column;
    align-items: center;
    border-radius: 25px;
    box-shadow: 20px white;
    box-shadow: -1px -1px 75px 9px rgba(255, 255, 255, 0.35);
-webkit-box-shadow: -1px -1px 75px 9px rgba(249, 249, 249, 0.35);
-moz-box-shadow: -1px -1px 75px 9px rgba(255, 255, 255, 0.35);
}

img{
    width: 120px;
    height: 120px;
    margin-top: 30px;
    border-radius: 60px;
    border: 5px solid rgb(104, 158, 147);
    border-top-left-radius: 29px;
    border-top-right-radius: 29px;
    


}
h1{
    font-size: 2vh;
    font-family: sans-serif;
    background-color: rgb(156, 209, 173);
    padding: 5px;
    border-radius: 10px;
}
button{
    background-color:  rgb(156, 209, 173);
    padding: 10px 20px;
    border-radius: 25px;
    cursor: pointer;
    position: absolute;
    bottom: 20px;
}
button:hover{
    background-color: #252525;
    color: aliceblue;
    transition: 0.5s;
}
</style>