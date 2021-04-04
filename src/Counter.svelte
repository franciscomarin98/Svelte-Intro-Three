<script>
    import Triple from "./Triple.svelte";

    let number = 0;
    const handleCount = () => (number += 1);
    $: doubleNumber = number * 2;
</script>

<div class="counter">
    <h5>
        Counter {number}
    </h5>
    <p>{doubleNumber} es el doble de {number}</p>
    <Triple {number} />
    <button on:click={() => (number += 1)}>+ forma 1</button>
    <button on:click={handleCount}>+ forma 2</button>
</div>

<!-- Apuntes:
Reactividad es hacer que una variable cambie al darse el cambio de otra variable

$: <- es simbolo significa reactividad
-->
