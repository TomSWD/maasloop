<template>
  <div class="cta">
    <div class="cta__container">
      <h5 class="cta__txt1">To na co wydasz zaoszczędzoną gotówkę?</h5>
      <a href="#" class="cta__btn btn">
        <div>KUP <span class="btn__price">8499 zł</span></div>
      </a>
      <div class="cta__txt2">
        Brzmi dobrze? <br class="resp__br" />Uważaj. Dopiero się rozkręcamy!
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "CtaSection",
};
</script>

<style scoped lang="scss">
.cta__container {
  display: flex;
  flex-direction: column;
  align-items: center;
  max-width: 460px;
  margin: 60px auto 110px;
  padding: 0px 20px 0px 20px;
  gap: 60px;
}
.cta__txt1 {
  text-align: center;
}
.cta__btn {
  max-width: 386px;
  width: 100%;
  height: 80px;
  border-radius: 48px;
  font-size: 24px;
}
.btn__price {
  font-weight: 400;
}
.btn {
  display: flex;
  justify-content: center;
  align-items: center;
  font-weight: 900;
  background-color: $orange;
  box-shadow: 0px 34px 64px -10px rgba(0, 0, 0, 0.15);
}
.btn:hover {
  transition: 0.8s;
  background-color: #212121;
  color: $orange;
}
.cta__txt2 {
  font-size: 20px;
  font-weight: 900;
  line-height: 24px;
  text-align: center;
}
@media (min-width: 630px) {
  .cta__container {
    margin-top: 85px;
    margin-bottom: 150px;
  }
  .cta__txt2 {
    font-size: 28px;
    line-height: 34px;
    margin-top: 20px;
  }
  .cta__btn {
    height: 95px;
  }
  .resp__br {
    display: none;
  }
}
</style>