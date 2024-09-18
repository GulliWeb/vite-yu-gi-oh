<script>
import MainLoader from './MainLoader.vue';
import MainMonsterList from './MainMonsterList.vue';

export default {
  data() {
    return {
      isLoaded : true,
      
    }
  },
  components: {
    MainLoader,
    MainMonsterList
  }
}
</script>

<template>
  <MainLoader v-if="!isLoaded"/>
  <MainMonsterList v-else />
</template>

<style lang="scss" scoped>
</style>