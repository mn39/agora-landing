<template>
  <div class="body">
    <div class="img">
      <div class="catchPrise">이용가이드를 참고하세요!</div>
      <div class="startBtn">가이드 보기</div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
.body {
  padding-top: 0px;
  width: 100vw;
  height: 80vh;

  background-color: #001e3d;
}
.img {
  width: 100vw;
  height: 80vh;
  background-image: url("../assets/guide.png");
  background-size: cover;
  /* opacity: 0.7; */
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}

.detail {
  margin-top: 180px;
  margin-bottom: 20px;

  font-family: "Atomy";
  /* font-style: normal;
    font-weight: 500; */
  font-size: 20px;
  line-height: 28px;
  text-align: center;
  color: #3a5d81;
}

.catchPrise {
  font-family: "Atomy";
  /* font-style: normal;
    font-weight: 700; */
  font-size: 40px;
  line-height: 55px;
  text-align: center;
  color: #fbfbfb;
}

.startBtn {
  display: flex;
  flex-direction: column;
  justify-content: space-around;
  width: 145px;
  height: 49px;

  margin-top: 50px;

  background: #e9b66a;
  border-radius: 100px;

  color: #ffffff;
  font-family: "Atomy";
  /* font-style: normal;
  font-weight: 700; */
  font-size: 18px;
  line-height: 25px;
  text-align: center;
}
</style>
