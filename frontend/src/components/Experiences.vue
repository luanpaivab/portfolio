<template>
  <div class="experiences">
    <span>Experiências</span>
    <div class="flex-container py-5 px-3 my-4" v-b-toggle.collapse-2>
      <span class="pl-3">Desenvolvedor Front-End</span>
      <div class="info-experience py-3">
        <img
          class="mr-3"
          src="https://image.flaticon.com/icons/png/128/4252/4252360.png"
          alt=""
          height="60"
          width="60"
        />
        <div class="details-experience">
          <span>Advocacia Geral da União - AGU</span>
          <span style="color: rgb(159, 159, 159)"
            >Julho de 2021 - Até Hoje</span
          >
          <span>Estágio</span>
        </div>
      </div>
      <b-collapse id="collapse-2" class="mt-2">
        <span>Tecnologias Utilizadas:</span>
        <p style="font-size: 0.8rem; font-weight: 450">
          - IDE: Visual Studio Code<br /> - Linguagem: JavaScript<br />
          - SGBD: MySQL<br />
          - Arquitetura: REST <br />- API Client: Insomnia<br />
          - Versionamento: GitLab <br />- Front-end: Vue.Js | Vuex <br />
          - Hospedagem: Heroku.
        </p>
      </b-collapse>
    </div>

    <div class="flex-container py-5 px-3 my-3" v-b-toggle.collapse-1>
      <span class="pl-3">Desenvolvedor Full Stack</span>
      <div class="info-experience py-3">
        <img
          class="mr-3"
          src="https://image.flaticon.com/icons/png/128/1268/1268455.png"
          alt=""
          height="60"
          width="60"
        />
        <div class="details-experience">
          <span>Guarda Municipal de Belém</span>
          <span style="color: rgb(159, 159, 159)"
            >Outubro de 2020 - Abril de 2020</span
          >
          <span>Estágio</span>
        </div>
      </div>
      <b-collapse id="collapse-1" class="mt-2">
        <span>Tecnologias Utilizadas:</span>
        <p style="font-size: 0.8rem; font-weight: 450">
          - IDE: Visual Studio Code <br />- Linguagem: JavaScript<br />
          - SGBD: MySQL<br />
          - Arquitetura: REST <br />- API Client: Insomnia<br />
          - Versionamento: GitLab <br />- Front-end: Vue.Js | Vuex <br />-
          Back-end - Node.js<br />
          - Hospedagem: Surge.
        </p>
        <p style="font-size: 0.9rem">
          Programador Full Stack no Desenvolvimento de uma plataforma web de
          gestão, destinada ao setor administrativo da Guarda Municipal de
          Belém.
        </p>
        <p style="font-size: 0.9rem">
          Resumo - Regras de Negócio: O sistema foi arquitetado visando
          organizar os diversos setores da guarda municipal, de forma que permite
          ao usuário visualizar documentos enviados, dar baixa em documentos,
          cadastrar ocorrências, cadastrar funcionários, verificar quantidade de
          ocorrências semanais, mensais ou anuais na forma de gráfico. Cada
          setor tem seu painel e cada funcionário é cadastrado no seu devido
          setor, então, só poderá ter acesso a determinado setor o usuário que
          estiver cadastrado no mesmo.
        </p>
      </b-collapse>
    </div>
  </div>
</template>

<script>
export default {
  name: "Experiences",
};
</script>

<style>
.info-experience {
  display: flex;
  flex-direction: row;
  align-items: center;
  /* font-weight: 400; */
}

.details-experience {
  display: flex;
  flex-direction: column;
  margin: 0;
  border-left: solid 1px rgb(179, 179, 179);
  padding-left: 20px;
}
/* .details-experience h1{
  font-size: 1.3rem;
} */
</style>