
<template>
    <div class="container">
        <img src="../assets/logo.svg" alt="logo">
        <div class="link">
        <a :href="linkone">{{one}}</a>
        <a :href="linktwo">{{two}}</a>
        <a :href="linkthree">{{three}}</a>
        </div>
    </div>
</template>
<script>
export default{
    name:'Navbar',
    props:{
        one: String,
        two: String,
        three: String,
        linkone:String,
        linktwo:String,
        linkthree:String

    }
}

</script>
<style scoped>
*{
    margin: 0;
    padding: 0;
}
.link{
    display: flex;
    gap: 20px;
    position: absolute;
    right: 30px;
}
.container{
display: flex;
background-color: #252525;
padding: 20px;
border-radius: 25px;
}
img{
    width: 30px;
    height: 30px;
}

</style>