---
title: "Det mobile arbeidsområdet Salgsordrer"
description: "Dette emnet gir informasjon om det mobile arbeidsområdet for salgsordrer, som er tilgjengelig for Microsoft Dynamics 365 for Operations-mobilappen. Dette arbeidsområdet holder deg oppdatert om salgsordrene hvor som helst og når som helst."
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
ms.custom: 267134
ms.assetid: 0ce96511-002b-4de7-b31e-4303f94edc84
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mirzaab
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 119b80e5d8067ffbf75d8b067f4803558c2c94b0
ms.contentlocale: nb-no
ms.lasthandoff: 04/25/2017


---

# <a name="sales-orders-mobile-workspace"></a>Det mobile arbeidsområdet Salgsordrer

[!include[banner](../includes/banner.md)]


Dette emnet gir informasjon om det mobile arbeidsområdet for salgsordrer, som er tilgjengelig for Microsoft Dynamics 365 for Operations-mobilappen. Dette arbeidsområdet holder deg oppdatert om salgsordrene hvor som helst og når som helst. 

<a name="overview-of-the-sales-orders-mobile-workspace"></a>Oversikt over det mobile arbeidsområdet for salgsordrer
---------------------------------------------

Det mobile arbeidsområdet **Salgsordrer** har tilgang til Microsoft Dynamics 365 for Operations og lar deg vise detaljert informasjon om hver salgsordre. Denne informasjonen inkluderer statusen for ordren, kontaktinformasjon for kunden og kontaktinformasjon for ordremottakeren Det mobile arbeidsområdet **Salgsordrer** inneholder en øyeblikkelig visning av salgsordrer. Du kan vise alle salgsordrer, vise salgsordrer etter kunde eller vise informasjon om en bestemt salgsordre. Det mobile arbeidsområdet inneholder to visninger som lar deg analysere salgsordrer i dybden.

### <a name="view-all-sales-orders"></a>Vis alle salgsordrer

Denne visningen viser alle salgsordrer.

-   Bruk ett av filtrene nedenfor for velger salgsordren du vil vise:
    -   Søk etter salgsordre
    -   Søk etter kundekonto
    -   Søk etter kundenavn
    -   Søk etter status
    -   Søk etter frigivelsesstatus
    -   Søk etter opprettingsdato og -klokkeslett
-   Når du har valgt salgsordrene, kan du vise detaljene for bestemte ordrer. Du kan vise følgende informasjon:
    -   Informasjon om navn og adresse for kunde
    -   Forskjellige datoer for salgsordren, for eksempel ønsket forsendelsesdato og bekreftet forsendelsesdato
    -   Kontaktinformasjon for ordremottaker
    -   Kontaktinformasjon for kunde
    -   Ordrelinjer
    -   Forsendelser som viser hvordan og når en salgsordre ble levert

### <a name="view-orders-for-a-customer"></a>Vise ordrer for en kunde

Denne visningen viser salgsordrer etter kunde.

-   Bruk et av filtrene nedenfor for å vise ordrer for en kunde:
    -   Søk etter navn
    -   Søk etter konto
-   Når du velger en kunde, kan du vise følgende informasjon:
    -   Navn på kunde og gruppe
    -   Kontaktinformasjon for kunde
    -   Kundesalgsordrer og detaljer om salgsordrene:
        -   Informasjon om navn og adresse for kunde
        -   Forskjellige salgsordredatoer
        -   Kontaktinformasjon for ordremottaker
        -   Kontaktinformasjon for kunde
        -   Ordrelinjer
        -   Forsendelser som viser hvordan og når en salgsordre ble levert

## <a name="prerequisites"></a>Forutsetninger
Før du kan bruke det mobile arbeidsområdet for **Salgsordrer**, må du kontrollere at systemansvarlig har følgende forutsetninger på plass.

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
<td>Det mobile arbeidsområdet for <strong>Salgsordrer</strong> må publiseres til Dynamics-365 for Operations-mobilappen.</td>
<td>Systemansvarlig</td>
<td><ol>
<li>Start Dynamics 365 for Operations i nettleseren.</li>
<li>På siden <strong>Systemparametere</strong> velger du <strong>Behandle mobile arbeidsområder</strong>.</li>
<li>Velg arbeidsområdet <strong>Salgsordrer</strong>.</li>
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

## <a name="view-information-about-sales-orders-for-a-customer-by-using-the-mobile-workspace"></a>Vise informasjon om salgsordrer for en kunde ved å bruke det mobile arbeidsområdet
1.  Velg **Salgsordrer**-arbeidsområdet på mobilenheten.
2.  Velg **Vis ordrer for en kunde**.
3.  Bruk konto- eller kundenavninformasjon for å finne kunden.
4.  Velg kunden.
5.  Velg **Kontaktinformasjon** eller **Salgsordrer**. Hvis du velger **Salgsordrer**, vises en liste over salgsordrer for kunden.
6.  Velg **Salgsordre**. Du kan nå vise informasjon om salgsordrelinjer, informasjon om leveringer, kontaktinformasjon for kunden og kontaktinformasjon for ordremottaker.





