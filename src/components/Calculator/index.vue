<template>
  <v-container>
    <section class="title">
      <div>
        <h1>Le/Tip</h1>
      </div>
    </section>

    <section class="content-components">
      <InputValues />
      <ExitValues />
    </section>
  </v-container>
</template>

<style lang="scss" scoped>
.title {
  display: flex;
  justify-content: center;
  padding: 35px 0;
  margin-bottom: 30px;
  h1 {
    font-weight: normal;
    font-size: 60px;
  }
}
.content-components {
  width: 100%;
  max-width: 1170px;
  display: flex;
  justify-content: center;
  margin: 0 auto;
}
</style>

<script>
import InputValues from "@/components/Calculator/InputValues";
import ExitValues from "@/components/Calculator/ExitValues";

export default {
  components: {
    InputValues,
    ExitValues,
  },
};
</script>
