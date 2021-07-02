<template>
  <div class="math">
    <h3> Calculator </h3>
    <form>
      <input type="text" class="form-control" v-model="value1">
      <input type="text" class="form-control" v-model="value2">
      <button @click="addNumbers" type="button" class="btn btn-light">Add</button>
      <button @click="subtractNumbers" type="button" class="btn btn-light">Subtract</button>
      <button @click="multiplyNumbers" type="button" class="btn btn-light">Multipy</button>
      <button @click="divideNumbers" type="button" class="btn btn-light">Divide</button>
    </form>
    <p><strong>Result:</strong> {{ result }} </p>
  </div>
</template>
<script>
import { ref } from 'vue';

export default {
  name: 'Calculator',

  setup() {
    let value1 = ref(0);
    let value2 = ref(0);
    let result = ref(0);

    function addNumbers() {
      result.value = parseInt(value1.value) + parseInt(value2.value)
    }

    function subtractNumbers() {
      result.value = parseInt(value1.value) - parseInt(value2.value)
    }

    function multiplyNumbers() {
      result.value = parseInt(value1.value) * parseInt(value2.value)
    }

    function divideNumbers() {
      result.value = parseInt(value1.value) / parseInt(value2.value)
    }

    return {
      value1,
      value2,
      result,
      addNumbers,
      subtractNumbers,
      multiplyNumbers,
      divideNumbers
    }
  },
}
</script>