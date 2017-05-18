---
title: "Leverandørsamarbeid med eksterne leverandører"
description: "Dette emnet forklarer hvordan innkjøpsagenter samarbeide med eksterne leverandører for å utveksle informasjon om bestillinger og forsendelseslager."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 221264
ms.assetid: dde49743-1541-4353-a030-63ca3069cd7d
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: c8947f9335b3a2de83ab00bad1043ee14d35f2c8
ms.contentlocale: nb-no
ms.lasthandoff: 04/25/2017


---

# <a name="vendor-collaboration-with-external-vendors"></a>Leverandørsamarbeid med eksterne leverandører

[!include[banner](../includes/banner.md)]


Dette emnet forklarer hvordan innkjøpsagenter samarbeide med eksterne leverandører for å utveksle informasjon om bestillinger og forsendelseslager.

Modulen **Leverandørsamarbeid** er beregnet på leverandører som ikke har integrering av utveksling av elektroniske data (EDI) med Microsoft Dynamics 365 for Operations. Det lar leverandører arbeide med bestillings-, faktura- og forsendelseslagerinformasjon. Dette emnet beskriver hvordan du kan samarbeide med eksterne leverandører som bruker grensesnittet for leverandørsamarbeid for å arbeide med bestillinger og forsendelseslager. Det beskriver også hvordan du aktiverer bruk av leverandørsamarbeid for en bestemt leverandør, og hvordan du definerer opplysningene alle leverandører ser når de svarer på en bestilling. Hvis du vil ha mer informasjon om hva eksterne leverandører kan gjøre i grensesnittet for leverandørsamarbeid, kan du se [Leverandørsamarbeid med kunder](vendor-collaboration-work-customers-dynamics-365-operations.md).  

Hvis du vil ha mer informasjon om hvordan leverandører kan bruke leverandørsamarbeid i faktureringsprosesser, kan du se [Arbeidsområde for leverandørsamarbeidsfakturering](/dynamics365/operations/financials/accounts-payable/vendor-portal-invoicing-workspace). Hvis du vil ha informasjon om hvordan du klargjør en ny bruker for leverandørsamarbeid, kan du se[Administrere brukere av leverandørsamarbeid](manage-vendor-collaboration-users.md).

## <a name="define-the-information-shown-to-vendors-when-they-respond-to-pos"></a>Angi informasjonen som vises til leverandører når de svarer på bestillinger
Når leverandører svarer på en bestilling du sender dem, ser de se en dialogboks der de må bekrefte at de vil godta, avvise, eller godta bestillingen med endringene. Informasjonen som skal vises på til leverandøren på dette tidspunktet, må være spesifikke for din virksomhet, slik at du kan angi teksten som vises i hver av de tre bekreftelsesmeldingene. Teksten kan for eksempel informere leverandøren om de neste trinnene i prosessen, eller om vilkår og betingelser.  

Slik definerer du teksten som vises i bestillingssvaret:

1.  Åpne siden **Informasjon for leverandører som svarer på bestillinger**.
2.  Velg én av svartypene.
3.  Klikk **Rediger**.
4.  Angi informasjonen som du vil at leverandører skal se i **Informasjonsmelding**-boksen.

Hvis du vil legge til meldinger på flere språk, kan du opprette egne meldinger med de aktuelle språkkodene. Meldingen vises til leverandøren på språket de bruker.

## <a name="set-the-vendor-collaboration-options-for-a-specific-vendor"></a>Angi alternativer for leverandørsamarbeid for en bestemt leverandør
De generelle innstillingene for leverandørsamarbeid i Dynamics 365 for Operations konfigureres av administrator. De vil for eksempel bestemmer hvilke sikkerhetsroller som er tilgjengelige for alle leverandørene som du samarbeider med. Det finnes også noen innstillinger som kan være forskjellige for hver leverandørkonto, og du bør angi disse:

-   Aktiver leverandørsamarbeid.
-   Bestem om du vil at leverandører skal se prisinformasjon.

### <a name="enable-vendor-collaboration"></a>Aktivere leverandørsamarbeid

Før du kan opprette brukerkontoer for en ekstern leverandør, må du konfigurere leverandørkontoen som lar dem å bruke leverandørsamarbeid. Hvis du vil gjøre dette, setter du feltet **Samarbeidsaktivering** til aktiv i kategorien **Generelt** på **Leverandører**-siden. Det er to alternativer du kan velge:

-   **Aktive (bestilling bekreftes automatisk)** – Bestillinger bekreftes automatisk når leverandøren godtar dem uten endringer.
-   **Aktive (bestilling bekreftes ikke automatisk)** – Bestillinger må bekreftes manuelt av organisasjonen etter at leverandøren har godtatt dem.

### <a name="decide-whether-you-want-the-vendor-to-see-price-information"></a>Bestemme om du vil at leverandører skal se prisinformasjon

Hvis du vil dele prisinformasjon, for eksempel enhetspris, rabatter og tillegg via grensesnittet for samarbeid, må du sette alternativet **Priser/beløp for bestilling** til **Ja** i leverandørkontoen. Dette alternativet er tilgjengelig i kategorien **Bestillingsstandarder**.

## <a name="work-with-pos-when-using-vendor-collaboration"></a>Arbeide med bestillinger med leverandørsamarbeid
### <a name="sending-a-po-to-the-vendor"></a>Sende en bestilling til leverandøren

Bestillinger klargjøres i Dynamics 365 for Operations. Når bestillingen har statusen **Godkjent**, sender du den til leverandøren ved hjelp av handlingen **Send for bekreftelse** på **Bestilling**-siden. Statusen for bestillingen endres til **Til ekstern vurdering**. Etter at bestillingen er sendt, kan leverandøren se den på siden **Bestillinger for vurdering** i grensesnittet for leverandørsamarbeid, der de kan godta, avvise eller foreslå endringer i ordren. Leverandøren kan også legge til merknader for å formidle informasjon, for eksempel endringer i bestillingen. Hvis du vil trekke leverandørens oppmerksomhet til en ny bestilling, kan du også bruke utskriftsbehandlingssystemet til å sende bestillingen via e-post.

### <a name="confirmation-and-acceptance-of-the-po-by-the-vendor"></a>Bekreftelse og godkjenning av bestillingen av leverandøren

Når en leverandør har godtatt en bestilling, kan bestillingen bekreftes automatisk, eller det kan hende den må bekreftes manuelt. Dette er avhengig av om feltet **Leverandøraktivering** er satt til **Aktiv (bestilling bekreftes automatisk)** for leverandøren, eller til **Aktiv (bestilling bekreftes ikke automatisk)**.  

Tabellen nedenfor viser den vanlige utveksling av informasjon, avhengig av hvordan leverandøren svarer når du sender dem en bestilling for bekreftelse.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Leverandørsvar</strong></td>
<td><strong>Resultat</strong></td>
</tr>
<tr class="even">
<td>Leverandøren <strong>godtar</strong> ordren. Dynamics 365 for Operations er konfigurert til automatisk å bekrefte bestillinger når leverandøren godtar.</td>
<td>Statusen for ordren oppdateres til <strong>Bekreftet</strong>. Hvis noe forhindrer at ordren blir oppdatert, registreres likevel leverandørsvaret som <strong>Godtatt</strong>, men statusen for bestillingen blir værende <strong>Til ekstern vurdering</strong>.</td>
</tr>
<tr class="odd">
<td>Leverandøren <strong>godtar</strong> ordren. Dynamics 365 for Operations er ikke konfigurert til automatisk å bekrefte bestillinger når leverandøren godtar.</td>
<td>Leverandørsvaret registreres som <strong>Godtatt</strong>, men statusen for bestillingen blir værende <strong>Til ekstern vurdering</strong>.</td>
</tr>
<tr class="even">
<td>Leverandøren <strong>avviser</strong> ordren.</td>
<td>Leverandørsvaret registreres som <strong>Avvist</strong>, og statusen for bestillingen blir værende <strong>Til ekstern vurdering</strong>. Avslaget mottas sammen med leverandørmerknaden.</td>
</tr>
<tr class="odd">
<td>Leverandøren <strong>godtar ordren med endringer</strong>. Endringer blir foreslått på linjenivå. Det er mulig å godta eller avvise enkeltlinjer. Andre mulige endringer omfatter:
<ul>
<li>Endre datoer eller antall.</li>
<li>Dele linjer for ulike leveringsdatoer eller antall.</li>
<li>Erstatte en vare.</li>
</ul>
Prisinformasjon og tillegg kan ikke endres av leverandøren. Forslag til endringer i disse kan gjøres ved hjelp av merknader.</td>
<td>Leverandørsvaret registreres som <strong>Godtatt med endringer</strong>, <strong></strong>og statusen for bestillingen blir forblir <strong>Til ekstern vurdering</strong>.</td>
</tr>
</tbody>
</table>

Du kan bruke arbeidsområdet **Bestillings****klargjøring** til å overvåke hvilke bestillinger leverandøren har svart på. Arbeidsområdet inneholder to lister som inneholder bestillinger med statusen **Til eksterne vurdering**:

-   Til ekstern vurdering krever handling.
-   Til ekstern vurdering, venter på svar fra leverandør.

### <a name="changing-a-po"></a>Endre en bestilling

Når du skal endre en bestilling som allerede er svart på, må du sende en ny versjon av bestillingen til leverandøren. Den nye bestillingen har et versjonssuffiks til å angi at det er en endret versjon av en bestilling som tidligere ble formidlet. Siden **Logg for leverandørbekreftelse for bestilling** lar deg og leverandørene spore historikken for hver ordre. Den tidligere bekreftede versjonen av bestillingen forblir i listen over bekreftede bestillinger til den nye bestillingen er bekreftet.

### <a name="cancelling-a-po"></a>Annullere en bestilling

Når du avbryter en bestilling, endres statusen til **Godkjent**. Du må sende bestillingen tilbake til leverandøren via leverandørportalen, slik at leverandøren kan bekrefte eller avvise annulleringen. Når annulleringen er bekreftet, vises bestillingen i leverandørens liste over bekreftede bestillinger som **Annullert**.

### <a name="adding-attachments-to-a-po"></a>Legge til vedlegg i en bestilling

Du kan legge til vedlegg, for eksempel filer, bilder og merknader, i bestillingen ved hjelp av dokumentbehandlingssystemet. Vedlegg som er lagt til med begrensningen av typen **Ekstern**, vil være synlig for leverandøren når du sender bestillingen til dem.

## <a name="purchase-order-statuses-and-versions"></a>Statuser og versjoner for bestilling
Denne delen beskriver de ulike statusene som en bestilling kan ha på tidspunktet den bekreftes, og på hvilket tidspunkt nye versjoner av bestillingen gjøres tilgjengelig for leverandøren. Det finnes forskjeller for dette avhengig av om du bruker endringsadministrasjon for bestillinger. 

### <a name="versions-and-statuses-if-you-dont-use-change-management"></a>Versjoner og status hvis du ikke bruker endringsadministrasjon

Tabellen nedenfor viser et eksempel på endringene i status og versjon som en bestilling kan gå gjennom.

|                                                                          |                                                                                                                                                              |
|--------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Handling**                                                               | **Status og versjon**                                                                                                                                       |
| Den første versjonen av Bestillingen opprettes i Dynamics 365 for Operations. | Statusen er **Godkjent**.                                                                                                                                  |
| Bestillingen er sendt til leverandøren.                                            | En versjon registreres i grensesnittet for leverandørsamarbeid, og statusen endres til **Til ekstern vurdering**.                                          |
| Leverandøren sender svaret **Godtatt med endringer**.                  | Statusen er fortsatt **Til ekstern vurdering**.                                                                                                                  |
| Du kan gjøre noen endringer som kreves av leverandøren.                  | Statusen endres til **Godkjent**.                                                                                                                        |
| Du sender den nye versjonen av bestillingen til leverandøren.                        | En ny versjon registreres i grensesnittet for leverandørsamarbeid, og statusen endres til **Til ekstern vurdering**.                                      |
| Leverandøren godtar den nye versjonen av bestillingen.                            | Statusen er fortsatt **Til ekstern vurdering** hvis ikke leverandørkontoen er konfigurert til å automatisk sette en bestilling til **Bekreftet**-tilstanden når de godkjenner den. |

Leverandører trenger ikke bekrefte bestillingen ved hjelp av grensesnittet for leverandørsamarbeid. De kan også sende en e-postmelding eller formidle at de godtar en bestilling via andre kanaler. Deretter kan du bekrefte ordren manuelt i Dynamics 365 for Operations. Hvis du gjør dette, får du en advarsel om at ordren blir bekreftet, selv om det ikke finnes noe svar fra leverandøren. Bestillingen vil vises i bekreftelsesloggen som en åpen bekreftet ordre som ikke har noen svar. Leverandøren vil ikke lenger ha muligheten til å bekrefte eller avvise bestillingen.  

**Obs!** Versjonen av bestillingen som er tilgjengelig for andre prosesser i Dynamics 365 for Operations, er alltid den nyeste versjonen, selv om denne versjonen ennå ikke er registrert i grensesnittet for leverandørsamarbeid.

### <a name="versions-and-statuses-if-you-use-change-management"></a>Versjoner og status hvis du bruker endringsadministrasjon

Hvis endringsadministrasjon er aktivert for bestillinger, går bestillingen gjennom en godkjenningsarbeidsflyt når den får statusen **Godkjent**. Denne prosessen er ikke synlig for leverandøren.  

Tabellen nedenfor viser et eksempel på endringene i status og versjon som en bestilling kan gå gjennom når endringsadministrasjon er aktivert: Versjonen registreres når bestillingen er godkjent, ikke når bestillingen sendes til leverandøren eller bekreftes.

|                                                                                                               |                                                                                                                                                                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Handling**                                                                                                    | **Status og versjon**                                                                                                                                                                                                                                                                                                                                                                      |
| Den første versjonen av Bestillingen opprettes i Dynamics 365 for Operations.                                      | Statusen er **Utkast**.                                                                                                                                                                                                                                                                                                                                                                    |
| Bestillingen sendes til godkjenningsprosessen. (Dette er en intern prosess som leverandøren ikke er involvert i.) | Statusen endres fra **Utkast** til **Til vurdering** til **Godkjenning** hvis bestillingen ikke avvises under godkjenningsprosessen. Den godkjente bestillingen registreres som en versjon.                                                                                                                                                                                                                     |
| Bestillingen er sendt til leverandøren                                                                                  | Versjon registreres i grensesnittet for leverandørsamarbeid, og statusen endres til **Til ekstern vurdering**.                                                                                                                                                                                                                                                                       |
| Du kan gjøre noen endringer som kreves av leverandøren.                                                       | Statusen endres tilbake til **Utkast**.                                                                                                                                                                                                                                                                                                                                                    |
| Bestillingen sendes til godkjenningsprosessen på nytt.                                                            | Statusen endres fra **Utkast** til **Til vurdering** til **Godkjenning** hvis bestillingen ikke avvises under godkjenningsprosessen. Systemet kan også konfigureres slik at spesifikke endringer i felter ikke krever ny godkjenning. I dette tilfellet endres statusen først til **Utkast** og oppdateres deretter automatisk til **Godkjent**. Den godkjente bestillingen registreres som en ny versjon. |
| Du sender den nye versjonen av bestillingen til leverandøren.                                                             | Den nye versjon registreres i grensesnittet for leverandørsamarbeid, og statusen endres til **Til ekstern vurdering**.                                                                                                                                                                                                                                                                   |
| Leverandøren godkjenner den nye versjonen av bestillingen.                                                                | Statusen endres til **Bekreftet**, enten automatisk eller når du mottar svaret fra leverandøren og deretter bekrefter bestillingen.                                                                                                                                                                                                                                                     |

## <a name="share-information-about-consignment-inventory"></a>Dele informasjon om forsendelseslager
Hvis du bruker forsendelseslager, kan leverandører bruke grensesnittet for leverandørsamarbeid til å vise informasjon på følgende sider:

-   **Bruk av forsendelseslager for bestillinger** – Bestillinger for forsendelseslager blir generert når eierskap av lageret endres fra leverandøren til firmaet. En produktkvittering posteres samtidig. Disse forsendelsesbestillingene vises bare på siden **Bruk av forsendelseslager for bestillinger**. De er ikke inkludert på siden **Alle bekreftede bestillinger** i modulen **Leverandørsamarbeid**.
-   **Produkter mottatt fra forsendelseslager** – Denne siden viser alle transaksjoner der eierskapet for produkter er blitt overført til fra leverandøren til firmaet. Leverandører kan bruke denne informasjonen for fakturere kunden.
-   **Forsendelseslager for beholdning** – Denne siden viser forsendelseslageret for beholdning som eies av leverandøren som er mottatt på lageret ditt.





