<template>
  <div>
    <div class="flex">
      <h1>Area Membros</h1>

      <button class="btn-secondary">Sair</button>
    </div>

    <hr />

    <p>Cursos Disponíveis &#8628;</p>

    <ul class="text-lg text-gray-700 font-semibold space-y-4">
      <li>Teste</li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "Dashboard",
  middleware: 'auth'
}
</script>

<style>

</style>