<template>
  <div class="calc">
    <div class="calc__container">
      <h3 class="calc__heading">Ile zaoszczędzisz?</h3>
      <h5 class="calc__txt">Rachunek jest prosty.</h5>
      <div class="calc__main">
        <div class="calc__cube">
          <div class="calc__cube-txt">
            Ile pojemników na szkło zapełniasz miesięcznie?
          </div>
          <input class="calc__cube-value" v-model="a" />
        </div>
        <div class="calc__cube">
          <div class="calc__cube-txt">
            Ile płacisz za wywóz jednego pojemnika na szkło?
          </div>
          <input class="calc__cube-value" v-model="b" />
        </div>
      </div>
      <div class="calc__sum">
        Dzięki kruszarce zaoszczędzisz
        <span class="calc__value">{{ savings }} zł</span> rocznie.
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "CalcSection",

  data() {
    return {
      isClosed: true,
      a: 20,
      b: 20,
    };
  },

  computed: {
    savings() {
      return this.calc(this.a, this.b);
    },
  },

  methods: {
    calc(a, b) {
      return 12 * (a * b - (a * b) / 5);
    },
  },
};
</script>

<style scoped lang="scss">
.calc__container {
  display: flex;
  flex-direction: column;
  align-items: center;
  max-width: 1052px;
  margin: 0px auto 0px;
  padding: 0px 20px 0px 20px;
}
.calc__heading {
  margin-bottom: 25px;
}
.calc__txt {
  margin-bottom: 60px;
}
.calc__main {
  display: flex;
  flex-direction: column;
  gap: 20px;
  margin-bottom: 20px;
  width: 100%;
}
.calc__cube {
  display: flex;
  flex-direction: column;
  align-items: center;
  max-width: 1012px;
  min-width: 320px;
  width: 100%;
  border-radius: 15px;
  background-color: $grey;
}
.calc__cube-txt {
  font-size: 16px;
  font-weight: 900;
  line-height: 20px;
  text-align: center;
  padding: 40px 20px 40px 20px;
}
.calc__cube-value {
  display: flex;
  text-align: center;
  width: 225px;
  height: 70px;
  font-size: 16px;
  color: #c2c2c2;
  line-height: 25px;
  border: 1px solid #212121;
  background-color: $white;
  border-radius: 15px;
  margin-bottom: 40px;
}
.calc__cube-value:active {
  border: none;
}
.calc__sum {
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: column;
  gap: 22px;
  font-size: 16px;
  font-weight: 900;
  line-height: 20px;
  color: $white;
  max-width: 1052px;
  min-width: 320px;
  width: 100%;
  padding: 55px 20px 40px 20px;
  background-color: #212121;
  border-radius: 15px;
}
.calc__value {
  font-size: 28px;
  font-weight: 900;
  line-height: 32px;
  color: $orange;
}
@media (min-width: 630px) {
  .calc__heading {
    margin-bottom: 39px;
  }
  .calc__txt {
    margin-bottom: 83px;
  }
  .calc__cube-txt {
    font-size: 20px;
    font-weight: 900;
    line-height: 30px;
    padding: 40px 0px 40px 0px;
  }
  .calc__cube-value {
    margin-bottom: 50px;
  }
  .calc__sum {
    flex-direction: row;
    font-size: 20px;
    line-height: 30px;
    padding: 55px 15px 45px 15px;
  }
  .calc__value {
    font-size: 24px;
  }
}
@media (min-width: 940px) {
  .calc__main {
    flex-direction: row;
    gap: 30px;
    margin-bottom: 30px;
  }
}
</style>