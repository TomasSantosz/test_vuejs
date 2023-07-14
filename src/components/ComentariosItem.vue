<template>
    <FormTodo v-on:add-todo="addComment"/>
    <div class="comment_div">
        <h1>{{ msg }}</h1>
        <div v-for="(comment, index) in comments" :key="index">
            <p>{{ comment.name  }}</p>
            <p>{{ comment.message  }}</p>
            <p>----</p>
        </div>
    </div>
</template>
<script>
import FormTodo from './FormTodo.vue';
/* ✓ GOOD */
export default {
  name: 'ComentariosItem',
  components:{
    FormTodo,
  },
  props: {
    msg: String
  },
  methods:{
    addComment(comment){
        this.comments.push(comment)
    }
  },
  data(){
    return {
      comments: []
    }
  }
}
</script>