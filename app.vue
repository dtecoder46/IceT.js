<script setup>

  function getItem(item) {
    if (process.client) {
      return localStorage.getItem(item);
    } else {
      return undefined;
    }
  }

  function setItem(item, value) {
    if (process.client) {
      localStorage.setItem(item, value);
      return true;
    } else {
      return false;
    }
  }

  function calculate() {
    const num1 = document.getElementById("num1").value;
    const num2 = document.getElementById("num2").value;
    const op = document.getElementById("op").value;

    const result = eval(equation);

    const equation = num1 + op + num2 + "=" + result;

    console.log(result);

    setItem("equation", equation);
  }

  function prev_calc() {
    console.log(getItem("equation"));
  }
</script>

<template>
  <div class="bg-hot-pink text-light-pink">
    <br>
    <h1 id="name" class="text-2xl ml-20 shadow-2xl shadow-light-pink w-64">Calculator App</h1><br>
    <form id="calculator" on:click.prevent() class="ml-20">
      <label for="num1">First number</label><br>
      <input id="num1" type="text" name="num1" class="bg-pumpkin border-2 border-pea-green shadow-2xl shadow-light-pink hover:bg-pea-green hover:border-pumpkin"><br><br>

      <label for="num2">Second number</label><br>
      <input id="num2" type="text" name="num2" class="bg-pumpkin border-2 border-pea-green shadow-2xl shadow-light-pink hover:bg-pea-green hover:border-pumpkin"><br><br>

      <label for="op">Operation sign</label><br>
      <input id="op" type="name" name="op" class="bg-pumpkin border-2 border-pea-green shadow-light-pink hover:bg-pea-green hover:border-pumpkin"><br><br>

      <br>

      <button v-on:click="calculate" type="submit" id="calculate" class="p-1.5 border-4 rounded-md border-dark-magenta bg-dark-grape hover:border-light-pink active:translate-y-px">Calculate</button><br><br>
      
      <button v-on:click="prev_calc" type="submit" id="get" class="p-1.5 border-4 rounded-md border-dark-magenta bg-dark-grape hover:border-light-pink active:translate-y-px">Get previous calculation</button>
    </form>

    <br>
  </div>
</template>

<style scoped>
  div {
    font-family: JetBrains Mono, monospace;
  }
</style>