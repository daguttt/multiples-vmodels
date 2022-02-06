<template>
  <img alt="Vue logo" src="./assets/logo.png" />
  <PersonalForm />
</template>

<script>
import PersonalForm from "./components/PersonalForm.vue";
export default {
  name: "App",
  components: {
    PersonalForm,
  },
  data() {
    return {
      name: "Daniel",
      age: 18,
      color: "#09F",
    };
  },
};
</script>
