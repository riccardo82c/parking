<template>
  <Transition name="modal">
    <div v-if="show" class="fixed inset-0 bg-gray-600 bg-opacity-50 overflow-y-auto h-full w-full flex items-center justify-center" @click.self="$emit('close')">
      <div class="relative bg-white rounded-lg shadow-xl p-8 m-4 max-w-xl w-full">
        <h2 class="text-2xl font-semibold mb-4">Contattaci</h2>
        <form @submit.prevent="submitForm">
          <div class="mb-4">
            <label for="name" class="block text-gray-700 text-sm font-bold mb-2">Nome</label>
            <input type="text" id="name" v-model="form.name" class="shadow appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline" required>
          </div>
          <div class="mb-4">
            <label for="email" class="block text-gray-700 text-sm font-bold mb-2">Email</label>
            <input type="email" id="email" v-model="form.email" class="shadow appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline" required>
          </div>
          <div class="mb-6">
            <label for="message" class="block text-gray-700 text-sm font-bold mb-2">Messaggio</label>
            <textarea id="message" v-model="form.message" class="shadow appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline h-32" required></textarea>
          </div>
          <div class="flex items-center justify-between">
            <button type="submit" class="bg-cyan-500 hover:bg-cyan-700 text-white font-bold py-2 px-4 rounded focus:outline-none focus:shadow-outline transition duration-300">
              Invia Messaggio
            </button>
            <button type="button" @click="$emit('close')" class="text-cyan-600 hover:text-cyan-700 font-bold py-2 px-4 rounded focus:outline-none focus:shadow-outline transition duration-300">
              Chiudi
            </button>
          </div>
        </form>
      </div>
    </div>
  </Transition>
</template>

<script>
import { reactive } from 'vue'

export default {
  name: 'ContactFormModal',
  props: {
    show: Boolean
  },
  emits: ['close', 'submit'],
  setup(props, { emit }) {
    const form = reactive({
      name: '',
      email: '',
      message: ''
    })

    const submitForm = () => {
      emit('submit', form)
      // Reset form after submission
      form.name = ''
      form.email = ''
      form.message = ''
    }

    return {
      form,
      submitForm
    }
  }
}
</script>

<style scoped>
.modal-enter-active,
.modal-leave-active {
  transition: opacity 0.3s ease;
}

.modal-enter-from,
.modal-leave-to {
  opacity: 0;
}
</style>
