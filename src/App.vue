<template>
  <div id="app">
    <MyHeader />
    <router-view path="$router.key"></router-view>
    <MyFooter />
  </div>
</template>

<script>
import MyHeader from './components/Header';
import './styles/global.css';
import MyFooter from './pages/Footer';

export default {
  name: 'App',
  components: {
    MyHeader,
    MyFooter
  }
}
</script>
