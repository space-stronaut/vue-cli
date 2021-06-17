<template>
    <div>
        <h1>{{ number }}</h1>
        <button @click="increment" class="btn btn-primary">+</button>
        <button @click="decrement" class="btn btn-primary ms-3">-</button>
    </div>
</template>

<script>
    export default({
        name : "Counter",
        data() {
            return {
                number: 0
            }
        },
        methods: {
            increment() {
                this.number = this.number + 1
            },
            decrement() {
                this.number -= 1;

                if (this.number < 0) {
                    this.number = 0
                }
            }
        },
    })
</script>

<style scoped>

</style>