<template>
  <div class="about">
    <h1>This is an about page</h1>
  </div>
</template>
<script lang="ts">
// vue-property-decorator 是在vue-class-component 上增强了更多结合vue 特性的装饰器，新增了这个7个装饰器
// @emit @Inject @Model @Prop @Provide @watch @Component(从vue-class-component继承)
  import { Component, Emit, Inject, Model, Prop, Provide, Vue, Watch } from 'vue-property-decorator'
  @Component
  export default class About extends Vue {
   @Prop()
   propA: number=1

   @Watch('child')
    onChildChange(val: string, oldval: string):void {}
  }
</script>
