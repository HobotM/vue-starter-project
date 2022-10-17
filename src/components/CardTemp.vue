<template>
  <div class="card">
    <slot />
  </div>
</template>

<!--In between the <div class="card">, add the <slot /> component.
  This is a component that is provided to you by Vue.
   There is no need to import this component;
    it is globally imported by Vue.js:  -->

<!-- Slots are a mechanism for Vue components that allows you to compose your components in a way other than the strict parent-child relationship.
  Slots give you an outlet to place content in new places or make components more generic. -->
<style>
.card {
  border: 3px solid;
  border-radius: .5rem;
  padding: 1rem;
  margin-bottom: 1rem;
}
</style>
