---
title: "Leverandørsamarbeid med eksterne leverandører"
description: "Dette emnet forklarer hvordan innkjøpsagenter samarbeide med eksterne leverandører for å utveksle informasjon om bestillinger og forsendelseslager."
author: BibiSp
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
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
ms.sourcegitcommit: b0aefc62f2d54da963f03dc74d492260722cd451
ms.openlocfilehash: aabb8277218895566edada3c74d99c02a83dae1e
ms.contentlocale: nb-no
ms.lasthandoff: 06/15/2017


---

# Leverandørsamarbeid med eksterne leverandører
<a id="vendor-collaboration-with-external-vendors" class="xliff"></a>

[!include[banner](../includes/banner.md)]


Dette emnet forklarer hvordan innkjøpsagenter samarbeide med eksterne leverandører for å utveksle informasjon om bestillinger og forsendelseslager.

Modulen **Leverandørsamarbeid** er beregnet på leverandører som ikke har integrering av utveksling av elektroniske data (EDI) med Microsoft Dynamics 365 for Finance and Operations. Det lar leverandører arbeide med bestillings-, faktura- og forsendelseslagerinformasjon. Dette emnet beskriver hvordan du kan samarbeide med eksterne leverandører som bruker grensesnittet for leverandørsamarbeid for å arbeide med bestillinger og forsendelseslager. Det beskriver også hvordan du aktiverer bruk av leverandørsamarbeid for en bestemt leverandør, og hvordan du definerer opplysningene alle leverandører ser når de svarer på en bestilling. Hvis du vil ha mer informasjon om hva eksterne leverandører kan gjøre i grensesnittet for leverandørsamarbeid, kan du se [Leverandørsamarbeid med kunder](vendor-collaboration-work-customers-dynamics-365-operations.md).  

Hvis du vil ha mer informasjon om hvordan leverandører kan bruke leverandørsamarbeid i faktureringsprosesser, kan du se [Arbeidsområde for leverandørsamarbeidsfakturering](/dynamics365/unified-operations/financials/accounts-payable/vendor-portal-invoicing-workspace). Hvis du vil ha informasjon om hvordan du klargjør en ny bruker for leverandørsamarbeid, kan du se[Administrere brukere av leverandørsamarbeid](manage-vendor-collaboration-users.md).

Hvis du vil ha mer informasjon om hvordan leverandører kan bruke leverandørsamarbeid i faktureringsprosesser, kan du se [Arbeidsområde for leverandørsamarbeidsfakturering](/dynamics365/operations/financials/accounts-payable/vendor-portal-invoicing-workspace). 

Hvis du vil ha informasjon om hvordan du klargjør en ny bruker for leverandørsamarbeid, kan du se[Administrere brukere av leverandørsamarbeid](manage-vendor-collaboration-users.md).

## Angi informasjonen som vises til leverandører når de svarer på bestillinger
<a id="define-the-information-that-is-shown-to-vendors-when-they-respond-to-pos" class="xliff"></a>
Når leverandører svarer på en bestilling du sender dem, ser de en meldingsboks der de må bekrefte at de vil godta, avvise, eller godta bestillingen med endringene. Ettersom informasjonen som skal vises på til leverandøren på dette tidspunktet, kan være spesifikk for din virksomhet, kan du angi teksten som vises i hver av de tre bekreftelsesmeldingene. Teksten kan for eksempel informere leverandøren om de neste trinnene i prosessen eller om vilkår og betingelser.  

Slik definerer du teksten som vises i bestillingssvaret:

1.  Åpne siden **Informasjon for leverandører som svarer på bestillinger**.
2.  Velg én av svartypene.
3.  Klikk **Rediger**.
4.  Angi informasjonen som du vil at leverandører skal se i **Informasjonsmelding**-boksen.

Hvis du må legge til meldinger på flere språk, kan du opprette egne meldinger og angi de aktuelle språkkodene for hver av dem. Meldingen som vises til leverandøren, vil være på språket som leverandøren bruker.

## Angi alternativer for leverandørsamarbeid for en bestemt leverandør
<a id="set-the-vendor-collaboration-options-for-a-specific-vendor" class="xliff"></a>
De generelle innstillingene for leverandørsamarbeid i Finance and Operations konfigureres av administrator. Administrator vil for eksempel bestemme hvilke sikkerhetsroller som er tilgjengelige for alle leverandørene som du samarbeider med. Det finnes også innstillinger som kan være forskjellige for hver leverandørkonto, og du bør angi disse:
-   Aktiver leverandørsamarbeid.
-   Bestem om du vil at leverandører skal se prisinformasjon.

### Aktivere leverandørsamarbeid
<a id="enable-vendor-collaboration" class="xliff"></a>

Før du kan opprette brukerkontoer for en ekstern leverandør, må du konfigurere leverandørkontoen som lar dem å bruke leverandørsamarbeid. Hvis du vil gjøre dette, setter du feltet **Samarbeidsaktivering** til aktiv i kategorien **Generelt** på **Leverandører**-siden. Det er to alternativer du kan velge:

-   **Aktive (bestilling bekreftes automatisk)** – Bestillinger bekreftes automatisk når leverandøren godtar dem uten endringer.
-   **Aktive (bestilling bekreftes ikke automatisk)** – Bestillinger må bekreftes manuelt av organisasjonen etter at leverandøren har godtatt dem.

### Bestemme om du vil at leverandører skal se prisinformasjon
<a id="decide-whether-you-want-the-vendor-to-see-price-information" class="xliff"></a>

Hvis du vil dele prisinformasjon, for eksempel enhetspris, rabatter og tillegg via grensesnittet for samarbeid, må du sette alternativet **Priser/beløp for bestilling** til **Ja** i leverandørkontoen. Dette alternativet er tilgjengelig i kategorien **Bestillingsstandarder**.

## Arbeide med bestillinger med leverandørsamarbeid
<a id="work-with-pos-when-using-vendor-collaboration" class="xliff"></a>
### Sende en bestilling til leverandøren
<a id="sending-a-po-to-the-vendor" class="xliff"></a>

Bestillinger klargjøres i Finance and Operations. Når bestillingen har statusen **Godkjent**, sender du den til leverandøren ved hjelp av handlingen **Send for bekreftelse** på **Bestilling**-siden. Statusen for bestillingen endres til **Til ekstern vurdering**. Etter at bestillingen er sendt, kan leverandøren se den på siden **Bestillinger for vurdering** i grensesnittet for leverandørsamarbeid. Leverandøren kan deretter godta ordren, avvise den eller foreslå endringer. Leverandøren kan også legge til merknader for å formidle informasjon, for eksempel endringer i bestillingen. Hvis du vil trekke leverandørens oppmerksomhet til en ny bestilling, kan du også bruke utskriftsbehandlingssystemet til å sende bestillingen via e-post.

### Bekreftelse og godkjenning av bestillingen av leverandøren
<a id="confirmation-and-acceptance-of-the-po-by-the-vendor" class="xliff"></a>

Når en leverandør har godtatt en bestilling, kan bestillingen bekreftes automatisk, eller det kan hende den må bekreftes manuelt. Dette er avhengig av om feltet **Leverandøraktivering** er satt til **Aktiv (bestilling bekreftes automatisk)** eller til **Aktiv (bestilling bekreftes ikke automatisk)** for leverandøren.  

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
<td>Leverandøren <strong>godtar</strong> ordren. Finance and Operations er konfigurert til automatisk å bekrefte bestillinger når leverandøren godtar.</td>

<td>Statusen for ordren oppdateres til <strong>Bekreftet</strong>. Hvis noe forhindrer at ordren blir oppdatert, registreres likevel leverandørsvaret som <strong>Godtatt</strong>, men statusen for bestillingen blir værende <strong>Til ekstern vurdering</strong>. 

Bestillingen som ble sendt til leverandøren, og som har statusen **Til ekstern vurdering**, oppdateres med bekreftede leveringsdatoer på linjene. Oppdateringen starter en ny versjon som oppdateres automatisk til **Bekreftet** status. Når bestillingen er bekreftet, vises den i grensesnittet for samarbeid for leverandøren.</td>
</tr>
<tr class="odd">
<td>Leverandøren <strong>godtar</strong> ordren. Finance and Operations er ikke konfigurert til automatisk å bekrefte bestillinger når leverandøren godtar.</td>
<td>Leverandørsvaret registreres som <strong>Godtatt</strong>, men statusen for bestillingen blir værende <strong>Til ekstern vurdering</strong>.

Bestillingen som ble sendt til leverandøren, og som har statusen **Til ekstern vurdering**, oppdateres med bekreftede leveringsdatoer på linjene. Oppdateringen starter en ny versjon som oppdateres automatisk til **Til ekstern vurdering**. Du kan deretter bekrefte bestillingen manuelt.</td>

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
<td>Leverandørsvaret registreres som <strong>Godtatt med endringer</strong>, og statusen for bestillingen forblir <strong>Til ekstern vurdering</strong>. Statusene viser hvilke typer endringer leverandøren har foreslått. For informasjon om automatisk forbruk av endringene kan du se delen nedenfor om hvordan du oppdaterer bestillingen når en leverandør foreslår endringer. </td>
</tr>
</tbody>
</table>

Du kan bruke arbeidsområdet **Bestillings****klargjøring** til å overvåke hvilke bestillinger leverandøren har svart på. Arbeidsområdet inneholder to lister som inneholder bestillinger med statusen **Til eksterne vurdering**:

-   Til ekstern vurdering krever handling.
-   Til ekstern vurdering, venter på svar fra leverandør.

### Endre en bestilling
<a id="changing-a-po" class="xliff"></a>

Når du skal endre en bestilling som allerede er besvart, må du sende en ny versjon av bestillingen til leverandøren. Den nye bestillingen har et versjonssuffiks til å angi at det er en endret versjon av en bestilling som tidligere ble formidlet. Siden **Logg for leverandørbekreftelse for bestilling** lar deg og leverandørene spore historikken for hver ordre. Den tidligere bekreftede versjonen av en bestilling forblir i listen over bekreftede bestillinger til den nye bestillingen er bekreftet.

### Annullere en bestilling
<a id="cancelling-a-po" class="xliff"></a>

Når du avbryter en bestilling, endres statusen til **Godkjent**. Du må sende bestillingen tilbake til leverandøren via leverandørportalen, slik at leverandøren kan bekrefte eller avvise annulleringen. Når annulleringen er bekreftet, vises bestillingen i leverandørens liste over bekreftede bestillinger som **Annullert**.

### Legge til vedlegg i en bestilling
<a id="adding-attachments-to-a-po" class="xliff"></a>

Du kan legge til vedlegg, for eksempel filer, bilder og merknader, i bestillingen ved hjelp av dokumentbehandlingssystemet. Vedlegg av **ekstern** type vil være synlige for leverandøren når du sender bestillingen.

## Oppdatere bestillingen når en leverandør foreslår endringer
<a id="update-the-po-when-a-vendor-suggests-changes" class="xliff"></a>
Når en leverandør har svart på Bestillingen og foreslått endringer, er neste trinn å behandle svaret.
I listen Til ekstern vurdering krever handling i **arbeidsområdet for bestillingsklargjøring** kan du identifisere en bestilling som en leverandør har besvart som godkjent med endringer. I listen Til ekstern vurdering krever handling kan du også navigere til leverandørens svar. En leverandør kan endre følgende informasjon i hodet på et svar.
 
-   Referanse for leverandørdokument
-   Leveringsmåte
-   Leveringsbetingelse
-   Bekreftet leveringsdato

Leverandøren kan også legge til et notat eller vedlegg

På linjene kan leverandøren endre antallet og leveringsdatoene, legge til notater og vedlegg, avvise en linje, erstatte en linje med et annet produkt som tastes inn som tekst, og dele opp en linje i flere leveringer. Avhengig av hvilke endringer som er foreslått av leverandøren, har linjestatusen forskjellige linjestatuser:
    
-   **Godtatt med endringer**
-   **Avvist**
-   **Erstattet** - I dette tilfellet legges en ekstra linje til som har statusen **Erstatning**.
-   **Bekreftet** delt inn i tidsplan - I dette tilfellet blir det lagt til ekstra linjer med statusen **Linjer i betalingsplan**.

Hvis en linje har ingen endringer, vises linjestatus som **Godkjent**.

I svaret, kan du se de tidligere nevnte linjestatusene som angir hvilke typer endringer som er gjort av leverandøren. I tillegg vises alle endrede felt i fet skrift for å hjelpe deg med å identifisere endringene.

Du kan oppdatere en bestilling ved å klikke på handlingen **Behandle bestillingsoppdatering** på svaret eller på én linje om gangen. En indikator, **Er bestillingsoppdateringen behandlet?**, i hodet, og linjene lar deg se om systemet har behandlet, hodet eller linjene for å oppdatere Bestillingen med alle mulige endringer som kommer fra svaret. Du kan kjøre prosessen **Behandle bestillingsoppdatering** bare én gang per hode eller linje.

Ikke alle foreslåtte endringer kan oppdateres på en bestilling. Bare oppdateringer i hodet og oppdateringer av datoer og antall på linjer kan oppdateres automatisk på Bestillingen. For andre endringer må du manuelt oppdatere Bestillingen. I dette tilfellet viser indikatoren **Er bestillingsoppdateringen behandlet?** **Manuell oppdatering**. Et eksempel på en endring som må behandles manuelt, vil være når det en leverandør foreslår å dele en linje inn i en tidsplan.

En linje med statusen **Godkjent** vil ha en bekreftet leveringsdato som vil bli oppdatert på Bestillingen når du utfører **Behandle bestillingsoppdatering**. Notater og vedlegg overføres ikke automatisk til den gjeldende Bestillingen. Legg merke til at når du oppdaterer den gjeldende Bestillingen via handlingen **Behandle bestillingsoppdatering**, vil ikke forretningsavtaler bli vurdert på nytt på bestillingslinjene.


## Statuser og versjoner for bestillinger
<a id="po-statuses-and-versions" class="xliff"></a>
Denne delen beskriver de forskjellige statusene som en bestilling kan ha opp til tidspunktet når den er bekreftet. Den beskriver også på hvilket punkt nyere versjoner av Bestillingen gjøres tilgjengelig for leverandøren. Virkemåten varierer, avhengig av om du bruker endringsadministrasjon for bestillinger. 

### Versjoner og status hvis du ikke bruker endringsadministrasjon
<a id="versions-and-statuses-if-you-dont-use-change-management" class="xliff"></a>

Tabellen nedenfor viser et eksempel på endringene i status og versjon som en bestilling kan gå gjennom.

|                                                                          |                                                                                                                                                              |
|--------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Handling**                                                               | **Status og versjon**                                                                                                                                       |
| Den første versjonen av Bestillingen opprettes i Finance and Operations. | Statusen er **Godkjent**.                                                                                                                                  |
| Bestillingen er sendt til leverandøren.                                            | En versjon registreres i grensesnittet for leverandørsamarbeid, og statusen endres til **Til ekstern vurdering**.                                          |
| Leverandøren sender svaret **Godtatt med endringer**.                  | Statusen er fortsatt **Til ekstern vurdering**.                                                                                                                  |
| Du kan gjøre noen endringer som kreves av leverandøren.                  | Statusen endres til **Godkjent**.                                                                                                                        |
| Du sender den nye versjonen av bestillingen til leverandøren.                        | En ny versjon registreres i grensesnittet for leverandørsamarbeid, og statusen endres til **Til ekstern vurdering**.                                      |
| Leverandøren godtar den nye versjonen av bestillingen.                            | Statusen er fortsatt **Til ekstern vurdering** hvis ikke leverandørkontoen er konfigurert til å automatisk sette en bestilling til **Bekreftet**-tilstanden når de godkjenner den. |


Leverandører trenger ikke bekrefte bestillingen ved hjelp av grensesnittet for leverandørsamarbeid. De kan også sende en e-postmelding eller formidle at de godtar en bestilling via andre kanaler. Deretter kan du bekrefte ordren manuelt i Finance and Operations. I så fall får du en advarsel om at ordren blir bekreftet, selv om det ikke finnes noe svar fra leverandøren. Bestillingen vil vises i bekreftelsesloggen som en åpen bekreftet ordre som ikke har noen svar. Leverandøren vil ikke lenger ha muligheten til å bekrefte eller avvise bestillingen.  


>[!NOTE]
>Versjonen av bestillingen som er tilgjengelig for andre prosesser i Dynamics 365 for Finance and Operations, er alltid den nyeste versjonen, selv om denne versjonen ennå ikke er registrert i grensesnittet for leverandørsamarbeid.

### Versjoner og status hvis du bruker endringsadministrasjon
<a id="versions-and-statuses-if-you-use-change-management" class="xliff"></a>

Hvis endringsadministrasjon er aktivert for bestillinger, går bestillingen gjennom en godkjenningsarbeidsflyt når den får statusen **Godkjent**. Denne prosessen er ikke synlig for leverandøren.  

Tabellen nedenfor viser et eksempel på endringene i status og versjon som en bestilling kan gå gjennom når endringsadministrasjon er aktivert: Versjonen registreres når bestillingen er godkjent, ikke når bestillingen sendes til leverandøren eller bekreftes.

|                                                                                                               |                                                                                                                                                                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Handling**                                                                                                    | **Status og versjon**                                                                                                                                                                                                                                                                                                                                                                      |
| Den første versjonen av Bestillingen opprettes i Finance and Operations.                                      | Statusen er **Utkast**.                                                                                                                                                                                                                                                                                                                                                                    |

| Bestillingen sendes til godkjenningsprosessen. (Godkjenningsprosessen er en intern prosess som leverandøren ikke er involvert i.) | Statusen endres fra **Utkast** til **Til vurdering** til **Godkjenning** hvis Bestillingen ikke avvises under godkjenningsprosessen. Den godkjente bestillingen registreres som en versjon.                                                                                                                                                                                                                     | | Bestillingen sendes til leverandøren                                                                                  | Versjonen registreres i grensesnittet for leverandørsamarbeid, og statusen endres til **Til ekstern vurdering**.                                                                                                                                                                                                                                                                       | | Du kan gjøre noen endringer som kreves av leverandøren, enten manuelt eller ved hjelp av handlingen på svaret for å oppdatere Bestillingen.                                                       | Statusen endres tilbake til **Utkast**.                                                                                                                                                                                                                                                                                                                                                    | | Bestillingen sendes til godkjenningsprosessen på nytt.                                                            | Statusen endres fra **Utkast** til **Til vurdering** til **Godkjenning** hvis bestillingen ikke avvises under godkjenningsprosessen. Systemet kan også konfigureres slik at spesifikke endringer i felter ikke krever ny godkjenning. I dette tilfellet endres statusen først til **Utkast** og oppdateres deretter automatisk til **Godkjent**. Den godkjente bestillingen registreres som en ny versjon. | | Du sender den nye versjonen av bestillingen til leverandøren.                                                             | Den nye versjon registreres i grensesnittet for leverandørsamarbeid, og statusen endres til **Til ekstern vurdering**.                                                                                                                                                                                                                                                                   | | Leverandøren godkjenner den nye versjonen av bestillingen.                                                                | Statusen endres til **Bekreftet**, enten automatisk eller når du mottar svaret fra leverandøren og deretter bekrefter bestillingen.                                                                                                                                                                                                                                                     |

## Dele informasjon om forsendelseslager
<a id="share-information-about-consignment-inventory" class="xliff"></a>
Hvis du bruker forsendelseslager, kan leverandører bruke grensesnittet for leverandørsamarbeid til å vise informasjon på følgende sider:

-   **Bruk av forsendelseslager for bestillinger** – Bestillinger for forsendelseslager blir generert når eierskap av lageret endres fra leverandøren til firmaet. En produktkvittering posteres samtidig. Disse forsendelsesbestillingene vises bare på siden **Bruk av forsendelseslager for bestillinger**. De er ikke inkludert på siden **Alle bekreftede bestillinger** i modulen **Leverandørsamarbeid**.
-   **Produkter mottatt fra forsendelseslager** – Denne siden viser alle transaksjoner der eierskapet for produkter er blitt overført til fra leverandøren til firmaet. Leverandører kan bruke denne informasjonen for fakturere kunden.
-   **Forsendelseslager for beholdning** – Denne siden viser forsendelseslageret for beholdning som eies av leverandøren som er mottatt på lageret ditt.





