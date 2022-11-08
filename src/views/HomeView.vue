<template>
  <AllHeader></AllHeader>
  <div class="card-area">
    <div class="card-container">
      <div class="card1 card-style">
        <div class="practice-img"></div>
        <div class="practice-name">Microsoft網站仿切</div>
      </div>
      <div class="card2 card-style">
        <div class="practice-img"></div>
        <div class="practice-name">BMI計算機</div>
      </div>
      <div class="card3 card-style">
        <div class="practice-img"></div>
        <div class="practice-name">色弱遊戲</div>
      </div>
      <div class="card4 card-style">
        <div class="practice-img"></div>
        <div class="practice-name">天氣卡片API串接</div>
      </div>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
import AllHeader from "@/components/AllHeader.vue";
export default {
  name: "HomeView",
  components: { AllHeader },
};
</script>

<style lang="scss">
//--Mixin
$gray-1: rgb(230, 230, 230);
$gray-2: rgb(180, 180, 180);
$gray-3: rgb(130, 130, 130);
$gray-4: rgb(100, 100, 100);
$gray-5: rgb(80, 80, 80);

@mixin size($w, $h) {
  width: $w;
  height: $h;
}

@mixin flex-row($justify_content, $align_items) {
  display: flex;
  justify-content: $justify_content;
  align-items: $align_items;
}

@mixin flex-col($justify_content, $align_items) {
  display: flex;
  flex-direction: column;
  justify-content: $align_items;
  align-items: $justify_content;
}

@mixin font($px, $weight, $family, $color) {
  font-size: $px;
  font-weight: $weight;
  font-family: $family;
  color: $color;
}

@mixin position-center {
  position: absolute;
  top: 50%;
  left: 50%;
  translate: -50% -50%;
}

@mixin keyframe(
  $animation_name,
  $animation_duration,
  $animation_count,
  $animation_time_function
) {
  animation-name: $animation_name;
  animation-duration: $animation_duration;
  animation-iteration-count: $animation_count;
  animation-timing-function: $animation_time_function;
}

@mixin transition($transition_time, $transition_delay, $transition_funtion) {
  transition-duration: $transition_time;
  transition-delay: $transition_delay;
  transition-timing-function: $transition_funtion;
}

//--End of Mixin

body {
  background-color: black;
}
.card-area {
  @include size(calc(100% - 200px), 100vh);
  @include flex-row(center, center);
  position: absolute;
  right: 0;
  //background-color: $gray-1;
  .card-container {
    @include size(80%, 80%);
    //background-color: $gray-1;
    @include flex-row(space-around, space-between);
    flex-wrap: wrap;
    .card-style {
      @include size(45%, 45%);
      border-radius: 20px;
      background-color: $gray-2;
      @include flex-col(center, space-between);
      .practice-img {
        @include size(100%, 80%);
      }
      .practice-name {
        @include size(100%, 15%);
        @include font(20px, bold, none, black);
      }
    }
  }
}
</style>
