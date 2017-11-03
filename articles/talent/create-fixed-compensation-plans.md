---
title: Opprette faste kompensasjonsplaner
description: "Fast kompensasjon refererer til en ansatts vanlige bruttolønn eller lønn. Denne artikkelen beskriver komponentene som må defineres før du kan opprette en fast kompensasjonsplan og registrere ansatte."
author: kherr75
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: HRCCompGrid, HRCCompRefPointSetup, HRMCompEligibility, HRMCompEvent, HRMFixedCompPlanTable
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations
ms.custom: 15991
ms.assetid: ef8cf992-176c-4c98-9dff-6510e1eb9f1c
ms.search.region: Global
ms.author: kherr75
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 399e1fee592c0ab31015e37e87d41c71f9282858
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---

# <a name="create-fixed-compensation-plans"></a>Opprette faste kompensasjonsplaner

[!include[banner](includes/banner.md)]


Fast kompensasjon refererer til en ansatts vanlige bruttolønn eller lønn. Dette emnet beskriver komponentene som må defineres før du kan opprette en fast kompensasjonsplan og registrere ansatte.

Beløp for fast kompensasjon kan beregnes for de ansatte basert på ulike faktorer, for eksempel ytelse, område og budsjettøkninger. Microsoft Talent støtter kompensasjon av typene trinn, klasse og segment.

## <a name="fixed-compensation-components"></a>Komponenter i fast kompensasjon
### <a name="compensation-levels"></a>Kompensasjonsnivåer

Du kan bruke **Kompensasjonsnivåer** til å angi kompensasjon for ulike jobber, for å bidra til å sikre at de ansatte som har disse jobbene, blir rettferdig betalt. På siden **Kompensasjonsnivåer** kan du angi kompensasjonsnivåer som er nødvendig for hver trinn-, klasse- og segmentplan. Bruk knappene **Opp** og **Ned** til å plassere nivåene i riktig rekkefølge i henhold til typen. Når du angir kompensasjonsnivåer for en jobb, er du med på å garantere at alle ansatte som har en stilling med denne jobben, får betalt på samme nivå.

### <a name="reference-points"></a>Referansepunkt

**Referansepunkt** er kolonnene i rutenettet som definerer kompensasjonsområdene for hvert nivå. Kompensasjonsnivået er raden i rutenettet. Vanlige referansepunkt for en plan av typen klasse er minimum, midtpunkt og maksimum. Du oppretter referansepunkt på siden **Referansepunktoppsett**.

### <a name="compensation-grids"></a>Kompensasjonsrutenett

Når du definerer nivåene og referansepunktene, kan de kombineres slik at de danner et **kompensasjonsrutenett**. På siden **Kompensasjonsrutenett** definerer du informasjon om rutenettet. Angi for eksempel hva rutenettet skal brukes til, hvilken type plan det skal brukes med, og hvilke referansepunkt eller kolonner som kreves i rutenettet. Når du er ferdig med å registrere denne informasjonen, klikker du **Kompensasjonsstruktur** for å legge til nivåer og beløp i rutenettet. 

**Tips!** Bruk **Masseendring**-funksjonen på kompensasjonsstrukturen for å angi startbeløp, og øk dem deretter med prosent eller beløp over alle nivåene eller referansepunktene.

### <a name="pay-frequencies"></a>Lønnsfrekvenser

**Lønnsfrekvenser** brukes til å definere hvordan en ansatts lønn angis (for eksempel NOK 100 per time og NOK 500 000 per år), og konverteringen mellom de timebaserte, ukentlige, månedlige (12 måneder) og årlige satsene. La oss si at et firma som bruker en 38-timers arbeidsuke for sine timebaserte ansatte, definerer en lønnsfrekvens som har en timesats på 1, en ukentlig sats på 38, en månedlig sats på 164,6666666667 og en årlig sats på 1 976. Konverteringene brukes til å beregne de ulike lønnssatsene som vises på en ansatts post for fast kompensasjon.

## <a name="fixed-compensation-plans"></a>Faste kompensasjonsplaner
Du kan utforme den faste kompensasjonsplanen slik at alle komponentene du har konfigurert, kombineres. Du kan opprette en fast kompensasjonsplan ved å åpne siden **Faste kompensasjonsplaner**. Her kan du gi planen et navn og en beskrivelse, velge hvilken type plan det er (trinn, klasse eller segment), velge lønnsfrekvensen du vil bruke for den ansattes lønnssats (beløp per time, beløp per år og så videre), og angi enkelte alternativer som kontrollerer hvordan kompensasjon behandles. 

Du kan bruke innstillingen **Utenfor område-toleranse** til å angi hvor strengt du vil sikre at kompensasjonsbeløp er mellom minimums- og maksimumsbeløpene. En **hard** toleranse krever at kompensasjon må være innenfor området som er definert for et gitt nivå. En **myk** toleranse varsler deg når kompensasjonsbeløpet er utenfor området, men lar deg fortsette. Hvis du setter toleransen til **Ingen**, kan du angi ønsket kompensasjonsbeløp for en ansatt uten å få advarsler eller feilmeldinger. 

Innstillingen for **Ansettelsesregel** lar deg angi om alle de ansatte skal få den samme økningen, uavhengig av ansettelsesdatoen (**Ansettelsesregel** = **Ingen**), eller om ansatte skal få en prosent av belønningen, basert på hvor lenge de var ansatt i syklusen (**Ansettelsesregel** = **Prosent**). 

En **områdeutnyttelsesmatrise** er nyttig hvis du ønsker å redusere tiden det tar for ansatte å nå midtpunktet i området, eller å øke tiden det tar for ansatte å nå det største referansepunktet i området. La oss si at du vil gi ansatte som er i de nederste 25 prosentene av området, 110 prosent av målbelønningen deres, men vil gi ansatte som er i de øverste 25 prosentene av området, bare 80 prosent av målbelønningen, for å unngå at de når maksimumet så raskt. 

Når du har definert alt det grunnleggende i den faste kompensasjonsplanen, kan du definere en kompensasjonsstruktur for planen. Klikk **Angi kompensasjon**. En dialogboks med en glidebryter åpnes og inneholder tre alternativer:

-   Opprett et nytt kompensasjonsrutenett ved å velge et referansepunktoppsett og gi rutenettet et navn.
-   Opprett et nytt kompensasjonsrutenett ved å kopiere et eksisterende rutenett du kan bruke som utgangspunkt.
-   Bruk et eksisterende kompensasjonsrutenett som allerede er definert. Alle kompensasjonsplaner som bruker samme rutenett, oppdateres hvis dette rutenettet endres.

Når du har valgt et alternativ, åpnes siden **Kompensasjonsstruktur**, og du kan gjøre endringer i det nye eller det eksisterende kompensasjonsrutenettet.

## <a name="fixed-compensation-enrollment"></a>Fast kompensasjonsregistrering
### <a name="determine-who-is-eligible-for-the-plan"></a>Avgjøre hvem som har rett til planen

Det første trinnet i registreringen av ansatte i en fast kompensasjonsplan, er å avgjøre hvem som har rett til kompensasjonen som er definert i planen. Du kan ikke tilordne planen til ansatte før du har avgjort hvem som er berettiget. Du definerer berettigelse ved å åpne siden **Rettighetsregler**. Her oppretter du en ny rettighetsregel for kompensasjonsplanen og definerer vilkårene som en ansatt må oppfylle for å ha rett til en plan. Du kan begrense rettighet basert på avdeling, fagforening, kompensasjonsområde (lokasjon), jobb, jobbfunksjon, jobbtype og/eller kompensasjonsnivå. Ansatte kan registreres i en kompensasjonsplan bare hvis de oppfyller alle betingelsene som er angitt i rettighetsregelen. 

**Obs!** Rettighetsregler brukes til å fastsette berettigelse for både faste og variable kompensasjonsplaner. 

Rettighetsregelen vurderer verdien i bestemte felt i postene Jobb, Stilling og Ansatt til å avgjøre om en ansatt har rett til en kompensasjonsplan:

-   Rettighetsregelen vurderer følgende felt på **Jobb**-siden:
    -   **Jobb**-feltet
    -   Feltene **Funksjon** og **Jobbtype** i fanen **Jobbklassifisering**
    -   **Nivå**-feltet i **Kompensasjon**-fanen
-   På **Stillinger**-siden vurderer rettighetsregelen feltene **Avdeling** og **Kompensasjonsområde**.

Rettighetsregelen vurderer også fagforeninger som er knyttet til den ansatte (Klikk **Personlige opplysninger** &gt; **Fagforeninger** i **Arbeider**-fanen på **Ansatte**-siden).

### <a name="define-fixed-compensation-actions"></a>Definere handlinger for fast kompensasjon

**Handlinger for fast kompensasjon** brukes når du angir eller bruker endringer på en fast kompensasjon for en ansatt. Handlinger for fast kompensasjon lar deg bruke beskrivende navn på handlingstypene en kompensasjons- og fordelsansvarlig kan utføre. Ulike handlingstyper er basert på en spesiell logikk, slik at de kan brukes til ulike tider. 

Når den faste kompensasjonen er definert for en ansatt, kan bare handlinger av typen **Ansette / ansette på nytt** brukes. I dette tilfellet vil du kanskje opprette tre ulike handlinger for typen **Ansette / ansette på nytt** og kalle dem **Ansett**, **Ansett på nytt** og **Overfør**. Dermed har du en mer beskrivende forklaring på hvorfor den faste kompensasjonen ble gitt til en ansatt eller endret.

### <a name="enroll-the-employee"></a>Registrere den ansatte

Nå kan du tilordne en ansatt til en fast kompensasjonsplan. Åpne **Ansatte**-siden, og velg den ansatte du vil registrere i kompensasjonsplanen. I handlingsruten klikker du **Kompensasjon** &gt; **Fast plan**. Nå kan du opprette en ny handling for fast kompensasjon. for den ansatte. 

**Obs!** Feltet for kompensasjonsplan viser bare planene som en ansatt har rett til i henhold til rettighetsreglene som ble definert for hver plan. Hvis ingen rettighetsregel er definert for en plan, har ingen ansatte rett til denne planen. 

Systemet kontrollerer at kompensasjonsbeløpet som er angitt for en kompensasjonsplan av typen klasse eller segment, er innenfor de minste og største referansepunktene for gitt kompensasjonsnivå i den ansattes jobb. Hvis kompensasjonsbeløpet er utenfor tillatt område, vises en advarsel eller feilmelding, avhengig av toleransenivået som er angitt i den faste kompensasjonsplanen.

<a name="see-also"></a>Se også
--------

[Kompensasjonsplaner](compensation-plans.md)




