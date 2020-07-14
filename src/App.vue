<template>
  <v-app>


    <v-content class="ma-12">
 <AddTodo />
      <Todos/>
    </v-content>
  </v-app>
</template>

<script>
import Todos from './components/Todos';
import AddTodo from './components/AddTodo';


export default {
  name: 'App',

  components: {
    Todos,
    AddTodo

  },

  data: () => ({
    //
  }),
};
</script>
