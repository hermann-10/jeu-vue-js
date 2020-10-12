<template>
    <div class="score" v-if="player">
        {{ score }}
    </div>
</template>

<script>
export default {
  name: 'score',
  props: ['score', 'player']
}
</script>

<style scoped>
  .score {
    display: block;
    height: 50px;
    width: 105px;
    font-size: 19pt;
    font-weight: 600;
    color: greenyellow;
    background: #666;
    padding: 5px;
    line-height: 40px;
    margin: 0 auto;
  }
</style>
