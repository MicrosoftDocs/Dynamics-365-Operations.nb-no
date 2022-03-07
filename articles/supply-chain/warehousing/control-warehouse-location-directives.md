---
title: Kontrollere lagerarbeid ved hjelp av arbeidsmaler og lokasjonsdirektiver
description: Dette emnet beskriver hvordan du bruker arbeidsmaler og lokasjonsdirektiver for å bestemme hvordan og hvor arbeid utføres i lageret.
author: perlynne
ms.date: 10/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSLocDirFailure, WHSLocDirHint, WHSLocDirTable, WHSLocDirTableUOM, WHSRFMenuItem, WHSWork, WHSWorkClass, WHSWorkPool, WHSWorkTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 72921
ms.assetid: 377ab8af-5b0c-4b5e-a387-06ac1e1820c0
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-09
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a7e955fba12e963a443c0304f0a8a0e395c46909dd34de12cd51fa9788491786
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6770150"
---
# <a name="control-warehouse-work-by-using-work-templates-and-location-directives"></a>Kontrollere lagerarbeid ved hjelp av arbeidsmaler og lokasjonsdirektiver

[!include [banner](../includes/banner.md)]

Dette emnet beskriver hvordan du bruker arbeidsmaler og lokasjonsdirektiver for å bestemme hvordan og hvor arbeid utføres i lageret.

Instruksjonene som lagermedarbeidere mottar på en mobil enhet, bestemmes av arbeidsmalene som du definerer i Dynamics 365 Supply Chain Management for å definere de ulike lagerprosesser og -oppgaver. Arbeidsmaler avgjør hvordan arbeidet skal utføres for hver lagerprosess. Ved å koble et lokasjonsdirektiv til arbeidsmaler kan du bidra til å garantere at arbeid skjer i bestemte fysiske områder på lagrene.

## <a name="work-templates"></a>Arbeidsmaler

Siden **Arbeidsmaler** lar deg definere arbeidsoperasjoner som må utføres på lageret. Vanligvis består lageroperasjoner av to handlinger: en lagerarbeider plukker opp beholdning på en lokasjon og plasserer den plukkede beholdningen på en annen lokasjon. 

Arbeidsmaler består av et hode og tilhørende linjer. Hver arbeidsmal gjelder en bestemt *arbeidsordretype*. Mange arbeidsordretyper assosieres med kildedokumenter, for eksempel bestillinger eller salgsordrer. Imidlertid representerer andre arbeidsordretyper egne lagerprosesser, for eksempel syklustelling. *Arbeidspulje-ID* gir deg muligheten til å organisere arbeidet i grupper. 

Bruk innstillingene i arbeidshodedefinisjonen til å bestemme når et nytt stykke arbeid skal opprettes. Du kan for eksempel angi et maksimalt antall plukklinjer og maksimalt forventet plukktid. Deretter, hvis arbeidet for en salgsordreplukkingsprosess overskrider en av disse verdiene, deles dette arbeidet inn i to stykker arbeid.

Bruk **Arbeidshodeskift**-knappen til å definere når systemet skal opprette nye arbeidshoder. Hvis du for eksempel vil opprette et arbeidshode for hvert _ordrenummer_, velger du **Rediger spørring** i handlingsruten, og deretter legger du til **Ordrenummer**-feltet i **Sortering**-fanen i redigeringsprogrammet for spørring. Felter som legges til i **Sortering**-fanen, kan velges som *grupperingsfelter*. Hvis du vil angi grupperingsfeltene, velger du **Arbeidshodeskift** i handlingsruten, og deretter merker du av i avmerkingsboksen i **Grupper etter dette feltet**-kolonnen for hvert felt du vil bruke som et grupperingsfelt.

Arbeidslinjene representerer de fysiske oppgavene som kreves for å behandle arbeidet. For en prosess for utgående lager kan det for eksempel være en linje for å plukke opp varene i lageret og en annen linje for å plassere disse varene i et oppsamlingsområde. Det kan deretter være en ekstra linje for å plukke varene fra oppsamling og en annen linje for å plassere varene i en lastebil som en del av lastingsprosessen. Du kan angi en *direktivkode* på arbeidsmallinjene. En direktivkode er koblet til et lokasjonsdirektiv, og bidrar derfor til å sikre at lagerarbeidet blir behandlet på riktig lokasjon i lageret.

Du kan definere en spørring til å kontrollere når en bestemt arbeidsmal brukes. Du kan for eksempel angi en begrensning slik at en bestemt mal kan brukes for arbeid bare i et bestemt lager. Du kan også ha flere maler som oppretter arbeid for utgående ordrebehandling, avhengig av salgsopprinnelsen. Systemet bruker **Serienummer**-feltet for å bestemme rekkefølgen som de tilgjengelig arbeidsmalene vurderes i. Hvis du har en bestemt spørring etter en bestemt arbeidsmal, bør du derfor gi den et lavt sekvensnummer. Denne spørringen vil deretter bli evaluert før den andre, mer generelle spørringer.

> [!NOTE]
> Hvis du vil hindre at systemet automatisk overskriver *sekvensnumre* for arbeidsmal etter at en mal er slettet, aktiverer du funksjonen *Bevar sekvensnumre for arbeidsmal ved sletting* i [Funksjonsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

Hvis du vil stoppe eller pause en arbeidsprosess, kan du bruke innstillingen **Stopp arbeid** for arbeidslinjen. I så fall vil arbeideren som utfører arbeidet, ikke bli bedt om å utføre neste arbeidslinjetrinn. For å flytte til neste trinn må denne arbeideren eller en annen arbeider velge arbeidet på nytt. Du kan også skille oppgavene i et stykke arbeid ved å bruke en annen *arbeidsklasse-ID* på arbeidsmallinjene.

## <a name="location-directives"></a>Lokasjonsdirektiver

Lokasjonsdirektiver er regler som bidrar til å identifisere plukke- og plasseringslokasjoner for lagerbevegelse. I en salgsordretransaksjon bestemmer for eksempel et lokasjonsdirektiv hvor varene blir plukket og hvor de plukkede varene skal plasseres. Lokasjonsdirektiver består av et hode og tilknyttede linjer, og du oppretter dem på siden **Lokasjonsdirektiver**.

I hodet må hvert lokasjonsdirektiv må være knyttet til en *arbeidsordretype* som angir typen lagertransaksjon som direktivet som skal brukes for, for eksempel salgsordrer, etterfylling eller råvareplukking. *Arbeidstypen* angir om lokasjonsdirektivet skal brukes for å plukke eller plassere arbeid eller en annen lagerprosess, for eksempel telle eller lagerstatusendringer. Du må også angi et *område* og et *lager*. En *direktivkode* som du angir i hodet, kan brukes til å koble lokasjonsdirektivet til én eller flere maler for arbeid. 

Som for arbeidsmaler kan du definere en spørring for å bestemme når et bestemt lokasjonsdirektiv skal brukes. Du kan for eksempel angi at når e-handel er opprinnelsen til en salgsordre, må beholdning plukkes fra et dedikert område i lageret. Systemet bruker **Serienummer**-feltet for å bestemme rekkefølgen som de tilgjengelig lokasjonsdirektivene vurderes i.

Lokasjonsdirektivlinjene setter tilleggsbegrensninger på bruken av reglene for lokasjonssøk. Du kan angi et minimums- og maksimumsantall som direktivet skal gjelde for, og du kan angi at direktivet skal være for en bestemt lagerenhet. Hvis måleenheten for eksempel er paller, kan varer på paller plasseres på en bestemt lokasjon. Du kan også angi om antallet kan deles på tvers av flere lokasjoner. Som lokasjonsdirektivhodet har hver lokasjonsdirektivlinje et sekvensnummer som bestemmer rekkefølgen som linjene vurderes i.

Lokasjonsdirektiver har et ekstra detaljnivå: *lokasjonsdirektivhandlinger*. Du kan definere flere lokasjonsdirektivhandlinger for hver linje. Et serienummer brukes igjen til å bestemme rekkefølgen som handlingene er vurdert i. På dette nivået kan du definere en spørring for å definere hvordan du finner den beste plasseringen i lageret. Du kan også bruke forhåndsdefinerte innstillinger for **Strategi** for å finne en optimal lokasjon.

Hvis du vil ha mer informasjon om hvordan du oppretter og konfigurerer lokasjonsdirektiver, kan du se [Opprette et lokasjonsdirektiv](create-location-directive.md).

### <a name="how-location-directives-work"></a>Slik fungerer lokasjonsdirektiver

Lokasjonsdirektiver bestemmer *hvor* varene skal plukkes og *hvor* de skal plasseres. Systemet evaluerer et lokasjonsdirektiv mot hver arbeidslinje og velger deretter en lokasjon, basert på arbeidslinjedetaljene. Systemet finner først alle lokasjonsdirektiver som samsvarer med en bestemt arbeidslinje (for eksempel at de er for det riktige lageret og samsvarer med spørringen). Deretter evalueres direktivene som det har funnet, sekvensielt.

> [!NOTE]
> Det finnes spesialtilfeller der plukkstedet eller plasseringsstedet er forhåndsvalgt. Under _innkjøpsregistreringen_ er for eksempel den første plukkingen alltid fra lokasjonen der registreringen inntreffer. Et annet eksempel er *lagerflyting med mal*, der lagerarbeideren velger plukklokasjonen, og bare plasseringslokasjoner blir funnet via lokasjonsdirektiver.

## <a name="additional-resources"></a>Tilleggsressurser

- Video: [Dyp dykk i konfigurasjon av lagerstyring](https://community.dynamics.com/365/b/techtalks/posts/warehouse-management-configuration-deep-dive-october-14-2020)
- Hjelpeemne: [Arbeide med lokasjonsdirektiver](create-location-directive.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]