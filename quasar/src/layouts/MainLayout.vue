<template>
  <q-layout view="hHh Lpr lff">
    <q-header elevated>
      <q-toolbar style = "background-color: #de7ca0">
        <q-btn
          flat
          dense
          round
          icon="menu"
          aria-label="Menu"
          @click="leftDrawerOpen = !leftDrawerOpen"
        />
        <q-toolbar-title>
          Cardápio Digital
        </q-toolbar-title>
        <!-- <q-item>
            <img src="~assets/logo.png" alt="">
          </q-item> -->

        <div>Quasar v{{ $q.version }}</div>
      </q-toolbar>
    </q-header>

    <q-drawer
      v-model="leftDrawerOpen"
      show-if-above
      bordered
      content-class="bg-grey-1"
    >
      <q-list>
        <q-item-label
          header
          class="text-grey-8"
        >
          Menu
        </q-item-label>
        <EssentialLink
          v-for="link in essentialLinks"
          :key="link.title"
          v-bind="link"
        />
      </q-list>
    </q-drawer>

    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<style>
  .q-item img {
    width: 10%;
    height: auto;
  }
</style>

<script>
import EssentialLink from 'components/EssentialLink';

export default {
  name: 'MainLayout',

  components: {
    EssentialLink,
  },

  data() {
    return {
      leftDrawerOpen: false,
      essentialLinks: [
        {
          title: 'Quero Pedir',
          caption: 'Faça seu pedido',
          icon: 'search',
          link: '#',
        },
        {
          title: 'Tenho um Cardápio',
          caption: 'Cadastre seu cardápio e receba pedidos',
          icon: 'menu_book',
          link: '#',
        },
        {
          title: 'Meus Pedidos',
          caption: 'Acompanhe seus últimos pedidos',
          icon: 'shopping_cart',
          link: '#',
        },
        {
          title: 'Entrar',
          caption: 'Acesse sua conta',
          icon: 'account_circle',
          link: '#',
        },
      ],
    };
  },
};
</script>
