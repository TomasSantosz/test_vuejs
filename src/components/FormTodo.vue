<template>
    <div class="form-todo form-group">
        <input placeholder="nome" text="text" name="author" class="form-control"
        v-model="name" />
        <textarea placeholder="comentario" name="message" class="form-control" 
        v-model="message"></textarea>
        <button v-on:click="addComment" type="submit" class="btn btn-primary">Comentar</button>
    </div>
</template>
<script>

    export default {
        data(){
            return {
                name: '',
                message: '',
            }
        }, 
        methods:{
            addComment(){
                if(this.message.trim()=== ''){
                    return;
                }

                this.$emit('add-todo',{
                    name: this.name,
                    message: this.message
                })

                this.name = "";
                this.message = "";
            }
        }
    }
</script>