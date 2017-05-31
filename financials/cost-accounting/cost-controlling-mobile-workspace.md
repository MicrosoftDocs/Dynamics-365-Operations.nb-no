---
title: "Mobilt arbeidsområde for kostnadskontroll"
description: "Dette emnet gir informasjon om det mobile arbeidsområdet for kostnadskontroll, som er tilgjengelig for Microsoft Dynamics 365 for Operations-mobilappen. I dette arbeidsområdet kan kostsenterledere se kostsenterresultater når som helst og hvor som helst."
author: YuyuScheller
manager: AnnBe
ms.date: 05/10/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: annbe
ms.search.scope: Operations, Core
ms.custom: 267114
ms.assetid: 612f2988-b2b9-420d-9825-40b99dc0e204
ms.search.region: global
ms.author: yuyus
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 09383c24b0dd2ad61a836f6c8dc97f4389915772
ms.contentlocale: nb-no
ms.lasthandoff: 05/25/2017


---

# <a name="cost-controlling-mobile-workspace"></a>Mobilt arbeidsområde for kostnadskontroll

[!include[banner](../includes/banner.md)]


Dette emnet gir informasjon om det mobile arbeidsområdet for kostnadskontroll, som er tilgjengelig for Microsoft Dynamics 365 for Operations-mobilappen. I dette arbeidsområdet kan kostsenterledere se kostsenterresultater når som helst og hvor som helst. 

<a name="overview-of-the-cost-controlling-mobile-workspace"></a>Oversikt over det mobile arbeidsområdet for kostnadskontroll
-------------------------------------------------

Mobilt arbeidsområde for **kostnadskontroll** gir en øyeblikkelig visning av den gjeldende ytelsen til kostsentre ved å sammenligne faktiske kostnader med de budsjetterte kostnadene. Du kan drille ned til statusene for individuelle kostnadselementer. 

En ansatt mottar for eksempel en invitasjon til en internasjonal konferanse, men organisasjonen må dekke alle reiseutgifter. Den ansatte ber om lederen om tillatelse til å delta på konferansen. Lederen åpner det mobile arbeidsområdet for **kostnadskontroll** på mobilenheten for å se om han/hun har budsjettert for at den ansatte kan delta på konferansen.

### <a name="data-security"></a>Datasikkerhet

Dataene i arbeidsområdet for **kostnadskontroll** er sikret gjennom brukerlegitimasjon. Kostsenterledere kan bare se data for sitt eget kostsenter. Tilgangsnivåsikkerhet behandles i modulen **Kostnadsregnskap**. 

Regnskapsførere definerer konfigurasjonen av det mobile arbeidsområdet for **kostnadskontroll** i modulen **Kostnadsregnskap**. Når arbeidsområdet er publisert til Microsoft Dynamics-365 for Operations-mobilappen, er det tilgjengelig i appen. Dette sikrer at alle kostsenterledere i organisasjonen ser dataene i det samme formatet.

### <a name="actions-views-and-links"></a>Handlinger, visninger og koblinger

Mobilt arbeidsområde for **kostnadskontroll** for Dynamics 365 for Operations-appen gir følgende handlinger, visninger og koblinger:

-   **Handlinger:**
    -   Bruk **Velg konfigurasjon** for å velge et oppsett.
    -   Bruk **Velg kostnadsobjekt** for å velge kostsentrene til å filtrere dataene på. **Merk:** Kostsentrene som vises i listen, avhenger av tilgangen som gis i modulen **Kostnadsregnskap**.
-   **Visninger:** Basert på handlingene som er valgt, og konfigurasjonen i modulen **Kostnadsregnskap**, kan du vise følgende informasjon på kortene.
    -   Faktisk i forhold til budsjett (gjeldende periode)
    -   Faktisk i forhold til revidert budsjett (gjeldende periode)
    -   Faktisk i forhold til budsjett (forrige periode)
    -   Faktisk i forhold til revidert budsjett (forrige periode)
    -   Faktisk i forhold til budsjett (hittil i år)
    -   Faktisk i forhold til revidert budsjett (hittil i år)

    Disse beløpene vises på hvert kort: faktisk, budsjett, avvik og varians %.
-   **Koblinger:**
    -   Detaljer for gjeldende periode
    -   Detaljer for forrige periode
    -   Detaljer for hittil i år

    Når du velger en kobling, vises et kort for hvert kostnadselement. Følgende beløp vises på hvert kort: faktisk, budsjett, budsjettavvik, budsjettavviks-%, revidert budsjett, revidert budsjettavvik og revidert budsjettavviks-%. 
    
    [![Kort for et kostnadselement ](./media/cost-controlling.png)](./media/cost-controlling.png)

## <a name="prerequisites"></a>Forutsetninger
Før du kan bruke det mobile arbeidsområdet for **kostnadskontroll**, må du kontrollere at systemansvarlig har følgende forutsetninger på plass.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Forutsetning</th>
<th>Rolle</th>
<th>beskrivelse</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Dynamics 365 for Operations versjon 1611 med plattformoppdatering 3 eller senere må implementeres.</td>
<td>Systemansvarlig</td>
<td>Hvis du ikke allerede har Dynamics 365 for Operations distribuert i organisasjonen, bør systemansvarlig se <a href="/dynamics365/operations/dev-itpro/deployment/deploy-demo-environment">Distribuere et Microsoft Dynamics 365 for Operations-demomiljø</a>.</td>
</tr>
<tr class="even">
<td>KB 4013633 må være implementert.</td>
<td>Systemansvarlig</td>
<td>KB 4013633 (en X++ oppdatering eller hurtigreparasjon for metadata) inneholder fire mobile arbeidsområder for forsyningskjedeadministrasjon. Systemadministrator må følge disse trinnene for å implementere KB 4013633:
<ol>
<li>Last ned KB 4013633 fra Microsoft Dynamics Lifecycle Services (LCS).</li>
<li><a href="/dynamics365/operations/dev-itpro/migration-upgrade/install-metadata-hotfix-package">Installer hurtigreparasjonen for metadata</a>.</li>
<li><a href="/dynamics365/operations/dev-itpro/deployment/create-apply-deployable-package">Opprett en distribuerbar pakke</a> som inneholder <strong>SCMMobile</strong>-modellen, og last deretter opp den distribuerbare pakken til LCS.</li>
<li><a href="/dynamics365/operations/dev-itpro/deployment/apply-deployable-package-system">Bruk den distribuerbare pakken</a> på Dynamics 365 for Operations-systemet.</li>
</ol></td>
</tr>
<tr class="odd">
<td>Det mobile arbeidsområdet for <strong>kostnadskontroll</strong> må publiseres til Dynamics-365 for Operations-mobilappen.</td>
<td>Systemansvarlig</td>
<td><ol>
<li>Start Dynamics 365 for Operations i nettleseren.</li>
<li>På siden <strong>Systemparametere</strong> velger du <strong>Behandle mobile arbeidsområder</strong>.</li>
<li>Velg arbeidsområdet <strong>Oversikt over kostnadsobjekt</strong>.</li>
<li>Klikk <strong>Publiser mobilt arbeidsområde</strong>.</li>
</ol></td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-dynamics-365-for-operations-mobile-app"></a>Laste ned og installere Dynamics 365 for Operations-mobilappen
Last ned og installer Microsoft Dynamics 365 for Operations-appen fra appbutikken for mobilenheten.

-   For Android: [Dynamics 365 for Operations på Google Play-butikken](https://play.google.com/store/apps/details?id=com.microsoft.dynamics365.operations.mobile)
-   For iPhone: [Dynamics 365 for Operations på iTunes-appbutikken](https://itunes.apple.com/us/app/dynamics-365-for-operations/id1180836730?mt=8)

## <a name="sign-in-to-the-dynamics-365-for-operations-mobile-app"></a>Logg på Dynamics 365 for Operations-mobilappen
1.  Start appen på mobilenheten.
2.  Angi URL-adressen for Dynamics 365 for Operations.
3.  Angi firmaet for å logge på. Skriv for eksempel **USMF**.
4.  Første gang du logger deg på, du blir bedt om brukernavn og passord for din Dynamics 365 for Operations-konto. Angi legitimasjon.
5.  Når du har logget deg på, kan du se tilgjengelige arbeidsområder for firmaet. Legg merke til at hvis systemansvarlig senere publiserer et nytt arbeidsområde, kan du dra for å oppdatere listen over mobile arbeidsområder. 

    [![Hent for å oppdatere](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)

## <a name="view-the-performance-of-your-cost-center-by-using-the-cost-controlling-mobile-workspace"></a>Vise ytelsen til kostsenteret ved hjelp av det mobile arbeidsområdet for kostnadskontroll
1.  Velg **Kostnadskontroll**-arbeidsområdet på mobilenheten.
2.  Velg **Kostnadsobjektobjekt**.
3.  Velg **Handlinger**.
4.  Klikk **Velg konfigurasjon** for å velge et kostnadskontrolloppsett.
5.  Velg **Ferdig**.
6.  Velg **Handlinger**.
7.  Klikk **Velg kostnadsobjekt** for å velge kostsentrene du har fått tilgang til.
8.  Velg **Ferdig**.
9.  Vis den totale ytelsen til kostsenteret.
10. Velg koblingen **Detaljer for gjeldende periode**.
11. Vise ytelsen til individuelle kostnadselementer.
12. Du kan også søke etter bestemte kostnadselementer.





