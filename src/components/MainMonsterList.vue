<script>
import MainMonsterListCard from './MainMonsterListCard.vue';
export default {
  data() {
    return {
      
    }
  }, 
  components:{
    MainMonsterListCard
  }
}
</script>

<template>
  <div class="card-wrapper">
    <MainMonsterListCard/>

  </div>


  
</template>

<style lang="scss" scoped>
// Card container 
.card-wrapper{
  display: flex;
  flex-wrap: wrap;
  height: calc(100vh - 190px);
  max-width: 1200px;
  margin: 0 auto;
  backdrop-filter: blur(3px);
  overflow: auto;
}

.card{
  width: 250px;
  height: 350px;
  border: 1px solid black;
}
</style>