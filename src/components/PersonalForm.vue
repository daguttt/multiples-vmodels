<template>
  <article class="content">
    <form class="form">
      <div class="control">
        <label for="name">Nombre</label>
        <input type="text" placeholder="Ingresa tu nombre" />
      </div>
      <div class="control">
        <label for="age">Edad</label>
        <input type="number" placeholder="Ingresa tu edad..." />
      </div>
      <div class="control">
        <label for="color">Color favorito</label>
        <input type="color" />
      </div>
    </form>
  </article>
</template>

<script>
export default {};
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