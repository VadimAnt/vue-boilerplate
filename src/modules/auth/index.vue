<template>
  <SignupForm v-if="currentRoute == '/signup'" />
  <SigninForm v-else />
</template>

<script>
import { mapGetters } from 'vuex';
import SignupForm from './components/SignupForm';
import SigninForm from './components/SigninForm';

const STORE_KEY = 'auth';

export default {
  name: 'AuthModule',
  data: () => ({
    currentRoute: window.location.pathname,
  }),
  components: {
    SignupForm,
    SigninForm,
  },
};
</script>
