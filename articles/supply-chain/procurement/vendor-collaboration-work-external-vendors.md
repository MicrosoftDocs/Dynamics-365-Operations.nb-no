---
title: Leverandørsamarbeid med eksterne leverandører
description: Dette emnet forklarer hvordan innkjøpsagenter samarbeide med eksterne leverandører for å utveksle informasjon om bestillinger og forsendelseslager.
author: mkirknel
manager: AnnBe
ms.date: 11/02/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchRFQCaseTableListPage, VendVendorPortalInvoicePart
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 221264
ms.assetid: dde49743-1541-4353-a030-63ca3069cd7d
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 733ecc7cfb4fee325560f5a6fe11612bb8ba57ef
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/18/2019
ms.locfileid: "2815301"
---
# <a name="vendor-collaboration-with-external-vendors"></a>Leverandørsamarbeid med eksterne leverandører

[!include [banner](../includes/banner.md)]

Modulen **Leverandørsamarbeid** er beregnet på leverandører som ikke har integrering av utveksling av elektroniske data (EDI) med Microsoft Dynamics 365 Supply Chain Management. Den lar leverandører arbeide med bestillinger, fakturaer, lagerinformasjon for forsendelse og forespørsler om tilbud (tilbudsforespørsler), og gir dem også tilgang til deler av hoveddataene for leverandøren. Dette emnet forklarer hvordan du kan samarbeide med eksterne leverandører som bruker grensesnittet for leverandørsamarbeid for å arbeide med bestillinger, tilbudsforespørsler og forsendelseslager. Det forklarer også hvordan du aktiverer bruk av leverandørsamarbeid for en bestemt leverandør, og hvordan du definerer opplysningene alle leverandører ser når de svarer på en bestilling.

Hvis du vil ha mer informasjon om hva eksterne leverandører kan gjøre i grensesnittet for leverandørsamarbeid, kan du se [Leverandørsamarbeid med kunder](vendor-collaboration-work-customers-dynamics-365-operations.md).

> [!NOTE]
> Informasjonen om leverandørsamarbeid i dette emnet gjelder bare for gjeldende versjonen av Supply Chain Management. I Microsoft Dynamics AX 7.0 (februar 2016) og Microsoft Dynamics AX programversjon 7.0.1 (mai 2016) kan du samarbeide med leverandører ved hjelp av modulen **Leverandørportal**. Hvis du vil ha mer informasjon om modulen **Leverandørportal**, kan du se [Samarbeide med leverandører ved hjelp av leverandørportalen](collaborate-vendors-vendor-portal.md).

Hvis du vil ha mer informasjon om hvordan leverandører kan bruke leverandørsamarbeid i faktureringsprosesser, kan du se [Arbeidsområde for leverandørsamarbeidsfakturering](../../financials/accounts-payable/vendor-portal-invoicing-workspace.md). Hvis du vil ha informasjon om hvordan du klargjør en ny bruker for leverandørsamarbeid, kan du se[Administrere brukere av leverandørsamarbeid](manage-vendor-collaboration-users.md).

## <a name="defining-the-information-that-is-shown-to-vendors-when-they-respond-to-pos"></a>Definere informasjonen som vises til leverandører når de svarer på bestillinger

Når leverandører svarer på en bestilling du sender dem, ser de en av tre meldingsbokser der de må bekrefte at de vil godta, avvise, eller godta bestillingen med endringene. Ettersom informasjonen som skal vises på til leverandøren på dette tidspunktet, kan være spesifikk for din virksomhet, kan du angi teksten som vises i hver bekreftelsesmelding. Teksten kan for eksempel informere leverandøren om de neste trinnene i prosessen eller om vilkår og betingelser.

Slik definerer du teksten som vises i bestillingssvaret:

1. På siden **Informasjon for leverandører som svarer på bestillinger**, velger du svartypen og velger deretter **Rediger**.
2. I boksen **Informasjonsmelding** skriver du inn informasjon som skal vises til leverandører i meldingsboksen.

Hvis du må legge til meldinger på flere språk, kan du opprette egne meldinger og angi den aktuelle språkkoden for hver av dem. Meldingen som vises til hver leverandør, vil være på språket som leverandøren bruker.

## <a name="setting-the-vendor-collaboration-options-for-a-specific-vendor"></a>Angi alternativer for leverandørsamarbeid for en bestemt leverandør

En administrator konfigurerer de generelle innstillingene for samarbeid med leverandøren, for eksempel sikkerhetsroller som er tilgjengelige for alle leverandører som du kan samarbeide med. Det finnes imidlertid også innstillinger som kan være forskjellige for hver leverandørkonto. Du bør konfigurere disse innstillingene.

- Aktiver leverandørsamarbeid.
- Angi om leverandøren skal se prisinformasjon.

### <a name="enabling-vendor-collaboration"></a>Aktivere leverandørsamarbeid

Før du kan opprette brukerkontoer for en ekstern leverandør, må du konfigurere leverandørkontoen, slik at leverandøren kan bruke leverandørsamarbeid. På siden **Leverandører**, på fanen **Generelt** angir du feltet **Samarbeidsaktivering**. Følgende alternativer er tilgjengelige:

- **Aktive (bestilling bekreftes automatisk)** – Bestillinger bekreftes automatisk hvis leverandøren godtar dem uten endringer.
- **Aktive (bestilling bekreftes ikke automatisk)** – Organisasjonen din må bekrefte bestillinger manuelt etter at leverandøren har godtatt dem.

### <a name="specifying-whether-the-vendor-should-see-price-information"></a>Angi om leverandøren skal se prisinformasjon

Hvis du vil dele prisinformasjon for bestillinger via grensesnittet for leverandørsamarbeid, må du sette alternativet **Priser/beløp for bestilling** på fanen **Bestillingsstandarder** for leverandørkontoen til **Ja**. Denne prisinformasjonen inkluderer enhetspris, rabatter og tillegg.

## <a name="working-with-pos-when-vendor-collaboration-is-used"></a>Arbeide med bestillinger når leverandørsamarbeid brukes

### <a name="sending-a-po-to-a-vendor"></a>Sende en bestilling til en leverandør

Bestillinger klargjøres i Supply Chain Management. Når en bestilling har statusen **Godkjent**, sender du den til leverandøren ved å velge **Send for bekreftelse** på **Bestilling**-siden. Statusen for bestillingen endres deretter til **Til ekstern vurdering**. Etter at bestillingen er sendt, kan leverandøren se den på siden **Bestillinger for vurdering** i grensesnittet for leverandørsamarbeid. Leverandøren kan deretter godta bestillingen, avvise den eller foreslå endringer. Leverandøren kan også legge til merknader for å formidle informasjon, for eksempel endringer i bestillingen. Hvis du vil trekke leverandørens oppmerksomhet til en ny bestilling, kan du også bruke utskriftsbehandlingssystemet til å sende bestillingen via e-post.

### <a name="confirmation-and-acceptance-of-a-po-by-a-vendor"></a>Bekreftelse og godkjenning av en bestilling av en leverandør

Når en leverandør har godtatt en bestilling, kan bestillingen bekreftes automatisk, eller den må kanskje bekreftes manuelt. Virkemåten avhenger av om feltet **Samarbeidsaktivering** er satt til **Aktiv (bestilling bekreftes automatisk)** eller til **Aktiv (bestilling bekreftes ikke automatisk)** for leverandøren.

Tabellen nedenfor viser den vanlige utvekslingen av informasjon, avhengig av svaret fra leverandøren når du sender dem en bestilling for bekreftelse.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr>
<th>Leverandørsvar</th>
<th>Resultat</th>
</tr>
</thead>
<tbody>
<tr class="even">
<td>Leverandøren <strong>godtar</strong> bestillingen, og Supply Chain Management konfigureres til automatisk bekreftelse av bestillinger som leverandøren godtar.</td>
<td>Statusen for ordren oppdateres til <strong>Bekreftet</strong>. Hvis bestillingen av en eller annen grunn ikke kan oppdateres, registreres likevel leverandørsvaret som <strong>Godtatt</strong>, men statusen for bestillingen blir værende <strong>Til ekstern vurdering</strong>. 

Bestillingen som ble sendt til leverandøren, og som har statusen <strong>Til ekstern vurdering</strong>, oppdateres med bekreftede leveringsdatoer på linjene. Denne oppdateringen starter en ny versjon som settes automatisk til <strong>Bekreftet</strong>-statusen. Når bestillingen er bekreftet, vises den i grensesnittet for leverandørsamarbeid.</td>
</tr>
<tr class="odd">
<td>Leverandøren <strong>godtar</strong> bestillingen, men Supply Chain Management konfigureres ikke til automatisk bekreftelse av bestillinger som leverandøren godtar.</td>
<td>Leverandørsvaret registreres som <strong>Godtatt</strong>, men statusen for bestillingen blir værende <strong>Til ekstern vurdering</strong>.

Bestillingen som ble sendt til leverandøren, og som har statusen <strong>Til ekstern vurdering</strong>, oppdateres med bekreftede leveringsdatoer på linjene. Denne oppdateringen starter en ny versjon som settes automatisk til <strong>Til ekstern vurdering</strong>-statusen. Du kan deretter bekrefte bestillingen manuelt.</td>
</tr>
<tr class="even">
<td>Leverandøren <strong>avviser</strong> ordren.</td>
<td>Leverandørsvaret registreres som <strong>Avvist</strong>, og statusen for bestillingen blir værende <strong>Til ekstern vurdering</strong>. Avslaget mottas sammen med leverandørmerknaden.</td>
</tr>
<tr class="odd">
<td>Leverandøren <strong>godtar</strong> bestillingen <strong>med endringer</strong>. Endringer blir foreslått på linjenivå. Leverandøren kan godkjenne eller avvise enkeltlinjer. Her er noen andre endringer som leverandøren kan foreslå:
<ul>
<li>Endre datoer eller antall.</li>
<li>Dele linjer for ulike leveringsdatoer eller antall.</li>
<li>Erstatte en vare.</li>
</ul>
Leverandøren kan ikke endre prisinformasjon og tillegg. Leverandøren kan imidlertid foreslå disse endringene ved hjelp av merknader.</td>
<td>Leverandørsvaret registreres som <strong>Godtatt med endringer</strong>, og statusen for bestillingen forblir <strong>Til ekstern vurdering</strong>. Statusene viser hvilke typer endringer som leverandøren har foreslått. For informasjon om automatisk forbruk av endringene kan du se delen &quot;Oppdatere bestillingen når en leverandør foreslår endringer&quot; senere i dette emnet. </td>
</tr>
</tbody>
</table>

Du kan bruke arbeidsområdet **Bestillingsklargjøring** til å overvåke hvilke bestillinger leverandøren har svart på. Arbeidsområdet inneholder to lister som inneholder bestillinger med statusen **Til ekstern vurdering**:

- Til ekstern vurdering krever handling
- Til ekstern vurdering, venter på svar fra leverandør

### <a name="changing-a-po"></a>Endre en bestilling

Når du skal endre en bestilling som en leverandør allerede har besvart, må du sende en ny versjon av bestillingen til leverandøren. Den nye bestillingen har et versjonssuffiks til å angi at det er en endret versjon av en bestilling som tidligere ble sendt. Siden **Logg for leverandørbekreftelse for bestilling** lar deg og leverandørene spore historikken for hver ordre. Den tidligere bekreftede versjonen av en bestilling forblir i listen over bekreftede bestillinger til den nye bestillingen er bekreftet.

### <a name="canceling-a-po"></a>Annullere en bestilling

Når du avbryter en bestilling, endres statusen til **Godkjent**. Du må sende bestillingen tilbake til leverandør så leverandøren kan bekrefte eller avise kanselleringen. Når annulleringen er bekreftet, vises bestillingen i leverandørens liste over bekreftede bestillinger som **Annullert**.

### <a name="adding-attachments-to-a-po"></a>Legge til vedlegg i en bestilling

Du kan legge til vedlegg, for eksempel filer, bilder og merknader, i bestillingen ved hjelp av dokumentbehandlingssystemet. Vedlegg av **ekstern** type vil være synlige for leverandøren når du sender bestillingen.

## <a name="updating-a-po-when-a-vendor-suggests-changes"></a>Oppdatere en bestilling når en leverandør foreslår endringer

Hvis en leverandør har svart på en bestilling og foreslått endringer, er neste trinn å behandle svaret.

I arbeidsområdet **Bestillingsklargjøring** i listen **Til ekstern vurdering krever handling** kan du identifisere bestillinger som en leverandør har godkjent med endringer. Du kan også navigere til leverandørens svar fra denne listen.

En leverandør kan endre følgende informasjon i hodet på et svar:
 
- Referanse for leverandørdokument
- Leveringsmåte
- Leveringsbetingelse
- Bekreftet leveringsdato

Leverandøren kan også legge til et notat eller vedlegg.

På linjene kan leverandøren endre antallet og leveringsdatoene, legge til notater og vedlegg, avvise en linje, erstatte en linje med et annet produkt som angis som tekst, og dele opp en linje i flere leveringer. Statusen for en linje varierer, avhengig av endringene som leverandøren har foreslått:
    
- **Godtatt med endringer**
- **Avslått**
- **Erstattet** – I dette tilfellet legges det til en ekstra linje som har statusen **Erstatning**.
- **Bekreftet**
- **Delt inn i tidsplan** – I dette tilfellet blir det lagt til ekstra linjer med statusen **Linjer i betalingsplan**.

Hvis en linje har ingen endringer, vises linjestatus som **Godkjent**.

I svaret forteller linjestatusene deg hvilke typer endringer som er gjort av leverandøren. I tillegg vises alle felt som ble endret, i fet skrift for å hjelpe deg med å identifisere endringene.

Du kan oppdatere en bestilling ved å velge **Behandle bestillingsoppdatering** på svaret eller på én linje om gangen. Feltet **Er bestillingsoppdateringen behandlet?** i hodet og på linjene indikerer om systemet har behandlet hodet eller linjene for å oppdatere bestillingen med alle endringer som kommer fra svaret. Du kan kjøre handlingen **Behandle bestillingsoppdatering** bare én gang per hode eller linje.

Ikke alle foreslåtte endringer kan oppdateres på en bestilling. Bare oppdateringer i hodet og oppdateringer av datoer og antall på linjer kan oppdateres automatisk på bestillingen. For andre endringer må du manuelt oppdatere Bestillingen. I dette tilfellet er verdien i feltet **Er bestillingsoppdateringen behandlet?** **Manuell oppdatering**. Hvis for eksempel en leverandør foreslår at en linje skal deles inn i en tidsplan, må denne endringen gjøres manuelt.

Alle linjer som har statusen **Godkjent**, har en bekreftet leveringsdato. Når du kjører handlingen **Behandle bestillingsoppdatering**, oppdateres denne datoen på bestillingen. Notater og vedlegg overføres ikke automatisk til den gjeldende bestillingen. Forretningsavtaler blir heller ikke vurdert på nytt på bestillingslinjene når du oppdaterer den gjeldende bestillingen via handlingen **Behandle bestillingsoppdatering**.

## <a name="po-statuses-and-versions"></a>Statuser og versjoner for bestillinger

Denne delen beskriver de forskjellige statusene som en bestilling kan ha opp til tidspunktet når den er bekreftet. Den beskriver når nyere versjoner av en bestilling blir gjort tilgjengelig for leverandøren. Virkemåten varierer, avhengig av om du bruker endringsadministrasjon for bestillinger. 

### <a name="versions-and-statuses-if-you-dont-use-change-management"></a>Versjoner og status hvis du ikke bruker endringsadministrasjon

Tabellen nedenfor viser et eksempel på endringene i status og versjon som en bestilling kan gå gjennom.

| Handling | Status og versjon |
|--------|--------------------|
| Den første versjonen av Bestillingen opprettes i Supply Chain Management. | Statusen er **Godkjent**. |
| Bestillingen er sendt til leverandøren. | En versjon registreres i grensesnittet for leverandørsamarbeid, og statusen endres til **Til ekstern vurdering**. |
| Leverandøren sender svaret **Godtatt med endringer**. | Statusen er fortsatt **Til ekstern vurdering**. |
| Du kan gjøre noen endringer som leverandøren har forespurt. | Statusen endres til **Godkjent**. |
| Du sender den nye versjonen av bestillingen til leverandøren. | En ny versjon registreres i grensesnittet for leverandørsamarbeid, og statusen endres til **Til ekstern vurdering**. |
| Leverandøren godtar den nye versjonen av bestillingen. | Statusen er fortsatt **Til ekstern vurdering** hvis ikke leverandørkontoen er konfigurert til å automatisk sette bestillinger til statusen **Bekreftet** når leverandøren godkjenner den. |

Leverandører trenger ikke bekrefte en bestilling ved hjelp av grensesnittet for leverandørsamarbeid. De kan også sende en e-postmelding eller formidle at de godtar en bestilling via andre kanaler. Du kan deretter bekrefte ordren manuelt. I så fall får du en advarsel om at ordren blir bekreftet, selv om det ikke finnes noe svar fra leverandøren. Bestillingen vil vises i bekreftelsesloggen som en åpen bekreftet ordre som ikke har noen svar. På dette tidspunktet har leverandøren ikke lenger muligheten til å bekrefte eller avvise bestillingen.

> [!NOTE]
> Versjonen av bestillingen som er tilgjengelig for andre prosesser i Supply Chain Management, er alltid den nyeste versjonen, selv om denne versjonen ennå ikke er registrert i grensesnittet for leverandørsamarbeid.

### <a name="versions-and-statuses-if-you-use-change-management"></a>Versjoner og status hvis du bruker endringsadministrasjon

Hvis endringsadministrasjon er aktivert for bestillinger, går bestillingene gjennom en godkjenningsarbeidsflyt for å få statusen **Godkjent**. Denne prosessen er ikke synlig for leverandøren.

Tabellen nedenfor viser et eksempel på endringene i status og versjon som en bestilling kan gå gjennom når endringsadministrasjon er aktivert: En versjon registreres når bestillingen er godkjent, ikke når bestillingen sendes til leverandøren eller bekreftes.

| Handling | Status og versjon |
|--------|--------------------|
| Den første versjonen av Bestillingen opprettes i Supply Chain Management. | Statusen er **Utkast**. |
| Bestillingen sendes til godkjenningsprosessen. (Godkjenningsprosessen er en intern prosess som leverandøren ikke er involvert i.) | Statusen endres fra **Utkast** til **Til vurdering** til **Godkjenning** hvis bestillingen ikke avvises under godkjenningsprosessen. Den godkjente bestillingen registreres som en versjon. | 
| Bestillingen er sendt til leverandøren. | Versjon registreres i grensesnittet for leverandørsamarbeid, og statusen endres til **Til ekstern vurdering**. |
| Du kan gjøre noen endringer som kreves av leverandøren, enten manuelt eller ved hjelp av handlingen **Behandle bestillingsoppdatering** på svaret for å oppdatere bestillingen. | Statusen endres tilbake til **Utkast**. |
| Bestillingen sendes til godkjenningsprosessen på nytt. | Statusen endres fra **Utkast** til **Til vurdering** til **Godkjenning** hvis bestillingen ikke avvises under godkjenningsprosessen. Systemet kan også konfigureres slik at spesifikke endringer i felter ikke krever ny godkjenning. I dette tilfellet endres statusen først til **Utkast** og oppdateres deretter automatisk til **Godkjent**. Den godkjente bestillingen registreres som en ny versjon. |
| Du sender den nye versjonen av bestillingen til leverandøren. | Den nye versjon registreres i grensesnittet for leverandørsamarbeid, og statusen endres til **Til ekstern vurdering**. |
| Leverandøren godkjenner den nye versjonen av bestillingen. | Statusen endres til **Bekreftet**, enten automatisk eller når du mottar svaret fra leverandøren og deretter bekrefter bestillingen. |

## <a name="sharing-information-about-consignment-inventory"></a>Dele informasjon om forsendelseslager

Hvis du bruker forsendelseslager, kan leverandører bruke grensesnittet for leverandørsamarbeid til å vise informasjon på følgende sider:

- **Bruk av forsendelseslager for bestillinger** – Bestillinger for forsendelseslager blir generert når eierskap av lageret endres fra leverandøren til firmaet. En produktkvittering posteres samtidig. Disse forsendelsesbestillingene vises bare på siden **Bruk av forsendelseslager for bestillinger**. De er ikke inkludert på siden **Alle bekreftede bestillinger** i modulen **Leverandørsamarbeid**.
- **Produkter mottatt fra forsendelseslager** – Denne siden viser alle transaksjoner der eierskapet for produkter er blitt overført til fra leverandøren til firmaet. Leverandører kan bruke denne informasjonen for fakturere kunden.
- **Forsendelseslager for beholdning** – Denne siden viser forsendelseslageret for beholdning som eies av leverandøren som er mottatt på lageret ditt.

## <a name="working-with-rfqs-when-you-use-vendor-collaboration"></a>Arbeide med tilbudsforespørsler når du bruker leverandørsamarbeid

Denne delen beskriver interaksjonene mellom kunder og leverandører i løpet av tilbudsforespørselsprosessen. Den forklarer også hvordan informasjonen blir kommunisert til leverandørene. For en grunnleggende oversikt over støtte for tilbudsforespørselsprosessen, se [Oversikt over tilbudsforespørsler (RFQ-er)](request-quotations.md).

### <a name="alternates-attachments-amendments-and-returns"></a>Alternativer, vedlegg, endringer, og returer

- **Alternativer** – I hodet i en tilbudsforespørselssak kan du angi at alternativer er tillatt for linjer for ikke-katalogvarer. Når alternativer er aktivert, kan leverandører legge til en alternativ linje for hver forespurte linje.
- **Vedlegg** – Vedlegg kan legges til på både overskrifts- og linjenivå i en tilbudsforespørselssak. Vedlegg kan klassifiseres som enten interne eller eksterne. Interne vedlegg kan vises bare på kundesiden, mens leverandører kan vise eksterne vedlegg etter at de sendes.

    Leverandører kan også legge til vedlegg i budsvarene sine. Disse vedleggene kan vises på kundesiden etter at en leverandør har sendt budsvaret. Vedlegg som leverandører legger til, klassifiseres alltid som eksterne. Hvis du vil åpne et vedlegg som en leverandør har sendt sammen med et bud, velger du **Vedlegg i bud** eller **Vedlegg på budlinje**.
    
    Hvis du vil åpne et vedlegg som ble sendt sammen med tilbudsforespørselssaken, kan du bruke binderssymbol for dokumentbehandling i svaret.

- **Endringer** – Når en endring er ferdig, fjernes eksisterende budsvar, slik at de kan erstattes av oppdaterte verdier. Informasjon som linjepris og antall fra tidligere budsvar kan vises via journalene i tilbudsforespørselssaken.

    For å fremtvinge endringsbehandling, på siden **Parametere for innkjøp og leverandører**, på hurtigfanen **Tilbudsforespørsler**, angi alternativet **Lås tilbudsforespørsler når de er sendt** til **Ja**. (Dette alternativet er angitt og kreves for offentlig sektor.)

- **Returer** – Hvis en leverandør har sendt et bud, men mer eller endret informasjon er nødvendig for tilbudsforespørselsaken, kan kunden returnere budet til leverandøren. Dataene fra budet som ble sendt tidligere, beholdes, og leverandøren kan gjøre de ønskede endringene uten å starte budprosessen på nytt.

## <a name="public-sector-extensions"></a>Utivdelser for offentlig sektor

For offentlig sektor gjør den utvidede funksjonaliteten at en tilbudsforespørselssak kan sendes til leverandører og publiseres. Når du publiserer en tilbudsforespørsel, kan alle som ber om informasjonen, vise arbeidet som er i samsvar med de fleste offentlige bestemmelser. Alt tilgjengelig arbeid vises på listesiden **Åpne publiserte tilbudsforespørsler**, og de annullerte, ventende eller tildelte tilbudsforespørslene kan vises i på listesidden **Lukkede publiserte tilbudsforespørsler**. Disse dokumentene kan også vises på et område utenfor Supply Chain Management via integrasjoner med følgende dataenheter:

- Publiserte tilbudsforespørsler
- Publisert linje i tilbudsforespørsler
- Publiserte hodevedlegg for tilbudsforespørsler

Med disse enhetene kan personer som ikke er klargjorte brukere i Supply Chain Management, men som har anonym tilgang til det eksterne området, vise arbeid som er tilgjengelig og lukket. I tillegg gjør den utvidede funksjonaliteten i **Send og publiser** det mulig for brukeren som definerer parametere for tilbudsforespørssaken, å definere en e-postmal. Deretter, når innkjøpsansvarlig oppretter tilbudsforespørselssaken, må han eller hun velge e-postmalen for å sende den nødvendige informasjonen til leverandørene i tilbudsforespørselssaken. 

Brukeren som definerer parametere for tilbudsforespørselsprosessen, kan opprette flere e-postmaler. Disse e-postmaler kan inneholde både statisk tekst og følgende erstatningstokener. Tokene erstattes med kontekstavhengige verdier når det opprettes en e-post.

- %RFQCase%
- %RFQCaseName%
- %bidType%
- %inviteOnly%
- %expiryDateTime%
- %requester%
- %requestingDepartment%
- %accountnum%
- %todaysdate%
- %createddate%

Hvis en endring er nødvendig, og sendes etter at tilbudsforespørselen er sendt, sendes tilbudsforespørselen på nytt til alle inviterte leverandører. Det publiserte dokumentet oppdateres også på siden **Åpne publiserte tilbudsforespørsler**.
