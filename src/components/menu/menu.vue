<template>
  <ul class="sideBar">
    <slot></slot>
  </ul>
</template>

<script>
export default {
  name: 'sideBar',
  componentName: 'sideBar'
}
</script>

<style lang="sass">
  $color-primary: #2a333c;
  .sideBar,ul{
    background:$color-primary;
    list-style:none;
    width:200px;
    overflow:hidden;
    color:#fff;
    line-height:40px;
    height:100%;
    margin:0;
    padding:0;
  }

</style>
