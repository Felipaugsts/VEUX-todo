<template>
  <v-app class="text-center">

<div class="d-flex flex-row flex-wrap justify-center">
<div 
v-for="(todos, index) in allTodos" :key="index"
class="ma-5 text-center ">
<v-card
color="green d-flex justify-center align-center pa-5"
height="90px"
width="300px"

>{{todos.title}} 

<v-spacer></v-spacer><v-btn   @click="deleteTodo(todos.id)" icon> <v-icon color="white">mdi-delete</v-icon></v-btn>

</v-card>

</div>

</div>

  </v-app>
</template>
<script>
import { mapGetters, mapActions} from 'vuex';
export default {
  methods: {
    ...mapActions(["fetchTodo","deleteTodo"])
  },
  computed: mapGetters(['allTodos']),
  created() {
    this.fetchTodo();
  }
  
}
</script>