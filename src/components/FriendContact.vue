<template>
    <li>
        <h2>{{ name }}</h2>
        <button @click="toggleDetail">Show Detail</button>
        <ul v-if="isVisible">
            <li><strong>Phone:</strong>{{ phone }}</li>
            <li><strong>Email:</strong>{{ email }}</li>
        </ul>
    </li>
</template>

<script>
export default {
    props: ['name', 'phone', 'email'],
    emits: {
        'toggle-events': function (id) {
            return id || false
        },
    },
    // emits: [],
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
            // this.$emit('toggle-events', this.isVisible)
        },
    },
}
</script>
