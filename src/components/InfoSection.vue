<template>
  <div class="info">
    <div class="info__container">
      <h3 class="info__heading">
        Płać 5 razy mniej za wywóz odpadów szklanych.
      </h3>
      <h5 class="info__txt">
        Kruszarka zmniejsza gabaryty szklanych śmieci, a Ty płacisz
        PIĘ-CIO-KROT-NIE niższe rachunki za ich wywóz.
      </h5>
    </div>
  </div>
</template>

<script>
export default {
  name: "InfoSection",
};
</script>

<style scoped lang="scss">
.info {
  max-width: 1440px;
  margin: 0px auto 70px;
}
.info__container {
  display: flex;
  flex-direction: column;
  justify-content: center;
  margin: auto;
  background-color: $orange;
  border-radius: 10px;
}
.info__heading {
  text-align: center;
  padding: 50px 40px 30px 40px;
}
.info__txt {
  max-width: 360px;
  align-self: center;
  text-align: center;
  padding: 0px 20px 70px 20px;
}
@media (min-width: 630px) {
  .info__container {
    border: 20px solid $white;
    border-radius: 30px;
  }
  .info__heading {
    max-width: 710px;
    align-self: center;
  }
  .info__txt {
    max-width: 735px;
  }
}
</style>