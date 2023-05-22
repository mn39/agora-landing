<template>
  <div class="body">
    <div class="logoContainer">
      <div class="logo"></div>
    </div>
    <div class="detail">
      <div class="detailText">
        주(아고라)
        <br />
        <br />

        사업자 등록번호 : 000-00-00000 | 대표 : 홍길동
        <br />
        통신판매업 신고번호 : 2022-서울강남-00000 사업자정보확인
        <br />
        12345 서울특별시 강남구 가나다로 123, 45층 (라마동, 바사아빌딩)
        <br />
        <br />

        고객센터 : 000-0000-0000
      </div>
    </div>
    <div class="links"></div>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
.body {
  width: 100vw;
  height: auto;
  padding-top: 40px;
  padding-bottom: 40px;
  display: flex;
  background-color: #f9fafb;
}
.logoContainer {
  flex: 1;
  display: flex;
  flex-direction: row-reverse;
}
.logo {
  margin-top: 0;
  margin-right: 170px;
}
.detail {
  flex: 1;
  font-family: "Atomy";
  /* font-style: normal;
  font-weight: 500; */
  font-size: 13px;
  line-height: 18px;

  color: #969696;
}
.links {
  flex: 1;
}
.detailText{
    margin-left:50px;
}
</style>
