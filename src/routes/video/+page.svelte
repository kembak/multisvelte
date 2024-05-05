<script>
    import porschevideo from "$lib/assets/porsche720p.mp4";
</script>
<h2>Digital video</h2>

<p>Digital video består av en serie av bilder (rammer) som vises i rask rekkefølge.
    En viktig faktor i digital video er dataraten (data rate), som angir hvor mye data som overføres per sekund. Dataraten påvirker både bildekvaliteten og filstørrelsen. Jo høyere datarate, desto bedre bildekvalitet, men også større filstørrelse.
    <br><br>
    Bildeoppløsningen er også en nøkkelkomponent i digital video. Denne måler antall piksler i hver ramme og påvirker tydeligheten og detaljnivået i videoen. Vanlige oppløsninger inkluderer HD (1280x720 piksler), Full HD (1920x1080 piksler), og 4K (3840x2160 piksler).
    <br><br>
    Ved lagring og overføring av digital video, blir den ofte komprimert for å redusere filstørrelsen. Dette gjøres ved hjelp av ulike video <a href="https://no.wikipedia.org/wiki/Videokomprimering">komprimeringsformater</a> som for eksempel H.264, H.265 (også kjent som HEVC), eller VP9. Komprimering reduserer filstørrelsen ved å fjerne redundans i dataene og ved å bruke avanserte algoritmer for å kode videoen mer effektivt. Dette kan føre til en viss reduksjon i bildekvalitet, spesielt ved lavere datarater, men moderne komprimeringsalgoritmer forsøker å opprettholde best mulig bildekvalitet samtidig som de reduserer filstørrelsen.
    <br><br>
    <div class="columnar">
    <video class="artikkelbilde" controls alt="video av porshce">
        <source src={porschevideo} type="video/mp4">
    </video>
    <h3>Porsche reklame - HD video i mp4 format 1 mbps</h3>
    </div>
    <br>
    <p>
    Oppsummert består digital video av en serie av bilder som vises i rask rekkefølge, med datarate og bildeoppløsning som viktige faktorer som påvirker bildekvaliteten og filstørrelsen. Videoen kan komprimeres for å redusere filstørrelsen, men dette kan også påvirke bildekvaliteten avhengig av valgt komprimeringsformat og datarate.
    </p>

<div class="flexbetween">
  <a class="navknapp" href="/bilde">
    <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="3" stroke="currentColor" class="w-6 h-6" style="height: 3rem; vertical-align:middle;">
        <path stroke-linecap="round" stroke-linejoin="round" d="M15.75 19.5 8.25 12l7.5-7.5" />
      </svg>
      Bilde
    </a>
  <a class="navknapp" href="/quiz">Quiz  
      <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="3" stroke="currentColor" class="w-6 h-6" style="height: 3rem; vertical-align:middle;">
        <path stroke-linecap="round" stroke-linejoin="round" d="m8.25 4.5 7.5 7.5-7.5 7.5" />
      </svg>    
  </a>
</div>