<template>
  <main>
    <section class="container">
      <h1>Sobre</h1>
      <div class="about">
        <p>
          Bacharel em administração, com ampla experiência na área
          administrativa, o qual me identifiquei e me apaixonei pela área de
          programação, esta qual tem sido meu foco de estudo, e que venho
          atrelando a minha expertise em ADM, o que me proporcionou o privilégio
          de participar do desenvolvimento de aplicações (em Delphi) complexas
          de migrações de bancos de dados de escritórios contábeis, de mais de
          47 tipos de DBs diferentes para o FireBird.
        </p>
        <br />
        <p>
          Hoje meu foco de trabalho se divide em duas áreas, sou supervisor e
          responsável pelo treinamento de novos funcionários, e reciclagem dos
          veteranos, nos conceitos básicos de programação em Delphi; manipulação
          de bancos SQL (criação de banco, inserção de dados, alteração de dados
          e remoção de informações); e programão através do paradigma POO
          (Programação Orientada a Objeto), princípios do S.O.L.I.D (Single
          Responsibility Principle (Princípio da responsabilidade única),
          Open-Closed Principle (Princípio Aberto-Fechado), Liskov Substitution
          Principle (Princípio da substituição de Liskov), Interface Segregation
          Principle (Princípio da Segregação da Interface) e Dependency
          Inversion Principle (Princípio da inversão da dependência) ) e sobre o
          padrão de projetos MVC (Model (modelo), View (visão) e Controller
          (Controle)).
        </p>
        <br />
        <p>
          E também estou trabalhando na área de desenvolvimento Web full stack,
          em especial no aperfeiçoamento e manutenção de uma ferramenta de
          auxílio e integração das áreas internas de vendas, migração e suporte
          técnico da Tron.
        </p>
      </div>
    </section>
  </main>
</template>

<script>
import api from "@/services/api.js";

export default {
  name: "Sobre",
  data() {
    return {
      about: "",
    };
  },
  mounted() {
    api.get("/about.json").then((response) => {
      this.about = response.data.about;
    });
  },
};
</script>

<style scoped>
main {
  align-items: center;
}

.about {
  margin-bottom: 40px;
  color: var(--color-text-dark);
}
</style>