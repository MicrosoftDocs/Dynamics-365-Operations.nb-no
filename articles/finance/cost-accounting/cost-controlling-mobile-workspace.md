---
title: Mobilt arbeidsområde for kostnadskontroll
description: Dette emnet gir informasjon om det mobile arbeidsområdet for kostnadskontroll. I dette arbeidsområdet kan kostsenterledere se kostsenterresultater når som helst og hvor som helst.
author: AndersGirke
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 267114
ms.assetid: 612f2988-b2b9-420d-9825-40b99dc0e204
ms.search.region: global
ms.author: aevengir
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 27381a408df64b8f11323b2f164d242bb2c4b6c5
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/30/2019
ms.locfileid: "2249707"
---
# <a name="cost-controlling-mobile-workspace"></a>Mobilt arbeidsområde for kostnadskontroll

[!include [banner](../includes/banner.md)]

Dette emnet gir informasjon om det mobile arbeidsområdet **Kostnadskontroll**. I dette arbeidsområdet kan kostsenterledere se kostsenterresultater når som helst og hvor som helst.

Dette mobile arbeidsområdet er ment å brukes sammen med Finance and Operations-mobilappen.

## <a name="overview"></a>Oversikt
Mobilt arbeidsområde for **kostnadskontroll** gir en øyeblikkelig visning av den gjeldende ytelsen til kostsentre ved å sammenligne faktiske kostnader med de budsjetterte kostnadene. Du kan drille ned til statusen for individuelle kostnadselementer.

En ansatt mottar for eksempel en invitasjon til en internasjonal konferanse, men organisasjonen må dekke alle reiseutgifter. Den ansatte ber lederen om tillatelse til å delta på konferansen. Lederen åpner det mobile arbeidsområdet for **kostnadskontroll** på mobilenheten for å se om han/hun har budsjettert for at den ansatte kan delta på konferansen.

### <a name="data-security"></a>Datasikkerhet
Dataene i arbeidsområdet for **kostnadskontroll** er sikret gjennom brukerlegitimasjon. Kostsenterledere kan bare se data for sitt eget kostsenter. Tilgangsnivåsikkerhet behandles i modulen **Kostnadsregnskap**.

Regnskapsførere definerer konfigurasjonen av det mobile arbeidsområdet for **kostnadskontroll** i modulen **Kostnadsregnskap**. Etter at arbeidsområdet er publisert på mobilappen, er det tilgjengelig i appen. Dette sikrer at alle kostsenterledere i organisasjonen ser dataene i det samme formatet.

### <a name="actions-views-and-links"></a>Handlinger, visninger og koblinger
Det mobile arbeidsområdet **Kostnadskontroll** har følgende handlinger, visninger og koblinger:

-   **Handlinger:**

    -   Bruk **Velg konfigurasjon** for å velge et oppsett.
    -   Bruk **Velg kostnadsobjekt** for å velge kostsentrene til å filtrere dataene på.
    
        > [!NOTE]
        > Kostsentrene som vises i listen, avhenger av tilgangen som gis i modulen **Kostnadsregnskap**.

-   **Visninger:** Basert på handlingene som er valgt, og konfigurasjonen i modulen **Kostnadsregnskap**, kan du vise følgende informasjon på kortene:

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
    
    [![Kort for et kostnadselement ](./media/Cost-controlling.png)](./media/Cost-controlling.png)

## <a name="prerequisites"></a>Forutsetninger
Forutsetningene varierer avhengig av hvilken versjon av Microsoft Dynamics 365 som er distribuert i organisasjonen.

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-finance"></a>Forutsetninger hvis du bruker Microsoft Dynamics 365 Finance
Hvis Finance har blitt innført i organisasjonen din, må systemadministrator publisere det mobile arbeidsområdet **Kostnadskontroll**. Hvis du vil ha instruksjoner, kan du se [Publisere et mobilt arbeidsområde](../../dev-itpro/mobile-apps/publish-mobile-workspace.md).

### <a name="prerequisites-if-you-use-version-1611-with-platform-update-3-or-later"></a>Forutsetninger hvis du bruker versjon 1611 med Platform update 3 eller nyere
Hvis versjon 1611 med Platform update 3 eller nyere er distribuert i organisasjonen, må systemansvarlig oppfylle følgende forutsetninger.

<table>
<thead>
<tr class="header">
<th>Forutsetning</th>
<th>Rolle</th>
<th>beskrivelse</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Implementere KB 4013633.</td>
<td>Systemansvarlig</td>

<td>KB 4013633 er en X++-oppdatering eller hurtigreparasjon for metadata som inneholder det mobile arbeidsområdet <strong>Kostnadskontroll</strong>. Systemadministrator må følge trinnene nedenfor for å implementere KB 4013633.
<ol>
<li><a href="../../dev-itpro/migration-upgrade/download-hotfix-lcs.md">Last ned hurtigreparasjonen for metadata fra Microsoft Dynamics Lifecycle Services (LCS)</a>.</li>
<li><a href="../../dev-itpro/migration-upgrade/install-metadata-hotfix-package.md">Installer hurtigreparasjonen for metadata</a>.</li>
<li><a href="../../dev-itpro/deployment/create-apply-deployable-package.md">Opprett en distribuerbar pakke</a> som inneholder <strong>SCMMobile</strong>-modellen, og last deretter opp den distribuerbare pakken til LCS.</li>
<li><a href="../../dev-itpro/deployment/apply-deployable-package-system.md">Bruk den distribuerbare pakken</a>.</li>

</ol></td>
</tr>
<tr class="even">
<td>Publiser det mobile arbeidsområdet <strong>Kostnadskontroll</strong>.</td>
<td>Systemansvarlig</td>
<td>Se <a href="../../dev-itpro/mobile-apps/publish-mobile-workspace.md">Publisere et mobilt arbeidsområde</a>.</td>
</tr>
</tbody>
</table>


## <a name="download-and-install-the-mobile-app"></a>Laste ned og installere mobilappen
Laste ned og installere Finance and Operations-mobilappen:

-   [For Android-telefoner](https://go.microsoft.com/fwlink/?linkid=850662)
-   [For iPhone](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a>Logge på mobilappen

1.  Start appen på mobilenheten.
2.  Skriv inn URL-adressen for Dynamics 365.
3.  Første gang du logger deg på, blir du bedt om brukernavn og passord. Angi legitimasjon.
4.  Når du har logget deg på, vises tilgjengelige arbeidsområder for firmaet. Legg merke til at hvis systemansvarlig senere publiserer et nytt arbeidsområde, må du oppdatere listen over mobile arbeidsområder.

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

