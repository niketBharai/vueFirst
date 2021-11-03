<template>
<h3>{{data.name}}</h3>
<h4>{{data.email}}</h4>
<button v-on:click="getUser(info)">Send Info</button>
</template>

<script>
export default {
    name: "Users",
    props: {
        data: Object,
        getUser: Function,
    },
    data() {
        return {
            info: "the info of " + this.data.name
        }
    }
}
</script>
