<script>
    import audioenheter from "$lib/assets/audiodevices.jpg";
    import sangHøy from "$lib/assets/IronMaidenAcesHigh.mp3";
    import sangLav from "$lib/assets/IronMaidenAcesHigh-low.mp3";
</script>
<h2>Lær om lyd</h2>
<p>Digital lyd består av en kontinuerlig strøm av lydbølger som er digitalisert og representert som tallverdier. 
    Når lyden spilles av, oversettes disse tallverdiene til lydbølger som vi kan høre.
    <br><br>
    En viktig faktor i digital lyd er <a href="https://no.wikipedia.org/wiki/Bitrate">bitrate</a> som angir hvor mye data som overføres per sekund. 
    Bitrate påvirker lydkvaliteten og filstørrelsen. Jo høyere bitrate, desto bedre lydkvalitet, 
    men også større filstørrelse. 
    Bitraten oppgis som regel i enheten kbps (kb/s) som står for hvor mange tusen bit data som blir overført per sekund i en lydfil.
    <br><br>
    Lydkvaliteten bestemmes også av samplingsfrekvensen, 
    som angir hvor ofte lydsignalet blir målt per sekund. 
    Jo høyere samplingsfrekvens, desto bedre gjengis lyden, spesielt høyfrekvente lyder.</p>
    <br><br>
    <div class="columnar">
        <img src={audioenheter} class="artikkelbilde" alt="illustrasjon av mp3 spiller og platespiller">
        <h3>En digital mp3 spiller og en analog platespiller</h3>
    </div>
    <br>
    <p>Ved lagring og overføring av digital lyd, som for eksempel i form av musikkfiler eller strømmetjenester, 
    komprimeres lyden for å redusere filstørrelsen. 
    Dette gjøres gjennom ulike lydkomprimeringsformater som for eksempel MP3, AAC eller OGG. 
    Komprimering kan føre til en viss reduksjon i lydkvalitet, spesielt ved lavere bitrate, 
    men moderne komprimeringsalgoritmer forsøker å opprettholde best mulig lydkvalitet
    samtidig som de reduserer filstørrelsen.
    <br><br>
    Oppsummert består digital lyd av tallverdier som representerer lydsignaler, 
    med bitrate og samplingsfrekvens som viktige faktorer som påvirker lydkvaliteten. 
    Lyden kan komprimeres for å redusere filstørrelsen, 
    men dette kan også påvirke lydkvaliteten avhengig av valgt komprimeringsformat og bitrate.
    <br><br>
    Hør forskjellen på to mp3 filer av samme sang med forskjellig bitrate.</p>
<div class="flexeven">
    <div class="columnar">
        <audio controls src={sangHøy}></audio>
        <h3>Iron Maiden - Aces High 168kbps</h3>
    </div>
    <div class="columnar">
        <audio controls src={sangLav}></audio>
        <h3>Iron Maiden - Aces High 64kbps</h3>
    </div>
</div>

<div class="flexbetween">
  <a class="navknapp" href="/">
    <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="3" stroke="currentColor" class="w-6 h-6" style="height: 3rem; vertical-align:middle;">
        <path stroke-linecap="round" stroke-linejoin="round" d="M15.75 19.5 8.25 12l7.5-7.5" />
      </svg>
      Hjem
    </a>
  <a class="navknapp" href="/bilde">Bilde  
      <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="3" stroke="currentColor" class="w-6 h-6" style="height: 3rem; vertical-align:middle;">
        <path stroke-linecap="round" stroke-linejoin="round" d="m8.25 4.5 7.5 7.5-7.5 7.5" />
      </svg>    
  </a>
</div>