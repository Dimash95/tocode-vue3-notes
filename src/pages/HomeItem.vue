<template>
  <FormItem @onSubmit="handleSubmit" />
</template>

<script>
import FormItem from '@/components/Notes/FormItem.vue'

export default {
  components: { FormItem },
  methods: {
    handleSubmit(note) {
      console.log(note)
    }
  }
}
</script>
