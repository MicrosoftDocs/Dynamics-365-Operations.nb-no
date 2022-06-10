---
title: Det mobile arbeidsområdet Salgsordrer
description: Dette emnet gir informasjon om det mobile arbeidsområdet for salgsordrer. Dette arbeidsområdet holder deg oppdatert om salgsordrene hvor som helst og når som helst.
author: Henrikan
ms.date: 05/24/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: 267134
ms.assetid: 0ce96511-002b-4de7-b31e-4303f94edc84
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: henrikan
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: be9fd32f5f5d80bb9bce5f0de7e4ff92d6f5d28f
ms.sourcegitcommit: 336a0ad772fb55d52b4dcf2fafaa853632373820
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/28/2022
ms.locfileid: "8811574"
---
# <a name="sales-orders-mobile-workspace"></a>Det mobile arbeidsområdet Salgsordrer

[!include [banner](../includes/banner.md)]
[!include [mobile app deprecation](../../fin-ops-core/dev-itpro/includes/mobile-app-deprecation-banner.md)]

Dette emnet gir informasjon om det mobile arbeidsområdet **Salgsordrer**. Dette arbeidsområdet holder deg oppdatert om salgsordrene hvor som helst og når som helst. 

Dette mobile arbeidsområdet er ment å brukes sammen med Økonomi og drift (Dynamics 365)-mobilappen.

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

### <a name="prerequisites-if-you-use-supply-chain-management"></a>Forutsetninger hvis du bruker Supply Chain Management 
Hvis Supply Chain Management har blitt innført i organisasjonen din, må systemadministrator publisere det mobile arbeidsområdet **Salgsordrer**. Hvis du vil ha instruksjoner, kan du se [Publisere et mobilt arbeidsområde](../../fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace.md).

### <a name="prerequisites-if-you-use-dynamics-365-for-operations-version-1611-with-platform-update-3-or-later"></a>Forutsetninger hvis du bruker Dynamics 365 for Operations versjon 1611 med plattformoppdatering 3 eller senere
Hvis Dynamics 365 for Operations versjon 1611 med plattformoppdatering 3 eller senere er distribuert i organisasjonen, må systemansvarlig oppfylle følgende forutsetninger. 

<table>
<thead>
<tr class="header">
<th>Forutsetning</th>
<th>Rolle</th>
<th>Beskrivelse</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Implementere KB 4013633.</td>
<td>Systemansvarlig</td>

<td>KB 4013633 er en X++-oppdatering eller hurtigreparasjon for metadata som inneholder det mobile arbeidsområdet <strong>Salgsordrer</strong>. Systemadministrator må følge trinnene nedenfor for å implementere KB 4013633.
<ol>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/download-hotfix-lcs">Last ned hurtigreparasjonen for metadata fra Microsoft Dynamics Lifecycle Services (LCS)</a>.</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/install-metadata-hotfix-package">Installer hurtigreparasjonen for metadata</a>.</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/deployment/create-apply-deployable-package">Opprett en distribuerbar pakke</a> som inneholder <strong>SCMMobile</strong>-modellen, og last deretter opp den distribuerbare pakken til LCS.</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/deployment/apply-deployable-package-system">Bruk den distribuerbare pakken</a>.</li>

</ol></td>
</tr>
<tr class="even">
<td>Publiser det mobile arbeidsområdet <strong>Salsordrer</strong>.</td>
<td>Systemansvarlig</td>
<td>Se <a href="/dynamics365/fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace">Publisere et mobilt arbeidsområde</a>.</td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a>Laste ned og installere mobilappen
Last ned og installer mobilappen Økonomi og drift (Dynamics 365):

-   [For Android-telefoner](https://go.microsoft.com/fwlink/?linkid=850662)
-   [For iPhone](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a>Logge på mobilappen

1.  Start appen på mobilenheten.
2.  Skriv inn URL-adressen for Dynamics 365.
3.  Første gang du logger deg på, blir du bedt om brukernavn og passord. Angi legitimasjon.
4.  Når du har logget deg på, vises tilgjengelige arbeidsområder for firmaet. Legg merke til at hvis systemansvarlig senere publiserer et nytt arbeidsområde, må du oppdatere listen over mobile arbeidsområder.

[![Hent for å oppdatere.](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)

## <a name="view-information-about-sales-orders-for-a-customer-by-using-the-sales-order-mobile-workspace"></a>Vise informasjon om salgsordrer for en kunde ved å bruke det mobile arbeidsområdet Salgsordre

1.  Velg **Salgsordrer**-arbeidsområdet på mobilenheten.
2.  Velg **Vis ordrer for en kunde**.
3.  Bruk konto- eller kundenavninformasjon for å finne kunden.
4.  Velg kunden.
5.  Velg **Kontaktinformasjon** eller **Salgsordrer**. Hvis du velger **Salgsordrer**, vises en liste over salgsordrer for kunden.
6.  Velg **Salgsordre**. Du kan nå vise informasjon om salgsordrelinjer, informasjon om leveringer, kontaktinformasjon for kunden og kontaktinformasjon for ordremottaker.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
