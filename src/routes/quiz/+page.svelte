<script>
  let quizData;

  async function fetchQuizData() {
    const response = await fetch(
      "https://raw.githubusercontent.com/kembak/multisvelte-json/main/quiz.json"
    );
    quizData = await response.json();
  }

  fetchQuizData();
  //definerer variabler
  let sporsmalIndex = 0;
  let antallRiktige = 0;
  let svar;

  function avgiSvar(svar) {
    if (svar === quizData[sporsmalIndex].riktigsvar) {
      antallRiktige++;
      // hvis svaret er likt som fasit øker antallet riktige svar
    }
    nyttSvar()
  }
  function nyttSvar() {
    //øker indexen til spørmsål og resetter svar variable til neste spørsmål
    sporsmalIndex++;
    svar = "";
  }

  function avsluttQuiz() {
    // viser antall riktige svar fra quizen som en melding
    alert(`Du fikk ${antallRiktige} av ${quizData.length} riktige.`);
    sporsmalIndex = 0;
    antallRiktige = 0;
    svar = "";
    // resetter alle verdiene igjen når quizen avsluttes
  }
</script>

<br><br>

{#if quizData}
  {#if sporsmalIndex < quizData.length}
    <div class="quizkont">
      <!--Konteiner for quizen-->
      <h2>{quizData[sporsmalIndex].sporsmal}</h2>
      {#if quizData[sporsmalIndex].type === "text"}
      <!--hvis json opjektet har type lik text vises html koden under-->
        <div class="inputsvar">
        <input type="text" bind:value={svar} />
        <!--binder input til svar-->
        <button on:click={() => avgiSvar(svar)}>SVAR</button>
        <!--svaret blir input til funksjonen som sjekker riktig svar-->
        </div>
      {:else if quizData[sporsmalIndex].type === "button"}
      <!--Hvis objekter er av type button vises html koden under-->
        {#each quizData[sporsmalIndex].alternativer as alternativ}
        <!--Viser hvert alternativ som en knapp-->
          <div class="columnar">
            <button class="svaralternativ" on:click={() => avgiSvar(alternativ)}
              >{alternativ}</button
            >
          </div>
        {/each}
      {/if}
    </div>
  {:else}
  <!--hvis objektet har ingen type er quizen ferdig og html koden under vises-->
    <div class="quizkont">
    <div class="columnar">
      <button class="svaralternativ" style="margin-top: 10rem; width: 30%" on:click={avsluttQuiz}>Avslutt Quiz</button>
    </div>
    </div>
  {/if}
{/if}


<h2 style="margin-top: 8rem;">Psuedokode for quizen</h2>
<br><ol>
  <li>Hent quiz-data fra JSON-fil</li><br>
  <li>Definer variabler:</li>
    <ul>
      <li>quizData: Holder den hentede quiz-dataen</li>
      <li>spørsmålIndex: Sporer indeksen til gjeldende spørsmål som vises</li>
      <li>antallRiktige: Sporer antall riktige svar</li>
    </ul><br>
  <li>Funksjon fetchQuizData():</li>
    <ul>
      <li>Hent quiz-data fra github med fetch</li>
      <li>Lagre JSON-responsen i variabelen quizData</li>
    </ul><br>
  <li>Lag to forskjellige typer spørsmål</li>
    <ul>
      <li>En med inputfelt og en med alternativer som knapper, hvert objekt i json filen har enten tekst eller knapp som type.</li>
      <li>Lag en each løkke for å vise alle alternativer viss typer er knapp som trigger funksjonen avgiSvar.</li>
      <li>Lag en knapp hvis typen er tekst som også trigger avgiSvar</li>
    </ul><br>
  <li>Funksjon avgiSvar(svar):</li>
    <ul>
      <li>Sjekk om det innsendte svaret er likt det riktige svaret for gjeldende spørsmål</li>
      <li>Hvis det er riktig, øk antallRiktige</li>
      <li>Gå videre til neste spørsmål ved å øke spørsmålIndex</li>
    </ul><br>
  <li>Funksjon avsluttQuiz():</li>
    <ul>
      <li>Vis en melding med antall riktige svar av totalt antall spørsmål</li>
      <li>Tilbakestill variablene for å starte quizen på nytt</li>
    </ul>
</ol>

<style>
  ol{
    font-size: 1.25rem;
    line-height: 1.75rem;
    color: #4085fc;
  }
  ul{
    font-size: 1.125rem;
    color: white;
  }
  .quizkont {
    padding: 3rem;
    font-family: garamond;
    min-height: 60vh;
    color: black;
  }
  .quizkont h2 {
    color: white;
    text-transform: uppercase;
    font-size: xx-large;
  }
  .svaralternativ {
    display: block;
    width: 50%;
    color: black;
    background-color: #ffcc66;
    font-size: larger;
    margin: 0.5rem 0 0.5rem 0;
    padding: 0.75rem;
    border: 0px solid white;
    border-radius: 2rem;
    transition: 0.1s ease;
  }
  .svaralternativ:hover, .inputsvar button:hover {
    background-color: white;
    box-shadow: 0 0 .5rem rgba(0, 0, 0, 0.5);
  }
  .inputsvar{
    width: 60%;
    margin: 6rem auto;
    display: flex;
    justify-content: space-between;
  }
  .inputsvar button{
    all: unset;
    font-family: Arial, Helvetica, sans-serif;
    font-size: larger;
    text-align: center;
    width: 8rem;
    background-color: #ffcc66;
    color: black;
    border-radius: 2rem;
    transition: 0.1s ease;
  }
  .inputsvar input{
    all: unset;
    text-align: center;
    font-family: Arial, Helvetica, sans-serif;
    background-color: white;
    width: 100%;
    margin-right: 1rem;
    font-size: larger;
    padding: .75rem;
    border: none;
    border-radius: 2rem;
  }
  .inputsvar input:focus, input:hover{
    box-shadow: 0 0 .5rem rgba(0, 0, 0, 0.5);
  }
</style>
