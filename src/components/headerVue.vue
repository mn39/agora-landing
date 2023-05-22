<template>
  <div class="headerBox">
    <div class="logo"></div>
    <div class="contents">
      <div>소개</div>
      <div>가이드</div>
      <div>Token 거래</div>
      <div>NFTs</div>
      <div>governance tool</div>
      <div>Contact Us</div>
    </div>
    <!-- <div class="wallet">지갑 연결</div> -->
  </div>
</template>

<script>
export default {};
</script>

<style>
.logo {
  margin: auto;
  margin-left: 18%;
  margin-right: 0px;
  width: 126px;
  height: 50px;
  background-size: cover;
  background-image: url("../assets/logo_text.png");
}

.headerBox {
  height: 80px;
  width: 100%;
  display: flex;

  position: fixed;

  top:0;
  background-color:#FFFFFF;
  z-index: 15;
}

.contents {
  flex: 1;
  display: flex;
  margin: auto;
  margin-left: 8%;
  margin-right: 18%;
  justify-content: space-between;

  font-family: "Atomy";
  font-style: normal;
  font-weight: 500;
  font-size: 15px;
  color: #001e3d;
}
</style>
