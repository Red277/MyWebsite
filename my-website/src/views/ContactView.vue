<template>
  <div style="display: flex; justify-content: center; align-items: center; height: inherit; position: relative;">
    <TitleGraphic title="Contact" />
    <v-sheet width="50%" rounded>

      <p style="padding-bottom: 3rem;">Have any questions or just want to get in touch?</p>
      <form @submit.prevent="submit" style="width: 100%; height: 100%;">
        <v-text-field v-model="name.value.value" :counter="10" :error-messages="name.errorMessage.value"
          label="Name"></v-text-field>
        <v-text-field v-model="email.value.value" :error-messages="email.errorMessage.value"
          label="E-mail"></v-text-field>
        <v-textarea v-model="title" label="Message" maxlength="120" counter single-line></v-textarea>
        <v-btn class="me-4" type="submit">submit</v-btn>
        <v-btn @click="handleReset">clear</v-btn>
      </form>
    </v-sheet>
  </div>
</template>

<script setup>
import TitleGraphic from '@/components/TitleGraphic.vue';
import { ref } from 'vue'
import { useField, useForm } from 'vee-validate'

const { handleSubmit, handleReset } = useForm({
  validationSchema: {
    name(value) {
      if (value?.length >= 2) return true

      return 'Name needs to be at least 2 characters.'
    },
    email(value) {
      if (/^[a-z.-]+@[a-z.-]+\.[a-z]+$/i.test(value)) return true

      return 'Must be a valid e-mail.'
    },
    name(value) {
      if (value?.length >= 2) return true

      return 'Max 500 characters.'
    },
  },
})
const name = useField('name')
const phone = useField('phone')
const email = useField('email')
const select = useField('select')
const checkbox = useField('checkbox')

const items = ref([
  'Item 1',
  'Item 2',
  'Item 3',
  'Item 4',
])

const submit = handleSubmit(values => {
  alert(JSON.stringify(values, null, 2))
})
</script>