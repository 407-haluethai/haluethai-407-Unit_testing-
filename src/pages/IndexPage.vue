<template>
  <div class="htmlClass">
    <h1>{{ firstName }}</h1>
    <form>
      <input type="text" id="firstName" v-model="firstName" />
      <button @click="submitForm()" class="submitForm">Submit</button>
  </form>
    <h2>{{ secondName }}</h2>
    <form>
      <input type="text" id="secondName" v-model="secondName" />
  </form>
    <h3>{{ StudentId }}</h3>
    <form>
      <input type="text" id="StudentId" v-model="StudentId" />
  </form>
    <h4>{{ NickName }}</h4>
    <form>
      <input type="text" id="Nickname" v-model="NickName" />
  </form>
  </div>
</template>

<script>
export default {
  name: 'InputPage',
  data() {
    return {
      head: 'Vue is awesome.',
      firstName: 'หฤทัย',
      secondName: 'ยุวรัตน์',
      StudentId:'6604101407',
      NickName:'ตะวัน',
    }
  },
  methods: {
    submitForm() {
      this.$emit('submit form')
    },
  }
}
</script>

<style scoped></style>
