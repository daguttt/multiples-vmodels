<template>
  <article class="content">
    <form class="form">
      <div class="control">
        <label for="name">Nombre</label>
        <!-- El evento personalizado puede ser de esta forma... -->
        <input
          :value="name"
          @input="$emit('update:name', $event.target.value)"
          type="text"
          placeholder="Ingresa tu nombre"
        />
      </div>
      <div class="control">
        <label for="age">Edad</label>
        <!-- ... O de esta forma -->
        <input
          :value="age"
          @input="(event) => $emit('update:age', event.target.value)"
          type="number"
          placeholder="Ingresa tu edad..."
        />
      </div>
      <div class="control">
        <label for="color">Color favorito</label>
        <input
          :value="color"
          @input="(event) => $emit('update:color', event.target.value)"
          type="color"
          id="color"
          placeholder="Selecciona tu color favorito"
        />
      </div>
    </form>
  </article>
</template>

<script>
export default {
  name: "PersonalForm",
  props: ["name", "age", "color"],
};
</script>

<style scoped>
.content {
  max-width: 1280px;
  width: 100%;
  padding: 1rem;
  margin: 0 auto;
}
.form {
  margin: 0 auto;
  width: 75%;
}
.control {
  margin: 20px 0;
}
label {
  display: block;
}
input[type="text"],
input[type="number"] {
  width: 75%;
  padding: 0.5rem;
}
</style>