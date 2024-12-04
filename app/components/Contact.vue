<script setup>
import { ref } from 'vue'

const formData = ref({
  name: '',
  email: '',
  service: '',
  budget: '',
  message: ''
})

const services = [
  'Select project type',
  'Web Development',
  'Mobile Development',
  'UI/UX Design',
  'Consulting'
]

const budgets = [
  'Select project budget',
  'Less than $5,000',
  '$5,000 - $10,000',
  '$10,000 - $25,000',
  '$25,000+'
]

const handleSubmit = () => {
  // Handle form submission logic here
  console.log(formData.value)
}
</script>

<template>
  <div id="contact" class="container mx-auto my-24 max-w-7xl px-8 py-8">
    <div class="flex flex-col md:flex-row gap-16">
      <!-- Left Section -->
      <div class="flex-1">
        <h1 class="text-5xl font-bold mb-4">Let's Talk</h1>
        <p class="text-gray-600">
          Have some big idea or brand to develop and need help? Then reach out we'd love to hear about your project and provide help
        </p>
        
        <div class="mt-8">
          <h2 class="text-2xl font-semibold mt-8 mb-2">Email</h2>
          <a href="mailto:customercare@itsquarehub.com" class="text-gray-600 hover:text-purple-600">
            customercare@itsquarehub.com
          </a>
          
          <h2 class="text-2xl font-semibold mt-8 mb-2">Socials</h2>
          <div class="flex flex-col gap-2">
            <a href="#" class="text-gray-600 hover:text-purple-600 underline">Instagram</a>
            <a href="#" class="text-gray-600 hover:text-purple-600 underline">Twitter</a>
            <a href="#" class="text-gray-600 hover:text-purple-600 underline">Facebook</a>
          </div>
        </div>
      </div>

      <!-- Right Section -->
      <div class="flex-1">
        <form @submit.prevent="handleSubmit" class="flex flex-col gap-4">
          <div>
            <input 
              type="text" 
              v-model="formData.name" 
              placeholder="Name" 
              required
              class="w-full px-3 py-3 bg-gray-50 border border-gray-200 rounded-2xl focus:outline-none focus:ring-2 focus:ring-purple-500"
            >
          </div>
          
          <div>
            <input 
              type="email" 
              v-model="formData.email" 
              placeholder="Email" 
              required
              class="w-full px-3 py-3 bg-gray-50 border border-gray-200 rounded-2xl focus:outline-none focus:ring-2 focus:ring-purple-500"
            >
          </div>
          
          <div>
            <select 
              v-model="formData.service" 
              required
              class="w-full px-3 py-3 bg-gray-50 border border-gray-200 rounded-2xl focus:outline-none focus:ring-2 focus:ring-purple-500"
            >
              <option v-for="service in services" :key="service" :value="service">
                {{ service }}
              </option>
            </select>
          </div>
          
          <div>
            <select 
              v-model="formData.budget" 
              required
              class="w-full px-3 py-3 bg-gray-50 border border-gray-200 rounded-2xl focus:outline-none focus:ring-2 focus:ring-purple-500"
            >
              <option v-for="budget in budgets" :key="budget" :value="budget">
                {{ budget }}
              </option>
            </select>
          </div>
          
          <div>
            <textarea 
              v-model="formData.message" 
              placeholder="Message" 
              rows="4" 
              required
              class="w-full px-3 py-3 bg-gray-50 border border-gray-200 rounded-2xl focus:outline-none focus:ring-2 focus:ring-purple-500"
            ></textarea>
          </div>
          
          <button 
            type="submit" 
            class="w-full px-4 py-4 bg-purple-600 text-white font-medium rounded-2xl hover:bg-purple-700 transition-colors duration-200"
          >
            Submit
          </button>
        </form>
      </div>
    </div>
  </div>
</template>
