<template>
  <div>
    <div v-if="!token">
      <h3>Kirish</h3>
      <input v-model="username" placeholder="Foydalanuvchi nomi">
      <input v-model="password" type="password" placeholder="Parol">
      <button @click="login">Kirish</button>
    </div>

    <div v-else>
      <h3>✅ Xush kelibsiz, {{ username }}!</h3>
      <button @click="logout">Chiqish</button>
    </div>
  </div>


</template>
<script>
export default {
  data() {
    return {
      username: "",
      password: "",
      token: localStorage.getItem("token") || null
    }
  },
  methods: {
    login() {
      if (this.username == "admin" && this.password == "1234") {
        this.token = "fake-jwt-token-123456"
        localStorage.setItem("token", this.token)
        alert("Siz bilmasdan kirdingiz")
      } else {
        alert("Xato foydalanuvchi parol xato!")
      }
      setTimeout(() => {
        this.password = ""
        this.username = ""
      }, 100)
    },
    logout() {
      this.token = null
      localStorage.removeItem("token")
      alert("Yo'qaling")
    }
  }
}
</script>
<style></style>