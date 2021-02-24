<template>
    <div>
        <table>
            <tr v-for="(member, index) in members" :key="index">
                <td>{{ member.first_name }}</td>
                <td>{{ member.last_name }}</td>
            </tr>
        </table>
        <button @click="getMembers">Get members</button>
    </div>
</template>

<script>
import axios from 'axios'

export default {
    name: 'Members',
    data() {
        return {
            members: []
        }
    },
    mounted() {
        this.getMembers()
    },
    methods: {
        getMembers() {
            // axios request
            axios.request({
                url: 'http://localhost:5000/members',
                method: 'get',
                params: {}
            })
            .then((response) => {
                console.log('RESPONSE', response);
                // get the response data, and assign to our data model
                this.members = response.data
            });
            
        }
    }
}
</script>

<style scoped>

</style>