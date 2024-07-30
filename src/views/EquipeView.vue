<script>
export default {
  name: 'EquipeView',
  data() {
    return {
      equipe: [
        {
          nome: 'Nicole Brand',
          turma: '2INFO2'
        },
        {
          nome: 'Eduarda Heidemann',
          turma: '2INFO2'
        },
        {
          nome: 'Nathaly Adão',
          turma: '2INFO2'
        },
        {
          nome: 'Manuela Hostin',
          turma: '2INFO3'
        },
        {
          nome: 'Gabriel Vinícius',
          turma: '2INFO2'
        },
        {
          nome: 'Yasmin Mello',
          turma: '2INFO2'
        }
      ]
    }
  }
}
</script>

<template>
  <div class="team">
    <h1>Equipe</h1>
    <ul>
      <li v-for="membro in equipe" :key="membro.nome">
        <RouterLink :to="{ name: 'membro', params: { nome: membro.nome } }">
          <h2>{{ membro.nome }}</h2>
        </RouterLink>
        <p>{{ membro.turma }}</p>
      </li>
    </ul>
  </div>
</template>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Poppins:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&display=swap');
.team {
  padding-top: 4%;
  padding-left: 4%;
}
h1 {
  font-family: "Poppins", sans-serif;
  font-size: 280%;
  color: rgb(0, 0, 0);
}

a {
  font-family: Arial, Helvetica, sans-serif;
  color: rgb(53, 53, 53);
}


</style>
