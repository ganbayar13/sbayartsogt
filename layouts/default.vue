<template>
  <div>
    <nuxt />
  </div>
</template>
<style>
.bottom-line {
  position: relative;
  padding-bottom: 1.1em !important;
  letter-spacing: 2px !important;
}
.bottom-line:before {
  background: #1e87f0;
  bottom: 0;
  content: '';
  height: 1px;
  left: 50%;
  margin-left: -7px;
  position: absolute;
  width: 14px;
  z-index: 2;
}
.bottom-line:after {
  background: #e4e4e4;
  bottom: 0;
  content: '';
  height: 1px;
  left: 50%;
  margin-left: -40%;
  position: absolute;
  width: 80%;
}
</style>
