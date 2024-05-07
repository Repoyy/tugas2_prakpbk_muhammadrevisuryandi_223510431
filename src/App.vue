<template>
  <div class="flex items-center justify-center h-screen">
    <div class="bg-gray-700 text-white rounded-lg p-8 max-w-lg w-full">
        <form action="#" method="POST">
            <div class="mb-6">
                <label for="first-name" class="block mb-2 text-sm font-medium">Nama Depan</label>
                <input type="text" id="first-name" class="bg-gray-50 border border-gray-300 text-gray-900 text-sm rounded-lg focus:ring-blue-500 focus:border-blue-500 block w-full p-2.5" placeholder="Muhammad Revi" required>
            </div>
            <div class="mb-6">
                <label for="last-name" class="block mb-2 text-sm font-medium">Nama Belakang</label>
                <input type="text" id="last-name" class="bg-gray-50 border border-gray-300 text-gray-900 text-sm rounded-lg focus:ring-blue-500 focus:border-blue-500 block w-full p-2.5" placeholder="Suryandi" required>
            </div>
            <div class="mb-6">
                <label for="email" class="block mb-2 text-sm font-medium">Email</label>
                <input type="email" id="email" class="bg-gray-50 border border-gray-300 text-gray-900 text-sm rounded-lg focus:ring-blue-500 focus:border-blue-500 block w-full p-2.5" placeholder="revim1809@gmail.com" required>
            </div>
            <div class="mb-6">
                <label for="phone-number" class="block mb-2 text-sm font-medium">Nomor Hp</label>
                <input type="tel" id="phone-number" class="bg-gray-50 border border-gray-300 text-gray-900 text-sm rounded-lg focus:ring-blue-500 focus:border-blue-500 block w-full p-2.5" placeholder="+628....." required>
            </div>
            <div class="mb-6">
                <label for="message" class="block mb-2 text-sm font-medium">Masukkan Pesan</label>
                <textarea id="message" @click="showModal = true" class="bg-gray-50 border border-gray-300 text-gray-900 text-sm rounded-lg focus:ring-blue-500 focus:border-blue-500 block w-full p-2.5" placeholder="ketik pesan.." required></textarea>
            </div>
            <button type="submit" class="text-white bg-blue-700 hover:bg-blue-800 focus:ring-4 focus:outline-none focus:ring-blue-300 font-medium rounded-lg text-sm w-full sm:w-auto px-5 py-2.5 text-center">Kirim pesan</button>
        </form>
    </div>

    
    <div v-if="showModal" class="fixed inset-0 flex items-center justify-center z-50">
      <div class="absolute bg-white rounded-lg p-8 max-w-md">
        <h2 class="text-lg font-semibold mb-4">Masukkan pesan</h2>
        <textarea class="bg-gray-50 border border-gray-300 text-gray-900 text-sm rounded-lg focus:ring-blue-500 focus:border-blue-500 block w-full p-2.5" placeholder="Enter your message..."></textarea>
        <div class="mt-4 flex justify-end">
          <button @click="showModal = false" class="text-white bg-blue-700 hover:bg-blue-800 px-4 py-2 rounded-lg">Close</button>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      showModal: false
    };
  },
  methods: {
    toggleModal() {
      this.showModal = !this.showModal;
    }
  }
};
</script>


<style scoped>
  @import 'tailwindcss/base';
  @import 'tailwindcss/components';
  @import 'tailwindcss/utilities';
  @import 'flowbite';


</style>