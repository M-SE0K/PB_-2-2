<template>
  <div><h1>E-01-instance</h1><E01Instance /></div>
  <div><h1>E-02-reactive</h1><E02Reactive /></div>
  <div><h1>E-03-binding</h1><E03Binding /></div>
  <div><h1>E-04-directives</h1><E04Directives /></div>
  <div><h1>Example 3: Parent-Child (Props/Events)</h1><Example3Parent /></div>
  <!-- <div><h1>Child_Component</h1><Child_Component /></div> -->
  <div><h1>Example 4: Provide/Inject</h1><Example4Parent /></div>
  <div><h1>Child Component 1</h1><ChildComponent1 /></div>
  <div><h1>Child Component 2</h1><ChildComponent2 /></div>
  <div><h1>E-07-Options-API</h1><E07OptionsApi /></div>
  <div><h1>E-08-composition-api</h1><E08CompositionApi /></div>
  <div><h1>E-09-composition-API2</h1><E09CompositionApi2 /></div>
  <div><h1>E-10-ref</h1><E10Ref /></div>
  <div><h1>E-11-reactive</h1><E11Reactive /></div>
  <div><h1>E-12-ref-component</h1><E12RefComponent /></div>
</template>

<script setup lang="ts">
  import E01Instance from "@/components/example1/E-01-instance.vue";
  import E02Reactive from "@/components/example1/E-02-reactive.vue";
  import E03Binding from "@/components/example1/E-03-binding.vue";
  import E04Directives from "@/components/example2/E-04-directives.vue";
  import Example3Parent from "@/components/example3/ParentComponent.vue";
  import Child_Component from "@/components/example3/ChildComponent.vue";
  import Example4Parent from "@/components/example4/ParentComponent.vue";
  import ChildComponent1 from "@/components/example4/ChildComponent1.vue";
  import ChildComponent2 from "@/components/example4/ChildComponent2.vue";
  import E07OptionsApi from "@/components/example5/E-07-Options-API.vue";
  import E08CompositionApi from "@/components/example5/E-08-composition-api.vue";
  import E09CompositionApi2 from "@/components/example5/E-09-composition-API2.vue";
  import E10Ref from "@/components/example6/E-10-ref.vue";
  import E11Reactive from "@/components/example6/E-11-reactive.vue";
  import E12RefComponent from "@/components/example6/E-12-ref-component.vue";
</script>

<style>
</style>
