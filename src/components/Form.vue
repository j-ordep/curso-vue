<template>
  <form action="">
    <div>
      <InputText />
    </div>
    <div>
        <InputText />
    </div>
    <div>
      <InputSubmit />
    </div>
  </form>
</template>

<script>
import InputSubmit from './form/InputSubmit.vue';
import InputText from './form/InputText.vue';

export default {
  name: "Form",
  components: {
    InputText,
    InputSubmit
  }
}
</script>