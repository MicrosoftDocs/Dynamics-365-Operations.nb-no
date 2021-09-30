---
title: Lagrede visninger
description: Dette emnet beskriver hvordan du bruker lagrede visninger-funksjonene.
author: jasongre
ms.date: 09/13/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2019-07-31
ms.dyn365.ops.version: Platform update 28
ms.openlocfilehash: d6a7b1b21816db43a92364584e15ec04b891c611
ms.sourcegitcommit: 7a2001e4d01b252f5231d94b50945fd31562b2bc
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/15/2021
ms.locfileid: "7487847"
---
# <a name="saved-views"></a>Lagrede visninger

[!include [banner](../includes/banner.md)]

## <a name="introduction"></a>Innledning

Personlig tilpasning spiller en viktig rolle for å gi brukere og organisasjoner muligheten til å optimalisere brukeropplevelsen for å dekke behovene deres. Hvis du vil ha mer informasjon om tilpassing, se [Tilpasse brukeropplevelsen](personalize-user-experience.md).

Med tradisjonell tilpasning kan brukere bare ha ett sett av personlige tilpasninger per side. Funksjonen **Lagrede visninger** utvider personlig tilpasning på mange viktige måter:

- Visninger lar brukere ha flere navngitte sett med personlige tilpasninger per skjema, som de raskt kan bytte etter behov. Dermed kan en bruker opprette flere optimaliserte visninger av en side, der hver visning er tilpasset for å få plass til behovene for å utføre en bestemt forretningsoppgave. 
- Visninger som opprettes for bestemte sidetyper, kan også inneholde brukertillagte filtre eller sorteringer, som gjør at brukere raskt kan gå tilbake til vanlige datasett. Se delen [Hvilke sider som støtter visninger](saved-views.md#what-pages-support-views) for mer informasjon. 
- Visninger kan publiseres til brukere i bestemte sikkerhetsroller og bestemte juridiske enheter. Derfor kan alle brukere som har en bestemt rolle i og tilgang til en bestemt juridisk enhet, få tilgang til og bruke denne visningen, selv om brukeren kanskje ikke har tillatelse til å tilpasse den. Ved hjelp av denne publiseringsfunksjonen kan organisasjoner definere standardvisninger som er optimalisert for deres virksomhet. Se delen [Administrere tilpasninger på organisasjonsnivå med visninger](saved-views.md#managing-personalizations-at-an-organizational-level-with-views) for mer informasjon.
- I motsetning til tradisjonell tilpasning lagres ikke visninger automatisk når en bruker utfører tilpasninger eller filtrerer en liste. Eksplisitte lagringer er nødvendig for å gi brukerne fleksibilitet til å opprette en visning før eller etter at endringene som er knyttet til denne visningen, er gjort. Dette kravet sikrer også at visningsdefinisjoner ikke endres utilsiktet av filtre eller personlige tilpasninger som ikke er ment for langvarig bruk. Elementer som systemet lagrer automatisk som en del av vanlig sidebruk (for eksempel kolonnebredder eller den utvidede eller sammenslåtte tilstanden til inndelinger), blir lagret per visning.
- Visninger kan legges til arbeidsområder som fliser, lister eller koblinger. Derfor kan et filtrert datasett vises i et arbeidsområde, og brukere kan knytte sammen et sett med tilpasninger som er relevante for dette datasettet med en flis eller kobling.

## <a name="switching-between-views"></a>Bytte mellom visninger

Når visninger har blitt gjort tilgjengelige for et miljø, vil toppen av alle sider som støtter visninger, ha en skjult visningsvelgerkontroll som viser navnet på gjeldende visning.

Visningsvelgeren har to størrelsesvariasjoner: 

- **Store visningsvelgere** – Sider som tydelig viser en liste, vil ha en større visningsvelger av flere årsaker. Det viktigste er at store visningsvelgere angir sidene der visningen kan inkludere brukerdefinerte filtre. Fordi filtre er inkludert i visningene, er den større velgerstørrelsen også egnet fordi visningsnavnene ofte vil være den beste beskrivelsen av dataene som vises på skjermen, og forventningen er at brukerne vil bytte mellom visninger oftere på disse sidetypene.
- **Små visningsvelgere** – Alle andre fullskjermsider (med unntak av arbeidsområder og instrumentbordet) har en mindre visningsvelger som vises ved siden av sidetittelen. Visninger på disse sidene inkluderer bare tilpasninger, ikke brukerdefinerte filtre. På disse sidene er teksten eller posttittelen ofte den viktigste informasjonen øverst på siden. Den mindre størrelsen på visningsvelgeren gjenspeiler også en lavere forventet frekvens for visningsskifte på disse sidene. 
 
Hvis du velger visningsnavnet, åpnes visningsvelgeren og viser listen over tilgjengelige visninger for siden.

**Versjon 10.0.21 eller senere:** Hvis funksjonen **Forbedret støtte for juridiske enheter for lagrede visninger** er aktivert, viser visningsvelgeren de tilgjengelige visningene i to deler. Den første delen viser alle visninger som gjelder for gjeldende juridiske enhet, og den andre viser visninger som er tilgjengelige for alle juridiske enheter. Den første delen er bare synlig hvis det finnes visninger for siden som er spesifikke for juridiske enheter.

- **Standardvisning** – **Standard**-visningen er standardvisningen av siden, der ingen tilpasninger er brukt.
- **Personlige visninger** – Visningene uten hengelås representerer dine personlige visninger. Dette er visninger som enten du har opprettet, eller som en administrator har gitt deg.
- **Låste visninger** – Noen visninger (for eksempel **Standard**-visningen og alle visninger som publiseres til din rolle) har et hengelåssymbol ved siden av seg i visningsvelgeren. Dette symbolet angir at du ikke kan redigere disse visningene. Endringer som gjenspeiler sidebruk, lagres imidlertid automatisk. Disse endringene omfatter endringer i bredden på en rutenettkolonne, og endringer i den utvidede eller skjulte tilstanden til en hurtigfane. Du kan imidlertid opprette en personlig visning basert på en låst visning ved hjelp av handlingen **Lagre som** hvis du har rettigheter til personalisering.
- **Nye visninger** – Publiserte visninger som ennå ikke er åpnet, har et gnistsymbol til venstre for visningsnavnet.

Hvis du vil bytte til en annen visning, åpner du først visningsvelgeren og velger deretter visningen du vil laste inn. 

## <a name="creating-and-modifying-views"></a>Opprette og endre visninger

I motsetning til tradisjonell tilpasning lagres ikke visninger automatisk når en bruker tilpasser siden, eller når en bruker bruker et filter på en liste eller sorterer den. Det kreves en eksplisitt handling for å lagre disse endringene i en visning. Dette kravet gir brukerne fleksibilitet til å opprette en visning før eller etter at endringene som er knyttet til denne visningen, er gjort. Det sikrer også at visningsdefinisjoner ikke endres utilsiktet av éngangsfiltre eller personlige tilpasninger. Legg merke til at vanlige sidebrukselementer (for eksempel kolonnebredder eller den utvidede eller sammenslåtte tilstanden til inndelinger) lagres automatisk i den gjeldende visningen, selv for låstse visninger.

For å sikre at gjeldende status for visningen er kjent, vises det en stjerne (\*) ved siden av gjeldende visningsnavn når du begynner å endre en visning ved å tilpasse eller filtrere den. Dette symbolet angir at du ser på en ulagret, endret versjon av denne visningen.

Hvis du vil lagre disse endringene, følger du disse trinnene.

1. Velg visningsnavnet for å åpne visningsvelgeren.
2. Velg **Lagre** for å endre den eksisterende visningen. Legg merke til at denne handlingen ikke er tilgjengelig for låste visninger. 
3. Slik oppretter du en ny visning:

    1. Velg **Lagre som**. 
    2. I ruten **Lagre visning som** angir du et navn og eventuelt en beskrivelse for visningen.
    3. Hvis du vil at denne visningen skal være standardvisningen, velger du **Bruk som standard**. Hvis du vil ha mer informasjon om standardvisninger, kan du se delen [Endre standardvisningen](#changing-the-default-view) som følger. 
    4. **Versjon 10.0.21 eller senere:** Hvis funksjonen **Forbedret støtte for juridiske enheter for lagrede visninger** er aktivert, kan du velge om du vil at denne visningen skal være tilgjengelig for alle juridiske enheter, eller bare et delsett av dem.
    5. Velg **Lagre**.

## <a name="changing-the-default-view"></a>Endre standardvisningen

Standardvisningen er visningen systemet prøver å åpne når du først åpner siden. Du bør angi standardvisningen til visningen som du forventer å bruke oftest. 

> [!NOTE]
> - I basisfunksjonen **Lagrede visninger** finnes det én enkelt, global standardvisning på tvers av juridiske enheter. Hvis du endrer standardvisningen, vil denne visningen åpnes som standard, uansett hvilken juridisk enhet du befinner deg i for øyeblikket.
> - **Versjon 10.0.21 eller senere:** Når funksjonen **Forbedret støtte for juridiske enheter for lagrede visninger** er aktivert, kan hver juridiske enhet ha sin egen standardvisning per side.

Følg disse trinnene for å endre standardvisningen for en side:

1. Bytt til visningen du bruker som standard. 
2. Velg visningsnavnet for å åpne visningsvelgeren. 
3. Velg **Merk** og deretter **Bruk som standard**.

Når du oppretter en ny visning (ved hjelp av **Lagre som**-handling), kan du gjøre denne nye visningen til standardvisning ved å velge **Bruk som standard**-valget før du lagrer visningen.

> [!WARNING]
> I noen tilfeller vil spørringen som er knyttet til standardvisningen, ikke kjøres første gang du åpner en side. Hvis du for eksempel åpner siden via en flis, blir flisens spørring kjørt uansett hvilken spørring som er knyttet til standardvisningen. Hvis du åpner en side som har en **Standard**-visning som allerede har en definert spørring, vil den opprinnelige spørringen kjøres i stedet for standardvisningens spørring. I dette tilfellet vil du motta en informasjonsmelding når visningen lastes inn. Hvis du bytter visning etter at siden er lastet, skal visningsspørringen kunne kjøres som forventet. I versjon 10.0.10 og senere vil informasjonsmeldingen du mottar, ha en innebygd handling som gir deg muligheten til å laste inn spørringen til standardvisningen direkte.

## <a name="managing-personal-views"></a>Behandle personlige visninger

Dialogboksen **Behandle mine visninger** gir deg grunnleggende vedlikeholdsfunksjoner for personlige visninger og rekkefølgen på visningene i visningsvelgeren. Hvis du vil åpne denne siden, velger du visningsnavnet for å åpne rullegardinmenyen, velger **Mer** og deretter **Behandle mine visninger**.

**Versjon 10.0.21 eller senere:** Hvis funksjonen **Forbedret støtte for juridiske enheter for lagrede visninger** er aktivert, viser delen **Mine visninger** i dialogboksen **Behandle mine visninger** de tilgjengelige visningene for siden i deler. Alle visninger som er spesifikke for gjeldende juridiske enhet, vises i sin egen del. Delen **Globale visninger** vises alltid, slik at du kan styre visningene som er tilgjengelige for siden, i alle juridiske enheter. 

Hvis du vil ha en liste over tilgjengelige visninger for denne siden, er følgende sett med handlinger tilgjengelige.

- **Endre standardvisning** – Bruk funksjonen **Bruk som standard** for å gjøre den merkede visningen til standardvisning for denne siden. Hvis funksjonen **Importer støtte for juridiske enheter for lagrede visninger** er aktivert, kan du i delen **Globale visninger** se standardvisningen for den gjeldende juridiske enheten eller for alle juridiske enheter.
- **Endre rekkefølgen på visningene** – Bruk handlingene **Flytt opp** og **Flytt ned** for å omorganisere visningene i en bestemt rekkefølge.
- **Gi en visning nytt navn** – Bruk **Gi nytt navn**-handlingen for å endre navnet på den valgte personlige visningen. Denne handlingen er deaktivert for låste visninger. 
- **Slette en visning** – Bruk **Slett**-handlingen for å slette gjeldende valgte visning fra siden permanent. Det er ikke mulig å gjenopprette en visning etter at du har fjernet den.

Endringer som gjøres i denne dialogboksen, vil tre i kraft når du har valgt **Oppdater**-knappen.

## <a name="managing-personalizations-at-an-organizational-level-with-views"></a>Administrere personlige tilpasninger på et organisasjonsnivå med visninger

For å hjelpe deg med å forstå hvordan lagrede visninger bidrar til å forbedre administrasjonen av personlige tilpasninger på et organisasjonsnivå, beskriver dette avsnittet noen forskjeller i administrasjon av personlige tilpasinger med og uten funksjonen **Lagrede visninger**.

Uten visninger vil administratorer bruke et sett med personlige tilpasninger på en side for en bruker eller en gruppe av brukere via personaliseringssiden. Hvis disse brukerne hadde tilpasningsrettigheter, ville de personlige tilpasningene gjelde for den siden. Det var imidlertid ikke mulig å hindre brukere i å tilpasse siden ytterligere, som betød at organisasjonen ikke kan sikre at brukerne har et konsekvent brukergrensesnitt. Hvis noen av disse brukerne ikke hadde tilpasningsrettigheter, ble ikke tilpasningene som ble gitt til dem av en administrator, lastet inn. Hvis nye brukere ble ansatt i en organisasjon, måtte administratorer manuelt laste inn et sett med personlige tilpasninger for brukeren. Det var ingen automatisk mekanisme for å angi at et bestemt sett med personlige tilpasninger skal være tilgjengelig for brukere i denne rollen.

Med funksjonen **Lagrede visninger** er organisasjonens administrasjon av tilpasninger mye enklere, primært fordi visninger kan publiseres til grupper av brukere. Når en visning er publisert, vil alle brukere som har en av de definerte sikkerhetsrollene, og som har tilgang til en av de angitte juridiske enhetene, kunne se og bruke visningen, selv om brukeren ikke har tilgang til tilpasning. Selv om hver bruker har en kopi av den publiserte visningen der sidebrukelementer brukes automatisk, kan ingen brukere lagre personlige tilpasninger eller spørringsoppdateringer til en publisert visning. Publiserte visninger er med andre ord låst. Hvis nye brukere blir tilordnet roller i juridiske enheter som visninger er publisert til, vil de automatisk se visningene som er knyttet til rollene og juridiske enheter. Ingen tilleggshandling kreves av administratoren. Hvis brukere endrer roller i en organisasjon eller får tilgang til ulike juridiske enheter, kan det hende at de ikke lenger får tilgang til visningene som tidligere ble publisert til dem. Her kreves det heller ingen tilleggshandling av administratoren.

Oppdateringer til en publisert visning kan lett distribueres til brukere ved å publisere visningen på nytt til de riktige sikkerhetsrollene og juridiske enhetene.

Publiseringsfunksjonen gjør det mulig for organisasjoner å definere standardvisninger som er optimalisert for deres virksomhet, som er målrettet til brukere i spesifikke sikkerhetsroller.

## <a name="publishing-views"></a>Publiseringsvisninger

Under publiseringsprosessen kan visninger tilordnes til én eller flere sikkerhetsroller for én eller flere juridiske enheter. Derfor har alle brukere som har tilgang til en juridisk enhet, og som er tilordnet til én av disse rollene, tilgang til og kan bruke visningene. Brukeren kan imidlertid ikke redigere visningene. Som standard har systemadministratorer tilgang til **Publiser**-handlingen i rullegardinmenyen for visningsvalg. Andre klarerte brukere i organisasjonen kan imidlertid også få tilgang til å vise publiseringen via den nye administratorrollen **Lagrede visninger**.

Hvis du vil publisere en visning, gjør du følgende:

1. Opprett og lagre en personlig kopi av visningen du vil publisere. 
2. Når den aktuelle visningen er lastet, velger du visningsnavnet for å åpne rullegardinmenyen for visningsvalg. 
3. Velg **Mer**-knappen, og velg deretter **Publiser**. Dialogboksen Publiser åpnes.
4. Angi et navn for visningen. Navnet du angir, er navnet som brukeren som mottar denne visningen, vil se i visningsvelgerne. Navnene på publiserte visninger for en side må være unike. Ingen like navn er tillatt, selv om listen over roller eller judiriske enheter som visningene brukes på, varierer.
5. **Oppdatering 10.0.17 eller nyere:** Hvis funksjonen **(Forhåndsversjon) Oversettelsesstøtte for organisasjonsvisninger** er aktivert, kan du legge til oversettelser for visningsnavnet på så mange språk som organisasjonen krever, ved å velge **Oversettelser**-knappen ved siden av **Navn**-feltet. Visningsnavnet vises deretter for brukere på det gjeldende språket deres. Du kan også angi standardspråket for å angi oversettelsen som skal vises for brukere som kjører språk som det ikke er definert noen oversettelse for.
5. Valgfritt: Angi en beskrivelse for visningen, slik at brukere som får denne visningen, bedre kan forstå formålet med den. 
6. Avgjør om visningen skal publiseres som standardvisning for de valgte brukerne. Når en visning blir gjort til standardvisning, ser brukerne den neste gang de åpner målsiden. Den enkle, globale standardvisningen for hver målbruker vil bli endret. Brukerne kan imidlertid fremdeles endre standardvisningen sin etter at publiseringen har skjedd.

    > [!NOTE]
    > Vær oppmerksom på følgende atferd når du publiserer en visning som standardvisning:
    >
    > - Hvis du publiserer en visning som standardvisning for noen eller alle juridiske enheter, skjer følgende:
    >
    >    - Hvis bare basisfunksjonen **Lagrede visninger** er aktivert, endres den enkelte, globale standardvisningen for hver målbruker. 
    >    - **Versjon 10.0.21 eller senere:** Hvis funksjonen **Forbedret støtte for juridiske enheter for lagrede visninger** er aktivert, og du publiserer visningen i et delsett av juridiske enheter, endres standardvisningen for disse juridiske enhetene for hver målbruker.
    >
    > - Hvis en bruker har roller der flere visninger publiseres som standardvisningen, brukes den siste visningen som ble publisert, som brukerens standardvisning. 

8. Legg til sikkerhetsrollene som samsvarer med brukerne som målrettes av denne visningen. 
9. Avgjør om du vil publisere visningen til de underordnede rollene for hver sikkerhetsrolle som er valgt. Hvis du gjør dette, merker du av for **Inkluder underordnede roller** i raden for de aktuelle sikkerhetsrollene. Vær oppmerksom på at denne avmerkings boksen ikke er tilgjengelig for roller som ikke har underordnede roller.
10. Legg til de juridiske enhetene som denne visningen skal være tilgjengelig for. 

    > [!NOTE]
    > Vær oppmerksom på følgende atferd hvis du publiserer en visning til en spesifikk juridisk enhet, men når du ikke publiserer denne visningen som standardvisning.
    >
    > - Hvis bare basisfunksjonen **Lagrede visninger** er aktivert, viser brukerens visningsvelger for siden først visningen bare for de angitte juridiske enhetene. Når visningen er lastet inn for første gang, vil visningsvelgeren for siden alltid vise den, uavhengig av den juridiske enheten.
    > - **Versjon 10.0.21 eller senere:** Hvis funksjonen **Forbedret støtte for juridiske enheter for lagrede visninger** er aktivert, viser visningsvelgeren kun visningen for de angitte juridiske enheten.

11. Velg **Publiser**.

Legg merke til at i noen miljøer kan det ta litt tid (opptil en time) før brukerne ser den publiserte visningen.

## <a name="modifying-a-published-view"></a>Endre en publisert visning

Når du har publisert en visning, kan det hende du vil endre den. Selv om du ikke kan foreta direkte endringer i en publisert visning, kan du publisere en visning på nytt for å oppdatere den, fordi disse visningene er låst for redigering for alle brukere (inkludert utgivere).

Hvis endringene du vil gjøre i en publisert visning, bare vil involvere publiseringsparameterne (navnet på og beskrivelsen av visningen eller sikkerhetsrollene som visningen er publisert til), gjør du følgende:

1. Bytt til visningen som er publisert for parameterne du vil oppdatere. 
2. Velg **Publiser på nytt** på rullegardinmenyen for visningsvelgeren. Hvis du bruker versjon 10.0.12 eller tidligere, må du velge **Publiser** og deretter **Ja** for å oppdatere den eksisterende visningen.
3. Oppdater navnet, beskrivelsen sikkerhetsrollene og de juridiske enhetene for visningen. 
4. Velg **Publiser**. Hvis du opprinnelig valgte denne publiserte visningen som standardvisning, vil den være standardvisning for brukerne på nytt etter at du har publisert den på nytt. 

Hvis endringene i den publiserte visningen omfatter endringer i tilpasningene eller filtrene som er knyttet til visningen, følger du denne fremgangsmåten.

1. Last inn den publiserte visningen du vil endre. 
2. Utfør de nødvendige endringene i det lokale utkastet.
3. Velg **Publiser på nytt** på rullegardinmenyen for visningsvelgeren.
4. Velg **Ja** for å angi at du vil publisere visningen sammen med endringene som ikke er lagret. 
5. Juster eventuelle publiseringsparametere som må justeres, og velg deretter **Publiser**. 

## <a name="managing-published-views"></a>Behandle publiserte visninger

I likhet med behandling av personlige visninger gir dialogboksen **Behandle mine visninger** brukere med publiseringsrettigheter grunnleggende vedlikeholdsfunksjoner for sidens publiserte visninger (i tillegg til sine egne personlige visninger). Hvis du vil åpne denne siden, velger du visningsnavnet for å åpne rullegardinmenyen, velger **Mer** og deretter **Behandle mine visninger**.

Selv om alle brukere har en **Mine visninger**-kategori som viser personlige visninger, har brukere med publiseringsrettigheter også en **Organisasjonsvisninger**-kategori, som viser alle publiserte og upubliserte visninger for siden. Fordi flere brukere kan publisere visninger, er det viktig at du kan administrere hele listen over publiserte visninger, selv om du ikke er brukeren som har publisert en gitt visning.

Hvis du vil ha en liste over alle publiserte visninger for siden, er følgende sett med handlinger tilgjengelige. 

- **Publiser på nytt** – Bruk handlingen **Publiser på nytt** til å publisere en visning på nytt etter at publiseringsparametere (navn, beskrivelse, sikkerhetsroller eller juridiske enheter) er endret.
- **Publiser** – Bruk **Publiser**-handlingen til å publisere en visning som for øyeblikket ikke er publisert. 
- **Opphev publisering** – Bruk handlingen **Opphev publisering** til å gjøre en visning inaktiv. Visningen vil fortsatt være tilgjengelig i systemet, men brukerne kan ikke se den i visningsvelgeren før visningen er publisert på nytt.
- **Lagre som personlig** – Bruk **Lagre som personlig**-handlingen til å opprette en personlig utkastkopi av den publiserte visningen. Denne funksjonen kan hjelpe deg å forstå innholdet i en visning som ikke ble publisert for deg, eller som ennå ikke er publisert. Du kan også bruke den til å redigere og publisere en visning på nytt.
- **Slett** – Bruk handlingen **Slett** til å slette en publisert eller upublisert visning permanent. Denne handlingen fjerner også visningen for alle brukere i systemet. Fjerning av publiserte visninger trer i kraft når **Lagre**-knappen er valgt. Når en visning er slettet, kan den ikke gjenopprettes. 

## <a name="managing-views-globally"></a>Behandle visninger globalt

Selv om enkelte administrasjonsfunksjoner vises på alle sidene, som angitt i dette emnet, kan **systemadministratorer** og **administratorer av lagrede visninger** behandle visninger mer holistisk for systemet via **Tilpasning**-siden. Denne siden har spesielt følgende inndelinger og funksjoner: 

- **Publiserte visninger** – i denne delen vises en liste over alle visninger som er publisert for organisasjonen. Herfra kan du publisere en visning på nytt etter at du har justert sikkerhetsrollene eller de juridiske enhetene som visningen målrettes mot. Du kan eksportere, slette eller oppheve publisering av disse visningene. Du kan bruke handlingen **Lagre som personlig** til å opprette en personlig kopi av en visning, slik at du kan oppdatere visningen eller få en bedre forståelse av innholdet. 
- **Upubliserte visninger** – Denne delen viser en liste over alle organisasjonsvisningene i systemet som for tiden ikke er publisert. Disse visningene kommer som oftest inn i systemet ved hjelp av importfunksjonen. Du kan publisere, eksportere eller slette disse visningene. **Hurtigpublisering**-handlingen som ble lagt til i versjon 10.0.12, gjør det mulig at flere visninger fra denne inndelingen kan publiseres i én handling, ved hjelp av de eksisterende konfigurasjonene for sikkerhetsrolle og juridisk enhet. Du kan bruke handlingen **Lagre som personlig** til å opprette personlige kopier av disse visningene, slik at du kan få en bedre forståelse av innholdet i dem.
- **Personlige visninger** – I denne delen ser du alle visningene som er opprettet av brukere i systemet. Her kan du publisere en personlig visning til organisasjonen eller kopiere én eller flere av disse visningene til andre brukere. Du kan også eksportere eller slette disse visningene etter behov.
- **Brukerinnstillinger** – Velg en bruker som skal vises, eller juster brukerens mulighet til å bruke tilpasning, enten for hele systemet eller for bestemte sider som brukeren har besøkt. Du kan vise og samhandle med brukerens tilpasninger i systemet. Du kan også slette alle tilpasninger for den aktuelle brukeren eller tilbakestille bildeforklaringer for funksjonen for brukeren. Hvis bildeforklaringer for funksjonen tilbakestilles, vil alle popup-vinduer som introduserte nye funksjoner, og som brukeren tidligere har lukket, vises igjen neste gang brukeren støter på disse funksjonene.
- **Systeminnstillinger** – Du kan midlertidig deaktivere tilpasninger for alle brukere i systemet. I dette tilfellet brukes ingen alle personlige tilpasninger for noen som helst bruker, og alle sidene tilbakestilles til standardtilstanden. Hvis du reaktiverer tilpasning senere, vil alle tilpasninger bli brukt på nytt. Du kan også permanent slette alle tilpasninger for alle brukere i systemet. Tilpasninger som er slettet, kan ikke gjenopprettes. Før du utfører denne oppgaven må du eksportere tilpasninger du kanskje vil bruke senere.

Brukere som har tilgang til siden **Tilpasning**, kan også importere personlige visninger eller organisasjonsvisninger ved hjelp av **Importer visninger**-knappen i handlingsruten. For organisasjonsvisninger kan du velge **Publiser umiddelbart** for å gjøre visningene tilgjengelige for brukere uten en eksplisitt publisering i tillegg.

## <a name="known-issues"></a>Kjente problemer

Hvis du vil ha en liste over kjente problemer med lagrede visninger, kan du se [Bygge skjemaer som benytter lagrede visninger fullt ut](../../dev-itpro/user-interface/understanding-saved-views.md).

## <a name="frequently-asked-questions"></a>Vanlige spørsmål

### <a name="how-do-i-enable-saved-views-in-my-environment"></a>Hvordan aktiverer jeg lagrede visninger i miljøet?

> [!NOTE]
> Funksjonen **Lagrede visninger** krever at tilpassingssystemet i Finance and Operations er aktivert. Hvis tilpassing er deaktivert for hele miljøet, vil visninger bli deaktivert selv om du følger fremgangsmåten nedenfor. 

Du kan aktivere og deaktivere funksjonen **Lagrede visninger** via Funksjonsbehandling i alle miljøer. Etter at den er aktivert, aktiveres lagrede visninger i alle påfølgende brukerøkter.

### <a name="what-happens-to-existing-personalizations-when-views-are-enabled"></a>Hva skjer med eksisterende personlige tilpasninger når visninger er aktivert? 

Når visninger aktiveres, blir eksisterende personlige tilpasninger for en bruker og et skjema lagret i en ny visning kalt **Min visning**, som automatisk blir angitt som standardvisning. Dette er ment å sikre en konsekvent brukeropplevelse før og etter at visningene er aktivert, bortsett fra at visningsvelgerkontrollen vises i skjemaer.

### <a name="what-pages-support-views"></a>Hvilke sider støtter visninger? 

Visninger er tilgjengelige på de fleste, men ikke alle sider. Spesifikt er visninger tilgjengelige for alle fullskjermsider, bortsett fra instrumentbord og arbeidsområder. Sider som ikke er i fullskjerm, som inkluderer dialogbokser, rullegardindialogbokser, oppslag, utvidede forhåndsvisninger, støtter for øyeblikket heller ikke visninger. Visningsstøtte for flere sidetyper, for eksempel arbeidsområder og dialogbokser, kan bli vurdert for en fremtidig oppdatering.

### <a name="who-is-allowed-to-publish-views"></a>Hvem kan publisere visninger?

Bare systemadministratorer og brukere som er tilordnet til administratorrollen **Lagrede visninger**, har rettigheter til å publisere visninger. 

### <a name="why-am-i-not-able-to-save-filters-with-this-view"></a>Hvorfor kan jeg ikke lagre filtre med denne visningen? 

Det kan være flere grunner til at et filter ikke ser ut til å lagres med en visning: 

- Det kan hende at siden ikke støtter lagring av filtre som en del av visningsdefinisjonen. Vær oppmerksom på at bare sider med store visningsvelgere gjør det mulig å lagre endringer som en visning. Se delen **Bytte visninger** for mer informasjon. 
- Den aktuelle siden støtter kanskje ikke visninger på riktig måte, siden den kan ignorere visningsspørringen fullstendig eller operere på en midlertidig tabell med data som ikke er vedvarende. 

### <a name="what-data-will-i-see-when-i-visit-a-page"></a>Hvilke data får jeg se når jeg besøker en side?

For sider med små visningsvelgere (bare personlige tilpasninger kan lagres i visningen) vil du se de samme dataene som du alltid har når du besøker siden. 

For sider med store visningsvelgere (både personlige tilpasninger og spørringer kan lagres i visningen) vil du vanligvis se dataene som er knyttet til spørringen som er forbundet med standardvisningen. Det finnes to hovedunntak:

- Hvis du navigerer til en side fra en flis, vil flisspørring utføres uansett hvilken spørring som er knyttet til standardvisningen. Hvis du opprettet denne flisen etter at visninger var aktivert, vil valg av en flis åpne siden med visningen som er knyttet til flisen.
- Hvis du navigerer til en side, og det inngangspunktet inkluderer en spørring, vil den opprinnelige spørringen utføres opprinnelig i stedet for standardvisningens spørring. Når dette skjer, skal di bli varslet av en informasjonsmelding når visningen lastes inn. Du kan også bekrefte ved å bytte til denne visningen etter at siden er lastet inn, som gjør at visningsspørringen kan kjøres uansett.

### <a name="why-is-a-view-that-was-published-for-a-specific-legal-entity-visible-in-all-legal-entities"></a>Hvorfor er en visning som er publisert for en bestemt juridisk enhet, synlig i alle juridiske enheter?

Hvis du publiserer en visning til en spesifikk juridisk enhet, men når du ikke publiserer denne visningen som standardvisning, inntreffer følgende atferd:

- Hvis bare basisfunksjonen **Lagrede visninger** er aktivert, viser brukerens visningsvelger for siden først visningen bare for de angitte juridiske enhetene. Når visningen er lastet inn for første gang, vil visningsvelgeren for siden alltid vise den, uavhengig av den juridiske enheten. Dette skjer fordi brukere får sin egen personlige kopi av den publiserte visningen når den lastes inn, og personlige visninger er globale.
- **Versjon 10.0.21 eller senere:** Hvis funksjonen **Forbedret støtte for juridiske enheter for lagrede visninger** er aktivert, viser visningsvelgeren kun visningen for de angitte juridiske enheten. Dette skjer fordi funksjonen gjør det mulig å koble visninger (inkludert personlige visninger) til bestemte juridiske enheter.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
