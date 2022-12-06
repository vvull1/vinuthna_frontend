<template>
 
    <div
      class="House">
      
       <h3>{{property.Type }}</h3>
      <div class="House-body" style="text-align: intial">
        <h5 class="House-text">Year built: {{ property.Year }}</h5>
        <h5 class="House-text">Number of Rooms: {{ property.Rooms }}</h5>
        <h5 class="House-text">Price: ${{ property.Price }}</h5>
        <h5 class="House-text">Area: {{ property.Area }} Sq ft</h5>
      </div>
    </div>

</template>

<script>
export default {
  name: 'Rental_Item',
  props: {
    property: Array,
  },
};
</script>

<style scoped>
.House-text {
  text-align: left;
  font-size: 15px;
}
.House{
        position: relative;
    flex-direction: column;
    min-width: 0;
    word-wrap: break-word;
    background-clip: border-box;
    border: 1px solid rgba(0,0,0,.125);
    border-radius: 0.25rem;
    color: white;
    background-color :#D2691E;
    margin-bottom: 1rem;
    width: calc(90% - 20px);
    display: inline-flex; 
    padding: 0.5em

}

.House-header{
    font-weight:700;
}

h5 {
  margin: 1px;
}

div {
  background-color: #008080;
  color: black;
  padding: 1em;
}

.red {
  background-color: orangered !important;
}

</style>