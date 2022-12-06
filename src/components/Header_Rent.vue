<template>
<div>
    <h1> {{titlename}} </h1>
    <h1> {{propertytype}} </h1>

</div>
</template>

<script>

export default{
    name: 'Header_Rent',
    props:{
        titlename: String,
        propertytype: String
    }
}

</script>

<style scoped>

div{
    text-align: center;
    color:rgb(5, 1, 15);
    font-family: 'Times New Roman', Times, serif;
    margin: 3px solid black;
    backgroundcolor: red;
}

h1{
    margin: 2px;
    backgroundcolor: gray;
}

</style>