<template>
  <section :style="{ backgroundColor: color }">
    <img alt="Vue logo" src="./assets/logo.png" />
    <PersonalForm
      :name="name"
      :age="age"
      :color="color"
      @update:name="updateName"
      @update:age="updateAge"
      @update:color="updateColor"
    />
  </section>
  <pre>{{ $data }}</pre>
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
      color: "#0099FF",
    };
  },
  methods: {
    updateName(val) {
      this.name = val;
    },
    updateAge(val) {
      this.age = val;
    },
    updateColor(val) {
      this.color = val;
    },
  },
};
</script>
