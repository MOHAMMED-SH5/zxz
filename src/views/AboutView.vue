<template>
<div>
      <ValidationProvider
      name="value"
      rules="required|email"
      :bails="false"
      v-slot="{ errors, ariaMsg, ariaInput }"
    >
    <div>
      <input type="text" v-model="value" v-bind="ariaInput">
      <span v-bind="ariaMsg">{{ errors[0] }}</span>
    </div>
  </ValidationProvider>



</div>
</template>