<script>
    import before from "$lib/assets/hansgude-liten.jpg";
    import after from "$lib/assets/hansgude-stor.jpg";
    let bredde = 50;
</script>

<div class="image-comparison">
    <div class="images-container">
        <img class="before-image" src={before} alt="Frisk bris av Hans Gude" style="--ny-bredde: {bredde + "%"}">
        <img class="after-image" src={after} alt="Frisk bris av Hans Gude">

        <div class="slider-line" style="--ny-bredde: {bredde + "%"}"></div>
        <div class="slider-icon" style="--ny-bredde: {bredde + "%"}">
            <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-6 h-6">
                <path stroke-linecap="round" stroke-linejoin="round" d="M8.25 15 12 18.75 15.75 15m-7.5-6L12 5.25 15.75 9" />
            </svg>
              
        </div>
        <input type="range" bind:value={bredde} class="slider" min="0" max="100">
        <!--Det ligger en usynlig input type range over bildet som er bindet til den reaktive variablen
        "slideren" som har opasitet er kun en strek i form av en div og et ikon som begge har en css variabel for posisjon som er lik den reaktive variablen til input range elementet-->
    </div>
</div>

<!--Istedenfor å bruke javascript til å lage denne slidere slapp jeg unna med kun én svelte
reaktiv variabel kombinert med styling og css-varaibler.
Dette er et sveltekomponent som kan importeres og vises hvor som helst i routes på samme måte som slot fungerer for layout-->

<style>
    .image-comparison{
        max-width: 650px;
        max-height: 425px;
        margin: 1rem auto 1rem;
        border-radius: 1rem;
        overflow: hidden;
    }
    .image-comparison img{
        width: 100%;
        height: 100%;
        object-fit: cover;
        object-position: left;
    }
    .image-comparison .images-container{
        position: relative;
        display: flex;
    }
    .image-comparison .images-container .before-image{
        position: absolute;
        top: 0;
        width: var(--ny-bredde);
    }
    .image-comparison .slider{
        position: absolute;
        inset: 0;
        opacity: 0;
    }
    .image-comparison .slider-line{
        position: absolute;
        height: 100%;
        width: 3px;
        background-color: black;
        left: var(--ny-bredde);
        transform: translateX(-50%);
    }
    .image-comparison .slider-icon{
        position: absolute;
        left: var(--ny-bredde);
        top: 50%;
        width: 70px;
        height: 70px;
        color: black;
        transform: translate(-50%, -50%) rotateZ(90deg);
    }
</style>