<template>
  <q-page class="container">
    <div id="info">
      <div class="row justify-center q-pa-lg">
      <div class="col-xs-12 col-sm-12 col-md-7 col-lg-3">
          <header><h2>Cursos de Tecnologia e Negócios Digitais</h2></header>
          <p>Você vai estudar e aprender em uma comunidade de inquietos e inovadores.</p>
        </div>
        <div class="col col-xs-12 col-sm-12 col-md-5 col-lg-3">
          <img src="../assets/estudante.svg" alt="estudante com seus livros">
        </div>
      </div>
    </div>
    <section id="descCursos" class="q-pb-xl">
      <div class="row justify-center q-pa-lg items-start q-gutter-md">
        <header><h3 class="text-cyan-10">FORMAÇÕES</h3></header>
      </div>
       
      <div class="q-pa-md row justify-start wrap q-gutter-md">
        <q-card class="my-card" v-for="curso in cursos" :key="curso.id">
          <q-card-section>
               <q-img class="curso-img-svg" :src="curso.imagem" spinner-color="white" />
            <div class="text-h5 text-indigo-9">{{curso.titulo}}</div>
          </q-card-section>
          <q-card-section class="q-pt-none">
           <p> {{ curso.descricao }}</p>
           <q-btn color="primary" label="Começar"/>
          </q-card-section>
        </q-card>
      </div>
    </section> <!--#descursos-->
      <section id="depoimentos" class="bg-indigo-1 q-pb-xl">
   <div class="row q-pa-md q-gutter-md">
    <div class="col col-lg-4 offset-lg-2">
      <header><h4 class="text-blue-9 q-mt-xs">A maior plataforma brasileira de cursos de tecnologia.</h4>
      </header>
      <p class="text bady1">São 1272 cursos, 100% em português. E novos lançamentos todas as semanas.</p>
  </div> <!-- /.col -->
   <div class="col col-lg-2">
  <q-card class="p-pa-md">
     <q-card-section>
       <div class="text-h5 text-indigo-9">José Pedro</div>
      </q-card-section>
     
     <q-card-section class="q-pt-nome">
       <p>Se você não sabe a ordem do que deve aprender e praticar para dominar uma tecnologia, a forma como os cursos estão organizados e estruyurados nos ajuda muito.</p>
     </q-card-section>
    </q-card>
   </div> <!-- /.col -->
   <div class="col col-lg-2">
  <q-card class="p-pa-md">
     <q-card-section>
       <div class="text-h5 text-indigo-9">Mariana Souza</div>
      </q-card-section>
     
     <q-card-section class="q-pt-nome">
       <p>Consegui fazer uma mundça de carreira em uma área muito disputada e estou muito feliz:</p>
     </q-card-section>
    </q-card>
   </div> <!-- /.col -->
  </div> <!-- /.row -->
</section> <!-- /#depoimentos -->
  </q-page>
</template>

<script>
export default {
  name: 'PageIndex',
  data (){
   return {
  		cursos:[{
  			id:1,
  			titulo: "Curso HTML5 e CSS3",
  			descricao: "O Curso de HTML5 e CSS3 vai ensinar a criar sites usando a linguagem de marcação hipertexto (HTML) e folhas de estilo em cascata (CSS).",
        imagem:"../../svg/css-file.svg"
  		},
      {
        id:2,
        titulo: "GITHUB",
        descricao: "Curso de Git e Github grátis prático e sem usar comando no terminal.",
        imagem:"../../svg/git.svg"
      },
      {
        id:3,
        titulo: "Javascript",
        descricao: "O curso de html5 e css3 vai ensinar a criar site usando a linguagem de marcação hipertexto (html) e folhas de estilo em cascata.",
        imagem:"../../svg/coding.svg"
      },
      {
        id:4,
        titulo: "Vue.js",
        descricao: "Construa do zero uma SPA e crie seus próprios componentes.",
        imagem:"../../svg/device.svg"
      }]
    }
  }
}
</script>

<style scoped>

div#info{
  background-color: #2a7ae4;
  color: #fff;
}

div#info h2{
  font-weight: 800;
}

section#descCursos h3 {
	margin-bottom: 0.2em;
   font-weight: 300;
   }

div#info p {
  font-size: 23px;
}

.my-card {
  width: 100%;
  max-width: 250px;
}

.curso-img-svg {
  width: 80px;
}
</style>
