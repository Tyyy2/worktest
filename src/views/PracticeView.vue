<template>
  <div class="card-container">
    <div class="practice-card1"></div>
    <div class="practice-card2"></div>
    <div class="practice-card3"></div>
    <div class="practice-card4"></div>
  </div>
</template>

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
  background-color: white;
}
.card-container {
  @include size(80%, 80vh);
  @include position-center();
  background-color: gray;
}
</style>


<script>
export default {
  name: "PracticeView",
};
</script>