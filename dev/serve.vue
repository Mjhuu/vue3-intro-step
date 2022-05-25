<script lang="ts">
import { defineComponent } from 'vue';
import Vue3IntroStep from '@/vue3-intro-step.vue';

export default defineComponent({
  name: 'ServeDev',
  components: {
    Vue3IntroStep
  },
  data(){
    return{
      lastName: '',
      show: false,
      config: {
        tips: [
          {
            el: '#xxx',
            tipPosition: 'bottom',
            title: '欢迎使用问答管理系统',
            content: '点击左侧菜单进行操作',
          }
        ]
      }
    }
  },
  methods: {
    close(){
      this.show = false;
    }
  }
});
</script>

<template>
  <div id="app">
    <img id="xxx" alt="Vue logo" src="http://pic.iask.cn/fimg/183674993053.jpg">
    <button @click="show = true">改变</button>
    {{lastName}}
    {{show}}
    <vue3-intro-step v-model:show="show" :config="config" />
  </div>
</template>
