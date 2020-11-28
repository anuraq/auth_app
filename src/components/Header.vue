<template>
    <header class="header">
        <span>
            <h1>Auth App</h1>
        </span>
    </header>
</template>

<script>
export default {
    name: "Header"
}
</script>

<style scoped>
    .header {
        background-color:  #6e4a90;
        color: #fff;
        text-align: center;
        padding: 10px;
        }
    h1 {
        font-size: 3rem;
    }
    span:hover {
        color: black;
        cursor: pointer;
    }
</style>