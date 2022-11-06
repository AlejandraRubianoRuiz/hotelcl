<template>
    <div class="container">
        <form class="form-group col-6 ">
            <input class="" type="text" placeholder="Usuario" v-model="username" />
            <input class="" type="password" placeholder="Password" v-model="password" />
            <div class="text-center">
                <p v-if="error" class="text-danger text-start ms-4 fs-5">
                    Por favor llena todos los campos
                </p>
                <button @click="login" type="submit" class="btn btn-dark mt-4">
                    Login
                </button>
            </div>
        </form>
        <br /><!-- Eliminar una vez acabe testeo -->
        <p v-for="user in users" :key="user.id">
            Su usuario es: {{ user.username }}, contraseña es: {{ user.password }}.
        </p>
    </div>
</template>

<script>
import axios from "axios";

export default {
    data() {
        return {
            username: "",
            password: "",
            error: false,
            users: [],
        };
    },
    methods: {
        login(e) {
            e.preventDefault();

            if (this.username == "" || this.password == "") {
                this.error = true;
                console.log("There's been errors");
            } else {
                this.error = false
                axios
                    .get("http://localhost:3000/users")
                    .then((res) => (this.users = res.data))
                    .catch((err) => console.log(`There was an error: ${err}`));
            }
        },
    },
};
</script>

<style>
form {
    margin: auto;
}

input {
    padding: 5px;
    width: 90%;
    margin-bottom: 25px;
    background: #f8f8f8;
    border: none;
    border-bottom: 1.5px solid #333;
}

button {
    background: #2e4372 !important;
}
</style>
