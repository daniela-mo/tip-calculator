<template>
  <div class="container-content">
    <section class="container-content__entrance">
      <div class="container-content__entrance__convert">
        <p>EUR</p>
        <switches
          v-model="enabled"
          class="container-content__entrance__convert__switches"
        ></switches>
        <p>USD</p>
      </div>
      <div class="container-content__entrance__total">
        <label>Valor</label>
        <div class="container-content__entrance__total__lbl">
          <span>$</span>
          <input type="number" value="0.00" :v-model="bill" />
        </div>
      </div>
      <div class="container-content__entrance__wrapper">
        <div>
          <label>Gorjeta: </label>
          <span id="tipPercent">0%</span>
        </div>
        <div>
          <label>10 </label>
          <input
            type="range"
            min="5"
            max="20"
            step="5"
            value="10"
            v-model="tip"
          />
          <label> 20</label>
        </div>
      </div>
      <div class="container-content__entrance__wrapper">
        <div>
          <label for="noOfPeople">Pessoas: </label>
          <span id="splitNum">0</span>
        </div>
        <div>
          <label>2 </label>
          <input
            type="range"
            min="2"
            max="16"
            step="2"
            value="2"
            v-model="numPeople"
          />
          <label> 16</label>
        </div>
      </div>
    </section>
  </div>
</template>

<script>
import Switches from "vue-switches";

export default {
  components: {
    Switches,
  },
  data() {
    return {
      enabled: false,
      // commitConvert: "",
      bill: "",
      tip: "",
      numPeople: "",
    };
  },

  methods: {
    calculateTip() {
      var billtotal = (this.tip / 100) * this.bill;
      tipPercent = billtotal;
      console.log(aqui);
    },
  },
};
</script>

<style lang="scss">
.container-content {
  display: flex;
  border: 1px solid yellowgreen;
  &__entrance {
    display: flex;
    flex-direction: column;
    align-items: center;
    width: 600px;
    font-size: 30px;
    border: 1px solid red;
    &__convert {
      display: flex;
      align-items: center;
      padding: 20px 0;
      p {
        font-size: 18px;
        font-weight: 600;
      }
      &__switches {
        margin: 0 7px;
      }
    }
    &__total {
      display: flex;
      align-items: center;
      padding: 20px 0;
      label {
        font-size: 14px;
        font-weight: 600;
      }
      &__lbl {
        display: flex;
        align-items: center;
        margin-left: 10px;
        input {
          padding: 7px 0;
          font-size: 20px;
          text-align: center;
          font-weight: 600;
          font-family: "Architects Daughter", cursive;
        }
      }
    }
    &__wrapper {
      display: flex;
      flex-direction: column;
      padding: 20px 0;
      label {
        font-size: 14px;
        font-weight: 600;
      }
      span {
        font-size: 22px;
        font-weight: 600;
      }
    }
  }
}
</style>
