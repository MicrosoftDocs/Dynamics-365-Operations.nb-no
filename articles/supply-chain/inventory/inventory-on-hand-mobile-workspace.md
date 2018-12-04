---
title: "Mobilt arbeidsområde for lagerbeholdning"
description: "Dette emnet gir informasjon om det mobile arbeidsområdet for lagerbeholdning. Dette arbeidsområdet gir deg mobil innsikt i reservert og tilgjengelig lager når som helst og hvor som helst."
author: Mirzaab
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 267094
ms.assetid: 3fa385ba-894d-4a9e-b394-ef3697abf895
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mirzaab
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: 735a25d625774892ff71d4799932f15c258dfbfa
ms.contentlocale: nb-no
ms.lasthandoff: 03/26/2018

---

# <a name="inventory-on-hand-mobile-workspace"></a>Mobilt arbeidsområde for lagerbeholdning

[!include [banner](../includes/banner.md)]

Dette emnet gir informasjon om det mobile arbeidsområdet for **lagerbeholdning**. Dette arbeidsområdet gir deg innsikt i reservert og tilgjengelig lager når som helst og hvor som helst.

Dette mobile arbeidsområdet er ment å brukes med mobilappen Microsoft Dynamics 365 for Unified Operations.

## <a name="overview"></a>Oversikt
Selskaper har vanligvis flere leveringer og flere mottak til lager hver dag. Disse flyttingene endrer kontinuerlig lagerbeholdningsstatusen. Det mobile arbeidsområdet for **lagerbeholdning** lar deg se lagerbeholdningsstatus på tvers av firmaet, slik at du kan få den nyeste innsikten i lagerdata på den mobile enheten du velger. Uansett om du arbeider i lager, innkjøp, salg, produksjon eller management, eller har andre roller, kan du få tilgang til dataene i lagerbeholdningen når som helst og hvor som helst. 

Det mobile arbeidsområdet gir en umiddelbar oversikt over lagerstatusen på tvers av kontorer. Du kan vise lagerbeholdning på tvers av kontorer, gjeldende materialreservasjoner og ureservert lagerbeholdning. Du kan også angi varenumrene for å spørre om lagerbeholdning og filtrert søke etter produkter på lager eller varianter. 

Spesielt inneholder mobil arbeidsområdet disse funksjonene:

-   Du kan søke etter produktnummeret eller produktnavnet for å finne produkter å vise lagerbeholdning status for.
-   For de valgte produktene kan du vise følgende informasjon:

    -   Lagerbeholdning etter område
    -   Lagerbeholdning etter lager
    -   Lagerbeholdning etter lokasjon
    -   Lagerbeholdning etter parti (for partikontrollerte produkter)
    -   Lagerbeholdning etter beholdningsstatus
    
-   Lagerbeholdning for produktet vises på følgende måter:

    -   Etter fysisk lager (denne visningen representerer den totale mengden).
    -   Etter fysisk reservert (denne visningen representerer den reserverte mengden).
    -   Etter fysisk tilgjengelig (denne visningen representerer tilgjengelig mengde uten reservasjoner.)

## <a name="prerequisites"></a>Forutsetninger
Forutsetningene varierer avhengig av hvilken versjon av Microsoft Dynamics 365 som er distribuert i organisasjonen.

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-for-finance-and-operations"></a>Forutsetninger hvis du bruker Microsoft Dynamics 365 for Finance and Operations 
Hvis Microsoft Dynamics 365 for Finance and Operations har blitt innført i organisasjonen din, må systemadministrator publisere det mobile arbeidsområdet **Lageberholdning**. Hvis du vil ha instruksjoner, kan du se [Publisere et mobilt arbeidsområde](../../dev-itpro/mobile-apps/publish-mobile-workspace.md).

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-for-operations-version-1611-with-platform-update-3-or-later"></a>Forutsetninger hvis du bruker Microsoft Dynamics 365 for Operations versjon 1611 med plattformoppdatering 3 eller senere
Hvis Microsoft Dynamics 365 for Operations versjon 1611 med plattformoppdatering 3 eller senere er distribuert i organisasjonen, må systemansvarlig oppfylle følgende forutsetninger. 

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

<td>KB 4013633 er en X++-oppdatering eller metadatahurtigreparasjon som inneholder det mobile arbeidsområdet for <strong>lagerbeholdning</strong>. Systemadministrator må følge trinnene nedenfor for å implementere KB 4013633.
<ol>
<li><a href="../../dev-itpro/migration-upgrade/download-hotfix-lcs.md">Last ned hurtigreparasjonen for metadata fra Microsoft Dynamics Lifecycle Services (LCS)</a>.</li>
<li><a href="../../dev-itpro/migration-upgrade/install-metadata-hotfix-package.md">Installer hurtigreparasjonen for metadata</a>.</li>
<li><a href="../../dev-itpro/deployment/create-apply-deployable-package.md">Opprett en distribuerbar pakke</a> som inneholder <strong>SCMMobile</strong>-modellen, og last deretter opp den distribuerbare pakken til LCS.</li>
<li><a href="../../dev-itpro/deployment/apply-deployable-package-system.md">Bruk den distribuerbare pakken</a>.</li>

</ol></td>
</tr>
<tr class="even">
<td>Publiser mobilt arbeidsområde for <strong>lagerbeholdning</strong>.</td>
<td>Systemansvarlig</td>
<td>Se <a href="../../dev-itpro/mobile-apps/publish-mobile-workspace.md">Publisere et mobilt arbeidsområde</a>.</td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a>Laste ned og installere mobilappen

Last ned og installer mobilappen Dynamics 365 for Unified Operations:

-   [For Android-telefoner](https://go.microsoft.com/fwlink/?linkid=850662)
-   [For iPhone](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a>Logge på mobilappen

1.  Start appen på mobilenheten.
2.  Skriv inn URL-adressen for Dynamics 365.
3.  Første gang du logger deg på, blir du bedt om brukernavn og passord. Angi legitimasjon.
4.  Når du har logget deg på, vises tilgjengelige arbeidsområder for firmaet. Legg merke til at hvis systemansvarlig senere publiserer et nytt arbeidsområde, må du oppdatere listen over mobile arbeidsområder.

    [![Hent for å oppdatere](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)

## <a name="view-the-on-hand-inventory-for-a-product-by-using-the-inventory-on-hand-mobile-workspace"></a>Vise lagerbeholdningen for et produkt ved å bruke det mobile arbeidsområdet for lagerbeholdning

1.  Velg **Lagerbeholdning**-arbeidsområdet på mobilenheten.

2.  Velg **Kontroller lagerbeholdning for en vare**. Du kan se en liste over produkter som er lastet inn i ditt program for frakoblet bruk. 50 varer blir lastet inn som standard, men en utvikler kan endre dette antallet. Utviklere kan se [Mobil plattform](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md) for mer informasjon.
3.  Hvis elementet ikke finnes i listen, velger du **Søk etter flere**. Søk etter produktnummer, eller bytte til et søk etter produktnavn.

4.  Velg et produkt. Hvis varen har et bilde, vises bildet.
5.  Velg ett av følgende alternativer for å vise statusen for lagerbeholdningen:

    -   Vis lagerbeholdning etter område
    -   Vis lagerbeholdning etter lager
    -   Vis lagerbeholdning etter lokasjon
    -   Vis lagerbeholdning etter parti (for partikontrollerte produkter)
    -   Vis lagerbeholdning per beholdningsstatus

    Lagerbeholdning for produktet vises på følgende måter:
    -   Etter fysisk lager (denne visningen representerer den totale mengden).
    -   Etter fysisk reservert (denne visningen representerer den reserverte mengden).
    -   Etter fysisk tilgjengelig (denne visningen representerer tilgjengelig mengde uten reservasjoner.)

