<template>
  <q-page padding>
    <div class="flex flex-center">
      <img alt="Quasar logo" src="~assets/logo.png">
    </div>

    <!-- <div class="flex flex-center">
      <h3 class="q-display-3">Escolha seu docinho</h3>
    </div> -->

    <div id="conteudo" class="row gutter-md">
      <div class="col-xs-12 col-sm-4">
        <q-card>
          <q-title>
            Usar minha localização atual
          </q-title>
          <q-separator/>
          <q-card>
            Próximo de...
          </q-card>
          <q-card-actions>
            <q-btn to="list-restaurant" color="primary" label="Ver localização"/>
          </q-card-actions>
        </q-card>
      </div>

      <div class="col-xs-12 col-sm-4">Acessar a conta</div>
      <div class="col-xs-12 col-sm-4">Listar localizações cadastradas</div>
    </div>
  </q-page>

</template>

<style>
  .q-page img{
    width: 10%;
    height: auto;
    margin-bottom: 30px;
  }

  #conteudo div {
    text-align: center;
  }

  .q-card {
    width: 50%;
    height: auto;
  }
</style>

<script>
export default {
  name: 'PageIndex',
};
</script>
