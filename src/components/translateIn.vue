<template>
    <div id="translateIn">Translation
        <form v-on:submit="formSubmit">
            <input v-model="textoTraducir" type="text" placeholder="Escriba la palabra">    
            <input type="submit" value="traducir">
        </form>    
        <h1>{{textoTraducir}}</h1>
    </div>    
</template>

<script>

export default {
    name: "translateIn",
    data(){
        return {
            textoTraducir: '',
            idioma:'en'
        }
    },
    methods:{
        formSubmit(e){
            this.$http.get(`https://translate.yandex.net/api/v1.5/tr.json/translate?key=trnsl.1.1.20190622T213455Z.f67e95598c7aee64.c0c49d0594aa527178d83c8e3c1a81ed05709a56&lang=${this.idioma}&text=${this.textoTraducir}`)
            .then((res)=>{
                this.textoTraducir=res.body.text[0]               
                
            });
            e.preventDefault();
        },

    
    }
}
</script>

