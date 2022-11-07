<template>
  <header>
    <div class="slide-menu">
      <div class="name-area">
        <div class="svg-1"></div>
      </div>
      <ul class="slide-list">
        <li class="slide-btn-style slide-btn1"><a href=""> 個人履歷</a></li>
        <li class="slide-btn-style slide-btn2"><a href=""> 作品集</a></li>
        <li class="slide-btn-style slide-btn2"><a href=""> 專題</a></li>
      </ul>
    </div>
  </header>
</template>


<script>
export default {
  name: "AllHeader",
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

header {
  @include size(200px, 100vh);
  position: fixed;
  left: 0;
  background-color: $gray-1;
  .slide-menu {
    @include size(100%, 100%);

    .name-area {
      @include size(100%, 25%);
      @include flex-row(center, center);
      .svg-1 {
        @include size(150px, 150px);
        background-color: $gray-2;
        border-radius: 30px;
      }
    }
    .slide-list {
      @include size(100%, 70%);
      @include flex-col(center, space-around);
      background-color: $gray-2;

      .slide-btn-style {
        @include size(150px, 100px);
        @include flex-row(center, center);
        background-color: $gray-3;
        list-style: none;
        border-radius: 30px;
        a {
          text-decoration: none;
          @include font(32px, bold, none, black);
        }
      }
    }
  }
}
</style>