<div class="centerdivheading">
    <div class="heading">
        <h1>MULTIMEDIA 101</h1>
    </div>
    <div class="navbar">
        <a href="/">Hjem</a>
        <a href="/lyd">Lyd</a>
        <a href="/bilde">Bilde</a>
        <a href="/video">Video</a>
        <a href="/quiz">Quiz</a>
    </div>
</div>

<div class="maindiv">
<slot />
</div>

<!--Jeg har valgt å definere globale stiler i denne filen.Layout
slot ligger inne i en kontiener div og jeg bruker svelte sin nestede css syntax for å lage stiler som kan brukes inni denne konteineren-->

<footer>
    <p style="font-family:Arial, Helvetica, sans-serif; font-size:large; color:#575f75; text-align:center; margin:10rem auto 2rem auto;">
        &#169; 2024 MULTIMEDIA 101 - <i>Alle Rettigheter Reservert</i></p>
</footer>

<style>
:global(body){
    font-family: 'Libre Baskerville', Georgia, 'Times New Roman', Times, serif;
    background-color: #141824;
    color: white;
    margin: 0;
}
.centerdivheading{
    max-width: fit-content;
    margin-top: 12vh;
    margin-inline: auto;
    /*border: 1px dotted green;*/
}
:global(.maindiv .centerdiv){
    margin: 1rem auto;
    border: 2px solid white;
}
:global(.maindiv .flexeven){
    display: flex;
    justify-content: space-evenly;
}
:global(.maindiv .columnar){
    display: flex;
    flex-direction: column;
    align-items: center;
}
:global(.maindiv .artikkelbilde){
    width: 75%;
    border-radius: 1rem;
}
.maindiv{
    max-width: 800px;
    padding: 1rem;
    margin-inline: auto;
    min-height: 100vh;
    /*border: 1px dotted red;*/
}
.centerdivheading h1{
    display: inline;
    font-size: 4rem;
    font-weight: 400;
    word-wrap: break-word;
}
.heading{
    font-family: Garamond, Georgia, "Times New Roman", times,  serif;
    text-align: center;
    padding: .5rem;
}
.navbar{
    display: flex;
    justify-content: space-between;
    font-size: 1.375rem;
    font-weight: 700;
    flex-wrap: wrap;
    font-family: garamond;
}
.navbar a{
    text-decoration: none;
    color: #9dd2bb;
    color: #fc4085;
    transition: 0.2s ease;
    padding: .5rem;

}
.navbar a:hover{
    color: #fc4085;
    color: #9dd2bb;
    font-weight: 700;
}
:global(.maindiv h2){
    text-align: center;
    color: #ffcc66;
    font-size: 1.75rem;
    font-family: Garamond, Georgia, 'Times New Roman', Times, serif;
}
:global(.maindiv h3){
    color: #bae67e;
    text-align: center;
    font-family: Garamond, Georgia, 'Times New Roman', Times, serif;
}
:global(.maindiv p){
    font-size: 1.125rem;
    line-height: 1.5;
}
:global(.maindiv a){
    font-size: 1.125rem;
    line-height: 1.25;
    text-decoration: none;
    color: #4085fc;
}
:global(.maindiv a:hover){
    text-shadow: 0px 0px 4px rgba(255, 255, 255, .7);
}
:global(.maindiv .navknapp){
    text-decoration: none;
    padding: 0rem;
    margin: 2rem 0 3rem 0;
    color: #da70d6;
    font-size: 1.5rem;
    font-weight: 700;
    font-family: Garamond;
    transition: 0.2s ease;
}
:global(.maindiv .navknapp:hover){
    color: white;
}
:global(.maindiv .flexbetween){
    display: flex;
    justify-content: space-between;
}
</style>