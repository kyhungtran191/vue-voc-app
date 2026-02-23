<template>
    <h2>My Friends</h2>
    <ul>
        <!-- <li v-for="friend in friends" :key="friend.id">{{ friend.name }}</li> -->
        <friend-contact
            v-for="friend in friends"
            :key="friend.id"
            v-bind="friend"
        ></friend-contact>
    </ul>
</template>
<script>
const app = {
    data() {
        return {
            friends: [
                {
                    id: 'manuel',
                    name: 'Manuel',
                    phone: '1231231',
                    email: 'manuel@example.com',
                },
                {
                    id: 'justin',
                    name: 'Justin',
                    phone: '1231231',
                    email: 'justin@example.com',
                },
            ],
        }
    },
}
export default app
</script>
