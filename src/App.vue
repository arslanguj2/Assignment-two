<template>
    <Loader v-if="isLoading" />

    <template v-else>
        <div class="container">
            <div class="row">
                <CardItem v-for="user in users" :key="user.username" :user="user" />
            </div>
        </div>
    </template>
</template>

<script>
import CardItem from "./components/CardItem.vue";
import Loader from "./components/Loader.vue";

export default {
    components: { CardItem, Loader },
    data() {
        return { users: [], isLoading: false };
    },
    mounted() {
        this.isLoading = true;
        fetch("https://jsonplaceholder.typicode.com/users")
            .then((data) => data.json())
            .then((data) => (this.users = data))
            .finally(() => (this.isLoading = false));
    },
};
</script>

<style>
@import "./assets/main.css";
</style>
