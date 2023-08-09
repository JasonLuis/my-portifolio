<template>
  <div class="container">
    <div class="perfil">
      <div class="my-card q-pa-xl">
        <h1 class="title">
          Bem-vindo ao meu portfolio pessoal
        </h1>
        <p>
          Meu nome é Djeison Luis, sou um Desenvolvedor Fullstack, com
          experiência de dois anos em desenvolvimento web. Proficiente em uma
          variedade de tecnologias de front-end e back-end, incluindo HTML/CSS,
          JavaScript, TypeScript, Vue, NodeJS, Java, PHP, SQL, entre outros.
          Sempre buscando por desafios para aplicar minhas habilidades e
          progredir em minha carreira como Programador.
        </p>
      </div>
    </div>
    <div class="skills row justify-center">
      <div class="my-card q-pa-xl col-12 q-mt-md">
        <h1 class="skill-title">
          Habilidades Técnicas
        </h1>
        <div class="skill-card row justify-between">
          <div class="skill-list">
            <span class="sub-title q-mt-none"> Tecnologias Backend </span>
            <ul class="q-pa-none">
              <li class="q-ml-lg">
                PHP
              </li>
              <li class="q-ml-lg">
                Java
              </li>
              <li class="q-ml-lg">
                Spring Framework
              </li>
              <li class="q-ml-lg">
                Hibernate
              </li>
              <li class="q-ml-lg">
                Kotlin
              </li>
              <li class="q-ml-lg">
                Javascript/TypeScript
              </li>
              <li class="q-ml-lg">
                NodeJS
              </li>
            </ul>
          </div>
          <div class="skill-list">
            <span class="sub-title"> Tecnologias Frontend </span>
            <ul class="q-pa-none">
              <li class="q-ml-lg">
                HTML/CSS
              </li>
              <li class="q-ml-lg">
                SASS
              </li>
              <li class="q-ml-lg">
                Bootstrap
              </li>
              <li class="q-ml-lg">
                Quasar
              </li>
              <li class="q-ml-lg">
                Vuetify
              </li>
              <li class="q-ml-lg">
                VueJS
              </li>
            </ul>
          </div>
          <div class="skill-list">
            <span class="sub-title"> Bancos de Dados </span>
            <ul class="q-pa-none">
              <li class="q-ml-lg">
                MySQL
              </li>
              <li class="q-ml-lg">
                PostgreSQL
              </li>
              <li class="q-ml-lg">
                SQLite
              </li>
              <li class="q-ml-lg">
                Oracle
              </li>
            </ul>
          </div>
        </div>
      </div>
      <div class="my-card q-pa-xl col-12">
        <h1 class="project-title">
          Projetos Pessoais
        </h1>
        <div class="pesonal-projects">
          <div v-for="(project, index) in projects" :key="index">
            <UiPersonalProject
              :name="project.name"
              :description="project.description"
              :image="project.image"
            />
          </div>
        </div>
      </div>
      <div class="my-card q-pa-xl col-12 q-mb-xl">
        <h1 class="experience-title">
          Experiência Profissional
        </h1>
        <div class="pesonal-projects">
          <div
            v-for="(professionalExperience, index) in professionalExperiences"
            :key="index"
          >
            <UiProfessionalExperience
              :name="professionalExperience.name"
              :description="professionalExperience.description"
            />
          </div>
        </div>
      </div>
      <div class="my-card q-pa-xl col-12 q-mb-xl">
        <h1 class="academic-title">
          Formação Academica
        </h1>
        <div class="pesonal-projects">
          <div
            v-for="(academicEducation, index) in academicsEducations"
            :key="index"
          >
            <UiAcademicEducation
              :name="academicEducation.name"
              :description="academicEducation.description"
            />
          </div>
        </div>
      </div>
    </div>
    <div class="footer row justify-center">
      <div class="my-card q-pa-xl col-12">
        <h1 class="q-mb-none">
          Contato
        </h1>
        <p>Vamos conversar? Estou pronto para explorar novas oportunidades!</p>
        <ul class="contact">
          <li>
            <q-img :src="whatsappLogo" />
            (11) 96232-7519
          </li>
          <li>
            <q-img :src="github" />
            https://github.com/JasonLuis
          </li>
          <li>
            <q-img :src="gmailLogo" />
            jason20luis@gmail.com
          </li>
          <li>
            <q-img :src="linkedinLogo" />
            https://www.linkedin.com/in/djeison-l-185703122/
          </li>
        </ul>
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
import UiPersonalProject from '../core/components/PesonalProject/PersonalProject.vue'
import UiProfessionalExperience from '../core/components/ProfessionalExperience/ProfessionalExperience.vue'
import UiAcademicEducation from '../core/components/AcademicEducation/AcademicEducation.vue'

const whatsappLogo = new URL(
  '../core/assets/images/icons/whatsapp.png',
  import.meta.url
).href
const gmailLogo = new URL(
  '../core/assets/images/icons/gmail.png',
  import.meta.url
).href
const linkedinLogo = new URL(
  '../core/assets/images/icons/linkedin.png',
  import.meta.url
).href
const github = new URL(
  '../core/assets/images/icons/github.png',
  import.meta.url
).href
const projects = [
  {
    name: 'LinkNLearn',
    image: 'linknlearn.jpg',
    description:
      'O projeto LinkNLearn é uma plataforma inovadora de educação online que permite a interação perfeita entre alunos e professores, facilitando a venda e compra de cursos. Com uma base sólida em tecnologias modernas, o backend foi construído com NodeJS e TypeScript, enquanto o frontend foi desenvolvido em ReactJS.'
  },

  {
    name: 'Hero Hairdresses',
    image: 'hero-hairdresses.png',
    description:
      'O projeto Hero Hairdresses é uma plataforma web inovadora desenvolvida com tecnologias de ponta, incluindo ReactJS para o frontend e NodeJS para o backend. Com o objetivo de revolucionar a experiência de agendamento em salões de beleza, o projeto também incorpora recursos avançados, como o uso do serviço de armazenamento S3 da Amazon para gerenciar imagens.'
  },
  {
    name: 'News Home Page',
    image: 'news-home-page.png',
    description:
      'O projeto News Homepage é uma página de destino elegante e responsiva, criada para proporcionar uma experiência envolvente aos visitantes interessados em notícias e informações relevantes. Desenvolvida utilizando a tecnologia VueJS, essa página oferece um design atraente e moderno, adaptando-se perfeitamente a diferentes dispositivos.'
  }
]

const professionalExperiences = [
  {
    name: 'Desenvolvedor Júnior | Globalweb Corp',
    description:
      'Como Desenvolvedor Júnior na Globalweb, fui responsável por criar componentes dinâmicos utilizando as versões Vue 2 e Vue 3, combinando-as com TypeScript para garantir um código robusto e eficiente. Minha contribuição incluiu a documentação detalhada dos componentes por meio do Storybook, facilitando a compreensão e colaboração da equipe.'
  },
  {
    name: 'Estagiário | Globalweb Corp',
    description:
      'Durante minha etapa como estagiário na Globalweb Corp, concentrei-me na aprendizagem contínua de Vue.js, TypeScript e JavaScript. Contribuí para a equipe por meio da criação ocasional e documentação de componentes.'
  },
  {
    name: 'Analista de Suporte Jr | CDF - Central de Funcionamento',
    description:
      'Na função de Analista de Suporte Jr na CDF, forneci assistência por telefone a clientes, auxiliando-os na configuração de dispositivos como computadores, Smart TVs e equipamentos de linha branca.'
  }
]

const academicsEducations = [
  {
    name: 'Sistemas de Informação | FIAP',
    description:
      'Formado em Sistemas de Informação pela FIAP em dezembro de 2021, minha jornada acadêmica se estendeu de fevereiro de 2018 a dezembro de 2021. Durante esse período, adquiri um sólido entendimento em sistemas, desenvolvimento de software e análise de dados, preparando-me para uma carreira dinâmica na área de tecnologia.'
  },
  {
    name: 'Técnico em Informática | SENAI',
    description:
      'Graduado como Técnico em Informática pela escola SENAI Professor Vicente Amato, adquiri sólidos conhecimentos em programação Java e desenvolvimento web com HTML, CSS e PHP. Minha formação técnica me proporcionou uma base sólida para compreender as complexidades da tecnologia e sua aplicação prática.'
  }
]
</script>
<style scoped lang="scss">
%inconsolata {
  font-family: 'Inconsolata';
}

%fira-sans {
  font-family: 'Fira Sans';
}

%text-gradient {
  background: linear-gradient(
    320deg,
    #0087ff 0,
    #5080ff 6.25%,
    #7c78ff 12.5%,
    #9b6ffd 18.75%,
    #b465f1 25%,
    #c85be4 31.25%,
    #d951d5 37.5%,
    #e746c6 43.75%,
    #f23cb5 50%,
    #fa33a4 56.25%,
    #ff2d93 62.5%,
    #ff2c81 68.75%,
    #ff2e70 75%,
    #ff355f 81.25%,
    #ff3e4f 87.5%,
    #fb483e 93.75%,
    #f4522e 100%
  );
  -webkit-background-clip: text; /* Para navegadores baseados em WebKit (Chrome, Safari) */
  -moz-background-clip: text; /* Para navegadores baseados em Gecko (Firefox) */
  background-clip: text;
  color: transparent;
}

%background-page {
  width: 100%;
  min-height: 100vh;
  height: 100%;
  background-color: #241631;
}

.container {
  display: block;
}

.perfil {
  background-image: linear-gradient(rgba(0, 0, 0, 0.8), rgba(0, 0, 0, 0.7)),
    url('../core/assets/images/9QTpESGBXa32D29J77VR3d-970-80.jpg.webp');
  min-height: 50vh;
  background-position: right center;
  background-repeat: no-repeat;
  background-size: cover;
  display: flex;
  align-items: center;
  justify-content: center;
  // height: 100vh;
}

.my-card {
  max-width: 990px;
}

.my-card h1 {
  @extend %inconsolata;
  @extend %text-gradient;
  font-weight: 700;
  font-size: 45px;
  filter: brightness(150%);
}

.my-card .title {
  font-size: 54px;
  max-width: 855px;
  line-height: 54px;
}

.my-card p {
  @extend %fira-sans;
  color: #dad1e6;
  filter: contrast(14.24);
  font-size: 18px;
  line-height: 30px;
  filter: brightness(200%);
}

.skills {
  @extend %background-page;
  /* display: flex;
    justify-content: center; */
}

.skills .my-card > h1,
.projects .my-card > h1 {
  margin-top: 0px;
  padding: 0px;
}

.skill-list {
  max-width: 897px;
}

.skill-list ul li {
  @extend %fira-sans;
  width: 270px;
  color: #dad1e6;
  font-size: 18px;
  margin-top: 0.5em;
}

.pesonal-projects {
  display: flex;
  justify-content: center;
  flex-wrap: wrap;
  gap: 35px;
}

.sub-title {
  @extend %inconsolata;
  @extend %text-gradient;
  font-size: 27px;
  font-weight: 700;
  max-width: 290px;
}

.footer {
  background-image: linear-gradient(
      rgba(36, 22, 49, 0.7),
      rgba(36, 22, 49, 0.7)
    ),
    url('../core/assets/images/footer4.jpg');
  background-position: right center;
  /* height: 400px; */
  background-repeat: no-repeat;
  background-size: cover;
}

.contact {
  list-style-type: none;
  padding-left: 2px;
}

.contact li {
  @extend %fira-sans;
  color: #dad1e6;
  font-size: 18px;
  font-weight: 500;
  margin-bottom: 15px;
}

.contact li .q-img {
  width: 24px;
  height: 24px;
  margin-right: 10px;
}

@media (max-width: $breakpoint-xs) {
  .skill-card {
    display: flex;
    justify-content: center;
    flex-wrap: wrap;
    gap: 40px;
    padding-left: 40px;
  }

  .skill-title,
  .project-title,
  .experience-title,
  .academic-title {
    text-align: center;
    line-height: 25px;
    font-size: 25px;
    margin-top: 50px;
    margin-bottom: 40px;
  }

  .my-card {
    width: 320px;
    padding: 0px;
  }

  .my-card .title {
    font-size: 23px;
    line-height: 25px;
  }

  .my-card h1 {
    @extend %inconsolata;
    @extend %text-gradient;
    font-weight: 700;
    font-size: 23px;
    filter: brightness(150%);
  }

  .my-card p {
    @extend %fira-sans;
    color: #DAD1E6;
    filter: contrast(14.24);
    font-size: 12px;
    line-height: 14px;
    filter: brightness(200%);
  }

  .skills .my-card > h1,
  .projects .my-card > h1 {
    margin-top: 50px;
  }

  .sub-title {
    font-size: 18px;
  }

  .skill-list ul li {
    font-size: 12px;
  }

  .footer .my-card h1 {
    line-height: 50px;
  }
  .contact li {
    font-size: 12px;
  }
}
</style>
