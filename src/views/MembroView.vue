
<template>
    <div class="card">
        
        <h1>{{ membro.nome }}</h1>
        <div v-if="membro">
         
            <p><strong>Turma:</strong> {{ membro.turma }}</p>
            <p><strong>Descrição:</strong> {{ membro.descricao }}</p>
            <p><strong>Email:</strong> {{ membro.email }}</p>
        </div>
        <div v-else>
            <p>Detalhes não encontrados.</p>
        </div>
    </div>
</template>

<script>
export default {
    name: 'MembroView',
    props: ['nome'],
    data() {
        return {
            membro: {} 
        }
    },

    created() {const equipe = [
            { nome: 'Nicole Brand', turma: '2INFO2', descricao: 'Natural de Joinville, atual estudante do IFC Araquari. Nascida em 2007, gosta de Banco de Dados e tem espírito de liderança.', email: 'nicoleabrand13@gmail.com' },
            { nome: 'Eduarda Heidemann', turma: '2INFO2', descricao: 'Mora em Joinville, tem 16 anos, estuda no IFC câmpus Araquari. Irá participar na criação do figma no projeto em grupo do Hackathon.', email: 'eduardafheidemann@gmail.com' },
            { nome: 'Nathaly Adão', turma: '2INFO2', descricao: 'Mora em Joinville, tem 16 anos, estuda no IFC câmpus Araquari. Irá participar na criação do figma no projeto em grupo do Hackathon.', email: 'nathalycarolineadaoo@gmail.com' },
            { nome: 'Manuela Hostin', turma: '2INFO3', descricao: 'Estudante da turma 2info3, gosto de programar com foco em backend e de circuitos', email: 'hostimmanu@gmail.com' },
            { nome: 'Gabriel Vinícius', turma: '2INFO2', descricao: 'Mora em Joinville, tem 17 anos e é estudante no IFC câmpus Araquari. Desenvolvedor back-end', email: 'gabrielviniciuscorrea204@gmail.com' },
            { nome: 'Yasmin Mello', turma: '2INFO2', descricao: 'Mora em Joinville, tem 17 anos, é estudante no IFC câmpus Araquari. Será a principal dev de CSS no projeto em grupo do Hackathon.', email: 'melloyasminm@gmail.com' }
        ];

        // Encontrar o membro com base no nome passado como prop
        this.membro = equipe.find(m => m.nome === this.$route.params.nome) || {};
    }
}
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Poppins:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&display=swap');
    .card{
        margin-left: 35%;
        margin-right: 35%;
        margin-top: 50px;
        padding: 5%;
        background:rgb(158, 158, 158);
        border-radius: 5px;
        color: rgb(0, 0, 0);
    }

    h1{
        font-family: "Poppins", sans-serif;
    }
</style>
