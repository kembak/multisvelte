
<div class="centerdiv">
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

<style>
:global(body){
    font-family: "Libre Baskerville";
    background-color: #141824;
    color: white;
    margin: 0;
}
.centerdiv{
    max-width: fit-content;
    margin-top: 12vh;
    margin-inline: auto;
    /*border: 1px dotted green;*/
}
.maindiv{
    max-width: 800px;
    padding: 1rem;
    margin-inline: auto;
    /*border: 1px dotted red;*/
}
.centerdiv h1{
    display: inline;
    font-size: 4rem;
    font-weight: 400;
    word-wrap: break-word;
}
.heading{
    font-family: garamond;
    text-align: center;
    /*background-color: slategray;*/
    padding: .5rem;
}
.navbar{
    display: flex;
    justify-content: space-between;
    /*border: 1px dotted blue;*/
    font-size: 22px;
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
    font-family: garamond;
}
:global(.maindiv p){
    font-size: 1.25rem;
}
:global(.maindiv a){
    font-size: 1.25rem;
    line-height: 1.25;
    text-decoration: none;
    color: #4085fc;
    font-family: "Libre Baskerville";
}
:global(.maindiv a:hover){
    text-shadow: 0px 0px 4px rgba(255, 255, 255, .7);
}
footer{
    background-color: #1d2021;
    margin-top: 4rem;
}
.footercontent{
    padding: 1rem;
    text-align: center;
    font-size: 1.25rem;
    color: white;
}
</style>