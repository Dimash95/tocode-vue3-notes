<template>
  <div class="note-form__wrapper">
    <form class="note-form" @submit.prevent="onSubmit">
      <textarea required v-model="value" placeholder="Type your note" />
      <button class="btn btnPrimary" type="submit">Add new note</button>
      <!-- <br />
    <div>
      <p v-for="(note, index) in notes" :key="index">
        {{ index + 1 }}. {{ note }}
        <span @click="remove(index)">✕</span>
      </p>
    </div> -->
    </form>
  </div>
</template>

<script>
export default {
  data() {
    return {
      value: ''
    }
  },
  methods: {
    onSubmit() {
      this.$emit('onSubmit', this.value)
      this.value = ''
    }
  }
}
</script>

<style lang="scss">
.note-form__wrapper {
  .note-form {
    max-width: 600px;
    display: flex;
    flex-direction: column;
    margin: 0 auto;
  }
}
</style>
