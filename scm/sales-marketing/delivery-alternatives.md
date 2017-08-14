---
title: Leveringsalternativer
description: "Salgsordretakere kan bruke siden Leveringsalternativer til å søke etter alternativer for ordrefullføring."
author: YuyuScheller
manager: AnnBe
ms.date: 04/10/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SalesLineDeliveryDetails
audience: Application User
ms.reviewer: annbe
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 271623
ms.assetid: 527f6084-44fe-41bb-924f-4386e926358a
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: crytt
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30T00:00:00.000Z
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 33fe96562777443bffc5dac30fd3a273bcffb6e0
ms.contentlocale: nb-no
ms.lasthandoff: 07/27/2017

---

# <a name="delivery-alternatives"></a>Leveringsalternativer

[!include[banner](../includes/banner.md)]


Salgsordretakere kan bruke siden Leveringsalternativer til å søke etter alternativer for ordrefullføring.

I Microsoft Dynamics 365 for Operations versjon 1611 (november 2016),kan salgsordretakere bruke siden **Leveringsalternativer** til å finne alternativer for ordrefullføring. Det nye sideoppsettet gir bedre oversikt over alle alternativer. Den lar også ordretakere se utenfor gjeldende firma for fullføringsmuligheter. De kan nå vise både konserninterne muligheter og muligheter fra eksterne leverandører. Salgsordretakere kan vise en intelligent liste med leveringsalternativer ved å sortere alternativene etter leveringsdato. I tillegg bidrar parametere til enklere administrasjon av foreslåtte leveringer. Siden transporttid kan påvirke leveringsdatoer, kan salgsordretakere utforske de forskjellige transportvalgene som transportører tilbyr. Siden det vises detaljert informasjon for hver forslag, kan salgsordretakere ta informerte avgjørelser direkte fra siden **Leveringsalternativer**.

## <a name="open-the-delivery-alternatives-page"></a>Åpne siden Leveringsalternativer
Du kan åpne siden **Leverings****alternativer** fra salgsordrelinjen.

1.  Klikk på **Produkter og forsyning** &gt; **Leveringsalternativer**.
2.  Klikk på **Linjedetaljer** &gt; **Levering** &gt; **Leveringsalternativer**.

Du kan også åpne siden **Leveringsalternativer** ved å åpne arbeidsområdet **Salgsordrebehandling og -spørring**, og deretter klikke på **Ordrer og favoritter** &gt; **Forsinkede ordrelinjer** &gt; **Leveringsalternativer** **Obs!** Du kan bare åpne siden **Leveringsalternativer** hvis begge følgende betingelser er oppfylt:

-   All obligatorisk informasjon for salgslinje er fylt ut.
-   Feltet **Leveringsdatokontroll** er satt til en annen verdi enn **Ingen**.

## <a name="delivery-date-control-methods"></a>Metoder for leveringsdatokontroll
Metoden for leveringsdatokontroll avgjør hvordan systemet oppretter leveringsdatoer, hvordan leveringsalternativer beregnes og hvilken informasjon som vises. Legg merke til at leveringsdatokontroll tar hensyn til kalendere. Kalenderne nedenfor kan derfor påvirke den foreslåtte mottaksdatoen: lagerkalender, transportkalender, leverandørkalender og kundekalender. Tabellen nedenfor beskriver alle metodene for leveringsdatokontroll.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Metode</strong></td>
<td><strong>Beskrivelse</strong></td>
</tr>
<tr class="even">
<td><strong>Ingen</strong></td>
<td><ul>
<li>Leveringsalternativer for salgslinjer støttes ikke. Dette alternativet deaktiverer leveringsdatokontroll.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Salgsleveringstid</strong></td>
<td><ul>
<li>Leveringsalternativer beregnes basert på den forhåndsdefinerte salgsleveringstiden. Transportdagene beregnes basert på leveringsmåten.</li>
<li>Leveringsalternativer omfatter lagre som har lagerbeholdning og forsynings-/behovsordrer.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>ATP</strong></td>
<td><ul>
<li>Leveringsalternativer beregnes basert på tilgjengelig for ordre-logikk (ATP). Det tas hensyn til gjeldende tilgjengelighet og forventet fremtidig tilgjengelighet. Transportdagene beregnes basert på leveringsmåten.</li>
<li>Leveringsalternativer omfatter lagre som har lagerbeholdning og forsynings-/behovsordrer.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>ATP + Avgang-margin</strong></td>
<td><ul>
<li>Leveringsalternativer beregnes som for ATP-metoden, men antall sikkerhetsdager er inkludert i beregningen.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>CTP</strong></td>
<td><ul>
<li>Leveringsalternativer beregnes basert på leveringskapasitetlogikk (CTP). MRP-nedbryting brukes til å bestemme tilgjengelighet. Legg merke til CTP forskyver minimumleveringsdatoer til salgsleveringstiden. Transportdagene beregnes basert på leveringsmåten.</li>
<li>Leveringsalternativer inkluderer forslag for følgende lagre:
<ul>
<li>Gjeldende lager</li>
<li>Standardlager</li>
<li>Alle lagre som har tilgjengelig lagerbeholdning</li>
<li>Alle lagre som har forsyningsordrer</li>
<li>Alle lagre som har aktive stykklisteversjoner</li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="view-information-about-delivery-alternatives"></a>Vise informasjon om leveringsalternativer
Dette avsnittet inneholder informasjon om leveringsalternativer som er tilgjengelige i hver kategori på siden **Leveringsalternativer**.

### <a name="products"></a>Produkter

Denne kategorien viser et sammendrag av produktet og detaljer om den gjeldende salgslinje.

### <a name="delivery-alternatives"></a>Leveringsalternativer

Denne kategorien viser en liste med leveringsalternativer som er sortert etter mottaksdata. Over listen kan du velge hvilke alternativer du vil basere forslagene på. Du kan også velge leveringsmåten, som bestemmer transportdagene. Følgende alternativer er tilgjengelige:

-   **Ta med andre produktvarianter** – Dette alternativet er tilgjengelig for produkter som har produktvarianter. Det inneholder leveringsalternativer for andre varianter av produktet. Dette alternativet er ikke tilgjengelig for CTP.
-   **Inkluder delvis antall** – Som standard inkluderbare forslag som oppfyller hele antallet for salgslinjen. Velg dette alternativet for å inkludere forslag som bare delvis oppfyller ordrelinjen. Dette alternativet er nyttig når kunden ber om en tidligere leveringsdato og godtar dellevering.
-   **Ta med senere datoer** – Som standard vise bare forslag som er bedre (tidligere) enn gjeldende datoer på salgslinjen. Velg dette alternativet for å inkludere senere datoer. Dette alternativet kan være nyttig i situasjoner der andre parametere enn datoen har prioritet. En bestemt leverandør eller lager kan for eksempel være foretrukket.
-   **Leveringsmåte** – Velg den foretrukne leveringsmåten for å optimalisere transporttiden og kostnadene. Virkningen på foreslåtte leveringsalternativer vises umiddelbart. Derfor er det enklere å sammenligne alternativene.
-   **Inkluder innkjøp** – Når innkjøp er valgt, vil foreslåtte leveringsalternativer inkludere alternativer for å produsere fra eksterne leverandører og andre firmaer i organisasjonen (konsernintern). Alternativet **Inkluder innkjøp** støttes for leveringsdatokontroll for ATP og ATP + Avgang-margin. Innkjøpsalternativer fra standard kjøpsleverandør for produktet og alle godkjente leverandører for produktet, er inkludert.
-   Beregningen er basert på leveringstiden for innkjøp for eksterne leverandører.
-   For konserninterne tar beregningen hensyn til hva som er tilgjengelig fra leverandørfirmaet, basert på leveringsdatokontroll i leverandørfirmaet.
-   **Leveringstype** (Relevant for innkjøp)
    -   **Lager** – Produkter sendes fra leverandørlageret til området/lageret på salgslinjen. De sendes deretter fra dette lageret til kunden.
    -   **Direktelevering** – Produktene leveres direkte fra leverandørlageret til kunden.

### <a name="availability-information"></a>Tilgjengelighetsinformasjon

Informasjon i denne kategorien er knyttet til leveringsalternativlinjen som er valgt. Følgende informasjon vises, avhengig av leveringsdatokontrollen for salgslinjen:

-   **Salgsleveringstid**
    -   **Tilgjengelig i dag** – Viser gjeldende fysiske beholdning, fysisk reservert og tilgjengelig fysisk lager.
    -   **Parametere** – Viser lagerenheten og salgsleveringstid.

-   **ATP og ATP + Avgang-margin**
    -   **Tilgjengelig i dag** – Viser gjeldende fysiske beholdning, fysisk reservert og tilgjengelig fysisk lager.
    -   **Parametere** – Viser lagerenheten og salgsleveringstid.
    -   **Fremtidig tilgjengelighet** – Viser en grafisk fremstilling av gjeldende og fremtidig tilgjengelighet for det valgte området og lageret under **Leveringsalternativer**. Du kan klikke diagramkolonnene for å vise mer detaljert informasjon om fremtidig tilgjengelighet for produktet. Glidebryteren viser en liste over relevante behovs- og forsyningsordrer i ATP-horisonten.

-   **CTP**
    -   **Tilgjengelig i dag** – Viser gjeldende fysiske beholdning, fysisk reservert og tilgjengelig fysisk lager.
    -   **Parametere** – Viser lagerenheten og salgsleveringstid.
    -   **Nedbryting** – Viser en forsyningsnedbryting av valgt leveringsalternativ. Du kan bruke **Oppsett** til å endre feltene og lagerdimensjonene som vises i nedbrytingen.

### <a name="impact-of-selected-alternative"></a>Innvirkning av valgt alternativ

Denne kategorien uthever effekten av det valgte leveringsalternativet. Hvis du klikker på **OK**, oppdateres salgslinjen med de uthevede verdiene i VALGT-kolonnene. Legg merke til at hvis antallet på det valgte leveringsalternativet er mindre enn antall på salgslinjen, opprettes en leveringsplan og ordrelinjen deles inn i to linjer: én linje for det valgte antallet og én linje for det restantallet. Du kan også oppdatere den kommersielle linjen, slik at den samsvarer med planlinjene og påvirker prissettingen.

<a name="see-also"></a>Se også
--------

[Ordrebekreftelse](/dynamics365/unified-operations/supplychain/sales-marketing/delivery-dates-available-promise-calculations)





