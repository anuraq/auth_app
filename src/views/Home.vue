<template>
    <div class="container">
        <div class="card-con">
            Already a User
            <router-link to="login">
                <div class="btn-con">LOGIN</div>
            </router-link>
        </div>
        <div class="card-con">
            New User
            <router-link to="signup">
                <div class="btn-con">SIGNUP</div>
            </router-link>
        </div>
    </div>
</template>

<script>
    export default {
        
    }
</script>

<style scoped>
.container {
    position: relative;
    display: flex;
    flex-direction: column;
    width: fit-content;
    height: fit-content;
    top: -10%;
}
.card-con {
    margin-top: 40px;
    font-size: 2rem;
}
.btn-con {
    margin-top: 20px;
    border-radius: 10px;
    box-sizing: content-box;
    padding: 10px;
    background-color: white;
    border: 3px solid black;
}
.btn-con:hover {
    background-color: black;
    color: whitesmoke;
    cursor: pointer;
}
a {
    color:#6E4A90;
    text-decoration: none;
}
</style>