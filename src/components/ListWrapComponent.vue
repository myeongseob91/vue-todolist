<template>
  <div class="listWrap">
      <ListComponent></ListComponent>
  </div>
</template>

<script>
import ListComponent from './ListComponent'
    export default {
        components : {
            ListComponent
        }
    }
</script>

<style scoped>
 .listWrap {
   width: 272px;
   margin: 0 4px;
   height: 100%;
   box-sizing: border-box;
   display: inline-block;
   vertical-align: top;
   white-space: nowrap;
 }
</style>
