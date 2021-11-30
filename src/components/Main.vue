<script setup>
import { ref } from 'vue'
import FeihuaCollection from '../FeihuaCollection.json'

const keys = Object.keys(FeihuaCollection)
let currentKey = 0
let content = ''

function handleChangeSession(index) {
  console.log(index);
  currentKey = index
}
function handleClickWord() {}
</script>

<template>
  <div id="main">
    <button v-for="(v, i) in keys" :key="i" @click="handleChangeSession(i)">
      {{ v }}
    </button>
    <br />
    <button v-for="(v, i) in FeihuaCollection[keys[currentKey]]" :key="i" @click="handleClickWord(i)">
      {{ v }}
    </button>
    <br />
    <textarea name="" id="" cols="30" rows="10" v-model="content"> </textarea>
  </div>
</template>

<style scoped></style>
