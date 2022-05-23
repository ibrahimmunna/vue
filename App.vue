<template>
<div v-bind:class ="centerClass">
<div v-bind:class ="boxClass">
  <RenderWord></RenderWord>
</div>
<div v-bind:class ="boxClass">
  <AttributeBinding></AttributeBinding>
</div>
<div v-bind:class ="boxClass">
  <EventListener></EventListener>
  <br>
  <br>
</div>
<div v-bind:class ="boxClass">
  <FormBinding></FormBinding>
  <br>
</div>
<div v-bind:class ="boxClass">
  <IfElse></IfElse>
</div>
<div v-bind:class ="boxClass">
  <ListRender></ListRender>
</div>
<div v-bind:class ="boxClass">
  <ComputedProperty></ComputedProperty>
</div>
<div v-bind:class ="boxClass">
  <LifeCycle></LifeCycle>
</div>
<div v-bind:class ="boxClass">
  <WatchersMethod></WatchersMethod>
</div>
<div v-bind:class ="boxClass">
  <ChildComponent :msg = 'greetings'></ChildComponent>
</div>
<div v-bind:class ="boxClass">
  <EmitEvent @response="(msg) => childMsg = msg"></EmitEvent>
  <p>{{childMsg}}</p>
</div>
</div>
</template>

<script>
import RenderWord from './components/render'
import AttributeBinding from './components/AttributeBindings'
import EventListener from './components/EventListener'
import FormBinding from './components/FormBinding.vue'
import IfElse from './components/IfElse.vue'
import ListRender from './components/ListRender.vue'
import ComputedProperty from './components/ComputedProperty.vue'
import LifeCycle from './components/LifeCycle.vue'
import WatchersMethod from './components/Watchers.vue'
import ChildComponent from './components/PropsComponents.vue'
import EmitEvent from './components/EmitEvent.vue'
export default {
  name: 'App',
  data(){
    return{
      greetings:"Props passed by Child components",
      childMsg: 'Not Activated',
      centerClass: 'center',
      boxClass:'box'
    }
  },
  components: {
   RenderWord,
   AttributeBinding,
   EventListener,
   FormBinding,
   IfElse,
   ListRender,
   ComputedProperty,
   LifeCycle,
   WatchersMethod,
   ChildComponent,
   EmitEvent
    
  }
}
</script>
<style>
.center{
  text-align: center;
}
.box{
  border: 10px solid blue;
  margin: 10px;
}
</style>

