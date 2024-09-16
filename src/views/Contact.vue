<template>
  <div class="max-w-md mx-auto">
    <div>
      <h1 class="text-2xl font-semibold mb-4">Contattaci</h1>
    </div>
    <div class="divide-y divide-gray-200">
      <div
        class="py-8 text-base leading-6 space-y-4 text-gray-700 sm:text-lg sm:leading-7"
      >
        <p>
          Siamo qui per rispondere alle tue domande. Contattaci in uno dei
          seguenti modi:
        </p>
        <ul class="list-disc space-y-2">
          <li class="flex items-start">
            <span class="h-6 flex items-center sm:h-7">
              <svg
                class="flex-shrink-0 h-5 w-5 text-cyan-500"
                viewBox="0 0 20 20"
                fill="currentColor"
              >
                <path
                  d="M2.003 5.884L10 9.882l7.997-3.998A2 2 0 0016 4H4a2 2 0 00-1.997 1.884z"
                />
                <path
                  d="M18 8.118l-8 4-8-4V14a2 2 0 002 2h12a2 2 0 002-2V8.118z"
                />
              </svg>
            </span>
            <p class="ml-2">Email: info@tuaazienda.com</p>
          </li>
          <li class="flex items-start">
            <span class="h-6 flex items-center sm:h-7">
              <svg
                class="flex-shrink-0 h-5 w-5 text-cyan-500"
                viewBox="0 0 20 20"
                fill="currentColor"
              >
                <path
                  d="M2 3a1 1 0 011-1h2.153a1 1 0 01.986.836l.74 4.435a1 1 0 01-.54 1.06l-1.548.773a11.037 11.037 0 006.105 6.105l.774-1.548a1 1 0 011.059-.54l4.435.74a1 1 0 01.836.986V17a1 1 0 01-1 1h-2C7.82 18 2 12.18 2 5V3z"
                />
              </svg>
            </span>
            <p class="ml-2">Telefono: +39 123 456 7890</p>
          </li>
          <li class="flex items-start">
            <span class="h-6 flex items-center sm:h-7">
              <svg
                class="flex-shrink-0 h-5 w-5 text-cyan-500"
                viewBox="0 0 20 20"
                fill="currentColor"
              >
                <path
                  fill-rule="evenodd"
                  d="M5.05 4.05a7 7 0 119.9 9.9L10 18.9l-4.95-4.95a7 7 0 010-9.9zM10 11a2 2 0 100-4 2 2 0 000 4z"
                  clip-rule="evenodd"
                />
              </svg>
            </span>
            <p class="ml-2">Indirizzo: Via Example 123, 00100 Roma, Italia</p>
          </li>
        </ul>
      </div>
      <div class="pt-6 text-base leading-6 font-bold sm:text-lg sm:leading-7">
        <p>Preferisci che ti contattiamo noi?</p>
        <p>
          <a
            @click.prevent="showModal = true"
            href="#"
            class="text-cyan-600 hover:text-cyan-700"
          >
            Compila il nostro modulo di contatto &rarr;
          </a>
        </p>
      </div>
    </div>

    <ContactFormModal
      :show="showModal"
      @close="showModal = false"
      @submit="handleSubmit"
    />
  </div>
</template>

<script>
import { ref } from 'vue'
import ContactFormModal from '../components/ContactFormModal.vue'

export default {
  name: 'Contact',
  components: {
    ContactFormModal,
  },
  setup() {
    const showModal = ref(false)

    const handleSubmit = (formData) => {
      // Qui puoi gestire l'invio del form, ad esempio inviando i dati a un'API
      console.log('Form submitted:', formData)
      showModal.value = false
    }

    return {
      showModal,
      handleSubmit,
    }
  },
}
</script>
Last edited 2 minutes ago
