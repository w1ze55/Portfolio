<script lang="ts">
export default {
    name: 'InfoSM',
    data() {
        return {
            name: 'Caue Peres',
            description: 'Welcome to my portfolio!',
            title: 'Developer FullStack Jr',
            aboutMe: 'Olá! 👋 Sou um desenvolvedor apaixonado por tecnologia e sempre em busca de novos desafios. Trabalho duro para criar soluções inovadoras e estou constantemente aprendendo e me aperfeiçoando em novas tecnologias. Este portfólio está em desenvolvimento e em breve você poderá conhecer mais sobre meus projetos e habilidades. Obrigado pela paciência! 🙌'
        }
    } 
}
</script>

<template>
    <div class="app">
        <div class="hero-container">
            <div class="img-section">
                <div class="img-logo">
                    <img src="../assets/foto eu.jpg" alt="Foto de perfil">
                </div>
            </div>
            
            <div class="content-section">
                <header class="hero">
                    <h1>{{ name }}</h1>
                    <h2>{{ title }}</h2>
                    <p class="description">{{ description }}</p>
                </header>
                
                <section class="about-section">
                    <h3>Sobre mim</h3>
                    <p class="about-text">{{ aboutMe }}</p>
                </section>
            </div>
        </div>
    </div>
</template>

<style scoped>
.app {
    max-width: 1200px;
    margin: 0 auto;
    padding: 2rem;
}

.hero-container {
    display: flex;
    align-items: flex-start;
    justify-content: space-between;
    gap: 10rem;
    margin-bottom: 4rem;
}

.img-section {
    flex: 0 0 auto;
    display: flex;
    justify-content: center;
}

.img-logo {
    position: relative;
}

.img-logo img {
    width: 250px;
    height: 250px;
    border-radius: 50%;
    object-fit: cover;
    border: 4px solid #007bff;
    box-shadow: 0 8px 32px rgba(0, 123, 255, 0.3);
    transition: transform 0.3s ease, box-shadow 0.3s ease;
}

.img-logo img:hover {
    transform: scale(1.05);
    box-shadow: 0 12px 40px rgba(0, 123, 255, 0.4);
}

.content-section {
    flex: 1;
    display: flex;
    flex-direction: column;
    justify-content: center;
}

.hero {
    margin-bottom: 2rem;
}

.hero h1 {
    font-size: 3rem;
    margin-bottom: 0.5rem;
    background: linear-gradient(135deg, #007bff, #00d4ff);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
}

.hero h2 {
    font-size: 1.5rem;
    color: #007bff;
    margin-bottom: 1rem;
    font-weight: 400;
}

.description {
    font-size: 1.1rem;
    line-height: 1.6;
    opacity: 0.9;
}

.about-section {
    margin-top: 1rem;
}

.about-section h3 {
    font-size: 2rem;
    border-bottom: 2px solid #007bff;
    padding-bottom: 0.5rem;
    margin-bottom: 1rem;
    color: #007bff;
}

.about-text {
    font-size: 1rem;
    line-height: 1.7;
    text-align: justify;
    opacity: 0.9;
}

/* Responsividade */
@media (max-width: 768px) {
    .hero-container {
        flex-direction: column;
        align-items: center;
        text-align: center;
        gap: 2rem;
    }
    
    .img-logo img {
        width: 200px;
        height: 200px;
    }
    
    .hero h1 {
        font-size: 2.5rem;
    }
    
    .hero h2 {
        font-size: 1.3rem;
    }
    
    .about-text {
        text-align: left;
    }
}

@media (max-width: 480px) {
    .app {
        padding: 1rem;
    }
    
    .img-logo img {
        width: 180px;
        height: 180px;
    }
    
    .hero h1 {
        font-size: 2rem;
    }
    
    .hero h2 {
        font-size: 1.2rem;
    }
}
</style>