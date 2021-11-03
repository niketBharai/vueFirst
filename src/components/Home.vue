<template>
<img alt="Vue logo" v-if="show" src="../assets/logo.png" />
<img alt="React logo" v-else src="../assets/react.png" width="280" />
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
<ul>
    <li v-for="item in frameworks" :key="item">
        {{item}}
    </li>
</ul>

<ul>
    <li v-for="item in users" :key="item">
        <Users :data="item" :getUser="getUserInfo"/>
    </li>
</ul>
</template>

<script>
import Users from './User.vue';

export default {
    name: "Home",
    components: {
        Users
    },
    data() {
        return {
            username: "Niket Bharai",
            email: null,
            mobile: null,
            show: true,
            frameworks: ["Vue", "React", "Angular"],
            users: [{
                    name: "Darlene",
                    email: "darlenealderson@kmail.com"
                },
                {
                    name: "Elliot",
                    email: "elliotalderson@kmail.com"
                },
                {
                    name: "Walter",
                    email: "walter@kmail.com"
                },
                {
                    name: "Edo",
                    email: "edovoss@dmail.com"
                }
            ]
        };
    },
    methods: {
        handleClick() {
            console.log("Values :", this.email, this.mobile)
        },
        getUserInfo(info) {
            alert(info)
        }
    },
};
</script>
