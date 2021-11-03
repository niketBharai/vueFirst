<template>
<img alt="Vue logo" v-if="show" src="../assets/logo.png" />
<img alt="React logo" v-else src="../assets/react.png" width="280"/>
<h1>Hello {{ username }}</h1>
<input type="text" placeholder="Enter Email" v-model="email" />
<br />
<br />
<input type="text" v-model="mobile" placeholder="Enter Mobile Number" />
<br />
<br />
<button v-on:click="handleClick()">Get Values</button>
<br />
<br />
<button v-on:click="show=!show">Change Image</button>

</template>

<script>
export default {
    name: "Home",
    data() {
        return {
            username: "Niket Bharai",
            email: null,
            mobile: null,
            show: true
        };
    },
    methods: {
        handleClick() {
            console.log("Values :", this.email, this.mobile)
        },
    },
};
</script>
