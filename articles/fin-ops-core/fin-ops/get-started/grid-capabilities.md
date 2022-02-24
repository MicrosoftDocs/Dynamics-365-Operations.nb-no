---
title: Rutenettfunksjoner
description: Dette emnet beskriver flere kraftfulle funksjoner i rutenettkontrollen. Den nye rutenettfunksjonen må være aktivert for at du skal kunne få tilgang til disse funksjonene.
author: jasongre
manager: AnnBe
ms.date: 11/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: DefaultDashboard
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2020-02-29
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: fb30cdded33f90bb472c8abdb70875077b1dd985
ms.sourcegitcommit: f5e31c34640add6d40308ac1365cc0ee60e60e24
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/08/2020
ms.locfileid: "4693780"
---
# <a name="grid-capabilities"></a>Rutenettfunksjoner

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Den nye rutenettkontrollen tilgjengeliggjør en rekke nyttige og kraftfulle funksjoner som kan brukes til å forbedre brukerproduktivitet, konstruere mer interessante visninger av dataene og få meningsfulle innsikter i dataene. Denne artikkelen dekker følgende funksjoner: 

-  Beregner totaler
-  Skriving i forkant av systemet
-  Evaluering av matematiske uttrykk 
-  Grupperetabelldata (aktivert separat ved hjelp av **funksjonen (Forhåndsvisning) Gruppering i rutenett**)
-  Låste systemkolonner

## <a name="calculating-totals"></a>Beregner totaler
I Finance and Operations-apper har brukere muligheten til å se totalverdier nederst i numeriske kolonner i rutenett. Disse totalverdiene vises i en bunntekstinndeling nederst i rutenettet. 

### <a name="showing-the-grid-footer"></a>Vise rutenettbunnteksten
Det er et bunntekstområde nederst i alle tabellrutenett i Finance and Operations -apper. Bunnteksten kan vise nyttig informasjon som er knyttet til dataene som vises i rutenettet. Her er noen eksempler på denne informasjonen:

- Antallet valgte rader i tabellen (når mer enn én oppføring er valgt)
- Hovedsummer nederst i konfigurerte numeriske kolonner
- Antallet rader i datasettet 

Denne bunnteksten er skjult som standard, men den kan enkelt aktiveres. Hvis du vil vise bunnteksten for et rutenett, høyreklikker du på en kolonneoverskrift i rutenettet og velger **Vis bunntekst**-alternativet. Når bunnteksten er aktivert for et bestemt rutenett, vil denne innstillingen bli husket til brukeren velger å skjule bunnteksten, noe som kan gjøres ved å høyreklikke på en kolonneoverskrift og velge **Skjul bunntekst**.  Vær oppmerksom på at plasseringen av **Vis bunntekst / Skjul bunntekst**-handlingen forventes å bli forflyttet i en fremtidig oppdatering. 

### <a name="specifying-columns-with-totals"></a>Angi kolonner med totalverdier
For øyeblikket er ingen kolonner konfigurert til å vise totalverdier som standard. I stedet betraktes dette som en engangsoppsettsaktivitet, som tilsvarer justering av bredden på kolonnene i rutenett. Når du har angitt at du vil se totalverdier for en kolonne, vil denne innstillingen bli husket neste gang du besøker siden.  

Det finnes to måter for å konfigurere en kolonne til å vise en totalverdi: 

- Høyreklikk i kolonnen du vil se en totalverdi for, og velg deretter **Summer denne kolonnen**. Denne handlingen fører til at tre hendelser skjer:

    1. Bunnteksten blir synlig. 
    2. Preferansene dine for å se totalverdien for denne kolonnen lagres. 
    3. En beregning av totalverdier startes for denne kolonnen og alle andre kolonner du tidligere konfigurerte til å se totalverdier for. Hvor lang tid det tar å vise en totalverdi, avhenger av størrelsen på datasettet du skal summere.

- Når bunnteksten er synlig, velger du **Vis totalverdi** i bunntekstområdet nederst i kolonnen som du vil vise en totalverdi for. Hvis det ikke finnes konfigurerte kolonner, vil **Vis totalverdi**-knappen være tilgjengelig for alle numeriske kolonner. 

    Når minst én kolonne er konfigurert for totalverdier, vil **Vis totalverdi**-knappene bare være tilgjengelige ved peking eller fokus. Handlingen ved å velge **Vis totalverdi** bare lagrer innstillingen for å vise en totalverdi i denne kolonnen, slik at innstillingen brukes ved fremtidige besøk på siden. I bunnteksten angis denne statusen av en bindestrek som vises i kolonnen. (Hvis datasettet er lite nok, vises også en totalverdi umiddelbart.)

Hvis du gjør en feil og ikke lenger ønsker å se en totalverdi i en bestemt kolonne, høyreklikker du på kolonnen og velger **Skjul totalverdi** eller velger **Skjul totalverdi**-knappen i bunnteksten i denne kolonnen. Denne innstillingen vil også bli lagret for fremtidige besøk på siden. 

### <a name="calculating-totals"></a>Beregner totaler
Når du kommer til en side der bunnteksten er synlig og kolonnene allerede er konfigurert for totalverdier, kan det hende at totalverdiene ikke vises i bunnteksten. Atferden avhenger av størrelsen på datasettet på siden. Hvis datasettet er tilstrekkelig lite, vises totalverdiene automatisk sammen med antallet rader i datasettet. Hvis det finnes streker i bunnteksten under kolonnene du har konfigurert for totalverdier, er datasettet for stort til at systemet kan vise totalverdier umiddelbart, og en eksplisitt handling er nødvendig for å beregne totalverdiene. Hvis du vil gjøre dette, klikker du på **Beregn**-knappen i bunnteksten, eller høyreklikker på en kolonne du vil ha totalverdi for, og velger **Summer denne kolonnen**.  

Hvis beregningen tar for lang tid, kan du avbryte operasjonen ved å velge **Avbryt**-knappen. Noen ganger vil datasettet imidlertid være for stort til å beregne totalverdier (en grense som pålegges av organisasjonen), og du vil i stedet få et varsel om at dataene må filtreres mer.

Totalverdier oppdateres automatisk når du oppdaterer, sletter eller oppretter rader i datasettet.  

## <a name="typing-ahead-of-the-system"></a>Skriving i forkant av systemet
I mange forretningsscenarier er muligheten til raskt å legge inn data i systemet svært viktig. Før den nye rutenetrkontrollen ble innført, kunne brukere bare endre data i den gjeldende raden. Før de kunne opprette en ny rad eller bytte til en annen rad, ble de tvunget til å vente på at systemet skal validere eventuelle endringer. I et forsøk på å redusere tiden som brukere venter på at disse valideringene skal fullføres, og for å forbedre brukerproduktiviteten, justerer det nye rutenettet disse valideringene slik at de er asynkrone. Derfor kan brukeren flytte til andre rader for å gjøre endringer mens tidligere radvalideringer venter. 

For å støtte denne nye virkemåten, er det lagt til en ny kolonne for radstatusen til høyre for radvelgerkolonnen når rutenettet er i redigeringsmodus. Denne kolonnen angir én av følgende statuser:

- **Tom** – ingen statusbilde angir at raden er lagret i systemet.
- **Behandling venter** – denne statusen angir at endringene i raden ikke er lagret på serveren ennå, men er i en kø av endringer som må behandles. Før du utfører handlinger utenfor rutenettet, må du vente på at alle ventende endringer skal behandles. I tillegg er teksten i disse radene i kursiv for å angi den ulagrede statusen for radene. 
- **Ugyldig tilstand** – denne statusen angir at en advarsel eller melding ble utløst under behandlingen av raden, og den kan ha forhindret systemet fra å lagre endringene i den raden. I det gamle rutenettet måtte du gå tilbake til raden for å løse problemet umiddelbart dersom lagringsoperasjonen mislyktes. I det nye rutenettet blir du imidlertid varslet om at det ble funnet et valideringsproblem, men du kan bestemme når du vil rette opp eventuelle problemer i raden. Når du er klar til å løse et problem, kan du flytte fokus tilbake til raden manuelt. Du kan også velge handlingen **Løs dette problemet**. Denne handlingen flytter umiddelbart fokus tilbake til raden som har problemet, og gjør det mulig å redigere i eller utenfor rutenettet. Legg merke til at behandlingen av påfølgende ventende rader blir stoppet til denne valideringsadvarselen blir løst. 
- **Midlertidig stanset** – denne statusen angir at behandlingen av serveren er stoppet midlertidig fordi valideringen av raden utløste en popup-dialogboks som krever inndata fra brukeren. Fordi brukeren kan registrere data i en annen rad, blir hurtigdialogboksen ikke umiddelbart presentert for denne brukeren. Den vil i stedet presenteres når brukeren velger å gjenoppta behandlingen. Denne statusen følges av et varsel som informerer brukeren om situasjonen. Varslingen inneholder en **Gjenoppta behandling**-handling som vil utløse hurtigdialogboksen.  
    
Når brukere angir data før serveren behandles, kan de forvente seg noen reduksjoner i dataregistreringsopplevelsen, for eksempel mangel på oppslag, validering på kontrollnivå og oppføring av standardverdier. Brukere som trenger en rullegardinliste for å finne en verdi, oppfordres til å vente til serveren blir oppdatert til gjeldende rad. Kontrollnivå-validering og registrering av standardverdier vil også forekomme når serveren behandler denne raden.   

### <a name="pasting-from-excel"></a>Lime inn fra Excel
Brukere har alltid hatt muligheten til å eksportere data fra rutenett i Finance and Operations-apper til Excel ved hjelp av funksjonen **Eksporter til Excel**. Muligheten til å angi data før systemet gjør imidlertid at det nye rutenettet kan støtte kopiering av tabeller fra Excel og lime dem direkte inn i rutenett i Finance and Operations-apper. Rutenettcellen som innlimingen startes fra, bestemmer hvor den kopierte tabellen begynner å limes inn. Innholdet i rutenettet overskrives av innholdet i den kopierte tabellen, med unntak av to tilfeller:

- Hvis antallet kolonner i den kopierte tabellen overskrider antall kolonner som beholdes i rutenettet, med start fra innlimingen, varsles brukeren om at de ekstra kolonnene er ignorert. 
- Hvis antall rader i den kopierte tabellen overskrider antall rader i rutenettet, med start fra innlimingen, blir de eksisterende cellene overskrevet av det innlimte innholdet, og eventuelle ekstra rader fra den kopierte tabellen blir satt inn som nye rader nederst i rutenettet. 

## <a name="evaluating-math-expressions"></a>Evaluering av matematiske uttrykk
Som en produktivitetsforsterkning kan brukeren legge inn matematiske formler i numeriske celler i et rutenett. De trenger ikke å utføre beregningen i en app utenfor systemet. Hvis du for eksempel angir **=15\*4** og deretter trykker på **Tab**-tasten for å gå ut av feltet, evaluerer systemet uttrykket og lagrer verdien **60** for feltet.

Hvis du vil at systemet skal gjenkjenne en verdi som et uttrykk, starter du verdien med et likhetstegn (**=**). Hvis du vil ha mer informasjon om de støttede operatorene og syntaksen, kan du se [Støttede matematiske symboler](http://bugwheels94.github.io/math-expression-evaluator/#supported-maths-symbols).

## <a name="grouping-tabular-data"></a>Gruppere tabelldata
Bedriftsbrukere må ofte utføre ad hoc-analyse av data. Selv om dette kan utføres ved å eksportere data til Microsoft Excel og bruke pivottabeller, gjør funksjonen **Gruppering i rutenett**, som er generelt tilgjengelig i versjon 10.0.16/Platform update 40 og er avhengig av den nye rutenettkontrollfunksjonen, det mulig for brukere å organisere sine tabelldata på interessante måter i Finance and Operations-apper. Ettersom denne funksjonen utvider **Totalverdier**-funksjonen, gjør **Gruppering** det mulig å få meningsfulle innsikter i dataene takket være oppgivelse av subtotalverdier på gruppenivå.

Hvis du vil bruke denne funksjonen, høyreklikker du kolonnen du vil gruppere etter, og velger **Grupper etter denne kolonnen**. Denne handlingen sorterer dataene etter den valgte kolonnen, legger til en ny **Grupper etter**-kolonne i begynnelsen av rutenettet og setter inn "topptekstrader" i begynnelsen av hver gruppe. Disse topptekstradene inneholder følgende informasjon om hver gruppe: 
-  Dataverdi for gruppen 
-  Kolonnenavn (denne informasjonen er spesielt nyttig når du har grupperinger på flere nivåer)  
-  Antallet datarader i denne gruppen
-  Subtotalverdier for enhver kolonne som er konfigurert for å vise totalverdier

Med [Lagrede visninger](saved-views.md) aktivert kan denne grupperingen lagres ved å tilpasning som en del av en visning for rask tilgang neste gang du besøker siden.  

### <a name="multiple-levels-of-grouping"></a>Flere nivåer med gruppering
Når du har gruppert data etter én enkelt kolonne, kan du gruppere dataene etter en annen kolonne ved å velge **Grupper etter denne kolonnen** på ønsket kolonne. Denne prosessen kan gjentas til du har 5 nestede nivåer av gruppering, som er den maksimale dybden som støttes. På dette stadiet vil du ikke lenger kunne gruppere etter flere kolonner.  

Du kan når som helst fjerne grupperingen på en kolonne ved å høyreklikke denne kolonnen og velge **Del opp gruppe**. Du kan også fjerne grupperingen fra alle kolonnene ved å velge **Alternativer for rutenett** og deretter velge **Del opp alle grupper**.   

Vær oppmerksom på at før versjon 10.0.16/Platform update 40, støttes bare ett nivå av gruppering. Hvis dataene er gruppert i disse versjonene, og du velger **Grupper etter denne kolonnen** for en annen kolonne, erstattes den opprinnelige grupperingen.  


### <a name="expanding-and-collapsing-groups"></a>Vise og skjule grupper
Den innledende grupperingen av data vil få alle grupper vist. Du kan opprette sammendragsvisninger av dataene ved å skjule enkeltstående grupper, eller du kan bruke gruppevisning og -skjuling for å hjelpe til med å navigere gjennom dataene. Hvis du vil vise eller skjule en gruppe, velger du knappen med vinkeltegnet (>) i den tilsvarende topptekstraden for gruppe. Legg merke til at vis/skjul-statusen til enkelt grupper **ikke** lagres i tilpassing.

### <a name="selecting-and-unselecting-rows-at-the-group-level"></a>Merke og oppheve merking av rader på gruppenivå
På samme måte som du kan merke (eller oppheve) alle radene i rutenettet ved å merke av øverst i den første kolonnen i rutenettet, kan du også raskt merke av for (eller oppheve merking) for alle radene i en gruppe ved å merke av i den tilsvarende topptekstraden for gruppe. Avmerkingsboksen i topptekstraden for gruppe vil alltid gjenspeile den gjeldende valgstatusen for rader i denne gruppen, uansett om alle rader er merket, ingen rader er merket, eller bare enkelte rader er merket.

### <a name="hiding-column-names"></a>Skjule kolonnenavn
Når du grupperer data, er standard virkemåte å vise kolonnenavnet i topptekstraden for gruppe. Fra og med versjon 10.0.14/plattformoppdatering 38, kan du velge å skjule kolonnenavnet i topptekstrader for gruppe ved å velge **Alternativer for rutenett** > **Skjul gruppekolonnenavn**.

## <a name="pinned-system-columns"></a>Låste systemkolonner
Radvelgingskolonnen og radstatuskolonnen i i det nye rutenettet er låst, eller frosset, på venstre side av rutenettet. Når disse kolonnene er inkludert i et rutenett, vil de alltid være synlige for brukeren, uavhengig av den vannrette rulleplasseringen i rutenettet.   

## <a name="frequently-asked-questions"></a>Vanlige spørsmål
### <a name="how-do-i-enable-the-new-grid-control-in-my-environment"></a>Hvordan aktiverer jeg den nye rutenettkontrollen i miljøet? 

**10.0.9 / Platform update 33 og senere**

Funksjonen **Ny rutenettkontroll** er tilgjengelig direkte i funksjonsbehandling i et hvilket som helst miljø. I likhet med andre forhåndsvisningsfunksjoner er aktivering av denne funksjonen i produksjonen underlagt [Ekstra vilkår for bruksavtalen](https://go.microsoft.com/fwlink/?linkid=2105274).  

**10.0.8 / Platform update 32 og 10.0.7 / Platform update 31**

Funksjonen **Ny rutenettkontroll** kan aktiveres i lag 1 (dev/test) og lag 2 (sandkasse) for å ytterligere testing og utformingsendringer ved å følge fremgangsmåten nedenfor.

1.  **Aktiver testversjonen**: Kjør følgende SQL-setning: 

    `INSERT INTO SYSFLIGHTING (FLIGHTNAME, enabled, FLIGHTSERVICEID, PARTITION) VALUES('CLIReactGridEnableFeature', 1, 0, 5637144576);`

2. **Tilbakestill IIS** for å tømme statisk buffer for testversjonering. 

3.  **Finn funksjonen**: Gå til arbeidsområdet **Funksjonsbehandling**. Hvis **Ny rutenettkontroll** ikke vises i listen over alle funksjoner, velger du **Se etter oppdateringer**.   

4.  **Aktiver funksjonen**: Finn funksjonen **Ny rutenettkontroll** i listen over funksjoner, og velg **Aktiver nå** i detaljruten. Vær oppmerksom på at det kreves en oppdatering av nettleseren. 

Alle etterfølgende brukerøkter starter med at den nye rutenettkontrollen er aktivert.

## <a name="developer-opting-out-individual-pages-from-using-the-new-grid"></a>[Utvikler] Velge bort enkeltsider fra å bruke det nye rutenettet 
Hvis organisasjonen oppdager en side der det er noen problemer med å bruke det nye rutenettet, er det tilgjengelig et API fra og med versjon 10.0.13 / Platform update 37 for å tillate at et enkelt skjema bruker den gamle rutenettkontrollen samtidig som resten av systemet brukes til å utnytte den nye rutenettkontrollen. Hvis du vil velge bort en enkelt side fra det nye rutenettet, legger du til følgende oppkallspost `super()` i skjemaets `run()`-metode.

 ```this.forceLegacyGrid();```

Dette API-et støttes til oktober 2021-versjonen når den nye rutenettkontrollen blir obligatorisk. Hvis problemer gjør at denne APIen brukes, rapporterer du dem til Microsoft.

## <a name="developer-size-to-available-width-columns"></a>[Utvikler] Skaler-til-tilgjengelig-bredde-kolonner
Hvis en utvikler setter egenskapen **WidthMode** til **SizeToAvailable** for kolonner i det nye rutenettet, har disse kolonnene i utgangspunktet samme bredde som de ville ha hvis egenskapen ble satt til **SizeToContent**. De kan imidlertid strekke seg for å bruke en eventuell ekstra tilgjengelig bredde i rutenettet. Hvis egenskapen er satt til **SizeToAvailable** for flere kolonner, deler alle disse kolonnene tilgjengelig ekstra bredde i rutenettet. Hvis en bruker imidlertid endrer størrelsen på en av disse kolonnene manuelt, blir kolonnen statisk. Den blir stående i denne bredden, og strekker seg ikke lenger til å bruke ekstra tilgjengelig rutenettbredde.  

## <a name="known-issues"></a>Kjente problemer
Denne delen inneholder en liste over kjente problemer for den nye rutenettkontrollen mens funksjonen er i en forhåndsvisningstilstand.  

### <a name="open-issues"></a>Åpne problemer
-  Når du har aktivert funksjonen **Ny rutenettkontroll**, vil noen sider fortsette å bruke den eksisterende rutenettkontrollen. Dette vil skje i følgende situasjoner:  
    -  Det finnes en kortliste på siden som gjengis i flere kolonner.
    -  Det finnes en gruppert kortliste på siden.
    -  En rutenettkolonne med en ikke-reagerende utvidbar kontroll.

    Når en bruker først støter på én av disse situasjonene, vil det vises en melding om oppdatering av siden. Når denne meldingen vises, vil siden fortsette å bruke det eksisterende rutenettet for alle brukere til neste oppdatering av produktversjonen. Bedre behandling av disse scenariene, slik at det nye rutenettet kan brukes, vurderes for en fremtidig oppdatering.    
    
-  [KB 4582758] Poster er utydelige når du endrer zooming fra 100 til en annen prosent
    
### <a name="fixed-as-part-of-10015"></a>Løst som del av 10.0.15    

-  [KB 4582723] Visningsalternativer som ikke vises når du er ferdig senere i skjemalivssyklusen

### <a name="fixed-as-part-of-10014"></a>Løst som del av 10.0.14

-  (Kvalitetsoppdatering) [KB 4584752] Uventet klientfeil for siden Fakturaforslag for prosjekt

### <a name="fixed-as-part-of-10013"></a>Løst som del av 10.0.13

-  (Kvalitetsoppdatering) [KB 4583880] Regression Suite Automation Tool (RSAT) Tester mislykkes på OpenLookup-handling med "Kan ikke lese egenskapen RowIndex for udefinert"
-  (Kvalitetsoppdatering) [KB 4583847] Uventet klientfeil ved navigering gjennom oppslag 
-  (Kvalitetsoppdatering) [Feil 471777] Kan ikke velge felt i et rutenett for å redigere eller opprette en mobilapp
-  [Feil 474851] Hyperkoblinger i referansegruppekontroller fungerer ikke 
-  [Feil 474848] Utvidede forhåndsvisninger med rutenett vises ikke
-  [KB 4582726] RotateSign-egenskapen blir ikke respektert  
-  [Feil 470173] Avmerkingsbokser i inaktive rader veksler når mellomrom i cellen klikkes
-  [Feil 474848] Utvidede forhåndsvisninger med rutenett vises ikke
-  [Feil 474851] Hyperkoblinger i referansegruppekontroller fungerer ikke 
-  [Feil 471777] Kan ikke velge felt i et rutenett for å redigere eller opprette en mobilapp
-  [KB 4569441] Problemer med å gjengi kortlister med flere kolonner, verktøytips på bilder og visningsalternativer for enkelte felt
-  [KB 4575279] Ikke alle merkede rader blir slettet i økonomijournalen
-  [KB 4575233] Visningsalternativer gjenopprettes ikke etter flytting til en annen rad
-  [Feil 477884] Oppslag returnerer feil verdi/post hvis ny rutenettkontroll er aktivert
-  [KB 4571095] Produktkvitteringspostering skjer når du trykker Enter ved en feiltakelse (riktig håndtering av en sides standardhandling)
-  [KB 4575437] Oppslag med redigerbare kontroller lukkes uventet
-  [KB 4569418] Duplikat linje opprettet i leveringsplanskjema
-  [KB 4575435] Forbedret forhåndsvisning vedvarer noen ganger, selv når musepekeren ikke er nær feltet
-  [KB 4575434] Oppslag filtrerer ikke når feltet er endret
-  [KB 4575430] Verdier i passordfelt blir ikke maskert i rutenettet.
-  [KB 4569438] "Behandlingen har stoppet på grunn av et valideringsproblem", vises etter markering av linjer under utregning av leverandørtransaksjoner
-  [KB 4569434] Oppdatering av skjemaet for juridiske enheter resulterer i færre poster
-  [KB 4575297] Fokus holder seg til oppgaveregistreringsruten når du redigerer og går gjennom kategorier i et rutenett
-  [KB 4566773] Korrigeringstransaksjoner vises ikke som negative på bilagstransaksjonsforespørsel 
-  [KB 4575288] Fokus tilbakestilles til den aktive raden når du velger kantlinjen mellom rader i en enkel liste
-  [KB 4575287] Fokuset går ikke tilbake til den første kolonnen når du bruker pil ned til å opprette en ny rad i journaler
-  [KB 4564819] Kan ikke slette linjer i en fritekstfaktura (fordi datasource ChangeGroupMode=ImplicitInnerOuter)
-  [KB 4563317] Verktøytips / forbedrede forhåndsvisninger vises ikke for bilder

### <a name="fixed-as-part-of-10012"></a>Løst som del av 10.0.12

- [KB 4558545] Tabellkontroller oppdaterer ikke innholdet i viste elementer.
- [KB 4558570] Varer vises fortsatt på siden etter at posten er slettet.
- [KB 4558572] Stiler som er knyttet til listepanelet **ExtendedStyle**, brukes ikke.
- [KB 4558573] Valideringsfeil kan ikke løses når den nødvendige endringen er utenfor rutenettet.
- [KB 4558584] Negative tall gjengis ikke riktig.
- [KB 4560726] Det oppstår en "uventet klientfeil" etter at bytting mellom lister utføres ved hjelp av en Listevisning-kontroll.
- [KB 4562141] Rutenettindekser deaktiveres etter at en ny post er lagt til.
- [KB 4562151] Alternativene **Valider** og **Kopier** for oppgaveopptaker er ikke tilgjengelige for dato/nummer-kontroller. 
- [KB 4562153] Avmerkingsbokser med flervalgsalternativer er ikke synlige i liste- og kortrutenett.
- [KB 4562646] Du kan av og til ikke klikke utenfor rutenettet etter at du har valgt flere rader i rutenettet.
- [KB 4562647] Fokus tilbakestilles til den første kontrollen i **Publiser**-dialogboksen etter at en ny rad er lagt til i rutenettet for sikkerhetsroller.
- [KB 4563310] Den utvidede forhåndsvisningen lukkes ikke etter at en rad er endret.
- [KB 4563313] Det oppstår en "uventet klientfeil" i Internet Explorer når en verdi velges i et oppslag.
- [KB 4564557] Oppslag og rullegardinmenyer åpnes ikke i Internet Explorer
- [KB 4563324] Navigasjon fungerer ikke etter at **Personaladministrasjon**-arbeidsområdet er åpnet.

### <a name="fixed-as-part-of-10011"></a>Løst som del av 10.0.11

- [Problem 432458] Tomme eller dupliserte linjer vises på begynnelsen av enkelte underordnede samlinger.
- [KB 4549711] Linjer i et betalingsforslag kan ikke fjernes riktig etter at den nye rutenett kontrollen er aktivert.
- [KB 4558374] Poster som krever en dialogboks for polymorfisk velger, kan ikke opprettes.
- [KB 4558375] Hjelpetekst vises ikke på kolonner i det nye rutenettet.
- [KB 4558376] Listepanel-rutenett er ikke gjengitt med riktig høyde i Internet Explorer.
- [KB 4558377] Kombinasjonsboks-kolonner med bredden **SizeToAvailable** gjengis ikke på enkelte sider.
- [KB 4558378] Gjennomgang åpner av og til feil post.
- [KB 4558379] Det oppstår en feil når oppslag åpnes der **ReplaceOnLookup**=**Nei**.
- [KB 4558380] Den tilgjengelige plassen i rutenettet fylles ikke umiddelbart etter at en del av siden er skjult.
- [KB 4558381] Negative tall gjengis ikke riktig / brukere blir noen ganger låst etter at valideringsproblemer oppstår.
- [KB 4558382] Det oppstår uventede klientfeil.
- [KB 4558383] Kontroller utenfor rutenettet oppdateres ikke etter at den siste posten er slettet.
- [KB 4558587] Referansegrupper som har kombinasjonsbokser for erstatningsfelt, viser ikke verdier.
- [KB 4562143] Felt oppdateres ikke etter en radendring / rutenettbehandling blir låst etter sletting av rader.
- [KB 4562645] Et unntak oppstår når et oppslag åpnes mens Regression Suite Automation Tool-tester (RSAT) kjører.

### <a name="fixed-as-part-of-10010"></a>Løst som del av 10.0.10

- [Problem 414301] Noen data fra tidligere linjer forsvinner når nye linjer opprettes.
- [Feil 417044] Det finnes ingen tomt rutenett-melding for rutenett i listestil.
- [KB 4539058] Noen rutenett (vanligvis på hurtigfaner) er noen ganger ikke gjengitt (men de vil vises hvis du zoomer ut).
- [KB 4549734] Aktive rader behandles ikke som merket hvis merkingskolonnen er skjult.
- [KB 4549796] Verdier kan ikke redigeres i et rutenett når det er i visningsmodus.
- [KB 4558367] Tekstmerking er inkonsekvent når rader endres.
- [KB 4558368] Flervalg via tastaturet er tillatt i enkeltvalg-scenarier.
- [KB 4558369] Statusbilder forsvinner i det hierarkiske rutenettet.
- [KB 4558370] En ny rad blir ikke rullet i visningen.
- [KB 4558372] Det nye rutenettet blir låst i behandlingsmodus hvis antallet kolonner i innholdet som limes inn, overstiger antallet gjenstående kolonner i rutenettet.
- [KB 4562631] Tidsverdier er ikke riktig formatert.

### <a name="quality-update-for-1009platform-update-33"></a>Kvalitetsoppdatering for 10.0.9/Platform update 33

- [KB 4550367] Tidsverdier er ikke riktig formatert.
