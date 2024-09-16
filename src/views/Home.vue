<template>
  <div class="max-w-4xl mx-auto">
    <div class="bg-white rounded-lg overflow-hidden">
      <div class="p-8">
        <h1 class="text-3xl font-bold text-gray-800 mb-4">Benvenuti nella nostra azienda</h1>
        <p class="text-gray-600 mb-6">
          Siamo lieti di presentarvi la nostra gamma di servizi innovativi e soluzioni su misura.
          Esplorate il nostro sito per scoprire come possiamo aiutarvi a raggiungere i vostri obiettivi.
        </p>
        <router-link to="/servizi" class="bg-green-500 text-white px-4 py-2 rounded hover:bg-green-600 transition duration-300">
          Scopri i nostri servizi
        </router-link>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Home'
}
</script>
