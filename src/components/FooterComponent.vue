<template>
    
     
        <div class="content">
            <h3>Copyright ©️{{ currentyear }} Random User</h3>
        </div>
    


    </template>
 <style >
 
    h1{
        color: aliceblue;

    }
    .content{
        background-color: rgb(39, 39, 40);
        width: 100%;
        margin: 0;
        padding: 0;
        display: flex;
        justify-content: center;
        align-items: center;
        position: absolute;
        margin-top: 160px;
        padding-top: 20px;
        border-top-left-radius: 25px;
        border-top-right-radius: 25px;
    }

</style>

<script>
export default{
    name:'Footer',
    props: {
        currentyear : String
    }
}

</script>