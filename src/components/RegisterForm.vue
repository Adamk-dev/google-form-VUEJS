<template>
  <div>
    <b-row>
      <b-col>
        <h2>Reigister here</h2>
      </b-col>
    </b-row>
    <b-form>
      <b-form-input
        id="name"
        v-model="formData.name"
        type="text"
        placeholder="Full name"
        required
      ></b-form-input>

      <b-form-input
        id="email"
        v-model="formData.email"
        type="email"
        placeholder="Email"
        required
      ></b-form-input>

      <b-form-input
        id="password"
        v-model="formData.password"
        type="password"
        placeholder="Password"
        required
      ></b-form-input>

      <b-form-input
        id="confirmPassword"
        v-model="formData.confirmPassword"
        type="password"
        placeholder="Confirm Password"
        required
      ></b-form-input>

      <b-button type="submit" variant="primary" @click="onSubmit"
        >Register</b-button
      >
    </b-form>
  </div>
</template>

<script>
export default {
  name: 'RegisterForm',
  data: () => ({
    formData: {
      name: '',
      email: '',
      password: '',
      confirmPassword: '',
    },
  }),
  methods: {
    onSubmit() {
      console.log(this.formData);
    },
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped></style>
