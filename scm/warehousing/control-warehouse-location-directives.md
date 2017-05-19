---
title: Kontrollere lagerarbeid ved hjelp av arbeidsmaler og lokasjonsdirektiver
description: "Denne artikkelen beskriver hvordan du bruker arbeidsmaler og lokasjonsdirektiver for å bestemme hvordan og hvor arbeid utføres i lageret."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: WHSLocDirFailure, WHSLocDirHint, WHSLocDirTable, WHSLocDirTableUOM, WHSRFMenuItem, WHSWork, WHSWorkClass, WHSWorkPool, WHSWorkTemplateTable
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 72921
ms.assetid: 377ab8af-5b0c-4b5e-a387-06ac1e1820c0
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: e90741b9151f19c70923685fdf1edb2552296a08
ms.contentlocale: nb-no
ms.lasthandoff: 04/25/2017


---

# <a name="control-warehouse-work-by-using-work-templates-and-location-directives"></a>Kontrollere lagerarbeid ved hjelp av arbeidsmaler og lokasjonsdirektiver

[!include[banner](../includes/banner.md)]


Denne artikkelen beskriver hvordan du bruker arbeidsmaler og lokasjonsdirektiver for å bestemme hvordan og hvor arbeid utføres i lageret.

Instruksjonene som lagermedarbeidere mottar på en mobil enhet, bestemmes av arbeidsmalene som du definerer i Microsoft Dynamics 365 for Operations for å definere de ulike lagerprosesser og -oppgaver. Arbeidsmaler avgjør hvordan arbeidet skal utføres for hver lagerprosess. Ved å koble et lokasjonsdirektiv til arbeidsmaler kan du bidra til å garantere at arbeid skjer i bestemte fysiske områder på lagrene.

## <a name="work-templates"></a>Arbeidsmaler
Siden **Arbeidsmaler** lar deg definere arbeidsoperasjoner som må utføres på lageret. Vanligvis består lageroperasjoner av to handlinger: en lagerarbeider plukker opp beholdning på en lokasjon og plasserer den plukkede beholdningen på en annen lokasjon. 

Arbeidsmaler består av et hode og tilhørende linjer. Hver arbeidsmal gjelder en bestemt *arbeidsordretype*. Mange arbeidsordretyper assosieres med kildedokumenter, for eksempel bestillinger eller salgsordrer. Imidlertid representerer andre arbeidsordretyper egne lagerprosesser, for eksempel syklustelling. *Arbeidspulje-ID* gir deg muligheten til å organisere arbeidet i grupper. 

Innstillingene i arbeidshodedefinisjonen kan brukes til å bestemme når et nytt stykke arbeid skal opprettes. Du kan for eksempel angi et maksimalt antall plukklinjer og maksimalt forventet plukktid. Deretter, hvis arbeidet for en salgsordreplukkingsprosess overskrider en av disse verdiene, deles dette arbeidet inn i to stykker arbeid. 

Arbeidslinjene representerer de fysiske oppgavene som kreves for å behandle arbeidet. For eksempel for en prosess for utgående lager, kan det være en arbeidslinje for å plukke opp varene i lageret og en annen linje for å plassere disse varene i et oppsamlingsområde. Det kan deretter være en ekstra linje for å plukke varene fra oppsamling og en annen linje for å plassere varene i en lastebil som en del av lastingsprosessen. Du kan angi en *direktivkode *på arbeidsmallinjene. En direktivkode er koblet til et lokasjonsdirektiv, og bidrar derfor til å sikre at lagerarbeidet blir behandlet på riktig lokasjon i lageret. 

Du kan definere en spørring til å kontrollere når en bestemt arbeidsmal brukes. Du kan for eksempel angi en begrensning slik at en bestemt mal kan brukes for arbeid bare i et bestemt lager. Du kan også ha flere maler som brukes til å opprette arbeid for utgående ordrebehandling, avhengig av salgsopprinnelsen. Systemet bruker **Serienummer**-feltet for å bestemme rekkefølgen som de tilgjengelig arbeidsmalene vurderes i. Hvis du har en bestemt spørring etter en bestemt arbeidsmal, bør du derfor gi den et lavt sekvensnummer. Denne spørringen vil deretter bli evaluert før andre, mer generelle spørringer. 

Hvis du vil stoppe eller pause en arbeidsprosess, kan du bruke innstillingen **Stopp arbeid** for arbeidslinjen. I så fall vil arbeideren som utfører arbeidet, ikke bli bedt om å utføre neste arbeidslinjetrinn. For å flytte til neste trinn må denne arbeideren eller en annen arbeider velge arbeidet på nytt. Du kan også skille oppgavene i et stykke arbeid ved å bruke en annen *arbeidsklasse-ID *på arbeidsmallinjene.

## <a name="location-directives"></a>Lokasjonsdirektiver
Lokasjonsdirektiver er regler som bidrar til å identifisere plukke- og plasseringslokasjoner for lagerbevegelse. I en salgsordretransaksjon bestemmer for eksempel et lokasjonsdirektiv hvor varene blir plukket og hvor de plukkede varene skal plasseres. Lokasjonsdirektiver består av et hode og tilknyttede linjer, og du oppretter dem på siden **Lokasjonsdirektiver**. 

I hodet må hvert lokasjonsdirektiv må være knyttet til en *arbeidsordretype *som angir typen lagertransaksjon som direktivet som skal brukes for, for eksempel salgsordrer, etterfylling eller råvareplukking. *Arbeidstypen *angir om lokasjonsdirektivet skal brukes for å plukke eller plassere arbeid eller en annen lagerprosess, for eksempel telle eller lagerstatusendringer. Du må også angi et *område *og et *lager*. En *direktivkode *som du angir i hodet, kan brukes til å koble lokasjonsdirektivet til én eller flere maler for arbeid. 

Som for arbeidsmaler kan du definere en spørring for å bestemme når et bestemt lokasjonsdirektiv skal brukes. Du kan for eksempel angi at når e-handel er opprinnelsen til en salgsordre, må beholdning plukkes fra et dedikert område i lageret. Systemet bruker **Serienummer**-feltet for å bestemme rekkefølgen som de tilgjengelig lokasjonsdirektivene vurderes i. 

Lokasjonsdirektivlinjene setter tilleggsbegrensninger på bruken av reglene for lokasjonssøk. Du kan angi et minimums- og maksimumsantall som direktivet skal gjelde for, og du kan angi at direktivet skal være for en bestemt lagerenhet. Hvis måleenheten for eksempel er paller, kan varer på paller plasseres på en bestemt lokasjon. Du kan også angi om antallet kan deles på tvers av flere lokasjoner. Som lokasjonsdirektivhodet har hver lokasjonsdirektivlinje et sekvensnummer som bestemmer rekkefølgen som linjene vurderes i. 

Lokasjonsdirektiver har et ekstra detaljnivå: *lokasjonsdirektivhandlinger*. Du kan definere flere lokasjonsdirektivhandlinger for hver linje. Et serienummer brukes igjen til å bestemme rekkefølgen som handlingene er vurdert i. På dette nivået kan du definere en spørring for å definere hvordan du finner den beste plasseringen i lageret. Du kan også bruke forhåndsdefinerte innstillinger for **Strategi**for å finne en optimal lokasjon.

### <a name="example-of-the-use-of-location-directives"></a>Eksempel på bruk av lokasjonsdirektiver

I dette eksemplet vil vi vurdere en bestillingsprosess der lokasjonsdirektivet må finne ledig kapasitet i et lager for lagervarer som nettopp er registrert i mottakssonen. Først må vil vi prøve å finne ledig kapasitet i lageret ved å konsolidere med eksisterende lagerbeholdning. Hvis konsolidering er ikke mulig, vil vi finne en ledig lokasjon. 

I dette scenariet må vi definere to lokasjonsdirektivhandlinger. Den første handlingen i sekvensen må bruke strategien **Konsolider** og andre må bruke strategien **Tom lokasjon uten innkommende arbeid**. Med mindre vi definerer en tredje handling for å håndtere et overflytscenario er to resultater mulig når det er ikke mer kapasitet i lageret: arbeid kan opprettes selv om ingen lokasjoner defineres, eller arbeidsopprettingsprosessen kan mislykkes. Resultatet bestemmes av oppsettet på siden **Feil med lokasjonsdirektiv** der du kan bestemme om du vil velge alternativet **Stopp arbeid ved feil med lokasjonsdirektiv** for hver arbeidsordretype.




