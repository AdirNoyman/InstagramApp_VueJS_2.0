<template>
  <q-layout view="lHh Lpr lFf">
    <q-header elevated>
      <q-toolbar>
        <q-btn
          flat
          dense
          round
          icon="menu"
          aria-label="Menu"
          @click="leftDrawerOpen = !leftDrawerOpen"
        />

        <q-toolbar-title>
          Adiros App
        </q-toolbar-title>

        <div>Quasar v{{ $q.version }}</div>
      </q-toolbar>
    </q-header> 
    <q-footer
       class="bg-white"
       bordered
     >      
      <q-tabs
        class="text-grey-10"
        active-color="primary"
        indicator-color="transparent"
      >      
        <q-route-tab
          icon="fas fa-home"                 
          to="/"
          exact
        />
        <q-route-tab
          icon="fas fa-camera"                   
          to="/camera"
          exact
        />
        
      </q-tabs>
      
      </q-footer>
    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script>


export default {
  name: 'MainLayout', 
  data () {
    return {
     
    }
  }
}
</script>

<style lang="sass">
.q-footer
   .q-tab__icon
     font-size: 30px
</style>
