<template lang="">
    <div class="my-profile-card">

      
        <p v-if="name">My name is : Sopat Phanthusuwan</p>
        <p v-else>My name is : โสพัส พันธุสุวรรณ</p>
        <p>My Nickname : {{ nickname }}</p>
        <p>I'm : {{ age }} year old.</p>
        <p>My Position : {{ position }}</p>
        <p>My favourite movies is :</p>
        <li v-for="myFavMovies in myFavMovies">{{ myFavMovies }}</li>
        <button class="btn" @click="count++">Click Me {{ count }}</button>

        <button class="btn" @click="name = !name">Change my name</button>
        <button class="btn" @click="awesome = !awesome">Toggle</button>
        <p v-if="awesome">Hello World !!</p>
        <p v-else>Hello Human !!</p>

    </div>
</template>

<script>
export default {
    data() {
        return {
            name: true,
            nickname: "Fair",
            age: "2x",
            position: "FontEnd Developer",
            myFavMovies: ["Fast and Furious", "Spider Man", "Doctor Strange "],
            count: 0,
            awesome: true
        }
    }
}
</script>

<style scoped>
.my-profile-card {
    color: black;
    background: pink;
    border-radius: 5px;
    box-shadow: 3px 3px 10px rgb(0, 0, 0, 0.3);
    padding: 1rem;
}

.btn {
    margin: 1rem;
}
</style>