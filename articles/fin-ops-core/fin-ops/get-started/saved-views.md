---
title: Lagrede visninger
description: Dette emnet beskriver hvordan du bruker lagrede visninger-funksjonene.
author: jasongre
manager: AnnBe
ms.date: 08/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2019-07-31
ms.dyn365.ops.version: Platform update 28
ms.openlocfilehash: 4b1bd7b869b68f82ce8056ac9f87a0d3bdce4102
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/27/2019
ms.locfileid: "2190885"
---
# <a name="saved-views"></a>Lagrede visninger

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

## <a name="introduction"></a>Innledning
Personlig tilpasning spiller en viktig rolle for å gi brukere og organisasjoner muligheten til å optimalisere brukeropplevelsen for å dekke behovene deres. Hvis du vil ha mer informasjon om tilpassing, se [Tilpasse brukeropplevelsen](personalize-user-experience.md).

Med tradisjonell tilpasning kan brukere bare ha ett sett av personlige tilpasninger per skjema. Lagrede visninger utvider personlig tilpasning på mange viktige måter:

-    Visninger lar brukere ha flere navngitte sett med personlige tilpasninger per skjema, som de raskt kan bytte etter behov. Dermed kan en bruker opprette flere optimaliserte visninger av en side, der hver visning er tilpasset for å få plass til behovene for å utføre en bestemt forretningsoppgave. 

-    Visninger som opprettes for bestemte sidetyper, kan også inneholde brukertillagte filtre eller sorteringer, som gjør at brukere raskt kan gå tilbake til vanlige datasett. Se delen [Hvilke sider som støtter visninger](saved-views.md#what-pages-support-views) for mer informasjon. 

-    Visninger kan publiseres til sikkerhetsroller, noe som betyr at alle brukere med denne rollen vil kunne få tilgang til og bruke denne visningen, uavhengig av brukerens mulighet til å tilpasse. Ved hjelp av denne publiseringsfunksjonen kan organisasjoner definere standardvisninger som er optimalisert for deres virksomhet. Se delen [Administrere tilpasninger på organisasjonsnivå med visninger](saved-views.md#managing-personalizations-at-an-organizational-level-with-views) for mer informasjon.

-    I motsetning til tradisjonell tilpasning lagres ikke visninger automatisk når en bruker utfører eksplisitte tilpasninger eller filtrerer en liste. Eksplisitte lagre er nødvendig for å gi fleksibilitet ved oppretting av en visning før eller etter at endringene som er knyttet til denne visningen, er gjort, og for å sikre at visningsdefinisjoner ikke endres utilsiktet av filtre eller personlige tilpasninger som ikke er ment for langsiktig bruk.  

## <a name="switching-between-views"></a>Bytte mellom visninger
Når visninger har blitt aktivert for et miljø, vil alle sider som støtter visninger, ha en skjult visningsvelgerkontroll øverst på skjemaet som viser navnet på gjeldende visning.  

Visningsvelgeren har to størrelsesvariasjoner: 

-   **Store visningsvelgere**: Sider som tydelig viser en liste, vil ha en større visningsvelger av flere årsaker. Det viktigste er at store visningsvelgere angir sidene der visningen kan inkludere brukerdefinerte filtre. Fordi filtre er inkludert i visningene, er den større velgerstørrelsen også egnet fordi visningsnavnene ofte vil være den beste beskrivelsen av dataene som vises på skjermen, og forventningen er at brukerne vil bytte mellom visninger oftere på disse sidetypene.  
 
-   **Små visningsvelgere**: Alle andre helsideskjemaer (med unntak av arbeidsområder og instrumentbordet) har en mindre visningsvelger som vises ved siden av sidetittelen. Visninger på disse sidene inkluderer bare personlige tilpasninger (og ikke brukerdefinerte filtre). På disse sidene er skjematittelen eller posttittelen ofte den viktigste informasjonen øverst i skjemaet. Den minste størrelsen gjenspeiler også en lavere forventet frekvens for visningsskifte på disse sidene. 
 
Hvis du klikker på visningsnavnet, åpnes visningsvelgeren og viser listen over tilgjengelige visninger for denne siden.

-    **Klassisk visning**: Den klassiske visningen er standardvisningen av siden, uten eksplisitte tilpasninger.  
-    **Personlige visninger**: Visningene uten hengelås representerer dine personlige visninger. Dette er visninger som enten du har opprettet, eller som en administrator har gitt deg.  
-    **Låste visninger**: Noen visninger (for eksempel Klassisk visning og visninger som er publisert til din rolle) har en hengelås ved siden av i visningsvelgeren, som angir at du ikke kan redigere disse visningene. Implisitte tilpasninger som gjenspeiler sidebruk, lagres imidlertid automatisk, for eksempel det å endre bredden på en rutenettkolonne eller vise eller skjule en hurtigfane. Du kan imidlertid opprette en personlig visning basert på en låst visning ved hjelp av handlingen **Lagre en kopi** hvis du har rettigheter til personalisering.
-    **Nye visninger**: Publiserte visninger som ennå ikke er åpnet, er merket med en gnist til venstre for visningsnavnet.  

Hvis du vil bytte til en annen visning, åpner du først visningsvelgeren og velger deretter visningen du vil laste inn. 

## <a name="creating-and-modifying-views"></a>Opprette og endre visninger
I motsetning til tradisjonell tilpasning lagres ikke visninger automatisk når en bruker utfører eksplisitte tilpasninger (eller filtrerer en liste). Det kreves en eksplisitt handling for å lagre disse endringene i en visning. Dette gir brukerfleksibilitet ved oppretting av en visning før eller etter at endringene som er knyttet til denne visningen, er gjort, og sikrer også at visningsdefinisjoner ikke endres utilsiktet av éngangsfiltre eller personlige tilpasninger. Merk at implisitte tilpasninger (som å vise eller skjule en hurtigfane eller endre bredden på en rutenettkolonne) automatisk lagres til gjeldende visning, selv for låste visninger. 

Hvis du vil sikre at gjeldende status for visningen er kjent, vises det en stjerne ved siden av det gjeldende visningsnavnet når du begynner å gjøre endringer i en visning ved å utføre en eksplisitt personalisering eller filtrering, som angir at du ser på en ulagret, endret versjon av denne visningen.

Hvis du vil lagre disse endringene, følger du disse trinnene.
1.  Velg visningsnavnet for å åpne visningsvelgeren.
2.  Slik endrer du den eksisterende visningen:
     1. Velg **Lagre**. Merk at denne handlingen ikke vil bli aktivert for låste visninger. 
3.  Slik oppretter du en ny visning:
     1.    Velg **Lagre en kopi**. 
     2.    Skriv inn et visningsnavn og (eventuelt) en beskrivelse.
     3.    Velg **Lagre**.

## <a name="changing-the-default-view"></a>Endre standardvisningen
Standardvisningen er visningen systemet vil prøve å åpne når du først går til siden. Du bør angi denne til visningen som du forventer å bruke oftest.  

Følg disse trinnene for å endre standardvisningen for en side: 
1.  Bytt til visningen du bruker som standard. 
2.  Velg visningsnavnet for å åpne visningsvelgeren. 
3.  Velg **Merk** og deretter **Bruk som standard**.  

Når du oppretter en ny visning (ved hjelp av **Lagre som kopi**-handling), kan du gjøre denne nye visningen til standardvisning ved å velge **Bruk som standard**-valget før du lagrer visningen.  

Vær oppmerksom på at i noen tilfeller vil spørringen som er knyttet til standardvisningen, ikke utføres første gang du navigerer til en side. Hvis du for eksempel navigerer via en flis til en side, blir flisens spørring utført uansett hvilken spørring som er knyttet til standardvisningen. Hvis du navigerer til en side der Klassisk visning allerede har en definert spørring, vil den opprinnelige spørringen utføres opprinnelig i stedet for standardvisningens spørring. Når dette skjer, vil du bli varslet av en informasjonsmelding når visningen lastes inn. Bytting av visninger etter at siden er lastet inn, skal gjøre at visningsspørringen kjøres som forventet.

## <a name="managing-personal-views"></a>Behandle personlige visninger 
Dialogboksen **Behandle mine visninger** gir deg grunnleggende vedlikeholdsfunksjoner for personlige visninger og rekkefølgen på visningene i visningsvelgeren. Hvis du vil åpne denne siden, klikker du visningsnavnet for å åpne rullegardinmenyen, velger **Mer** og deretter **Behandle mine visninger**.  

Hvis du vil ha en liste over tilgjengelige visninger for denne siden, er følgende sett med handlinger tilgjengelige.  
-    **Endre standardvisning**: Bruk funksjonen **Bruk som standard** for å gjøre den merkede visningen til standardvisning for denne siden.  
-    **Endre rekkefølgen på visningene**: Bruk handlingene **Flytt opp** og **Flytt ned** for å omorganisere visningene i en bestemt rekkefølge.  
-    **Gi en visning nytt navn**: Bruk **Gi nytt navn**-handlingen for å endre navnet på den merkede personlige visningen. Denne handlingen er deaktivert for låste visninger. 
-    **Slette en visning**: Bruk **Fjern**-handlingen for å slette gjeldende uthevede visning fra siden permanent. Det er ikke mulig å gjenopprette en visning etter at du har fjernet den.  

Endringer som gjøres i denne dialogboksen, vil tre i kraft når du har valgt **Lagre**-knappen.

## <a name="managing-personalizations-at-an-organizational-level-with-views"></a>Administrere personlige tilpasninger på et organisasjonsnivå med visninger
For å forstå forbedringene ved å administrere personlige tilpasninger på et organisasjonsnivå, må du først se hvordan behandling av personlige tilpasninger fungerte før visninger.  

Uten visninger vil administratorer bruke et sett med personlige tilpasninger på en side for en bruker eller en gruppe av brukere via personaliseringssiden. Hvis disse brukerne hadde tilpasningsrettigheter, ville de personlige tilpasningene gjelde for den siden. Det var imidlertid ikke mulig å hindre brukere i å tilpasse siden ytterligere, som betød at organisasjonen ikke kan sikre at brukerne har et konsekvent brukergrensesnitt. Hvis noen av disse brukerne ikke hadde tilpasningsrettigheter, ble ikke tilpasningene som ble gitt til dem av en administrator, lastet inn. Hvis nye brukere ble ansatt i en organisasjon, måtte administratorer manuelt laste inn et sett med personlige tilpasninger for brukeren. Det var ingen automatisk mekanisme for å angi at et bestemt sett med personlige tilpasninger skal være tilgjengelig for brukere i denne rollen.

Med funksjonen for lagrede visninger er organisasjonens administrasjon av tilpasninger betydelig enklere, primært på grunn av muligheten for å publisere visninger til sikkerhetsroller. Når en visning er publisert, kan en hvilken som helst bruker med denne rollen få tilgang til og bruke visningen, uavhengig av brukerens mulighet til å tilpasse. Hver bruker har en kopi av den publiserte visningen der sidebruk (implisitte tilpasninger) brukes automatisk, og ingen brukere kan lagre eksplisitte personlige tilpasninger eller oppdateringer i spørringen i den publiserte visningen (det vil si at publiserte visninger er låst). Hvis nye brukere får en rolle som visningen ble publisert til, vil de automatisk se visningene som er tilknyttet rollene sine, uten handling fra administratoren. På samme måte, hvis en bruker endrer roller i en organisasjon, vil ikke visningene som er tilknyttet den gamle rollen, lenger være tilgjengelige for dem, også denne gangen uten noen handling fra administratoren. Oppdateringer til en publisert visning kan lett distribueres til brukere ved å publisere visningen på nytt til de riktige sikkerhetsrollene.

Publiseringsfunksjonen gjør det mulig for organisasjoner å definere standardvisninger som er optimalisert for deres virksomhet, som er målrettet til brukere i spesifikke sikkerhetsroller.  

## <a name="publishing-views"></a>Publiseringsvisninger
Under publiseringsprosessen kan visninger tilordnes én eller flere sikkerhetsroller, noe som betyr at en hvilken som helst bruker med denne rollen vil ha tilgang til og bruke denne visningen, men de kan ikke redigere visningen. Det er for øyeblikket bare systemansvarlige som har rettigheter til **Publiser**-handlingen i rullegardinmenyen Vis velger, men en ny sikkerhetsrolle vil være tilgjengelig i en fremtidig oppdatering for å gi publiseringsrettigheter til andre klarerte brukere.  

Hvis du vil publisere en visning, gjør du følgende: 
1.  Opprett og lagre en personlig kopi av visningen du vil publisere. 
2.  Når den aktuelle visningen er lastet, velger du visningsnavnet for å åpne rullegardinmenyen for visningsvalg. 
3.  Velg **Mer**-knappen, og velg deretter **Publiser**. Dialogboksen Publiser åpnes.  
4.  Oppgi et navn og (eventuelt) en beskrivelse av visningen. Dette er navnet som brukeren som mottar denne visningen, vil se i visningsvelgerne. Vær oppmerksom på at det ikke er tillatt med like navn for publiserte visninger for en side, selv om listen over roller de brukes på, er forskjellige.  
5.  Legg til eventuelle sikkerhetsroller som samsvarer med brukerne som skal få denne visningen.  
6.  Velg **Publiser**.

Legg merke til at i noen miljøer kan det ta litt tid (opptil en time) før brukerne ser den publiserte visningen.

## <a name="modifying-a-published-view"></a>Endre en publisert visning
Når du har publisert en visning, vil du kanskje endre en publisert visning. Selv om du ikke kan foreta direkte endringer i en publisert visning, kan du publisere en visning på nytt for å foreta oppdateringer, fordi disse visningene er låst for redigering for alle brukere (inkludert utgivere).  

Hvis endringene du vil gjøre i en publisert visning, bare vil involvere publiseringsparameterne (navnet på og beskrivelsen av visningen eller sikkerhetsrollene som visningen er publisert til), gjør du følgende: 
1.  Bytt til visningen som er publisert for parameterne du vil oppdatere. 
2.  Velg **Publiser** fra rullegardinmenyen for visningsvelgeren. 
3.  Velg **Ja** hvis du vil oppdatere den eksisterende visningen (eller **Nei** hvis du vil publisere dette under et annet navn).
4.  Oppdater navnet, beskrivelsen og/eller sikkerhetsrollene for visningen. 
5.  Velg **Publiser**. 
6.  Hvis du oppdaterte navnet på den publiserte visningen, må du også slette den publiserte visningen med det gamle navnet (se delen **Behandle publiserte visninger** hvis du vil ha mer informasjon). 

Hvis endringene i den publiserte visningen omfatter endring av personlige tilpasninger eller filtre tilknyttet visningen, følger du denne fremgangsmåten: 
1.  Bytt til den publiserte visningen du vil endre. 
2.  Lagre en kopi av den publiserte visningen for å opprette en lokal kladd av den publiserte visningen. 
3.  Endre den lokale kladden med de nødvendige endringene.
4.  Publiser visningen med det opprinnelige navnet. 

## <a name="managing-published-views"></a>Behandle publiserte visninger
I likhet med behandling av personlige visninger gir dialogboksen **Behandle mine visninger** brukere med publiseringsrettigheter grunnleggende vedlikeholdsfunksjoner for sidens publiserte visninger (i tillegg til sine egne personlige visninger). Hvis du vil åpne denne siden, velger du visningsnavnet for å åpne rullegardinmenyen, velger **Mer** og deretter **Behandle mine visninger**.

Alle brukere ser kategorien **Mine visninger**, som viser personlige visninger, men brukere med publiseringsrettigheter ser også kategorien **Publisert** for siden. Fordi det kan være flere brukere som publiserer visninger, er det viktig å kunne behandle hele listen over publiserte visninger, uansett om du var brukeren som faktisk har publisert visningen.

Hvis du vil ha en liste over alle publiserte visninger for siden, er følgende sett med handlinger tilgjengelige. 

-    **Publiser**: Bruk handlingen **Publiser** til å publisere en visning på nytt med endrede publiseringsparametere (navn, beskrivelse, sikkerhetsroller).  
-    **Fjern**: Bruk handlingen **Fjern** til å slette en publisert visning permanent. Denne handlingen fjerner visningen for alle brukere i systemet.  
 
Endringer som gjøres i denne dialogboksen, vil tre i kraft når **Lagre**-knappen er valgt.

## <a name="frequently-asked-questions"></a>Vanlige spørsmål
### <a name="how-do-i-enable-saved-views-in-my-environment"></a>Hvordan aktiverer jeg lagrede visninger i miljøet? 
Hvis du vil aktivere lagrede visninger mens funksjonen er i forhåndsvisning, følger du fremgangsmåten nedenfor: 

1.  **Aktiver testversjonen**: Kjør følgende SQL-setning: 

    `INSERT INTO SYSFLIGHTING (FLIGHTNAME, enabled, FLIGHTSERVICEID, PARTITION) VALUES('CLISavedViewsEnableFeature', 1, 0, 5637144576);`

2. **Tilbakestill IIS** for å tømme statisk buffer for testversjonering. 

3.  **Finn funksjonen**: Gå til arbeidsområdet **Funksjonsbehandling**. Hvis **Lagrede visninger** ikke vises i listen, velger du **Se etter oppdateringer**.   

4.  **Aktiver funksjonen**: Finn funksjonen **Lagrede visninger** i listen over funksjoner, og velg **Aktiver nå** i detaljruten.

Alle etterfølgende brukerøkter starter med at lagrede visninger er aktivert.  

Vær oppmerksom på at hvis tilpassing er deaktivert for miljøet, vil visninger bli deaktivert selv om du følger fremgangsmåten ovenfor. Dette er fordi visningsfunksjonen er bygget på toppen av delsystemet for personalisering.

### <a name="what-happens-to-existing-personalizations-when-views-are-enabled"></a>Hva skjer med eksisterende personlige tilpasninger når visninger er aktivert? 
Når visninger aktiveres, blir eksisterende personlige tilpasninger for en bruker og et skjema lagret i en ny visning kalt **Min visning**, som automatisk blir angitt som standardvisning. Dette er ment å sikre en konsekvent brukeropplevelse før og etter at visningene er aktivert, bortsett fra at visningsvelgerkontrollen vises i skjemaer.  

### <a name="what-pages-support-views"></a>Hvilke sider støtter visninger? 
Visninger er tilgjengelige på de fleste, men ikke alle sider. Spesifikt er visninger tilgjengelige for alle fullskjermsider, bortsett fra instrumentbord og arbeidsområder. Sider som ikke er fullskjerm, som inkluderer dialogbokser, rullegardindialogbokser, oppslag, utvidede forhåndsvisninger, støtter for øyeblikket heller ikke visninger. Visningsstøtte for flere sidetyper, for eksempel arbeidsområder og dialogbokser, kan bli vurdert for en fremtidig oppdatering.   

### <a name="who-is-allowed-to-publish-views"></a>Hvem kan publisere visninger?
Gjeldende systemadministratorer er de eneste brukerne som har rettigheter til å publisere visninger.  En ny sikkerhetsrolle er planlagt i en senere oppdatering, noe som vil gi kundene mer fleksibilitet i forhold til hvem som kan publisere.  

### <a name="why-am-i-not-able-to-save-filters-with-this-view"></a>Hvorfor kan jeg ikke lagre filtre med denne visningen? 
Det kan være flere grunner til at et filter ikke ser ut til å lagres med en visning: 

- Det kan hende at siden ikke støtter lagring av filtre som en del av visningsdefinisjonen. Vær oppmerksom på at bare sider med store visningsvelgere gjør det mulig å lagre endringer som en visning. Se delen "Bytte visninger" for mer informasjon. 

- Hvis visningen er standardvisningen, og navigasjonsbanen til siden inneholder en spørring, kan ikke visningens spørring brukes i utgangspunktet. De to hovedscenarioene for dette er: 
     - Hvis du navigerer til en side fra en flis, vil flisspørring utføres uansett hvilken spørring som er knyttet til standardvisningen. 
     - Hvis du navigerer til en side, og det inngangspunktet inkluderer en spørring, vil den opprinnelige spørringen utføres opprinnelig i stedet for standardvisningens spørring. 
     
  Når slike situasjoner oppstår, skal du bli varslet av en informasjonsmelding når visningen lastes inn. Du kan også bekrefte ved å bytte til denne visningen etter at siden er lastet inn, som gjør at visningsspørringen kan kjøres uansett.  

- Den aktuelle siden støtter kanskje ikke visninger på riktig måte, siden den kan ignorere visningsspørringen fullstendig eller operere på en midlertidig tabell med data som ikke er vedvarende. 
