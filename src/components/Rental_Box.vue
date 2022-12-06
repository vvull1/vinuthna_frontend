<template>
    
     <div class="Rental_Box">
         
        <div v-for="property in property" :key="property.id" >
                
                <Rental_Item :property="property"/>
        </div>
    
        

     </div>

</template>

<script>

import Rental_Item from "./Rental_Item.vue"
export default{

    name: 'Rental_Box',
    components: {
        Rental_Item
    },
    props: {
        property: Array
    }

}

</script>


<style>

.Rental_Box{
    background-image: url("https://luxury-houses.net/wp-content/uploads/2020/12/Stunning-New-Modern-House-in-New-York-hits-Market-for-12500000-1.jpg");
    background-repeat: no-repeat;
    background-size: 1900px 600px;
   /*background-color: rgb(144, 168, 188);
   */ 
    padding: 40px;
    display: grid;
    grid-template-columns: 1fr 1fr 1fr;
    border:3px solid rgb(29, 70, 127);

}
</style>