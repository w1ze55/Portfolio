<script lang="ts">
export default {

}
</script>

<template>
    <nav>
        <ul>
            <li><a href="#">Home</a></li>
            <li><a href="#">About</a></li>
            <li><a href="#">Projects</a></li>
            <li><a href="#">Contact</a></li>
        </ul>
    </nav>
</template>

<style scoped>
ul li {
    display: inline-block;
    margin-right: 10px;
}

ul li a {
    text-decoration: none;
    transition: color 0.3s ease;
}

ul li a:hover {
    color: #777;
    transition: color 0.3s ease;
}


</style>