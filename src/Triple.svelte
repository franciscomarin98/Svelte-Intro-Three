<script>
    export let number;
    $: tripleNumero = number * 3;
</script>


<p>{tripleNumero} es el triple de {number}</p>