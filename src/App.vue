<template>
  <div id="app">
    <app-header></app-header>
    <router-view></router-view>
    <app-footer></app-footer>
    <notifications classes="kickstart-notification"/>
    <notifications group="kickstart-notification" />
  </div>
</template>

<script>
  import AppHeader from '@/components/AppHeader'
  import AppFooter from '@/components/AppFooter'

  export default {
    name: 'app',
    components: {
      AppHeader,
      AppFooter,
    },
  }
</script>

<style lang="scss">
  @import 'assets/styles/partials/mixins';
  @import 'assets/styles/partials/variables';
  @import 'assets/styles/partials/kickstart';

  .kickstart-notification {
    background: $yellow-warning !important;
    color: $c-white;
    font-size: 15px;
    text-align: center;
    margin-top: 20px;
    margin-right: 20px;
    border: 3px solid $c-white;

    .notification-title {
      text-decoration: underline;
      font-size: 18px;
    }
  }
</style>
