<!-- Esto de aqui, mas allá de ser una declarion de un componente como tal, es documentación de algunos casos de usos de la reactividad de Svelte -->
<script>
    // Imprimir en consola
    $: console.log(variable);

    //Ejecutar fragmentos de codigo
    $: {
        //Expresion
    }

    //Condicionales
    $: if (arguments) {
        //Hacemos algo
    } else {
        // Hacemos algo más
    }

    //Bucles
    $: for (let i = 0; i < array.length; i++) {
        console.log(array[i]);
    }

    // Funciones
    $: variable = argumentos =>{
        //return
    }

    //Acciones async
    $: async () => {
        bar = await Promise.resolve(argumentos)
    }

    //Definicion de variables que son propiedades de un objeto
    $: ({a,b} = objeto)
</script>
