<template>
  <div class="body">
    <div class="frame">
      <div class="catchPrise">
        <div class="agora">Agora</div>
        <div class="text">
          <div>NFT를 통해 정치인과</div>
          <div>직접 소통하세요!</div>
        </div>
      </div>
      <div class="scroll">
        <div class="oneNftRow firstRow">
          <div class="oneNft">
            <div class="nft">
              <div class="nftName">nft이름</div>
            </div>
          </div>
          <div class="oneNft">
            <div class="nft">
              <div class="nftName">nft이름</div>
            </div>
          </div>
          <div class="oneNft">
            <div class="nft">
              <div class="nftName">nft이름</div>
            </div>
          </div>
          <div class="oneNft">
            <div class="nft">
              <div class="nftName">nft이름</div>
            </div>
          </div>
        </div>

        <div class="oneNftRow">
          <div class="oneNft">
            <div class="nft">
              <div class="nftName">nft이름</div>
            </div>
          </div>
          <div class="oneNft">
            <div class="nft">
              <div class="nftName">nft이름</div>
            </div>
          </div>
          <div class="oneNft">
            <div class="nft">
              <div class="nftName">nft이름</div>
            </div>
          </div>
          <div class="oneNft">
            <div class="nft">
              <div class="nftName">nft이름</div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
.body {
  width: 100vw;
  height: 90vh;
  padding-top: 50px;
  background-color: #ffffff;

  display: flex;
  flex-direction: column;
  align-items: stretch;
}

.frame {
  margin-top: 100px;
  display: flex;
}

.agora {
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

.catchPrise {
  /* margin-left: 18.75vw; */
  margin-left: 10vw;
}

.oneNftRow {
  margin-left: 43px;
  /* flex: 1; */
  width: 1000px;
  display: flex;
  flex-direction: row;
}

.nft {
  width: 380px;
  height: 70px;
  border-radius: 20px;
  background-color: #e9b66a;

  padding-top: 190px;

  display: flex;
  flex-direction: column;
  align-items: center;
}
.scroll {
  flex-direction: column;
  overflow: auto;
}

.scroll::-webkit-scrollbar {
    display: none; /* Chrome, Safari, Opera*/
}
.nftName {
  width: 340px;
  height: 50px;

  background: rgba(0, 0, 0, 0.5);
  /* backdrop-filter: blur(5px); 상단바 위로 올라가서 없애놓음*/

  /* Note: backdrop-filter has minimal browser support */

  text-align: center;
  border-radius: 25px;

  display: flex;
  flex-direction: column;
  justify-content: center;
}

.oneNft {
  display: flex;
  flex-direction: row;
  margin-right: 50px;
}

.firstRow {
  margin-left: 200px;
  margin-bottom: 50px;
}
</style>
