<template>
  <div class="body">
    <div class="textContainer">
      <div class="agora">Agora</div>
      <div class="text">한 정치인마다 하나의 거버넌스를</div>
    </div>
    <div class="carouselContainer">
      <div class="phone">
        <transition name="fade">
          <div v-if="nameGo" class="party">정당 이름</div>
        </transition>
        <transition name="fade">
          <div v-if="nameGo" class="name">홍길동</div>
        </transition>
      </div>
      <!-- <img v-if="logo" class="logoWing" src="../assets/logosvgs/logosvg1.svg"> -->

      <transition name="logo">
        <img
          v-if="logo"
          class="logoWing"
          v-bind:src="require(`../assets/logosvgs/logosvg${nowurl}`)"
        />
      </transition>
      <transition name="fade">
        <div v-if="peopleGo" class="people"></div>
      </transition>

      <transition-group name="slide" class="transition">
        <span
          v-for="(n, index) in colorList"
          v-bind:key="n"
          class="slide"
          v-bind:style="{
            left: 1 + (index - 5) * 220 - 90 + 'px',
            backgroundColor: colorListR[n - 1],
          }"
        >
        </span>
      </transition-group>
    </div>
    <!-- <div v-on:click="moveLeft">click me!</div> -->
  </div>
</template>

<script>
export default {
  data() {
    return {
      peopleGo: true,
      nameGo: true,
      logo: true,
      colorList: [1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 16],
      colorListR: [
        "#7094BA",
        "#EDF0F2",
        "#7094BA",
        "#3A5D81",
        "#082E55",
        "#E9B66A",
        "#082E55",
        "#3A5D81",
        "#7094BA",
        "#EDF0F2",
        "#7094BA",
        "#3A5D81",
        "#082E55",
        "#E9B66A",
        "#082E55",
        "#3A5D81",
      ],
      temp: [],
      nownum: 1,
    };
  },
  computed: {
    nowurl() {
      return this.nownum + ".svg";
    },
  },
  methods: {
    moveLeft() {
      this.peopleGo = false;
      setTimeout(() => {
        this.nameGo = false;
      }, 60);
      setTimeout(() => {
        // this.nameGo = true;
        this.temp = this.colorList.slice();
        this.temp.push(this.temp.shift());
        this.colorList.splice(0, 16);
        this.logo = false;
      }, 530);
      setTimeout(() => {
        this.peopleGo = true;
      }, 1400);
      setTimeout(() => {
        this.nameGo = true;
      }, 1460);

      setTimeout(() => {
        this.colorList = this.temp;
        this.nownum = (Math.abs(((this.temp[4] - 1) % 8) - 4) % 8) + 1;
      }, 1530);

      setTimeout(() => {
        this.logo = true;
      }, 1700);
    },
    start() {
      setTimeout(() => {
        this.moveLeft();
        this.start();
      }, 3000);
    },
  },
  created() {
    setTimeout(() => {
      this.start();
    }, 2000);
  },
};
</script>

<style scoped>
.agora {
  font-family: "Rajdhani";
  font-style: normal;
  font-weight: 600;
  font-size: 24px;
  line-height: 31px;
  /* identical to box height */

  /* Primary */

  color: #001e3d;
}

.text {
  margin-top: 20px;
  font-family: "Atomy";
  font-style: normal;
  font-weight: 700;
  font-size: 40px;
  line-height: 55px;

  /* Bg navy */

  color: #fff;
}

.body {
  background: #adb2bf;
  width: 100vw;
  height: 115vh;

  padding-top: 150px;
}

.textContainer {
  display: flex;
  flex-direction: column;
  padding-left: 360px;
}

.slide {
  position: absolute;
  top: 620px;
  width: 180px;
  height: 180px;
  background: #3a5d81;
  border-radius: 30px;
  order: 2;
  z-index: 1;
}

.carouselContainer {
  position: relative;
  height: 900px;
  width: 100%;
  overflow: hidden;
  /* left:50%; */
}

.slide-enter-active,
.slide-leave-active {
  transition: all 1s ease;
}

.slide-enter {
  /* transform: translateX(40px); */
}

.slide-leave-to {
  transform: translateX(-220px);
}

.transition {
  position: relative;
  left: 50%;
}
.phone {
  display: flex;
  flex-direction: column;
  align-items: center;
  position: absolute;
  width: 360px;
  height: 700px;
  top: 0;
  left: 50%;

  /* Gray_E */

  border: 15px solid #edf0f2;
  border-radius: 50px;
  /* transform: rotate(90deg); */
  transform: translateX(-50%);
  z-index: 2;
  top: 130px;
}

.logoWing {
  position: absolute;
}

.party {
  margin-top: 60px;
  font-family: "Atomy";
  font-style: normal;
  font-weight: 500;
  font-size: 16px;
  line-height: 22px;
  text-align: center;

  /* Navy 3 */

  color: #3a5d81;
}

.name {
  font-family: "Atomy";
  font-style: normal;
  font-weight: 700;
  font-size: 30px;
  line-height: 42px;
  /* identical to box height */

  text-align: center;

  /* Bg navy */

  color: #001e3d;
  margin-top: 10px;
}

.people {
  position: absolute;
  width: 380px;
  height: 380px;
  left: 50%;
  top: 296px;
  transform: translateX(-50%);

  background-size: cover;
  background-image: url("../assets/abraham-lincoln.png");
  z-index: 0;
}

.fade-enter-active,
.fade-leave-active {
  transition: all 0.5s ease;
  opacity: 1;
}

.fade-leave-to,
.fade-enter {
  opacity: 0;
}

.logo-enter-active,
.logo-leave-active {
  transition: all 0.5s ease;
  opacity: 1;
}

.logo-leave-to,
.logo-enter {
  opacity: 0;
}

.logoWing {
  position: absolute;
  left: 50%;
  margin-left: 62px;
  top: 216px;
}
</style>
