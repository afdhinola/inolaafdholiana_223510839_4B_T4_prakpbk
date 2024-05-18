<template>
  <div id="app">
    <parent-component>
      <template v-slot>
        <p>Hii...</p>
        <p>My Name Is Inola Afdholiana</p>
      </template>
    </parent-component>
  </div>
</template>

<script>
import ParentComponent from './components/ParentComponent.vue';

export default {
  components: {
    ParentComponent,
  },
};
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  text-align: center;
  color: #accd46;
  margin-top: 60px;
}
</style>
