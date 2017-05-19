---
title: "Mobilt arbeidsområde for lagerbeholdning"
description: "Dette emnet gir informasjon om det mobile arbeidsområdet for lagerbeholdning, som er tilgjengelig for Microsoft Dynamics 365 for Operations-mobilappen. Dette arbeidsområdet gir deg mobil innsikt i reservert og tilgjengelig lager når som helst og hvor som helst."
author: YuyuScheller
manager: AnnBe
ms.date: 04/21/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: annbe
ms.search.scope: Operations, Core
ms.custom: 267094
ms.assetid: 3fa385ba-894d-4a9e-b394-ef3697abf895
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mirzaab
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: e703ae80800b993ebca1c7bee455af1be41c7d5f
ms.contentlocale: nb-no
ms.lasthandoff: 04/25/2017


---

# <a name="inventory-on-hand-mobile-workspace"></a>Mobilt arbeidsområde for lagerbeholdning

[!include[banner](../includes/banner.md)]


Dette emnet gir informasjon om det mobile arbeidsområdet for lagerbeholdning, som er tilgjengelig for Microsoft Dynamics 365 for Operations-mobilappen. Dette arbeidsområdet gir deg mobil innsikt i reservert og tilgjengelig lager når som helst og hvor som helst.

<a name="overview-of-the-inventory-on-hand-mobile-workspace"></a>Oversikt over mobilt arbeidsområde for lagerbeholdning
--------------------------------------------------

Selskaper har vanligvis flere leveringer og flere mottak til lager hver dag. Disse flyttingene endrer kontinuerlig lagerbeholdningsstatusen. Det mobile arbeidsområdet for **lagerbeholdning** lar deg se status for firmaene i lagerbeholdningen, slik at du kan få den nyeste innsikten i lagerdata på den mobile enheten du velger. Uansett om du arbeider i lager, innkjøp, salg, produksjon eller management, eller har andre roller, kan du få tilgang til dataene i lagerbeholdningen når som helst og hvor som helst. Det mobile arbeidsområdet gir en umiddelbar oversikt over lagerstatusen på tvers av kontorer. Du kan vise lagerbeholdning på tvers av kontorer, gjeldende materialreservasjoner og ureservert lagerbeholdning. Du kan også angi varenumrene for å spørre om lagerbeholdning og filtrert søke etter produkter på lager eller varianter. Spesielt inneholder mobil arbeidsområdet disse funksjonene:

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
Før du kan bruke det mobile arbeidsområdet for **lagerbeholdning**, må du kontrollere at systemansvarlig har følgende forutsetninger på plass.

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
<td>Microsoft Dynamics 365 for Operations versjon 1611 med plattformoppdatering 3 eller senere må implementeres.</td>
<td>Systemansvarlig</td>
<td>Hvis du ikke allerede har Dynamics 365 for Operations distribuert i organisasjonen, bør systemansvarlig se <a href="http://ax.help.dynamics.com/en/wiki/deploy-an-ax7-demo-environment/">Distribuere et Microsoft Dynamics 365 for Operations-demomiljø</a>.</td>
</tr>
<tr class="even">
<td>KB 4013633 må være implementert.</td>
<td>Systemansvarlig</td>
<td>KB 4013633 (en X++ oppdatering eller hurtigreparasjon for metadata) inneholder fire mobile arbeidsområder for forsyningskjedeadministrasjon. Systemadministrator må følge disse trinnene for å implementere KB 4013633:
<ol>
<li>Last ned KB 4013633 fra Microsoft Dynamics Lifecycle Services (LCS).</li>
<li><a href="https://ax.help.dynamics.com/en/wiki/configuring-and-installing-a-metadata-hotfix-package/">Installer hurtigreparasjonen for metadata</a>.</li>
<li><a href="https://ax.help.dynamics.com/en/wiki/create-and-apply-a-deployable-package/">Opprett en distribuerbar pakke</a> som inneholder <strong>SCMMobile</strong>-modellen, og last deretter opp den distribuerbare pakken til LCS.</li>
<li><a href="https://ax.help.dynamics.com/en/wiki/apply-a-deployable-package-on-a-dynamics-ax-system/">Bruk den distribuerbare pakken</a> på Dynamics 365 for Operations-systemet.</li>
</ol></td>
</tr>
<tr class="odd">
<td>Det mobile arbeidsområdet for <strong>lagerbeholdning</strong> må publiseres til Dynamics-365 for Operations-mobilappen.</td>
<td>Systemansvarlig</td>
<td><ol>
<li>Start Dynamics 365 for Operations i nettleseren.</li>
<li>På siden <strong>Systemparametere</strong> velger du <strong>Behandle mobile arbeidsområder</strong>.</li>
<li>Velg arbeidsområdet <strong>Lagerbeholdning</strong>.</li>
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

## <a name="view-the-onhand-inventory-for-a-product-by-using-the-inventory-onhand-mobile-workspace"></a>Vise lagerbeholdningen for et produkt ved å bruke det mobile arbeidsområdet for lagerbeholdning
1.  Velg **Lagerbeholdning**-arbeidsområdet på mobilenheten.
2.  Velg **Kontroller lagerbeholdning for en vare**. Du kan se en liste over produkter som er lastet inn i ditt program for frakoblet bruk. 50 varer blir lastet inn som standard, men en utvikler kan endre dette antallet. Utviklere kan se [Dynamics 365 for Operations-mobilplattform](http://ax.help.dynamics.com/en/wiki/mobile-development-handbook/) for mer informasjon.
3.  Hvis elementet ikke finnes i listen, velger du **Søk mer** for å utføre en online søk i Dynamics 365 for Operations. Søk etter produktnummer, eller bytte til et søk etter produktnavn.
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






