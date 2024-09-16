<template>
  <div class="max-w-3xl mx-auto">
    <div>
      <h1 class="text-3xl font-semibold mb-6">Benvenuti nella nostra azienda</h1>
    </div>
    <div class="grid md:grid-cols-2 gap-8">
      <div class="space-y-4">
        <p class="text-lg text-gray-700">Siamo lieti di presentarvi la nostra gamma di servizi innovativi e soluzioni su misura. La nostra missione è fornire soluzioni all'avanguardia che soddisfino le esigenze in continua evoluzione dei nostri clienti.</p>
        <router-link to="/servizi" class="inline-block bg-cyan-500 text-white px-6 py-2 rounded-lg hover:bg-cyan-600 transition duration-300">
          Scopri i nostri servizi
        </router-link>
      </div>
      <div class="space-y-4">
        <h2 class="text-xl font-semibold">I nostri punti di forza</h2>
        <ul class="space-y-2">
          <li class="flex items-start">
            <svg class="flex-shrink-0 h-6 w-6 text-cyan-500" fill="none" viewBox="0 0 24 24" stroke="currentColor">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7" />
            </svg>
            <span class="ml-3 text-gray-700">Soluzioni innovative</span>
          </li>
          <li class="flex items-start">
            <svg class="flex-shrink-0 h-6 w-6 text-cyan-500" fill="none" viewBox="0 0 24 24" stroke="currentColor">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7" />
            </svg>
            <span class="ml-3 text-gray-700">Servizi personalizzati</span>
          </li>
          <li class="flex items-start">
            <svg class="flex-shrink-0 h-6 w-6 text-cyan-500" fill="none" viewBox="0 0 24 24" stroke="currentColor">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7" />
            </svg>
            <span class="ml-3 text-gray-700">Assistenza clienti 24/7</span>
          </li>
        </ul>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Home'
}
</script>
