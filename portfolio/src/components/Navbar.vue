<script lang="ts">
export default {

}
</script>

<template>
    <nav class="navbar">
        <div class="nav-container">
            <ul class="nav-menu">
                <li class="nav-item"><a href="#" class="nav-link">About</a></li>
                <li class="nav-item"><a href="#" class="nav-link">Experiences</a></li>
                <li class="nav-item"><a href="#" class="nav-link">Projects</a></li>
                <li class="nav-item"><a href="#" class="nav-link">Contact</a></li>
            </ul>
        </div>
    </nav>
</template>

<style scoped>
.navbar {
    background: transparent;
    padding: 0;
    position: sticky;
    top: 0;
    z-index: 1000;
    width: 100%;
    overflow-x: hidden;
    box-sizing: border-box;
}

.nav-container {
    width: 100%;
    max-width: 100vw;
    padding: 20px;
    box-sizing: border-box;
    overflow-x: hidden;
}

.nav-menu {
    display: flex;
    align-items: center;
    justify-content: flex-end;
    list-style: none;
    margin: 0;
    padding: 0;
    height: 60px;
    flex-wrap: nowrap;
    overflow-x: auto;
    width: 100%;
    box-sizing: border-box;
}

.nav-item {
    margin-right: 32px;
}

.nav-item:last-child {
    margin-right: 0;
}

.nav-link {
    text-decoration: none;
    color: #ffffff;
    font-weight: 500;
    font-size: 16px;
    padding: 8px 12px;
    border-radius: 6px;
    transition: all 0.3s ease;
    position: relative;
}

.nav-link:hover {
    color: #007bff;
    transform: translateY(-1px);
}

.nav-link::after {
    content: '';
    position: absolute;
    width: 0;
    height: 2px;
    bottom: -2px;
    left: 50%;
    background-color: #007bff;
    transition: all 0.3s ease;
    transform: translateX(-50%);
}

.nav-link:hover::after {
    width: 100%;
}

/* Responsividade */
@media (max-width: 768px) {
    .nav-container {
        padding: 0 16px;
    }
    
    .nav-item {
        margin-right: 20px;
    }
    
    .nav-link {
        font-size: 14px;
        padding: 6px 8px;
    }
}
</style>