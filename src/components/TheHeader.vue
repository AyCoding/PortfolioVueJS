<script setup>
import {ref} from "vue";

const hero = ref({
    name: 'Aymeric DE LANGE',
    desc: 'Développeur Frontend'
})
</script>

<template>
    <div class="header">
        <h1>{{ hero.name }}</h1>
        <h2>{{ hero.desc }}</h2>
    </div>
</template>


<style scoped lang="scss">

.header {
  display: flex;
  align-items: center;
  justify-content: center;
  flex-flow: column;
  width: 100%;
  background: #2F80ED;
  color: #F2F2F2;

  text-align: center;
  height: 400px;

  h1 {
    font-size: 50px;
  }

  h2 {
    font-weight: 700;
  }
}

</style>