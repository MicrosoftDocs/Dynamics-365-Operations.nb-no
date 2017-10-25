---
title: "Det mobile arbeidsområdet Salgsordrer"
description: "Dette emnet gir informasjon om det mobile arbeidsområdet for salgsordrer. Dette arbeidsområdet holder deg oppdatert om salgsordrene hvor som helst og når som helst."
author: Mirzaab
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 267134
ms.assetid: 0ce96511-002b-4de7-b31e-4303f94edc84
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mirzaab
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: HT
ms.sourcegitcommit: d67ad79c068651f32ce7dc776bc460698557bc29
ms.openlocfilehash: abc117ad935b27cdfb15e43e4c12c9d0a65f176e
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---

# <a name="sales-orders-mobile-workspace"></a>Det mobile arbeidsområdet Salgsordrer

[!include[banner](../includes/banner.md)]

Dette emnet gir informasjon om det mobile arbeidsområdet **Salgsordrer**. Dette arbeidsområdet holder deg oppdatert om salgsordrene hvor som helst og når som helst. 

Dette mobile arbeidsområdet er ment å brukes med mobilappen Microsoft Dynamics 365 for Unified Operations.

## <a name="overview"></a>Oversikt
På det mobile arbeidsområdet **Salgsordrer** kan du vise detaljert informasjon om hver salgsordre. Denne informasjonen inkluderer statusen for ordren, kontaktinformasjon for kunden og kontaktinformasjon for ordremottakeren Det mobile arbeidsområdet **Salgsordrer** inneholder en øyeblikkelig visning av salgsordrer. Du kan vise alle salgsordrer, vise salgsordrer etter kunde eller vise informasjon om en bestemt salgsordre. 

Det mobile arbeidsområdet inneholder to visninger som lar deg analysere salgsordrer i dybden.

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
Forutsetningene varierer avhengig av hvilken versjon av Microsoft Dynamics 365 som er distribuert i organisasjonen.

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-for-finance-and-operations-enterprise-edition-july-2017"></a>Forutsetninger hvis du bruker Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition (juli 2017) 
Hvis Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition (juli 2017) har blitt innført i organisasjonen din, må systemadministrator publisere det mobile arbeidsområdet **Salgsordrer**. Hvis du vil ha instruksjoner, kan du se [Publisere et mobilt arbeidsområde](../../dev-itpro/mobile-apps/publish-mobile-workspace.md).

### <a name="prerequisites-if-you-use-dynamics-365-for-operations-version-1611-with-platform-update-3-or-later"></a>Forutsetninger hvis du bruker Dynamics 365 for Operations versjon 1611 med plattformoppdatering 3 eller senere
Hvis Dynamics 365 for Operations versjon 1611 med plattformoppdatering 3 eller senere er distribuert i organisasjonen, må systemansvarlig oppfylle følgende forutsetninger. 

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

<td>KB 4013633 er en X++-oppdatering eller hurtigreparasjon for metadata som inneholder det mobile arbeidsområdet <strong>Salgsordrer</strong>. Systemadministrator må følge trinnene nedenfor for å implementere KB 4013633.
<ol>
<li><a href="../../dev-itpro/migration-upgrade/download-hotfix-lcs.md">Last ned hurtigreparasjonen for metadata fra Microsoft Dynamics Lifecycle Services (LCS)</a>.</li>
<li><a href="../../dev-itpro/migration-upgrade/install-metadata-hotfix-package.md">Installer hurtigreparasjonen for metadata</a>.</li>
<li><a href="../../dev-itpro/deployment/create-apply-deployable-package.md">Opprett en distribuerbar pakke</a> som inneholder <strong>SCMMobile</strong>-modellen, og last deretter opp den distribuerbare pakken til LCS.</li>
<li><a href="../../dev-itpro/deployment/apply-deployable-package-system.md">Bruk den distribuerbare pakken</a>.</li>

</ol></td>
</tr>
<tr class="even">
<td>Publiser det mobile arbeidsområdet <strong>Salsordrer</strong>.</td>
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

## <a name="view-information-about-sales-orders-for-a-customer-by-using-the-sales-order-mobile-workspace"></a>Vise informasjon om salgsordrer for en kunde ved å bruke det mobile arbeidsområdet Salgsordre

1.  Velg **Salgsordrer**-arbeidsområdet på mobilenheten.
2.  Velg **Vis ordrer for en kunde**.
3.  Bruk konto- eller kundenavninformasjon for å finne kunden.
4.  Velg kunden.
5.  Velg **Kontaktinformasjon** eller **Salgsordrer**. Hvis du velger **Salgsordrer**, vises en liste over salgsordrer for kunden.
6.  Velg **Salgsordre**. Du kan nå vise informasjon om salgsordrelinjer, informasjon om leveringer, kontaktinformasjon for kunden og kontaktinformasjon for ordremottaker.
