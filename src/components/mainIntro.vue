<template>
  <div class="body">
    <div class="detail">새로운 탈중앙화 거버넌스</div>
    <div class="catchPrise">내 생각을 정치인에게</div>
    <div class="catchPrise">열린 소통의 장, 아고라</div>
    <div class="startBtn">시작하기</div>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
.body {
  width: 100vw;
  height: 90vh;
  background-image: url("../assets/introImg.png");
  background-size: cover;

  display: flex;
  flex-direction: column;
  align-items: center;
  z-index: 3;

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
  color: #001e3d;
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
