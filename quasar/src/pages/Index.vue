<template>
  <q-page padding>
    <!-- <div class="flex flex-center">
      <img alt="Quasar logo" src="~assets/logo.png">
    </div> -->

    <!-- <div class="flex flex-center">
      <h3 class="q-display-3">Escolha seu docinho</h3>
    </div> -->

    <div class="row gutter-md">
      <div class="col-xs-12 col-md-4">
        <q-card class="bg-green-7 text-white">
          <q-card-title>
            <strong>minha localização atual</strong>
          </q-card-title>
          <q-separator/>
          <q-card-main>
            Próximo de...
          </q-card-main>
          <q-card-actions>
            <q-btn to="list-restaurant" color="green-6" label="Ver Restaurante"/>
          </q-card-actions>
        </q-card>
      </div>

      <div class="col-xs-12 col-sm-4">
        <q-card class="bg-orange-8 text-white">
          <q-card-title>
            <strong>Acessar Conta</strong>
          </q-card-title>
          <q-separator/>
          <q-card-main>
            Você pode acessar nosso cardápio através de uma conta.
          </q-card-main>
          <q-card-actions>
            <q-btn to="list-restaurant" color="orange-6" label="Ver Restaurante"/>
          </q-card-actions>
        </q-card>
        </div>

      <div class="col-xs-12 col-md-4">
        <q-card class="bg-primary text-white">
          <q-card-title>
            <strong>Escolher uma zona</strong>
          </q-card-title>
          <q-separator/>
          <q-card-main>
            <q-btn
              color="white"
              text-color="primary"
              size="md"
              class="q-mr-md q-mb-md"
              :label="place"
              v-for="(place,index) in places"
              :key="index"
            />
          </q-card-main>
        </q-card>
      </div>
    </div>
  </q-page>

</template>

<style>
  .q-card{
    width: 90%;
    height: auto;
    padding: 10px 10px 10px 10px;
    margin: 10px 10px 10px 10px;
  }

  .q-separator {
    margin: 10px 0px 10px 0px;
  }

  .q-card__actions {
    padding: 10px 8px 0px 0px;
    align-items: center;
  }
</style>

<script>
export default {
  name: 'PageIndex',
  data() {
    return {
      places: [
        'Centro',
        'Norte',
        'Sul',
        'Leste',
        'Sudeste',
      ],
    };
  },
};
</script>
