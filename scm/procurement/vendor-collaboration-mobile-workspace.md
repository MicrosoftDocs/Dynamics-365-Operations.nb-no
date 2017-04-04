---
title: "Leverandør mobile samarbeidsområde for Microsoft Dynamics 365 for operasjoner app"
description: "Med det leverandøren mobile samarbeidsområdet, leverandørene kan holde deg oppdatert på bestillinger som er sendt til dem for godkjenning og vise informasjon om nye og oppdaterte bestillinger og kontakter."
author: YuyuScheller
manager: AnnBe
ms.date: 2017-01-12 16 - 36 - 37
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 267074
ms.assetid: fe8e912d-8446-4584-8a24-d8892e9028cd
ms.search.region: global
ms.author: mkirknel
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: f77012e7b64b7f153103e9bbe91e8ded202b509a
ms.openlocfilehash: 9f441508b745d22218316128572c9ec6aeb7207b
ms.lasthandoff: 03/31/2017


---

# <a name="vendor-collaboration-mobile-workspace-for-microsoft-dynamics-365-for-operations-app"></a>Leverandør mobile samarbeidsområde for Microsoft Dynamics 365 for operasjoner app

Med det leverandøren mobile samarbeidsområdet, leverandørene kan holde deg oppdatert på bestillinger som er sendt til dem for godkjenning og vise informasjon om nye og oppdaterte bestillinger og kontakter.

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
<td>Les om Microsoft Dynamics-365 for mobil plattform for operasjoner</td>
<td><a href="/dynamics365/operations/dev-itpro/mobile-apps/mobile-platform">Dynamics 365 for mobil plattform for operasjoner</a></td>
</tr>
<tr class="even">
<td>Dynamics 365 for operasjoner</td>
<td>Pass på at du bruker et miljø som har Microsoft Dynamics 365 for operasjoner versjon 1611 og for Microsoft Dynamics for operasjoner plattform oppdatere 3 (November 2016).</td>
</tr>
<tr class="odd">
<td><span style="color: #000000;">Mobil enhet som Dynamics-365 for operasjoner app installert</span></td>
<td><span style="color: #000000;">Last ned Dynamics-365 for operasjoner app fra din mobile app lager.</span></td>
</tr>
<tr class="even">
<td>Hurtigreparasjonen KB 3215650</td>
<td>Installere hurtigreparasjonen for å aktivere arbeidsområder som finnes i Dynamics 365 for operasjoner.</td>
</tr>
<tr class="odd">
<td><span style="color: #ff0000;"><span style="color: #000000;">Hurtigreparasjonen KB 3216943</span> </span></td>
<td>Installere hurtigreparasjonen for å aktivere det leverandøren mobile samarbeidsområdet.</td>
</tr>
<tr class="even">
<td>Leverandør-brukeren må har tilgang til webgrensesnittet for leverandør-samarbeid i Dynamics 365 for operasjoner og angi en leverandør samarbeid bruker.</td>
<td>Følg fremgangsmåten som er beskrevet i følgende emner for å opprette og arbeide med leverandøren samarbeid webgrensesnittet.
<ul>
<li><a href="vendor-collaboration-work-external-vendors.md">Bruk leverandør samarbeid for å arbeide med eksterne leverandører</a></li>
<li><a href="manage-vendor-collaboration-users.md">Administrere brukere av leverandørsamarbeid</a></li>
<li><a href="set-up-maintain-vendor-collaboration.md">Konfigurere og vedlikehold leverandørsamarbeid</a></li>
<li><a href="vendor-collaboration-work-customers-dynamics-365-operations.md">Bruk leverandør-samarbeid til å arbeide med kunder i Dynamics 365 for operasjoner</a></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="overview"></a>Oversikt
Leverandør mobile samarbeidsområdet beholder leverandører informert om nye bestillinger slik at de kan se og svare bestillinger i Dynamics-365 for operasjoner-webklienten.  

**Merk:** mobile arbeidsområdet som skal brukes som et supplement til webgrensesnittet leverandør samarbeid, men ikke en erstatning.  

Leverandørene kan vise nye bestillinger som er sendt til godkjenning med leverandøren samarbeid mobil arbeidsområdet. Det viser bestillingsinformasjon, for eksempel varer, antall og forespurte leveringsdatoer. Prisinformasjon er tilgjengelig, avhenger av konfigurasjonen for hver leverandør.  

Når en bruker logger på som en leverandør, vil de se hvilke bestillinger har blitt besvart, eller hvilke bestillinger som fortsatt venter på kunde-handling. Leverandøren kan ha foreslått en annen leveringsdato ikke er ennå er avtalt med kunden slik at bestillingen som venter på kunde-handling. Leverandøren vil også se en liste over bestillinger som er bekreftet, men som ennå ikke er levert.  

Hvis du vil svare på en bestilling, har leverandøren du bruker leverandøren samarbeid web-grensesnittet som er tilgjengelig i Dynamics-365 for operasjoner-webklienten. Dette er også der leverandøren vil ha mer informasjon om ordren, for eksempel dokument-vedlegg, adresse per linje og tillegg som er knyttet til leverandøren.  

Leverandøren kan vise hvilken kontakt personer er registrert for en leverandørkonto, med en spesiell sikkerhetsrolle. Leverandøren kan vise statusen for en brukerforespørsel som er sendt med samme sikkerhetsrollen.  

Opprette nye kontakter og sende nye brukerforespørsler må gjøres i samarbeid leverandør-grensesnittet som er tilgjengelig i Dynamics-365 for operasjoner-webklienten.  

Med mobile arbeidsområdet kan leverandøren:

-   Vis nye bestillinger som er sendt til leverandøren.
-   Vis bestillinger som leverandøren har svart på og venter på kunde-handling.
-   Vis bestillinger som er i en tilstand som er bekreftet og ikke er fullstendig mottatt.
-   Vis informasjon om kontaktpersonen som er registrert for leverandørkontoen (krever en rolle for ekstra sikkerhet).
-   Vis informasjon om og følg statusen for en brukerforespørsel som leverandøren har sendt (krever en rolle for ekstra sikkerhet).

## <a name="get-started"></a>Kom i gang
Å komme i gang på den mobile enheten:

1.  På din mobile app-butikk, kan du laste ned og installere Microsoft Dynamics 365 for operasjoner app.
2.  Start programmet på enheten.
3.  Skriv inn URL-adressen Dynamics 365.
4.  Angi firmaet å logge på. Angi for eksempel **USMF**.
5.  Første gang du logger deg på, du blir bedt om brukernavn og passord for din Microsoft Dynamics-365 for kontoen for operasjoner. 

Når du logger deg på programmet, vises ingen arbeidsområder. Hvis du vil vise arbeidsområder på din mobile app, må du først publisere ønsket arbeidsområder til Dynamics-365 for operasjoner app. Du må system administrasjon tillatelse til å publisere arbeidsområdet.

1.  Starte Dynamics 365 for operasjoner.
2.  Gå til **systemadministrasjon**&gt;**Setup**&gt;**systemparametere**.
3.  Velg **behandle mobile app**.
4.  Velg arbeidsområdet **leverandøren samarbeid** til å publisere til mobil plattform.
5.  Velg **publisere arbeidsområde for**.
6.  Oppdatere enheten for å se de publiserte delte arbeidsområdene.
7.  Velg den **leverandøren samarbeid** arbeidsområde. Vil du neste side.

[![leverandør-samarbeid-mobil-app](./media/vendor-collaboration-mobile-app.png)](./media/vendor-collaboration-mobile-app.png)

## <a name="contacts"></a>Kontakter
Den **kontakter** -siden kan du se alle kontaktene som er definert for leverandørkontoen. Den viser kontaktpersonen navn, Primær e-post og aliaset for brukere hvis de er tilgjengelige. Den viser også om kontaktpersonens brukerkontoen er aktiv. Når du velger en kontakt, kan du se kontaktinformasjon, for eksempel hvilke juridiske enheter personen er kontaktperson for, og kontaktinformasjon som telefonnummer eller en annen e-postadresse.

## <a name="user-requests"></a>Brukerforespørsler
Den **brukerforespørsler** side kan du se alle brukeren ber om at du har sendt inn via webgrensesnittet leverandør samarbeid og følge status. Når du velger en brukerforespørsel, kan du se hva som ble forespurt, legge til eller deaktivere en bruker, endre sikkerhet og se hvilke sikkerhetsroller ble forespurt for brukeren.

## <a name="purchase-orders-ready-for-review"></a>Bestillinger som er klart for gjennomgang
Den **bestillinger som er klare for gjennomgang** side kan du se alle bestillinger som ble sendt av kunden, og er ikke besvart. Du kan vise valgte informasjon om ordren, for eksempel hvilke produkter har blitt bedt om og når du skal levere. Prisinformasjon er bare tilgjengelig hvis dette er konfigurert for leverandøren.  

Du kan se om bestillingen har notater eller vedlegg. Hvis du vil åpne et vedlegg, må du bruke leverandør-samarbeid i webklienten. Velg **bestillingslinje** til å vise alle linjer med detaljer. Legg merke til at for hver linje, en indikator viser om det finnes merknader eller vedlegg, eller hvis det er en leveringsadresse som er forskjellig fra hva som skal vises i hodet.  

Hvis du vil svare på bestillingen, må du bruke webklienten leverandør samarbeid.

## <a name="awaiting-customer-action"></a>Venter på kundehandling
Den **venter på kunde handlingen** siden kan du finne bestillinger som du eller noen i firmaet som har også tilgang til leverandøren samarbeid, har svart på. Bestillingene er bare synlige i denne listen hvis kunden skal utføre én av følgende handlinger på bestillingen.

-   Hvis bestillingen ble avvist, vil kunden enten må oppdatere sendte rekkefølgen og sende på nytt, eller avbryte bestillingen og Send på nytt. Når bestillingen sendes på nytt, forsvinner den fra den **venter på kunde handlingen** siden.
-   Hvis bestillingen ble godkjent med endringer, må kunden til å oppdatere den opprinnelige ordren og Send til gjennomgang, eller oppdatere den i henhold til endringene og Bekreft det umiddelbart. I begge tilfeller forsvinner bestillingen fra den **venter på kunde handlingen** siden.
-   Hvis bestillingen ble godtatt og vises i den **venter på kunde handlingen** siden, er det fordi bestillingen ikke ble automatisk bekreftet når godkjenning ble utført. Venter på en innkjøper å endre rekkefølgen til bekreftet. Bestillingen vil vanligvis oppfattes som en avtale mellom kunden og leverandøren som leverandøren godtar rekkefølgen. Flytte bestillingen til statusen bekreftet, vil det være en formality.

Når du velger bestillingen, vises flere detaljer om svaret. Du kan se detaljer og svar for hver linje. Den linje status viser hvilke av følgende svar er gitt.

-   Godtatt
-   Avslått
-   Godtatt med endringer
-   Erstattet/erstatning
-   Delt inn i tidsplanen/linje

Vær oppmerksom på at en indikator viser **levere**= Ja/Nei, som brukes til å angi at linjene ikke skal leveres. Dette kan skyldes at linjen ble avvist eller erstattet der forventes ikke de opprinnelige linjene som skal leveres, eller en linje som er delt inn i flere linjer i tidsplanen og den opprinnelige linjen ikke forventes å bli levert som forespurt i rekkefølgen som er mottatt.  

Endringer som gjøres i rekkefølge linjen svaret vises, bortsett fra opplastede notater og vedlegg, som du kan se ved hjelp av webgrensesnittet for leverandør-samarbeid.

## <a name="open-confirmed-orders"></a>Åpne bekreftede ordrer
Når bestillingen er bekreftet av kunden, endres som betyr at bestillingen til bekreftet-status, vises den i den åpne bekreftede ordren. Forblir den i listen helt til den er registrert som mottatt av kunden.


