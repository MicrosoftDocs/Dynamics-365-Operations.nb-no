---
title: "Mobilt arbeidsområde for registrering av prosjekttid"
description: "Dette emnet gir informasjon om det mobile arbeidsområdet for registrering av prosjekttid. Dette arbeidsområdet lar brukere angi og lagre tid mot et prosjekt ved hjelp av mobilenheten."
author: KimANelson
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 272101
ms.assetid: 4505f021-b9bb-4b87-be24-6bf0bd88ee60
ms.search.region: Global
ms.search.industry: Service industries
ms.author: knelson
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: 9bf79af6eea6f899158fc3c8d523587cb11c90ad
ms.contentlocale: nb-no
ms.lasthandoff: 03/26/2018

---

# <a name="project-time-entry-mobile-workspace"></a>Mobilt arbeidsområde for registrering av prosjekttid

[!include[banner](../includes/banner.md)]

Dette emnet gir informasjon om det mobile arbeidsområdet for **registrering av prosjekttid**. Dette arbeidsområdet lar brukere angi og lagre tid mot et prosjekt ved hjelp av mobilenheten.

Dette mobile arbeidsområdet er ment å brukes med mobilappen Microsoft Dynamics 365 for Unified Operations. 

## <a name="overview"></a>Oversikt
Prosjektressurser er ofte på stedet eller reiser som en del av det daglige arbeidet. Det mobile arbeidsområdet **Registrering av prosjekttid** lar brukere angi fakturerbar eller ikke-fakturerbar tid mot et prosjekt på mobilenheten etter eget valg. Derfor kan prosjektressurser registrere oppføringer når som helst og hvor som helst. De kan også vise oppføringer som allerede er registrert. 

I det mobile arbeidsområdet **Tidsoppføring for prosjekt** kan brukere utføre disse oppgavene:

-   For en valgt dato kan du angi hvor mange timer du har brukt på en bestemt oppgave.
-   Søke etter prosjektnavn eller kunde til å finne prosjektet å angi tid for.
-   Angi kategori og aktivitet for tiden du har brukt.
-   Registrere tiden som fakturerbar eller ikke-fakturerbar for prosjektet.
-   Du kan også angi eventuelle eksterne eller interne kommentarer.

## <a name="prerequisites"></a>Forutsetninger
Forutsetningene varierer avhengig av hvilken versjon av Microsoft Dynamics 365 som er distribuert i organisasjonen.

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-for-finance-and-operations"></a>Forutsetninger hvis du bruker Microsoft Dynamics 365 for Finance and Operations
Hvis Microsoft Dynamics 365 for Finance and Operations har blitt innført i organisasjonen din, må systemadministrator publisere det mobile arbeidsområdet **Tidsoppføring for prosjekt**. Hvis du vil ha instruksjoner, kan du se [Publisere et mobilt arbeidsområde](../../dev-itpro/mobile-apps/publish-mobile-workspace.md).

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

<td>Implementer KB 4018050.</td>
<td>Systemansvarlig</td>
<td>KB 4018050 er en X++-oppdatering eller metadatahurtigreparasjon som inneholder det mobile arbeidsområdet for <strong>registrering av prosjekttid</strong>. Systemadministrator må følge trinnene nedenfor for å implementere KB 4018050.
<ol>
<li><a href="../../dev-itpro/migration-upgrade/download-hotfix-lcs.md">Last ned hurtigreparasjonen for metadata fra Microsoft Dynamics Lifecycle Services (LCS)</a>.</li>
<li><a href="../../dev-itpro/migration-upgrade/install-metadata-hotfix-package.md">Installer hurtigreparasjonen for metadata</a>.</li>
<li><a href="../../dev-itpro/deployment/create-apply-deployable-package.md">Opprett en distribuerbar pakke</a> som inneholder modellene <strong>ApplicationSuite</strong> og <strong>ProjectMobile</strong>, og laste deretter opp den distribuerbare pakken til LCS.</li>
<li><a href="../../dev-itpro/deployment/apply-deployable-package-system.md">Bruk den distribuerbare pakken</a>.</li>

</ol></td>
</tr>
<tr class="even">
<td>Publiser det mobile arbeidsområdet <strong>Tidsoppføring for prosjekt</strong>.</td>
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

## <a name="enter-time-by-using-the-project-time-entry-mobile-workspace"></a>Angi tid ved hjelp av det mobile arbeidsområdet Registrering av prosjekttid
1.  Velg arbeidsområdet **Registrering av prosjekttid** på mobilenheten.
2.  Velg **Tidsoppføring**. Du kan se kalenderdatoene for gjeldende uke.
3.  Velg **Handlinger** &gt; **Ny oppføring** for en valgt dato.
4.  Angi antallet timer som skal registreres.
5.  Velg prosjektet for timeregistreringen. Du kan se en liste over prosjekter som er lastet inn i ditt program for frakoblet bruk. 50 varer blir lastet inn som standard, men en utvikler kan endre dette antallet. Hvis du vil ha mer informasjon, kan du se [Mobil plattform](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md).
6.  Hvis prosjektet ikke finnes i listen, velger du **Søk etter**. Søk etter navn, eller bytt til å søke etter prosjektnavn eller kunde.
7.  Velg en kategori. Du kan se en liste over kategorier som er lastet inn i ditt program for frakoblet bruk. 50 varer blir lastet inn som standard, men en utvikler kan endre dette antallet. Hvis du vil ha mer informasjon, kan du se [Mobil plattform](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md).
8.  Hvis kategorien ikke finnes i listen, velger du **Søk etter**. Søk etter kategori, eller bytt til å søke etter kategorinavn.
9.  Velg en aktivitet. Du kan se en liste over aktiviteter som er lastet inn i ditt program for frakoblet bruk. 50 varer blir lastet inn som standard, men en utvikler kan endre dette antallet. Hvis du vil ha mer informasjon, kan du se [Mobil plattform](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md).
10. Hvis aktiviteten ikke finnes i listen, velger du **Søk etter**. Søke etter aktivitetsnummeret, eller bytt til å søke etter formål.

11. Velg linjeegenskapen.
12. Valgfritt: Angi eventuelle eksterne og interne kommentarer.
13. Velg **Ferdig**.

