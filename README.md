# Monaco for Vue

This is a component that wraps Microsoft's great Monaco editor for Vue.
(yes another one) (this one is better i promise)

All props are reactive except for `otherCfg`, which is only assigned at first render.

See below for (pretty self explanatory) usage.

You may use any theme from
[*here*](https://github.com/brijeshb42/monaco-themes/tree/master/themes)
by name.

```vue
<script setup lang="ts">
import {ref} from "vue";
import Monaco from "simple-vue-monaco";

let value = ref("");
</script>

<template>
<!--value and lang are required-->
  <Monaco
      v-model="value"
      lang="javascript"
      theme="Monokai"
      :readonly="false"
      height="30rem"
      width="20rem"
      :otherCfg="{}"
  />
</template>
```