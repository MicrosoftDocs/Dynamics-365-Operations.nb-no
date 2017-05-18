---
title: "Det mobile arbeidsområdet Reiseregning og utlegg"
description: "Dette emnet gir informasjon om det mobile arbeidsområdet for reiseregning og utlegg, som er tilgjengelig for Microsoft Dynamics 365 for Operations-mobilappen. Dette arbeidsområdet lar brukere registrere og laste opp en kvittering, slik at de kan knytte det til en reiseregningsrapport senere. Det mobile arbeidsområdet la også brukere raskt opprette en utgiftslinje ved hjelp av en tilknyttet kvittering."
author: annbe
manager: AnnBe
ms.date: 04/10/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: end user, IT Pro
ms.reviewer: annbe
ms.search.scope: Operations
ms.custom: 274023
ms.assetid: 3605eda1-a7ed-4675-8031-5279c5a8f5e4
ms.search.region: Global
ms.author: annbe
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: Human Translation
ms.sourcegitcommit: 8bc47c5b170fd7dd8f6288682aad6eae1d2dc09a
ms.openlocfilehash: 9d3b7a4d5184c3c4958f4298f1d3dd4de0cd06d6
ms.contentlocale: nb-no
ms.lasthandoff: 04/26/2017


---

# <a name="expense-management-mobile-workspace"></a>Det mobile arbeidsområdet Reiseregning og utlegg

[!include[banner](../includes/banner.md)]

"[!include[banner](../includes/banner.md)]"


Dette emnet gir informasjon om det mobile arbeidsområdet for reiseregning og utlegg, som er tilgjengelig for Microsoft Dynamics 365 for Operations-mobilappen. Dette arbeidsområdet lar brukere registrere og laste opp en kvittering, slik at de kan knytte det til en reiseregningsrapport senere. Det mobile arbeidsområdet la også brukere raskt opprette en utgiftslinje ved hjelp av en tilknyttet kvittering.

<a name="overview-of-the-expense-management-mobile-workspace"></a>Oversikt over mobilt arbeidsområde for reiseregning og utlegg
---------------------------------------------------

Mange organisasjoner krever at en kopi av en kvittering knyttes til en reiserelaterte eller forretningsrelatert reiseregningsrapport som en ansatt sender inn for refusjon. Dette mobile arbeidsområdet for **reiseregning og utlegg** lar brukere raskt opprette nye utgiftslinjer på mobilenheten etter eget valg, ved hjelp av et tilknyttet bilde av en kvittering. Brukere kan også ta et bilde av en kvittering, og deretter knytte den til en reiseregningsrapport senere. Det mobile arbeidsområdet for **reiseregning og utlegg** lar brukeren:

-   Ta et bilde av en kvittering og laste den opp til Microsoft Dynamics 365 for Operations. En bruker kan deretter knytte bildet til en reiseregningsrapport senere.
-   Laste opp en fil som en registrerte kvitteringer. En bruker kan deretter knytte filen til en reiseregningsrapport senere.
-   Opprette en ny utgiftslinje ved hjelp av en tilknyttet kvittering. En bruker kan deretter legge til linjeelementet i en reiseregningsrapport senere, og sende den inn til godkjenning og refusjon.

Resten av avsnittene i dette emnet forklarer hvordan du implementerer og bruke den det mobile arbeidsområdet for **reiseregning og utlegg**.

## <a name="prerequisites"></a>Forutsetninger
Før du kan implementere det mobile arbeidsområdet for **reiseregning og utlegg**, må du kontrollere at systemansvarlig har fullført forutsetningene nedenfor.

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
<td>KB 4019015 må være implementert.</td>
<td>Systemansvarlig</td>
<td>KB 4019015 (en X++ oppdatering eller hurtigreparasjon for metadata) inneholder fire mobile arbeidsområder for forsyningskjedeadministrasjon. Systemadministrator må følge disse trinnene for å implementere KB 4019015:
<ol>
<li>Last ned KB 4019015 fra Microsoft Dynamics Lifecycle Services (LCS).</li>
<li><a href="https://ax.help.dynamics.com/en/wiki/configuring-and-installing-a-metadata-hotfix-package/">Installer hurtigreparasjonen for metadata</a>.</li>
<li><a href="https://ax.help.dynamics.com/en/wiki/create-and-apply-a-deployable-package/">Opprett en distribuerbar pakke</a> som inneholder modellene <strong>ApplicationSuite</strong> og <strong>ExpenseMobile</strong>, og laste deretter opp den distribuerbare pakken til LCS.</li>
<li><a href="https://ax.help.dynamics.com/en/wiki/apply-a-deployable-package-on-a-dynamics-ax-system/">Bruk den distribuerbare pakken</a> på Dynamics 365 for Operations-systemet.</li>
</ol></td>
</tr>
<tr class="odd">
<td>Det mobile arbeidsområdet for <strong>reiseregning og utlegg</strong> må publiseres til Dynamics-365 for Operations-mobilappen.</td>
<td>Systemansvarlig</td>
<td><ol>
<li>Start Dynamics 365 for Operations i nettleseren.</li>
<li>På siden <strong>Systemparametere</strong> velger du <strong>Behandle mobile arbeidsområder</strong>.</li>
<li>Velg arbeidsområdet <strong>Reiseregning og utlegg</strong>.</li>
<li>Klikk <strong>Publiser mobilt arbeidsområde</strong>.</li>
</ol></td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-dynamics-365-for-operations-mobile-app"></a>Laste ned og installere Dynamics 365 for Operations-mobilappen
Last ned og installer Microsoft Dynamics 365 for Operations-appen fra appbutikken for mobilenheten.

-   For Android: [Dynamics 365 for Operations på Google Play-butikken](https://play.google.com/store/apps/details?id=com.microsoft.dynamics365.operations.mobile)
-   For iPhone: [Dynamics 365 for Operations på iTunes-appbutikken](https://itunes.apple.com/us/app/dynamics-365-for-operations/id1180836730?mt=8)
-   For Windows-telefon (Universal Windows Platform \[UWP\]): Kommer snart!

## <a name="sign-in-to-the-dynamics-365-for-operations-mobile-app"></a>Logg på Dynamics 365 for Operations-mobilappen
1.  Start appen på mobilenheten.
2.  Angi URL-adressen for Dynamics 365 for Operations.
3.  Angi firmaet for å logge på. Skriv for eksempel **USMF**.
4.  Første gang du logger deg på, du blir bedt om brukernavn og passord for din Dynamics 365 for Operations-konto. Angi legitimasjon.
5.  Når du har logget deg på, kan du se tilgjengelige arbeidsområder for firmaet. Legg merke til at hvis systemansvarlig senere publiserer et nytt arbeidsområde, kan du dra for å oppdatere listen over mobile arbeidsområder. [![Hent for å oppdatere](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)

## <a name="capture-a-receipt-by-using-the-expense-management-mobile-workspace"></a>Registrere en kvittering ved å bruke det mobile arbeidsområdet reiseregning og utlegg
1.  Velg arbeidsområdet **Reiseregning og utlegg** på mobilenheten.
2.  Velg **Registrer kvittering**.
3.  Velg **Ta bilde** eller **Velg bilde**.
4.  Hvis du har valgt **Ta bilde**, følger du denne fremgangsmåten:
    1.  Du kobles til kameraet på mobilenheten, slik at du kan ta et bilde av kvitteringen. Når du har tatt et bilde, klikker du på **OK** for å godta bildet.
    2.  Valgfritt: Angi et navn for bildet, og skriv inn eventuelle merknader.

     Hvis du har valgt **Velg bilde**, følger du denne fremgangsmåten:
    1.  Velg et bilde i listen.
    2.  Valgfritt: Angi et navn for bildet, og skriv inn eventuelle merknader.

5.  Velg **Ferdig**.

## <a name="quick-expense-entry-by-using-the-expense-management-mobile-workspace"></a>Hurtig utgiftsregistrering ved å bruke det mobile arbeidsområdet reiseregning og utlegg
1.  Velg arbeidsområdet **Reiseregning og utlegg** på mobilenheten.
2.  Velg **Hurtig utgiftsregistrering**.
3.  Velg kategorien for utgiften. Du ser en liste over utgifter som er lastet inn i appen for frakoblet bruk. Opptil 50 varer blir lastet inn som standard, men en utvikler kan endre dette antallet. Utviklere kan se [Dynamics 365 for Operations-mobilplattform](http://ax.help.dynamics.com/en/wiki/mobile-development-handbook/) for mer informasjon. Hvis kategorien ikke finnes i listen, velger du **Søk** for å utføre en online-søk i Dynamics 365 for Operations. Søk etter utgiftskategori, eller bytt til å søke etter utgiftstype.
4.  Angi transaksjonsdatoen for utgiften.
5.  Valgfritt: Angi forhandleren for utgiften.
6.  Angi utgiftsbeløpet.
7.  Angi valutaen for utgiften. Du ser en liste over valutakoder som er lastet inn i appen for frakoblet bruk. Opptil 400 valutaer blir lastet inn som standard, men en utvikler kan endre dette antallet. Utviklere kan se [Dynamics 365 for Operations-mobilplattform](http://ax.help.dynamics.com/en/wiki/mobile-development-handbook/) for mer informasjon. Hvis valutaen ikke finnes i listen, velger du **Søk** for å utføre en online-søk i Dynamics 365 for Operations. Søk etter valuta, eller bytt til å søke etter navn.
8.  Velg **Ta bilde** eller **Velg bilde**.
9.  Hvis du velger **Ta bilde**, kobles du til kameraet på mobilenheten, slik at du kan ta et bilde av kvitteringen. Når du har tatt et bilde, klikker du på **OK** for å godta bildet.  Hvis du velger **Velg bilde**, velge du et bilde i listen.
10. Velg **Ferdig**.






