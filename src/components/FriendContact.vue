<template>
    <li>
        <h2>{{ friend.name }}</h2>
        <button @click="toggleDetail">Show Detail</button>
        <ul v-if="isVisible">
            <li><strong>Phone:</strong>{{ friend.phone }}</li>
            <li><strong>Email:</strong>{{ friend.email }}</li>
        </ul>
    </li>
</template>

<script>
export default {
    props: ['name','phoneNumber', 'emailAddress'],
    data() {
        return {
            isVisible: false,
            friend: {
                id: 'manuel',
                name: 'Manuel',
                phone: '1231231',
                email: 'manuel@example.com',
            },
        }
    },
    methods: {
        toggleDetail() {
            this.isVisible = !this.isVisible
        },
    },
}
</script>
