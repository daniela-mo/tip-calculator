<template>
  <section>
    <div class="container-content__exit">
      <div class="container-content__exit__result">
        <label for="bill">Conta:</label>
        <span>$</span>
      </div>

      <div class="container-content__exit__result">
        <label>Gorjeta: </label>
        <span id="tipPerPerson">$</span>
      </div>

      <div class="container-content__exit__result">
        <label>Total com Gorjeta: </label>
        <span id="totalAmount">$</span>
      </div>

      <div class="container-content__exit__result">
        <label>por Pessoa: </label>
        <span id="totalPerPerson">$</span>
      </div>
      <!-- <Converter :commit="commitConvert" /> -->
      <Converter />
    </div>
  </section>
</template>

<script>
import Converter from "./Converter";

export default {
  components: {
    Converter,
  },

  // beforeMount() {
  //   this.fetch();
  // },

  // methods: {
  //   fetch() {
  //     const commitConvert = totalAmount;
  //     this.commitConvert = commitConvert;
  //   },
  // },

  //  tipPerPerson = (totalTip / noOfPeople).toFixed(2);
  //      totalPerPerson = (total / noOfPeople).toFixed(2);

  //  exitResult() {

  //      },
};
</script>

<style lang="scss">
.container-content__exit {
  display: flex;
  justify-content: center;
  flex-direction: column;
  width: 600px;
  font-size: 30px;
  border: 1px solid red;
  &__result {
    display: flex;
    align-items: center;
    flex-direction: column;
    padding: 20px 0;
    label {
      font-size: 14px;
      font-weight: 600;
    }
    span {
      margin: 0 7px;
      font-size: 22px;
      font-weight: 600;
    }
  }
}
</style>
