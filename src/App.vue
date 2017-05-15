<template>
  <div id="app">
    <side-bar>
      <side-bar-item v-for="obj in list">
        <side-bar-sub :length="obj.children.length">
          <template slot="title">{{obj.title}}</template>
          <side-bar-item v-for="children in obj.children">
            {{children}}
          </side-bar-item>
        </side-bar-sub>
  
      </side-bar-item>
    </side-bar>
  </div>
</template>

<script>
import sideBar from './components/menu/menu.vue'
import sideBarItem from './components/menu/menu-item.vue'
import sideBarSub from './components/menu/menu-sub.vue'
export default {
  data() {
    return {
      list: [
        {
          title: '导航一',
          children: ['导航一', '导航二', '导航三', '导航四']
        },
        {
          title: '导航二',
          children: ['导航一', '导航二', '导航三']
        },
        {
          title: '导航三',
          children: ['导航一', '导航二']
        },
        {
          title: '导航四',
          children: []
        }
      ]
    }
  },
  components: { sideBar, sideBarItem, sideBarSub }
}
</script>
<style>
html,
body {
  height: 100%;
  width: 100%;
  overflow: hidden;
  margin: 0;
  padding: 0;
  font-family: Helvetica, sans-serif;
}
#app{
  height: 100%;
}
</style>
