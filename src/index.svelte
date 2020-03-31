<script>
    let name = `What's your name?`
    let tempC = 20
    $:tempF = Math.round(tempC * 1.8) + 32
</script>

<h1 class="title">Hot Chocolate</h1>

<label>
    Name: 
    <input type="text" bind:value={name} />
</label>

<label>
    Drink temperature: 
    <input type="range" min="0" max="100" bind:value={tempC} />
</label>

{tempC}°C ({tempF}°F)

{#if tempC < 40}
    <p>A wee bit chilly ❄</p>
{:else if tempC > 90}
    <p>Ouch! Burnt tongue 🔥.</p>
{:else}
    <p>Very nice! ☕</p>
{/if}