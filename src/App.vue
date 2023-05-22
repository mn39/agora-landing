<template>
  <div>
    <headerVue></headerVue>
    <mainIntro></mainIntro>
    <OpinionToken></OpinionToken>
    <OneGovernance></OneGovernance>
    <PoliComu></PoliComu>
    <UseGuide></UseGuide>
    <footerVue></footerVue>
  </div>
</template>

<script>
import headerVue from "./components/headerVue.vue";
import mainIntro from "./components/mainIntro.vue";
import OpinionToken from "./components/opinionToken.vue";
import OneGovernance from "./components/oneGovernance.vue";
import PoliComu from "./components/poliComu.vue";
import UseGuide from "./components/useGuide.vue";
import FooterVue from './components/footerVue.vue';
export default {
  components: {
    headerVue,
    mainIntro,
    OpinionToken,
    OneGovernance,
    PoliComu,
    UseGuide,
    FooterVue
},
};
</script>

<style>
@font-face {
  font-family: "Atomy";
  src: url("https://cdn.jsdelivr.net/gh/projectnoonnu/noonfonts_four@1.0/Atomy-Bold.woff")
    format("woff");
  font-weight: normal;
  font-style: normal;
}
</style>
