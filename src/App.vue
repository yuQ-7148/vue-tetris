<template>
  <div class="app" :style="size">
    <div class="rect" :class="drop?'drop':''">
      <!-- <Decorate/> -->
      <div class="screen">
        <div class="panel">
          <Matrix :propMatrix="matrix" :cur="cur" :reset="reset" />
          <Logo :cur="!!cur" :reset="reset" />
          <div class="state">
            <Point :cur="!!cur" :max="max" :point="points" />
            <p>{{pContent}}</p>
            <Number :number='cur ? clearLines : startLines' />
            <p>{{level}}</p>
            <Number :number='cur?speedRun:speedStart' :length="1" />
            <p>{{nextText}}</p>
            <Next :data="next" />
            <!-- 左侧三个按钮 -->
            <div class="bottom">
              <Music :data="music" />
              <Pause :data="pause" />
              <Number :propTime="true" />
            </div>
          </div>
        </div>
      </div>
    </div>
    <!-- 操作按钮 -->
    <Keyboard :filling='filling' />
    <Guide/>
  </div>
</template>

<style lang="less">
@import './app.less';
@import './loader.less';
</style>

<script src="./app.js"></script>

