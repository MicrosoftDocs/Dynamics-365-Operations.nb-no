---
title: Mobilt arbeidsområde for leverandørsamarbeid
description: Dette emnet gir informasjon om det mobile arbeidsområdet for leverandørsamarbeid. Dette arbeidsområdet hjelper leverandørene med å holde seg oppdatert om bestillinger som er sendt til dem for godkjenning. De kan også vise informasjon om nye og oppdaterte bestillinger og kontakter.
author: kamaybac
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: 267074
ms.assetid: 1d293b3a-2fa2-418d-9347-78c2809d67fe
ms.search.region: global
ms.author: dabourq
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 21187bbc287c66ca1aee259089b2bebbabb72fdaa459b77359c8c5555b6cd801
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6727852"
---
# <a name="vendor-collaboration-mobile-workspace"></a>Mobilt arbeidsområde for leverandørsamarbeid

[!include [banner](../includes/banner.md)]

Dette emnet gir informasjon om det mobile arbeidsområdet for **leverandørsamarbeid**. Dette arbeidsområdet hjelper leverandørene med å holde seg oppdatert om bestillinger som er sendt til dem for godkjenning. De kan også vise informasjon om nye og oppdaterte bestillinger og kontakter.

Dette mobile arbeidsområdet er ment å brukes sammen med Finance and Operations-mobilappen.

## <a name="overview"></a>Oversikt 
Det mobile området **Leverandørsamarbeid** holder leverandører informert om nye bestillinger, slik at de kan vise bestillinger og deretter svare på dem i webklienten. 

>[!NOTE]
> Det mobile arbeidsområdet skal brukes som et supplement til webgrensesnittet for leverandørsamarbeid, ikke som en erstatning. 

Leverandørene kan bruke det mobile arbeidsområdet for **leverandørsamarbeid** til å vise nye bestillinger som sendes til dem for godkjenning. Det viser bestillingsinformasjon, for eksempel produkter, antall og forespurte leveringsdatoer. Prisinformasjon er også tilgjengelig avhengig av konfigurasjonen for hver leverandør. 

En bruker som logger på som leverandør, vil de se hvilke bestillinger som er besvarte, og hvilke bestillinger som fortsatt venter på kundehandling. En bestilling kan for eksempel vente på kundehandling fordi leverandøren har foreslått en annen leveringsdato, men kunden har ikke godtatt denne datoen ennå. Leverandøren kan også se en liste over bestillinger som er bekreftet, men som ikke er levert ennå. 

For å svare på en bestilling må leverandøren bruke webgrensesnittet for leverandørsamarbeid, som er tilgjengelig i webklienten. Der kan leverandøren også få mer informasjon om bestillingen, for eksempel dokumentvedlegg, leveringsadressen per linje og tillegg som er knyttet til leverandøren. 

Leverandører som har en spesiell sikkerhetsrolle, kan se hvilke kontaktpersoner som er registrert for en leverandørkonto. Med samme sikkerhetsrolle kan leverandøren vise statusen for brukerforespørsler som er sendt inn. 

Webgrensesnittet for leverandørsamarbeid i webklienten må brukes til å opprette nye kontakter og sende nye brukerforespørsler. 

Det mobile arbeidsområdet for **leverandørsamarbeid** gjør det mulig for en leverandør å utføre disse oppgavene:

-   Vise nye bestillinger som er sendt til leverandøren.
-   Vise bestillinger som leverandøren har svart på og som venter på kundehandling.
-   Vise bestillinger som er bekreftet, men ennå ikke er mottatt fullstendig.
-   Vise informasjon om kontaktperson som er registrert for leverandørkontoen. (Denne oppgaven krever en ekstra sikkerhetsrolle.)
-   Vise informasjon om en brukerforespørsel som er sendt av leverandøren, og følge statusen for forespørselen. (Denne oppgaven krever en ekstra sikkerhetsrolle.)

## <a name="prerequisites"></a>Forutsetninger
Forutsetningene varierer avhengig av hvilken versjon av Microsoft Dynamics 365 som er distribuert i organisasjonen.

### <a name="prerequisites-if-you-use-supply-chain-management"></a>Forutsetninger hvis du bruker Supply Chain Management
Hvis Supply Chain Management har blitt innført i organisasjonen din, må systemadministrator publisere det mobile arbeidsområdet **Leverandørsamarbeid**. Hvis du vil ha instruksjoner, kan du se [Publisere et mobilt arbeidsområde](../../fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace.md).

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
<td>KB 3216943 må være implementert hvis du bruker plattformoppdatering 3.</td>
<td>Systemansvarlig</td>
<td>KB 3216943 er en binær oppdatering som er nødvendig hvis du bruker plattformoppdatering 3. Systemansvarlig må følge disse trinnene for å implementere denne KB-en.
<ol>
<li>Laste ned KB 3216943 fra Microsoft Dynamics Lifecycle Services (LCS).</li>
<li>Installer den binære oppdateringen, som leveres som en distribuerbar pakke. Hvis du vil ha informasjon om hvordan du bruker en distribuerbar pakke, kan du se <a href="/dynamics365/fin-ops-core/dev-itpro/deployment/apply-deployable-package-system">Bruke en distribuerbar pakke</a>.</li>
</ol></td>
</tr>
<tr class="even">
<td>KB 4013633 må være implementert.</td>
<td>Systemansvarlig</td>
<td>KB 4013633 er en X++-oppdatering eller metadatahurtigreparasjon som inneholder det mobile arbeidsområdet for <strong>lagerbeholdning</strong>. Systemadministrator må følge trinnene nedenfor for å implementere KB 4013633.
<ol>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/download-hotfix-lcs">Last ned hurtigreparasjonen for metadata fra LCS</a>.</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/install-metadata-hotfix-package">Installer hurtigreparasjonen for metadata</a>.</li><li><a href="/dynamics365/fin-ops-core/dev-itpro/deployment/create-apply-deployable-package">Opprett en distribuerbar pakke</a> som inneholder <strong>SCMMobile</strong>-modellen, og last deretter opp den distribuerbare pakken til LCS.</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/deployment/apply-deployable-package-system">Bruk den distribuerbare pakken</a>.</li>
</ol></td>
</tr>
<tr class="odd">
<td>Det mobile arbeidsområdet for <strong>leverandørsamarbeid</strong> må publiseres.</td><td>Systemansvarlig</td>
<td>Se <a href="/dynamics365/fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace">Publisere et mobilt arbeidsområde</a>.</td>
</tr>
<tr class="even">
<td>Leverandørbrukeren må ha tilgang til webgrensesnittet for leverandørsamarbeid i webklienten og må angi en bruker for leverandørsamarbeid.</td><td>Innkjøpsansvarlige og systemansvarlig</td>
<td>Følg fremgangsmåten i emnene nedenfor for å konfigurere og arbeide med webgrensesnittet for leverandørsamarbeid.
<ul>
<li><a href="vendor-collaboration-work-external-vendors.md">Bruke leverandørsamarbeid for å arbeide med eksterne leverandører</a></li>
<li><a href="manage-vendor-collaboration-users.md">Administrere brukere av leverandørsamarbeid</a></li>
<li><a href="set-up-maintain-vendor-collaboration.md">Definere og vedlikeholde leverandørsamarbeid</a></li>
<li><a href="vendor-collaboration-work-customers-dynamics-365-operations.md">Bruke leverandørsamarbeid for å arbeide med kunder i Supply Chain Managements</a></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a>Laste ned og installere mobilappen

Laste ned og installere Finance and Operations-mobilappen:

-   [For Android-telefoner](https://go.microsoft.com/fwlink/?linkid=850662)
-   [For iPhone](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a>Logge på mobilappen
1.  Start appen på mobilenheten.
2.  Angi URL-adressen for Microsoft Dynamics365.
4.  Første gang du logger deg på, blir du bedt om brukernavn og passord. Angi legitimasjon.
5.  Når du har logget deg på, vises tilgjengelige arbeidsområder for firmaet. Legg merke til at hvis systemansvarlig senere publiserer et nytt arbeidsområde, må du oppdatere listen over mobile arbeidsområder.

    [![Hent for å oppdatere.](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)

## <a name="use-the-vendor-collaboration-mobile-workspace"></a>Bruk det mobile arbeidsområdet for leverandørsamarbeid
Når du velger arbeidsområdet for **leverandørsamarbeid**, vises følgende alternativer.

![Mobilt arbeidsområde for leverandørsamarbeid.](./media/vendor-collaboration-mobile-app.png)

Arbeidsområdet for **leverandørsamarbeid** inneholder følgende sider.

### <a name="contacts"></a>Kontakter
På **Kontakter**-siden kan du se alle kontaktene som er definert for leverandørkontoen. Det viser kontaktpersonens navn, primære e-postadresse og brukeralias, hvis kontakten har et alias. Denne siden viser også om kontaktpersonens brukerkonto er aktiv. Når du velger en kontakt, kan du se kontaktdetaljer, for eksempel de juridiske enhetene som personen er kontaktperson for. Du kan også se kontaktopplysninger, for eksempel telefonnummer eller en alternativ e-postadresse.

### <a name="user-requests"></a>Brukerforespørsler
Siden **Brukerforespørsler** lar deg se alle brukerforespørslene som du har sendt inn via webgrensesnittet for leverandørsamarbeid. Du kan også følge statusen for disse forespørslene. Når du velger en brukerforespørsel, kan du se hva som ble forespurt, legge til eller deaktivere en bruker, endre sikkerhet og se hvilke sikkerhetsroller som ble forespurt for brukeren.

### <a name="purchase-orders-ready-for-review"></a>Bestillinger som er klare for vurdering
Siden **Bestillinger klare for vurdering** lar deg se alle bestillingene som ble sendt av kunden, men som du ikke ennå har besvart. Du kan vise valgt informasjon om bestillingen, for eksempel hvilke produkter som er forespurt og når disse produktene skal leveres. Prisinformasjon er også tilgjengelig avhengig av konfigurasjonen for leverandøren.

Du kan også se om bestillingen har notater eller vedlegg. For å åpne notater og vedlegg må du imidlertid bruke webgrensesnittet for leverandørsamarbeid i webklienten. Velg **Bestillingslinje** for å se alle linjene sammen med detaljene. For hver linje viser en indikator om det finnes merknader eller vedlegg, eller om leveringsadressen er forskjellig fra leveringsadressen som vises i hodet.

Hvis du vil svare på bestillingen, må du bruke webgrensesnittet for leverandørsamarbeid i webklienten.

### <a name="awaiting-customer-action"></a>Venter på kundehandling
Siden **Venter på kundehandling** lar deg finne bestillinger som du eller en annen person i firmaet som har tilgang til leverandørsamarbeid, har svart på. Bestillingene vises i denne listen bare hvis kunden skal utføre én av følgende handlinger på bestillingen:

-   Hvis bestillingen ble avvist, må kunden enten oppdatere eller avbryte den opprinnelige ordren og deretter sende den på nytt. Når bestillingen er sendt på nytt, vises den ikke lenger på siden **Venter på kundehandling**.
-   Hvis bestillingen ble godkjent med endringer, må kunden enten oppdatere den opprinnelige bestillingen og deretter sende den på nytt til vurdering, eller oppdatere ordren i henhold til de ønskede endringene og deretter bekrefte den umiddelbart. I begge tilfeller forsvinner bestillingen fra siden **Venter på kundehandling**.
-   Hvis bestillingen ble godtatt, men fortsatt vises på siden **Venter på kundehandling**, ble bestillingen ikke automatisk bekreftet da den ble godtatt. Den venter nå på at en innkjøpsagent skal endre bestillingsstatusen til **Bekreftet**. En bestilling anses vanligvis som en avtale mellom kunden og leverandøren så snart leverandøren godtar bestillingen. Oppdateringen til statusen **Bekreftet** er derfor vanligvis bare en formalitet.

Når du velger en bestilling, vises flere detaljer om svaret. Du kan se linjedetaljene og svaret for hver linje. Linjestatusen viser hvilke av svarene nedenfor som er gitt:

-   Godtatt
-   Avslått
-   Godtatt med endringer
-   Erstattet/erstatt
-   Del inn i tidsplanen/tidsplanlinje

Legg merke til at **Levering**-feltet settes til enten **Ja** eller **Nei** for å angi om linjene skal leveres. Det kan hende at en linje ikke kan leveres på grunn av følgende:

- Linjen ble avvist.
- En erstatning ble gjort, og den opprinnelige linjen forventes ikke å bli levert som forespurt i den mottatte bestillingen.
- Linjen ble delt inn i flere tidsplanlinjer, og den opprinnelige linjen forventes ikke å bli levert som forespurt i den mottatte bestillingen.

Alle endringer som er gjort i bestillingslinjesvaret, vises. Imidlertid blir ikke opplastede notater og vedlegg vist. For å åpne notater og vedlegg må du bruke webgrensesnittet for leverandørsamarbeid i webklienten.

### <a name="open-confirmed-orders"></a>Åpne bekreftede ordrer
Når bestillingen er bekreftet av kunden (noe som betyr at status for bestillingen er endret til **Bekreftet**-status), vises den i den åpne bekreftede bestillingen. Den forblir i listen til den er registrert som mottatt av kunden.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]