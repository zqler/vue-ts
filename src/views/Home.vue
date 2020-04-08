<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js App"/>
    <span @click="onClick">点击</span>
  </div>
</template>

<script lang="ts">
// @ is an alias to /src
import Vue from 'vue'
import HelloWorld from '@/components/HelloWorld.vue'
import Component from 'vue-class-component'
// 推荐使用标准类写，不用语法糖

@Component({
  components: {
    HelloWorld
  }
})
export default class Home extends Vue {
    //初始数据可以直接声明为实例的属性 
    // initial data
     message: string = 'HelloWorld,every body';
     // mounted
     mounted(){
       this.onPrint();
     }
     // computed
      get computedMsg () {
        return 'computed ' + this.message
       }
     // methods
      onClick (): void {
         // window.alert(this.message)
       this.$router.push('About')
     }
     onPrint():void{
       window.alert(this.message)
     }
     callbackMessage(message:string){
       console.log(message)
     }
}
</script>
