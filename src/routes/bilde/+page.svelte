<script>
  import Slider from "$lib/slider.svelte";
</script>

<h2>Digitale Bilder</h2>
<p>
  Digitale bilder består av et stort antall små kvadratiske punkter som kalles
  piksler. Hver piksel representerer en enkelt farge, og når de kombineres,
  danner de et helhetsbilde. For å gjengi et bredt spekter av farger og nyanser
  brukes RGB-farge-modellen, der hver farge representeres av en kombinasjon av
  rød, grønn og blå.
  <br /><br />
  Bildet lagres vanligvis som en fil på en datamaskin eller annen enhet. Denne filen
  inneholder informasjon om hver piksel og deres fargeverdier. For å lagre denne
  informasjonen kreves minne, og mengden minne avhenger av bildeoppløsningen og fargedypet. Et bildet kan lagres
  i flere <a href="https://snl.no/bildeformat">bildeformater.</a>
  For å redusere størrelsen på bildefiler brukes komprimeringsteknikker.
  <br /><br />
  Vanlige bildekomprimeringsformater inkluderer JPEG og PNG. JPEG kan komprimere
  bildet til en ønsket størrelse. Dette er destruktiv komprimering hvor du mister
  detaljer i bildet ved at algoritmen som brukes slår piksler sammen til et støre
  område av samme farge. PNG formatet kan komprimere uten å miste detaljer ved tapsfri
  komprimering. Her brukes komprimeringsalgoritmer til å kode data på en mer effektiv
  måte uten å slå sammen piksler til et område. Det er derfor begrenset hvor mye
  mindre et bildet kan gjøres med tapsfri komprimering.
  <br /><br />
  Oppsummert fungerer digitale bilder ved å bruke små piksler for å representere
  farger, med RGB-fargemodellen for å skape ulike nyanser. Bildet lagres som en fil
  på en enhet, og størrelsen avhenger av oppløsningen og fargedypet. For å redusere
  filstørrelsen brukes komprimeringsteknikker.
  <br /><br />
</p>

<Slider />

<h3>Frisk bris av Hans Gude</h3>

<br>
<p>
  Bildene ovenfor er i JPEG format fra samme kilde og har samme oppløsning. Den
  ene er hele 10 ganger mindre i lagringsplass enn den andre. Kan du se
  forskjellen?
  <br />Zoom inn og bruke slideren for å sammenligne.
</p>

<div class="flexbetween">
  <a class="navknapp" href="/lyd">
    <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="3" stroke="currentColor" class="w-6 h-6" style="height: 3rem; vertical-align:middle;">
        <path stroke-linecap="round" stroke-linejoin="round" d="M15.75 19.5 8.25 12l7.5-7.5" />
      </svg>
      Lyd
    </a>
  <a class="navknapp" href="/video">Video  
      <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="3" stroke="currentColor" class="w-6 h-6" style="height: 3rem; vertical-align:middle;">
        <path stroke-linecap="round" stroke-linejoin="round" d="m8.25 4.5 7.5 7.5-7.5 7.5" />
      </svg>    
  </a>
</div>
