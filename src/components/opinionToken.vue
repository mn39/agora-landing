<template>
  <div class="body">
    <div class="computerImg">
      <div class="agora">Agora</div>
      <div class="text">토큰으로 명확한 의견 제시</div>
    </div>
  </div>
</template>

<script>
export default{};
</script>

<style scoped>
.body {
  width: 100vw;
  height: 100vh;
  padding-top: 50px;
  background-color: #ffffff;
}

.computerImg {
  margin: auto;
  width: 65vw;
  height: 53.7vw;
  background-image: url("../assets/computer.png");
  background-size: cover;

  display: flex;
  flex-direction: column;
}

.agora {
  margin-top: 100px;

  font-family: "Rajdhani";
  font-style: normal;
  font-weight: 600;
  font-size: 24px;
  line-height: 31px;
  /* identical to box height */

  /* Primary */

  color: #e9b66a;
}

.text {
  margin-top: 20px;
  font-family: "Atomy";
  font-style: normal;
  font-weight: 700;
  font-size: 40px;
  line-height: 55px;

  /* Bg navy */

  color: #001e3d;
}
</style>
