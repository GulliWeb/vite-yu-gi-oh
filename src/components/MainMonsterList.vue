<script>
import axios from 'axios';
import MainMonsterListCard from './MainMonsterListCard.vue';
export default {
  data() {
    return {
      monsterList: [],
      axiosUrl : "https://db.ygoprodeck.com/api/v7/cardinfo.php?num=20&offset=550"
      
    }
  }, 
  methods:{
    // Metodo per fare una chiamata API con axios
    getMonsters(){
      axios.get(this.axiosUrl)
      .then((response) => {
        console.dir(response.data.data);
        this.monsterList = response.data.data

      })
      .catch(function (error) {
        console.log(error);
      })
        }
      },
  components:{
    MainMonsterListCard
  },
  created(){
    this.getMonsters()
  }
}
</script>

<template>
  <div class="card-wrapper">
    <div class="card-row">
      <MainMonsterListCard 
        v-for="monster in monsterList" 
        :key="monster.id" 
        :monsterObject="monster" 
      />
    </div>
  </div>
</template>
  

<style lang="scss" scoped>
// Card container 
.card-wrapper{
  height: calc(100vh - 190px);
  max-width: 1400px;
  margin: 0 auto;
  backdrop-filter: blur(3px);
  overflow: auto;
}

.card-row{
  display: flex;
  flex-wrap: wrap;
}
</style>