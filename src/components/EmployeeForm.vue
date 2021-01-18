<template>
  <div id="employee-form">
    <form @submit.prevent="handleSubmit">
      <label>Employee Name</label>
      <input v-model="employee.name" type="text" name="" id="">
      <label>Employee Email</label>
      <input v-model="employee.email" type="email" name="" id="">
      <button>Add Employee</button>
    </form>
  </div>
</template>

<script>
export default {
  name: 'employee-form',
  data() {
    return {
      employee: {
        name: '',
        email: '',
      },
    }
  },
  methods: {
    handleSubmit() {
      console.log('Testing handleSubmit')
      this.$emit('add:employee', this.employee)
    }
  }
}
</script>

<style scoped>
  form {
    margin-bottom: 2rem;
  }
</style>