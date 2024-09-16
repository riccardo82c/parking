<template>
  <div class="max-w-3xl mx-auto">
    <h1 class="text-3xl font-semibold mb-6">I Nostri Servizi</h1>
    <div class="grid md:grid-cols-2 gap-8">
      <div class="space-y-4">
        <p class="text-lg text-gray-700">Offriamo una vasta gamma di servizi per soddisfare le vostre esigenze aziendali. Il nostro team di esperti è pronto a fornire soluzioni personalizzate per la vostra crescita.</p>
        <ul class="space-y-2">
          <li class="flex items-start">
            <svg class="flex-shrink-0 h-6 w-6 text-cyan-500" fill="none" viewBox="0 0 24 24" stroke="currentColor">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7" />
            </svg>
            <span class="ml-3 text-gray-700">Consulenza IT</span>
          </li>
          <li class="flex items-start">
            <svg class="flex-shrink-0 h-6 w-6 text-cyan-500" fill="none" viewBox="0 0 24 24" stroke="currentColor">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7" />
            </svg>
            <span class="ml-3 text-gray-700">Sviluppo software personalizzato</span>
          </li>
          <li class="flex items-start">
            <svg class="flex-shrink-0 h-6 w-6 text-cyan-500" fill="none" viewBox="0 0 24 24" stroke="currentColor">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7" />
            </svg>
            <span class="ml-3 text-gray-700">Soluzioni cloud</span>
          </li>
        </ul>
      </div>
      <div class="space-y-4">
        <h2 class="text-xl font-semibold">Perché scegliere noi</h2>
        <ul class="space-y-2">
          <li class="flex items-start">
            <svg class="flex-shrink-0 h-6 w-6 text-cyan-500" fill="none" viewBox="0 0 24 24" stroke="currentColor">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7" />
            </svg>
            <span class="ml-3 text-gray-700">Esperienza pluriennale nel settore</span>
          </li>
          <li class="flex items-start">
            <svg class="flex-shrink-0 h-6 w-6 text-cyan-500" fill="none" viewBox="0 0 24 24" stroke="currentColor">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7" />
            </svg>
            <span class="ml-3 text-gray-700">Soluzioni su misura per le vostre esigenze</span>
          </li>
          <li class="flex items-start">
            <svg class="flex-shrink-0 h-6 w-6 text-cyan-500" fill="none" viewBox="0 0 24 24" stroke="currentColor">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7" />
            </svg>
            <span class="ml-3 text-gray-700">Supporto continuo e assistenza post-vendita</span>
          </li>
        </ul>
        <div class="mt-6">
          <router-link to="/contatti" class="inline-block bg-cyan-500 text-white px-6 py-2 rounded-lg hover:bg-cyan-600 transition duration-300">
            Richiedi una consulenza
          </router-link>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Services'
}
</script>
