---
title: Oppsett for leveringsinformasjon
description: Dette emnet beskriver hvordan du definerer leveringsinformasjon for modulen Netto innkjøpspris.
author: sherry-zheng
manager: tfehr
ms.date: 12/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ITMPortTable, ITMLeadTimeTable, ITMLegTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-09
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 7b65e1c6bb1b6bf345fdde0f4de7015190052efa
ms.sourcegitcommit: 2b4809e60974e72df9476ffd62706b1bfc8da4a7
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/04/2021
ms.locfileid: "5500532"
---
# <a name="delivery-information-setup"></a>Oppsett for leveringsinformasjon

[!include [banner](../../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Dette emnet beskriver hvordan du definerer leveringsinformasjon for modulen **Netto innkjøpspris**.

## <a name="shipping-ports"></a>Forsendelseshavner

Forsendelseshavnene identifiserer hvor varer sendes fra og til. For hver sjøreise defineres det en til-havn og en fra-havn, basert på reisen som er valgt for sjøreisetransportmidlet. Forsendelseshavnene brukes til å sette sammen etappene i en reise samt sjøreiseaktiviteter. De defineres som regel ved å bruke navnet på byen og landet eller regionen der den fysiske forsendelseshavnen finnes.

Hvis du vil arbeide med leveringshavner, går du til **Netto innkjøpspris \> Oppsett av leveringsinformasjon \> Forsendelseshavner**. Der kan du vise, legge til og fjerne poster for forsendelseshavnene. Følgende tabell beskriver feltene som er tilgjengelige for hver post.

| Felt | beskrivelse |
|---|---|
| Forsendelseshavn | Angi et unikt identifikasjonsnavn/-nummer for forsendelseshavnen. |
| beskrivelse | Angi en beskrivelse av forsendelseshavnen. |

## <a name="tracking-control-center"></a><a name="tracking-control-center"></a>Sporingskontrollsenter

Du bruker sporingskontrollsenteret til å angi leveringstider, statusoppdateringer og informasjonsflyt som er knyttet til en sjøreise etter hvert som forsendelsescontainere flyttes fra en etappe til neste. Når du oppretter en sporingskontrollpost, knyttes den til en bestemt del av en etappe for en transportreise. Når en oppdaterer en etappe, oppdateres den tilknyttede posten og fylles ut som definert. Du kan oppdatere sporingsinformasjon for individuelle sjøreiser fra siden **Alle sjøreiser**.

Hvis du vil åpne sporingskontrollsenteret, går du til **Netto innkjøpspris \> Oppsett av leveringsinforamsjon \> Sporingskontrollsenter**.

Sporingskontrollsenteret viser én av de tre sidevisningene, avhengig av verdien som er valgt i feltet **Opprett type** i listen: *Tom*, *Leveringstid* eller *Statusoppdatering*. Hver opprettingstype oppdaterer et forskjellig sett med informasjon som er knyttet til forløpet til en sjøreise, fra opprinnelsesstedet til det endelige målet.

### <a name="common-rule-settings"></a>Vanlige regelinnstillinger

Tabellen nedenfor viser feltene som er tilgjengelige for alle de tre opprettingstypene i sporingskontrollsenteret.

| Felt | beskrivelse |
|---|---|
| Kildetabell, Kilde-felt | Disse feltene identifiserer en kildetabell og et felt i databasen. Regelen laster inn verdien i feltet, og bruker den deretter på den måten som er definert av andre innstillinger for regelen. |
| Måltabell, Mål-felt | Disse feltene identifiserer en måltabell og et felt i databasen. Regelen laster inn verdien i feltet, og bruker den (eller overskriver den) deretter på den måten som er definert av andre innstillinger for regelen. |
| Aktivitet | Dette feltet identifiserer aktivitetstypen som skal brukes på en forsendelsescontainer som samsvarer med en regel. |
| Samsvarskriterier | Dette feltet bestemmer hvordan systemet identifiserer et samsvar for en regel. I hver forekomst ser systemet gjennom dataene i kilde- og måltabellene for å finne ut om og når et felt skal oppdateres i måltabellen.<p>Kildetabellen er for eksempel *Sjøreiser*, og måltabellen er *Innkjøpshode* eller *Innkjøpslinjer*. Tabellen *Sjøreiser* har verdien *Hongkong* for **Fra-havn**, og tabellen *Innkjøpshode* har verdien *Shanghai* for **Fra-havn**. Det opprettes deretter en regel som har *Hongkong* som Fra-havn. I dette tilfellet vil verdiene i feltet **Samsvarende kriterier** fungere på følgende måte:</p><ul><li>**Begge** – Målfeltet blir ikke oppdatert, fordi én av de to havnene ikke samsvarer.</li><li>**Kilde** – Målfeltet vil bli oppdatert, fordi kildetabellens Fra-havn er *Hongkong*.</li><li>**Mål** – Målfeltet vil ikke bli oppdatert, fordi måltabellens Fra-havn er *Shanghai* (ikke *Hongkong*).</li></ul> |
| Kopier handling | De tilgjengelige verdiene er *Kopi* og *Standard*. Velg *Kopi* for å kopiere verdien i kildefeltet til målfeltet. Velg *Standard* for å angi en statisk verdi for målfeltet. |
| Standard | Når feltet **Kopier handling** er satt til *Standard*, definerer feltet **Standard** standardverdien for målfeltet. Hvis handlingen for eksempel er relatert til en havnoppdatering, og feltet **Kopier handling** er satt til *Standard*, identifiserer feltet **Standard** en havn. |
| Strekning | Dette feltet identifiserer etappen av reisen som den angitte handlingen oppstår for, for eksempel lasting eller toll. |
| Tjenesteleverandør | Hvis en bestemt tjenesteleverandør brukes for gjeldende statusoppdatering/del av reisen, identifiserer dette feltet tjenesteleverandøren. Tjenesteleverandører defineres i leverandørkontoen. |

### <a name="lead-time-rules"></a>Regler for leveringstid

Leveringstiden er den estimerte tiden som en sjøreise vil kreve for å fullføre en definert etappe av en reise for en sjøreise. Leveringstiden for hver etappe brukes til å beregne den forventede leveringsdatoen for sjøreisen. Denne datoen legges deretter inn i feltet **Bekreftet leveringsdato** på hver innkjøpslinje i sjøreisen.

Du bruker leveringstidsregler til å administrere datooppdateringer. Aktiviteter genereres automatisk når en reisemal brukes for en sjøreise.

Følg denne fremgangsmåten for å legge til en leveringstidsregel i sporingskontrollsenteret.

1. Følg ett av disse trinnene:

    - Gå til **Netto innkjøpspris \> Oppsett for reise med flere etapper \> Etapper**. Velg etappen du vil angi leveringstider for, og velg deretter **Sporingskontrollsenter** i handlingsruten. Sporingskontrollsenteret forhåndslastes med informasjon om den valgte etappen.
    - Gå til **Netto innkjøpspris \> Oppsett av leveringsinformasjon \> Sporingskontrollsenter**. Deretter må du manuelt velge en etappe i trinn 4 i denne prosedyren.

1. I listen setter du verdien for feltet **Opprett type** til *Leveringstid*.
1. Velg **Ny** i handlingsruten.
1. Hvis du startet fra sporingskontrollsenteret i trinn 1, setter du feltet **Etappe** til etappen du vil opprette en leveringstidsregel for. Hvis du startet fra siden **Etapper**, er feltet **Etappe** forhåndsutfylt med etappen du valgte før du åpne sporingskontrollsenteret.

    Basert på verdien i feltet **Etappe** fylles flere felt ut automatisk, som vist her:

    - **Kildetabell:** *Containeraktiviteter*
    - **Kildefelt:** *Startdato*
    - **Måltabell:** *Containeraktiviteter*
    - **Målfelt:** *Forventet sluttdato*

1. Velg aktiviteten som gjeldende regel skal gjelde for, i feltet **Aktiviteter**.
1. I feltet **Leveringstid** angir du leveringstiden (i dager) som skal brukes når den gjeldende regelen utløses.

### <a name="status-update-rules"></a>Regler for statusoppdatering

Poster der feltet **Opprett type** er satt til *Statusoppdatering*, oppdaterer statusen for innkjøpsordrelinjer, eller statusen på sjøreise-, forsendelsescontainer- eller folionivå. Du kan angi statuser uavhengig. Bruk dem til å informere brukeren eller avdelingen om stadiet til en sjøreise (for eksempel mottatte dokumenter eller varer i transitt).

Når feltet **Opprett type** er satt til *Statusoppdatering*, inkluderer sporingskontrollsenteret hurtigfanen **Linjer**, der du kan definere et kostnadsområde og sjøreisens oppdaterte status. Du har for eksempel en linje der feltet **Kostnadsområde** er satt til *Container*, og feltet **Sjøreisestatus** er satt til *Varer i transitt*. Når en ordre fullfører den angitte etappen, oppdateres verdien for feltet **Sjøreisestatus** for forsendelsescontaineren til *Varer i transitt*.

Statusoppdateringer gir statusen til en sjøreise gjennom hele salgsorden og bestillingslinjene som er tilknyttet denne sjøreisen. Etter hvert som en sjøreise går sin gang fra havnen via selve seilasen og innom ulike tollstasjoner frem til mållageret, gir feltet **Sjøreisestatus** for sjøreiseposten en hurtigvisning av stadiet som varene befinner seg i.

Følg denne fremgangsmåten for å legge til en statusoppdatering i sporingskontrollsenteret.

1. Følg ett av disse trinnene:

    - Gå til **Netto innkjøpspris \> Oppsett for reise med flere etapper \> Etapper**. Velg etappen du vil definere en statusoppdatering for, og velg deretter **Sporingskontrollsenter** i handlingsruten. Sporingskontrollsenteret forhåndslastes med informasjon om den valgte etappen.
    - Gå til **Netto innkjøpspris \> Oppsett av leveringsinformasjon \> Sporingskontrollsenter**. Deretter må du manuelt velge en etappe i trinn 4 i denne prosedyren.

1. I listen setter du verdien for feltet **Opprett type** til *Statusoppdatering*.
1. Velg **Ny** i handlingsruten.
1. Hvis du startet fra sporingskontrollsenteret i trinn 1, setter du feltet **Etappe** til etappen du vil opprette en statusoppdatering for. Hvis du startet fra siden **Etapper**, er feltet **Etappe** forhåndsutfylt med etappen du valgte før du åpne sporingskontrollsenteret.

    Basert på verdien i feltet **Etappe** fylles flere felt ut automatisk, som vist her:

    - **Kildetabell:** *Containeraktiviteter*
    - **Kildefelt:** *Faktisk sluttdato*
    - **Måltabell:** Dette feltet er tomt.
    - **Målfelt:** Dette feltet er tomt.

1. Velg aktiviteten som regelen skal gjelde for, i feltet **Aktiviteter**.
1. Angi statusoppdateringene for hvert kostnadsområde i hurtigfanen **Linjer**.

### <a name="blank-type-rules"></a>Regler for tom type

Du bruker poster som har verdien *Tom* for **Opprett type** for å overstyre eller angi en feltverdi basert på dataene i et annet felt. Et felt fra Netto innkjøpspris vil overskrive data i andre områder av Microsoft Dynamics 365 Supply Chain Management, basert på reglene som er definert i sporingskontrollsenteret.

1. Gå til **Netto innkjøpspris \> Oppsett av leveringsinformasjon \> Sporingskontrollsenter**.
1. I listen setter du verdien for feltet **Opprett type** til *Tom*.
1. Velg **Ny** i handlingsruten.
1. Definer kilde- og målverdiene, samsvarskriteriene, kopihandlingen og andre relevante parametere etter behov for regelen.

### <a name="required-tracking-control-setup"></a>Oppsett av obligatorisk sporingskontroll

For hver reisemal må det defineres to poster i sporingskontrollsenteret. Begge disse postene har verdien *Tom* for **Opprett type**, og de brukes i alle implementeringer for Netto innkjøpspris. Postene bidrar til å sikre at bekreftet dato for innkjøp og varer i forventede transittdatoer oppdateres for sjøreiser og på beslektede bestillingslinjer på forventet måte.

Den første posten kreves for å oppdatere innkjøpslinjer. Posten må ha følgende innstillinger:

- **Kildetabell:** *Containeraktiviteter*
- **Kildefelt:** *Forventet sluttdato*
- **Måltabell:** *Innkjøpslinjer*
- **Målfelt:** *Bekreftet dato eller leveringsdato*

Den andre posten kreves for å oppdatere transaksjoner for varer i transitt. Posten må ha følgende innstillinger:

- **Kildetabell:** *Containeraktiviteter*
- **Kildefelt:** *Forventet sluttdato*
- **Måltabell:** *Ordre for varer i transitt*
- **Målfelt:** *Forventet dato*
