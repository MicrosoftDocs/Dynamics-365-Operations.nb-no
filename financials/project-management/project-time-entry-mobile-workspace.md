---
title: "Mobilt arbeidsområde for registrering av prosjekttid for Dynamics 365 for Operations-appen"
description: "Dette emnet gir informasjon om det mobile arbeidsområdet for registrering av prosjekttid. Dette arbeidsområdet lar brukere angi og lagre tid mot et prosjekt ved hjelp av mobilenheten."
author: annbe
manager: AnnBe
ms.date: 04/21/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: annbe
ms.search.scope: Operations, Core
ms.custom: 272101
ms.assetid: 4505f021-b9bb-4b87-be24-6bf0bd88ee60
ms.search.region: Global
ms.search.industry: Service industries
ms.author: annbe
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: e3e0be36c045acc3750efbb739d79d81ab937c65
ms.contentlocale: nb-no
ms.lasthandoff: 04/25/2017


---

# <a name="project-time-entry-mobile-workspace"></a>Mobilt arbeidsområde for registrering av prosjekttid

[!include[banner](../includes/banner.md)]

"[!include[banner](../includes/banner.md)]"


Dette emnet gir informasjon om det mobile arbeidsområdet for registrering av prosjekttid for Dynamics 365 for Operations-mobilappen. Dette arbeidsområdet lar brukere angi og lagre tid mot et prosjekt ved hjelp av mobilenheten.

<a name="overview-of-the-project-time-entry-mobile-workspace"></a>Oversikt over mobilt arbeidsområde for registrering av prosjekttid
---------------------------------------------------

Prosjektressurser er ofte på stedet eller reiser som en del av det daglige arbeidet. Det mobile arbeidsområdet **Registrering av prosjekttid** lar brukere angi fakturerbar eller ikke-fakturerbar tid mot et prosjekt på mobilenheten etter eget valg. Derfor kan prosjektressurser registrere oppføringer når som helst og hvor som helst. De kan også vise oppføringer som allerede er registrert. 

Det mobil arbeidsområdet **Registrering av prosjekttid** inneholder disse funksjonene:

-   For en valgt dato kan du angi hvor mange timer du har brukt på en bestemt oppgave.
-   Søke etter prosjektnavn eller kunde til å finne prosjektet å angi tid for.
-   Angi kategori og aktivitet for tiden du har brukt.
-   Registrere tiden som fakturerbar eller ikke-fakturerbar for prosjektet.
-   Du kan også angi eventuelle eksterne eller interne kommentarer.

Hvis du vil implementere det mobile arbeidsområdet **Registrering av prosjekttid**, kan du se avsnittene nedenfor i dette emnet.

## <a name="prerequisites"></a>Forutsetninger
Før du kan implementere det mobile arbeidsområdet for **registrering av prosjekttid**, må du kontrollere at systemansvarlig har fullført forutsetningene nedenfor.

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
<td>Hvis du ikke allerede har Dynamics 365 for Operations distribuert i organisasjonen, bør systemansvarlig se <a href="https://docs.microsoft.com/en-us/dynamics365/operations/dev-itpro/deployment/deploy-demo-environment">Distribuere et Microsoft Dynamics 365 for Operations-demomiljø</a>.</td>
</tr>
<tr class="even">
<td>KB 4018050 må være implementert.</td>
<td>Systemansvarlig</td>
<td>KB 4018050 er en X++-oppdatering eller metadatahurtigreparasjon som inneholder det mobile arbeidsområdet for <strong>registrering av prosjekttid</strong>. Systemadministrator må følge trinnene nedenfor for å implementere KB 4018050.
<ol>
<li>Last ned KB 4018050 fra Microsoft Dynamics Lifecycle Services (LCS).</li>
<li><a href="https://docs.microsoft.com/en-us/dynamics365/operations/dev-itpro/migration-upgrade/install-metadata-hotfix-package">Installer hurtigreparasjonen for metadata</a>.</li>
<li><a href="https://docs.microsoft.com/en-us/dynamics365/operations/dev-itpro/deployment/create-apply-deployable-package">Opprett en distribuerbar pakke</a> som inneholder modellene <strong>ApplicationSuite</strong> og <strong>ProjectMobile</strong>, og laste deretter opp den distribuerbare pakken til LCS.</li>
<li><a href="https://docs.microsoft.com/en-us/dynamics365/operations/dev-itpro/deployment/apply-deployable-package-system">Bruk den distribuerbare pakken</a> på Dynamics 365 for Operations-systemet.</li>
</ol></td>
</tr>
<tr class="odd">
<td>Det mobile arbeidsområdet for <strong>registrering av prosjekttid</strong> må publiseres til Dynamics-365 for Operations-mobilappen.</td>
<td>Systemansvarlig</td>
<td><ol>
<li>Start Dynamics 365 for Operations i nettleseren.</li>
<li>På siden <strong>Systemparametere</strong>, i kategorien <strong>Behandle mobil arbeidsområder</strong>, velger du arbeidsområdet <strong>Registrering av prosjekttid</strong>.</li>
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

## <a name="enter-time-by-using-the-project-time-entry-mobile-workspace"></a>Angi tid ved hjelp av det mobile arbeidsområdet Registrering av prosjekttid
1.  Velg arbeidsområdet **Registrering av prosjekttid** på mobilenheten.
2.  Velg **Tidsoppføring**. Du kan se kalenderdatoene for gjeldende uke.
3.  Velg **Handlinger** &gt; **Ny oppføring** for en valgt dato.
4.  Angi antallet timer som skal registreres.
5.  Velg prosjektet for timeregistreringen. Du kan se en liste over prosjekter som er lastet inn i ditt program for frakoblet bruk. 50 varer blir lastet inn som standard, men en utvikler kan endre dette antallet. Utviklere kan se [Dynamics 365 for Operations-mobilplattform](/dynamics365/operations/dev-itpro/mobile-apps/mobile-platform) for mer informasjon.
6.  Hvis prosjektet ikke finnes i listen, velger du **Søk** for å utføre en online-søk i Dynamics 365 for Operations. Søk etter navn, eller bytt til å søke etter prosjektnavn eller kunde.
7.  Velg en kategori. Du ser en liste over kategorier som er lastet inn i ditt program for frakoblet bruk. 50 varer blir lastet inn som standard, men en utvikler kan endre dette antallet. Utviklere kan se [Dynamics 365 for Operations-mobilplattform](/dynamics365/operations/dev-itpro/mobile-apps/mobile-platform) for mer informasjon.
8.  Hvis kategorien ikke finnes i listen, velger du **Søk** for å utføre en online-søk i Dynamics 365 for Operations. Søk etter kategori, eller bytt til å søke etter kategorinavn.
9.  Velg en aktivitet. Du kan se en liste over aktiviteter som er lastet inn i ditt program for frakoblet bruk. 50 varer blir lastet inn som standard, men en utvikler kan endre dette antallet. Utviklere kan se [Dynamics 365 for Operations-mobilplattform](/dynamics365/operations/dev-itpro/mobile-apps/mobile-platform) for mer informasjon.
10. Hvis aktiviteten ikke finnes i listen, velger du **Søk** for å utføre en online-søk i Dynamics 365 for Operations. Søke etter aktivitetsnummeret, eller bytt til å søke etter formål.
11. Velg linjeegenskapen.
12. Valgfritt: Angi eventuelle eksterne og interne kommentarer.
13. Velg **Ferdig**.






