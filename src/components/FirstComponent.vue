<template>
    <div>
        <h1>Titre 1</h1>
        <h2>message : {{ msg }}</h2>
        <p>Seulement le premier mot : {{ onlyFirstWord }}</p>
        <p>{{ longText(world) }}</p>
    </div>
</template>

<script>
export default {
    data(){
        return{
            msg:'Hello big world',
            hello: 'Hello',
            world:'will world',
            
        }
    },
   computed:{
       onlyFirstWord(){
           return this.msg.split(' ')[0].toUpperCase();
       },
       longText(){
           return function fullText(mot){
               return this.hello + ' ' + mot
           }
       }
   },
   created(){

   },
   mounted(){

   },
   methods(){

   },
   
    
}
</script>

<style  scoped>

h1{
        color:red;
    }

</style>