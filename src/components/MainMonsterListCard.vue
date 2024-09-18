<script>
export default {
  data() {
    return {
      
    }
  },
  props:{
    monsterObject:{
      type: Object,
      required : true
    }
  },
  mounted(){
    console.log(this.monsterObject); 
  }
}
</script>

<template>
  <div class="card">
    <img :src="monsterObject.card_images[0].image_url" alt="IMAGE">
    <h3>{{ monsterObject.name }}</h3>
    <p>{{ monsterObject.type }}</p>
  </div>
</template>

<style lang="scss" scoped>
.card {
  width: 250px;
  margin-right: 20px;
  margin-bottom: 10px;
  height: 350px;
  border: 1px solid orange;
  color: white;
  text-shadow: 0.5;
  display: flex;
  flex-direction: column;
  align-items: center;
  text-align: center;
}

.card h3, .card p {
  background-color: rgba(0, 0, 0, 0.5); 
  color: white; 
  padding: 5px; 
  border-radius: 5px; 
}

.card img {
  max-width: 80%;
  height: auto;
}
</style>