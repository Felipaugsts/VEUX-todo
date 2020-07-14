<template>
    <div class="d-flex justify-center" >


    <v-card flat width="50vh" class=" mt-12 text-right">
    <v-form @submit="onSubmit"  > 
    <v-text-field v-model="title" label="Add To do" 
   outlined=""/> 
  
   <v-btn @keyup.enter.native="submit" type="submit" small text outlined color="blue"> Add todo </v-btn>
    </v-form>
    </v-card>

    </div>
</template>
<script>
import {mapActions} from 'vuex';
export default {
    name: "AddTodo",
    data() {
        return { 
            title: ''
        }
    },

    methods: { 
        ...mapActions(['addTodo']),
        onSubmit(e) { 
            e.preventDefault();
            this.addTodo(this.title);

        }
    }
}
</script>