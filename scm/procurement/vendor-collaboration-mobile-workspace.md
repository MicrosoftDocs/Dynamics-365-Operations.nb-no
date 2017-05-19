---
title: "Mobil område for leverandørsamarbeid for Microsoft Dynamics 365 for Operations-appen"
description: "Med det mobile området for leverandørsamarbeid kan leverandørene kan holde seg oppdaterte på bestillinger som er sendt til dem for godkjenning, og vise informasjon om nye og oppdaterte bestillinger og kontakter."
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
ms.custom: 267074
ms.assetid: 1d293b3a-2fa2-418d-9347-78c2809d67fe
ms.search.region: global
ms.author: mkirknel
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: d5157e6f4b10b6158aa08279a9f68dae676f5666
ms.contentlocale: nb-no
ms.lasthandoff: 04/25/2017


---

# <a name="vendor-collaboration-mobile-workspace-for-microsoft-dynamics-365-for-operations-app"></a>Mobil område for leverandørsamarbeid for Microsoft Dynamics 365 for Operations-appen

[!include[banner](../includes/banner.md)]


Med det mobile området for leverandørsamarbeid kan leverandørene kan holde seg oppdaterte på bestillinger som er sendt til dem for godkjenning, og vise informasjon om nye og oppdaterte bestillinger og kontakter.

<a name="prerequisites"></a>Forutsetninger
-------------

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Forutsetning</th>
<th>beskrivelse</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Les om Microsoft Dynamics 365 for Operations-mobilplattform</td>
<td><a href="https://ax.help.dynamics.com/en/wiki/mobile-development-handbook/">Dynamics 365 for Operations-mobilplattform</a></td>
</tr>
<tr class="even">
<td>Dynamics 365 for Operations</td>
<td>Pass på at du bruker et miljø som har Microsoft Dynamics 365 for Operations versjon 1611 og for Microsoft Dynamics for Operations plattformoppdatering 3 (november 2016).</td>
</tr>
<tr class="odd">
<td><span style="color: #000000">Mobilenhet som har Dynamics 365 for Operations-appen installert</span></td>
<td><span style="color: #000000">Last ned Dynamics 365 for Operations-appen fra appbutikken for mobilenheten.</span></td>
</tr>
<tr class="even">
<td>Hurtigreparasjon KB 4013633</td>
<td>Installer hurtigreparasjonen for å aktivere arbeidsområder som finnes i Dynamics 365 for Operations.</td>
</tr>
<tr class="odd">
<td><span style="color: #ff0000"><span style="color: #000000">Hurtigreparasjon KB 3216943</span> </span></td>
<td>Installer hurtigreparasjonen for å aktivere det mobile området for leverandørsamarbeid.</td>
</tr>
<tr class="even">
<td>Leverandørbrukeren må har tilgang til webgrensesnittet for leverandørsamarbeid i Dynamics 365 for Operations og angi en bruker for leverandørsamarbeid.</td>
<td>Følg fremgangsmåten som er beskrevet i emnene nedenfor, for å konfigurere og arbeide med webgrensesnittet for leverandørsamarbeid.
<ul>
<li><a href="https://ax.help.dynamics.com/en/wiki/using-vendor-collaboration-to-work-with-external-vendors/">Bruke leverandørsamarbeid for å arbeide med eksterne leverandører</a></li>
<li><a href="https://ax.help.dynamics.com/en/wiki/manage-vendor-collaboration-users/">Administrere brukere av leverandørsamarbeid</a></li>
<li><a href="https://ax.help.dynamics.com/en/wiki/set-up-and-maintain-vendor-collaboration/">Definere og vedlikeholde leverandørsamarbeid</a></li>
<li><a href="https://ax.help.dynamics.com/en/wiki/using-vendor-collaboration-to-work-with-customers-in-dynamics-365-for-operations/">Bruke leverandørsamarbeid for å arbeide med kunder i Dynamics 365 for Operations</a></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="overview"></a>Oversikt
Det mobile området for leverandørsamarbeid holder leverandører informert om nye bestillinger, slik at de kan se og svare på bestillinger i Dynamics 365 for Operations-webklienten. 

**Obs!** Det mobile arbeidsområdet som skal brukes som et supplement til webgrensesnittet for leverandørsamarbeid, ikke som en erstatning. 

Med det mobile arbeidsområdet for leverandørsamarbeid kan leverandørene vise nye bestillinger som er sendt til godkjenning. Det viser bestillingsinformasjon, for eksempel produkter, antall og forespurte leveringsdatoer. Prisinformasjon er tilgjengelig avhengig av konfigurasjonen for hver leverandør. 

Når brukere logger på som leverandør, vil de se hvilke bestillinger som er besvarte, eller hvilke bestillinger som fortsatt venter på kundehandling. Leverandøren kan ha foreslått en annen leveringsdato som ennå ikke er avtalt med kunden, slik at bestillingen venter på kundehandling. Leverandøren kan også se en liste over bestillinger som er bekreftet, men som ikke er levert ennå. 

For å svare på en bestilling må leverandøren bruke webgrensesnittet for leverandørsamarbeid, som er tilgjengelig i Dynamics 365 for Operations-webklienten. Dette er også der leverandøren får mer informasjon om bestillingen, for eksempel dokumentvedlegg, leveringsadresse per linje og tillegg som er knyttet til leverandøren. 

Med en spesiell sikkerhetsrolle kan leverandøren vise hvilke kontaktpersoner er registrert for en leverandørkonto. Med samme sikkerhetsrolle kan leverandøren vise statusen for brukerforespørsler som er sendt inn. 

Oppretting av nye kontakter og innsending av nye brukerforespørsler må gjøres i grensesnittet for leverandørsamarbeid, som er tilgjengelig i Dynamics 365 for Operations-webklienten. 

Med det mobile arbeidsområdet kan leverandøren:

-   Vise nye bestillinger som er sendt til leverandøren.
-   Vise bestillinger som leverandøren har svart på og som venter på kundehandling.
-   Vise bestillinger som er bekreftet og ikke er fullstendig mottatt.
-   Vise informasjon om kontaktpersonen som er registrert for leverandørkontoen (krever en tilleggsrolle for sikkerhet).
-   Vise informasjon om og følg statusen for en brukerforespørsel som er sendt inn av leverandøren (krever en tilleggsrolle for sikkerhet).

## <a name="get-started"></a>Kom i gang
Å komme i gang på den mobile enheten:

1.  Last ned og installer Microsoft Dynamics 365 for Operations-appen fra appbutikken for mobilenheten.
2.  Start appen på enheten.
3.  Skriv inn URL-adressen for Dynamics 365.
4.  Angi firmaet for å logge på. Skriv for eksempel **USMF**.
5.  Første gang du logger deg på, blir du bedt om brukernavn og passord for din Microsoft Dynamics 365 for Operations-konto.

Når du har logget på appen, vises ingen arbeidsområder. Hvis du vil vise arbeidsområder på mobilappen, må du først publisere ønskede arbeidsområder til Dynamics 365 for Operations-appen. Du må ha tillatelse for systemadministrasjon for å publisere arbeidsområdet.

1.  Start Dynamics 365 for Operations.
2.  Gå til **Systemadministrasjon** &gt; **Oppsett** &gt; **systemparametere**.
3.  Velg **Administrer mobilapp**.
4.  Velg arbeidsområdet **Leverandørsamarbeid** for å publisere til den mobile plattformen.
5.  Velg **Publiser arbeidsområde**.
6.  Oppdater enheten for å se de publiserte arbeidsområdene.
7.  Velg arbeidsområdet **Leverandørsamarbeid**. Siden nedenfor vil vises.

    [![Mobilapp for leverandørsamarbeid](./media/vendor-collaboration-mobile-app.png)](./media/vendor-collaboration-mobile-app.png)

## <a name="contacts"></a>Kontakter
På **Kontakter**-siden kan du se alle kontaktene som er definert for leverandørkontoen. Den viser kontaktpersonens navn, primære e-postadresse og brukeraliaset hvis de er tilgjengelige. Den viser også om kontaktpersonens brukerkonto er aktiv. Når du velger en kontakt, kan du se kontaktinformasjon, for eksempel hvilke juridiske enheter personen er kontaktperson for, og kontaktinformasjon som telefonnummer eller en annen e-postadresse.

## <a name="user-requests"></a>Brukerforespørsler
Siden **Brukerforespørsler** lar deg se alle brukerforespørslene som du har sendt inn via webgrensesnittet for leverandørsamarbeid, og følge statusen. Når du velger en brukerforespørsel, kan du se hva som ble forespurt, legge til eller deaktivere en bruker, endre sikkerhet og se hvilke sikkerhetsroller som ble forespurt for brukeren.

## <a name="purchase-orders-ready-for-review"></a>Bestillinger som er klare for vurdering
Siden **Bestillinger som er klare for vurdering** lar deg se alle bestillingene som ble sendt av kunden og som er ikke besvart. Du kan vise valgte informasjon om bestillingen, for eksempel hvilke produkter som er forespurt og når de skal leveres. Prisinformasjon er bare tilgjengelig hvis dette er konfigurert for leverandøren. Du kan se om bestillingen har notater eller vedlegg. Hvis du vil åpne vedlegg, må du bruke leverandørsamarbeid i webklienten. Velg **Bestillingslinje** for å se alle linjene med detaljer. Legg merke til at for hver linje viser indikator om det finnes merknader eller vedlegg, eller om det er en leveringsadresse som er forskjellig fra hva som vises i hodet. Hvis du vil svare på bestillingen, må du bruke webklienten for leverandørsamarbeid.

## <a name="awaiting-customer-action"></a>Venter på kundehandling
Siden **Venter på kundehandling** lar deg finne bestillinger som du, eller andre i firmaet som også har tilgang til leverandørsamarbeid, har svart på. Bestillingene vises bare i denne listen hvis kunden skal utføre én av handlingene nedenfor på bestillingen.

-   Hvis bestillingen ble avvist, må kunden må oppdatere den sendte bestillingen og sende den på nytt, eller avbryte bestillingen og send den på nytt. Når bestillingen er sendt på nytt, forsvinner den fra siden **Venter på kundehandling**.
-   Hvis bestillingen ble godkjent med endringer, må kunden oppdatere den opprinnelige bestillingen og sende den på nytt til vurdering, eller oppdatere den i henhold til endringene og bekrefte den umiddelbart. I begge tilfeller forsvinner bestillingen den fra siden **Venter på kundehandling**.
-   Hvis bestillingen ble godtatt og vises på siden **Venter på kundehandling**, er dette fordi bestillingen ikke ble automatisk bekreftet da godkjenningen ble utført. Den venter på at en innkjøpsagent skal endre bestillingen til Bekreftet. Bestillingen anses vanligvis som en avtale mellom kunden og leverandøren så snart leverandøren godtar bestillingen. Flytting av bestillingen til statusen Bekreftet er en formalitet.

Når du velger bestillingen, vises flere detaljer om svaret. Du kan se linjedetaljene og svaret for hver linje. Linjestatusen viser hvilke av svarene nedenfor som er gitt.

-   Godtatt
-   Avslått
-   Godtatt med endringer
-   Erstattet/erstatt
-   Del inn i tidsplanen/tidsplanlinje

Vær oppmerksom på at en indikator viser **Levering**= ja/nei, som brukes til å angi at linjene ikke skal leveres. Dette kan skyldes at linjen ble avvist eller erstattet der de opprinnelige linjene ikke forventes å bli levert, eller en linje som er delt inn i flere tidsplanlinjer og den opprinnelige linjen ikke forventes å bli levert som forespurt i den mottatte bestillingen. Alle endringer som gjøres i bestillingslinjen vises, bortsett fra opplastede notater og vedlegg, som du kan se ved hjelp av webgrensesnittet for leverandørsamarbeid.

## <a name="open-confirmed-orders"></a>Åpne bekreftede ordrer
Når bestillingen er bekreftet av kunden, noe som betyr at bestillingen er endret til Bekreftet-status, vises den i den åpne bekreftede bestillingen. Den forblir i listen til den er registrert som mottatt av kunden.





