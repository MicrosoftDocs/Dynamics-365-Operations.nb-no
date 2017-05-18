---
title: Operations-ressurser
description: "Operasjonsressurser utfører aktivitetene for et prosjekt eller en produksjonsprosess. De kan være av forskjellige typer og kan ha forskjellige funksjoner."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: WrkCtrCapability
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 61943
ms.assetid: a3847f07-fca4-4140-a26f-d83c6ac68dde
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 53700246fb072c4d9afb2e475ae27892700a078a
ms.contentlocale: nb-no
ms.lasthandoff: 04/25/2017


---

# <a name="operations-resources"></a>Operations-ressurser

[!include[banner](../includes/banner.md)]


Operasjonsressurser utfører aktivitetene for et prosjekt eller en produksjonsprosess. De kan være av forskjellige typer og kan ha forskjellige funksjoner. 

<a name="operations-resources"></a>Operations-ressurser
--------------------

Operasjonsressurser er maskiner, verktøy, ansatte, lokaler, fysiske områder eller leverandører som utfører aktivitetene for et prosjekt eller en produksjonsprosess. De kan være av forskjellige typer og kan ha forskjellige funksjoner.

-   **Leverandør** – En ekstern ressurs som utfører prosjektaktiviteter eller produksjonsoperasjoner. Et eksempel er en underleverandør. Ved å koble leverandørressurser til en leverandørkonto kan du generere innkjøp fra underleverandører, basert på linjene i stykklisten eller produksjonslinjer.
-   **Personale** – En prosjekt- eller produksjonsarbeider som utfører en aktivitet, enten alene eller som en operatør for et verktøy eller en maskin. Hvis du bruker Personale-funksjonaliteten, kan du koble personale til en arbeider. Planleggingsmotoren kan deretter tildele ressursene, basert på kompetansene som er definert for den tilsvarende arbeideren.
-   **Maskin** – En maskin eller annet produksjonsutstyr som kreves i produksjonen.
-   **Verktøy** – Et dokument eller en enhet som vanligvis brukes sammen med en annen ressurs for å utføre en aktivitet i et prosjekt eller i produksjon.
-   **Lokasjonen** – En fysisk plassering av en bestemt størrelse som kreves for å utføre en aktivitet. Et eksempel er et monteringsverksted.
-   **Fasilitet** – En bygging eller fast struktur som kreves for å utføre en aktivitet.

## <a name="calendars"></a>Kalendere
En kalender kan tilordnes til en operasjonsressurs, og beskriver kapasiteten (i timer) for ressursen. Arbeidstider for ressursen operasjoner, avhenger av kalenderen som er tilordnet ressursgruppen som ressursen operasjoner er en del av. Du kan angi en ikrafttredelsesdato og utløpsdato for kalenderen som er tilordnet. Deretter kan du tilordne mer enn én kalender til en operasjonsressurs. Datoene for de tilordnede kalenderne kan imidlertid ikke overlappe, og operasjonsressursen kan bare tilordnes én kalender samtidig. **Obs!** Hvis det ikke finnes gjeldende arbeidskalendere for en ressursgruppe, hvis for eksempel den siste eller eneste tilordnede kalenderen er utløpt, har du ikke lenger tilgang til operasjonsressursene som er tilordnet ressursgruppen for produksjonsplanlegging og grovplanlegging. Du kan også tilordne en kalender til en ressursgruppe for å angi arbeidstidene for både ressursgruppen og alle operasjonsressursene som er tilordnet ressursgruppen. Kapasiteten for ressursgruppen beregnes som summen av kapasitetene for hver operasjonsressurs som er tilordnet denne ressursgruppen. Kalenderen som er tilordnet en ressursgruppe, kan endres over tid.

## <a name="resource-capabilities"></a>Ressursfunksjoner
En funksjon er muligheten for en operasjonsressurs til å utføre en bestemt aktivitet. Deretter kan du tilordne én eller funksjoner til en operasjonsressurs. Planleggingsmotoren tildeler deretter ressurser ved å sammenligne ressurskravene for hver aktivitet med egenskapene til de tilgjengelige operasjonsressursene. Funksjoner som kan tilordnes til alle typer operasjonsressurser (**Verktøy**, **Leverandør**, **Maskin**, **Personale**, **Lokasjon** eller **Lokaler**). Du kan tilordne funksjoner til operasjonsressurser i en begrenset tid ved å definere en startdato og utløpsdato for funksjonstilordningen. Hvis du vil ha mer informasjon, se [Ressursfunksjoner](resource-capabilities.md).

## <a name="resource-groups"></a>Ressursgrupper
En ressursgruppe er et sett med operasjonsressurser som representerer kornetheten du vil planlegge ressurser ved når du bruker metoden for grovplanlegging. Ressursgrupper tilsvarer derfor vanligvis den fysiske organiseringen av arbeidsceller, definert av gule linjer på produksjon-Shop Floor. Ressursgruppen definerer området, produksjonsenheten og lagerkonteksten for operasjonsressurser som er tilordnet gruppen. Når du tilordner en operasjonsressurs til en ressursgruppe, kan ressursen planlegges på området der ressursgruppen finnes. Du trenger ikke å tilordne operasjonsressursene som du oppretter til en ressursgruppe. En operasjonsressurs må imidlertid tilordnes til en ressursgruppe før den kan planlegges til å utføre arbeidet. En operasjonsressurs kan tilordnes en ressursgruppe for en begrenset periode. Du kan også tilordne en operasjonsressurs til flere ressursgrupper, slik at du deretter kan dele ressursen på tvers av områder. Gyldige datoer og utløpsdatoer kan imidlertid ikke overlappe. Du kan altså ikke tilordne en operasjonsressurs til forskjellige ressursgrupper samtidig. Endringer i ressursgruppetildelinger påvirker bare nye ressurstildelinger. Kapasitetsreservasjoner for jobber, operasjoner og timeprognoser i prosjekt som allerede er planlagt, påvirkes ikke. **Obs!** Når du tilordner operasjonsressurser av typen **Leverandør** til en ressursgruppe, må alle operasjonsressurser som er tilordnet denne ressursgruppen, være av typen **Leverandør** og må være koblet til samme leverandørkonto.

## <a name="production-units"></a>Produksjonsenheter
En produksjonsenhet er en administrativ enhet som er en samling av ressursgrupper. En produksjonsenhet kan inneholde flere ressursgrupper, men en ressursgruppe kan bare være tilordnet til én produksjonsenhet. En produksjonsenhet gjenspeiler det fysiske oppsettet av produksjonsressursene og har ingen virkning på transaksjoner eller hvordan de blir behandlet. Du må knytte en produksjonsenhet til et område. Du kan også tilordne et plukklager og et oppbevaringslager til en produksjonsenhet. Du kan bruke en produksjonsenhet til å konsolidere og filtrere produksjonsrelaterte data. En shop floor-leder kan for eksempel vise en oversikt over gjenværende arbeidsmengde og tilgjengelig kapasitet for en bestemt produksjonsenhet. Du kan endre produksjonsenheten som er tilordnet en ressursgruppe. Du kan også slette en produksjonsenhet. Disse endringene i produksjonsenheten virker imidlertid bare for nye ordrer som er opprettet etter at hovedplanleggingen er kjørt. Hvis du vil bruke endringene i produksjonsenheten på eksisterende ordrer, må du gjøre det manuelt.

## <a name="resource-scheduling"></a>Ressursplanlegging
Operasjonsressurser tildeles aktiviteter når et prosjekt eller en produksjon planlegges. Det finnes to planleggingsmetoder: grovplanlegging og finplanlegging. Når du bruker grovplanlegging, planlegges hver operasjon eller prosjektaktivitet for ressursgruppen som inneholder operasjonsressurser som samsvarer med ressurskravene som er angitt for operasjonen. Hvis en bestemt operasjonsressurs er nødvendig for operasjonen, reserveres bare kapasitet på en bestemt operasjonsressurs i gruppen. Finplanlegging er en mer detaljert type planlegging enn grovplanlegging. Finplanlegging deler hver operasjon inn i individuelle oppgaver eller jobber. Disse jobbene tilordnes deretter til operasjonsressursene som skal utføre dem. Planlegging reserverer kapasitet i ressursgrupper, basert på operasjonstidene som er definert i produksjonsruten eller prosjektaktivitetene. Hvis du arbeider med begrenset kapasitet, avhenger tidsplanen av tilgjengeligheten av operasjonsressursene som kreves for å fullføre aktiviteten. For grovplanlegging er kapasiteten til ressursgruppen summen av tilgjengelig kapasitet i operasjonsressursene som er en del av denne gruppen. Kapasitetsreserveringer som allerede finnes for operasjonsressursene, regnes som utilgjengelig kapasitet. Hvis det ikke er nok tilgjengelig kapasitet for produksjonen, kan produksjonsordrer bli forsinket eller stoppet. På **Ressurser**-siden kan du definere flere egenskaper som styrer hvordan kapasitetsreserveringer gjøres:

-   **Kapasitet** – angi operasjonsressursens kapasitet per time når det gjelder måleenhet for kapasitet.
-   **Bunkekapasitet** – angi det maksimale antallet stykker som operasjonsressursen kan behandle per kjøring.
-   **Effektivitetsprosent** – Angi effektiviteten som du forventer fra operasjonsressursen. Effektivitetsprosenten justerer produksjonen for operasjonsressursen, og påvirker tiden som er reservert for ressursen. Leveringstider for operasjoner som bruker operasjonsressursen, blir også justert i henhold til dette. Følgende formel brukes ved beregningen: Planleggingstid = tid x 100 ÷ effektivitetsprosenten. I denne formelen inneholder *tid* både kjøretiden og oppstillingstiden.
-   **Grovplanleggingsprosent** – Angi maksimumsprosenten av kapasiteten til operasjonsressursen du vil bruke til grovplanlegging. Denne må være mindre enn 100 prosent for å tillate fleksibilitet i kapasiteten ved finplanlegging.
-   **Begrenset kapasitet** – Sett dette alternativet til **Ja** hvis operasjonsressursen skal planlegges på grunnlag av faktisk kapasitet som er tilgjengelig, og hvis eksisterende kapasitetsreservasjoner skal anses. Hvis dette alternativet er satt til **Nei**, antas operasjonsressursen å ha ubegrenset kapasitet, og ressursen kan derfor være overbestilt.
-   **Begrenset egenskap** – Sett dette alternativet til **Ja** hvis du vil at operasjonsressursen skal planlegges basert på den faktiske kapasiteten som er tilgjengelig med hensyn til nødvendige egenskaper for planlegging av driftstider.
-   **Eksklusiv** – Sett dette alternativet til **Ja** hvis du ikke vil at operasjonsressursen skal være tilgjengelig for en annen jobb eller operasjon til gjeldende produksjon er fullført. I dette tilfellet kan ikke operasjonsressursen brukes, selv om det er huller i kjøretiden for ressursen.
-   **Flaskehalsressurs** – Definer operasjonsressursenen som en flaskehalsressurs. En flaskehalsressurs planlegges ved å bruke begrenset kapasitet når alternativene **Begrenset kapasitet** og **Flaskehalsplanlegging** er valgt på **Hovedplaner**-siden.

Hvis du vil planlegge flere operasjonsressurser for utføring samtidig, for eksempel en operasjon i produksjon, må du angi kravene for de ulike ressursene ved hjelp av primære og sekundære operasjoner. Deretter kan du også reservere flere operasjonsressurser som har en annen kapasitet. Operasjonsressursen som er planlagt for den primære operasjonen, bestemmer varigheten til aktiviteten.

## <a name="lean-work-cells"></a>Lean-arbeidscellearbeidsceller
Du kan angi at en ressursgruppe er en lean-arbeidscelle. Ressursgruppen kan deretter være en del av en produksjonsflyt. Ved å angi en ressursgruppe som en lean-arbeidscelle kan du også forhindre at ressursgruppen og de tilordnede operasjonsressursene blir tildelt operasjonene til en produksjonsordre eller en prosjekttimeprognose. For hver ressursgruppe som fungerer som en lean-arbeidscelle, må du angi følgende informasjon:

-   **Kalender** – Arbeidskalenderen for arbeidscellen, som må ha egenskapen for en standard arbeidsdag.
-   **Innleveringslager og -lokasjon** – Standardplasseringen som brukes til å plukke materiale for en aktivitet.
-   **Utleveringslager og -lokasjon** – Standardplasseringen der alle utdata for arbeidscellen er plassert.
-   **Kostnadskategori for kjøretid** – Denne kategorien må være definert for arbeidscellen hvis direkte arbeid skal spores i etterkalkulering.

Når en ressursgruppe brukes som en lean-arbeidscelle, er kapasiteten for arbeidscellen angitt direkte i ressursgruppen. Du trenger derfor ikke å tilordne operasjonsressursene til ressursgruppen. Bare når arbeidscellen administreres av en underleverandør, må en operasjonsressurs av typen **Leverandør** være tilordnet til arbeidscellen. Hvis du tildeler en operasjonsressurs til en ressursgruppe som er merket som en arbeidscelle, påvirkes ikke kapasiteten for arbeidscellen.

## <a name="costing-resources"></a>Etterkalkuleringsressurser
Når du definerer en aktivitet, for eksempel en ruteoperasjon eller en prosjekttimeprognose, kan du angi behovet for en bestemt operasjonsressurs eller ressursgruppe. Du kan imidlertid også angi behovet for en operasjonsressurs av en bestemt type, eller en operasjonsressurs som har en bestemt funksjon eller kompetanse. Derfor gjøres ikke den faktiske ressurstildelingen før aktiviteten er planlagt og kapasiteten er reservert. I en ruteoperasjon kan du derfor angi at estimering og stykklisteberegning må være basert på en bestemt operasjonsressurs. Det refereres til denne operasjonsressursen som etterkalkuleringsressursen. Du kan også overføre kostnadskategoriene og operasjonstider fra etterkalkuleringsressursen til aktiviteten. Når operasjonen er planlagt, utføres anslag og stykklisteberegning ved hjel av operasjonsressursen som faktisk er planlagt.




