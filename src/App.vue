<template>
  <Calculator />
</template>

<style lang="scss">
*,
::before,
*::after {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

html,
body,
#app {
  font-family: "Architects Daughter", cursive;
  height: 100%;
  width: 100%;
  background: #f3f3f3;
}

#app {
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  // text-align: center;
}
</style>

<script>
import Calculator from "@/components/Calculator";
export default {
  components: {
    Calculator,
  },
};
</script>
