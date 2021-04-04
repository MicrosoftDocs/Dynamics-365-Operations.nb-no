---
title: Opprette varslingsregler
description: Dette emnet gir informasjon om varsler, og forklarer hvordan du oppretter en varslingsregel, slik at du får melding om hendelser, for eksempel en dato som kommer eller en bestemt endring som forekommer.
author: tjvass
manager: AnnBe
ms.date: 10/08/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EventCreateRule
audience: Application user
ms.reviewer: sericks
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2018-3-30
ms.dyn365.ops.version: Platform update 15
ms.openlocfilehash: b0c37c1f948b072c64c54308cb85c90cfa248700
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/09/2021
ms.locfileid: "5559414"
---
# <a name="create-alert-rules"></a>Opprette varslingsregler

[!include [banner](../includes/banner.md)]

## <a name="getting-started"></a>Komme i gang

Før du oppretter en varslingsregel, må du vurdere når eller i hvilke situasjoner du vil motta varsler. Når du vet hvilke hendelser du vil varsles om, kan du finne siden der dataene som forårsaker den hendelsen, vises. Hendelsen kan være en dato som kommer, eller en bestemt endring som forekommer. Du må derfor finne siden der datoen er angitt, eller hvor feltet som endres eller den nye posten som opprettes, vises. Etter at du har denne informasjonen, kan du opprette varslingsregelen.

Når du oppretter en varslingsregel, kan du definere vilkår som må oppfylles før varselet utløses. Kriterier er stort sett et samsvar mellom en hendelse og innfrielsen av bestemte betingelser. Når en hendelse forekommer, begynner systemet å kontrollere i henhold til betingelsene som er definert.

## <a name="ensure-the-alert-batch-jobs-are-running"></a>Sikre at de satsvise varslingsjobbene kjører

De satsvise jobbene for dataendring og forfallsdatovarslinger må kjøre for at varslingsbetingelsene skal bli behandlet og varslene sendes. Du kan kjøre satsvise jobber ved å gå til **Systemadministrasjon** > **Periodiske oppgaver** > **Varsler** og legge til en ny satsvis jobb for **Endringsbaserte varslinger** og/eller **Forfallsdatovarslinger**. Hvis det er behov for en lang og ofte kjørende satsvis jobb, velger du **Regelmessighet** og setter **Ingen sluttdato** med et **Gjentakelsesmønster** til **Minutter** og et **Antall** på **1**.

## <a name="events"></a>Hendelser

Hendelsen som utløser en varslingsregel kan være en dato som kommer, eller en bestemt endring som forekommer. Utløser for hendelser som er definert i hurtigfanen **Varsle meg når** i dialogboksen **Opprett varslingsregel**. Hendelsene som er tilgjengelige for et bestemt felt, avhenger av utløseren som er valgt.

Hvis du for eksempel definerer en varslingsregel for feltet **Startdato**, er forfallsdatohendelser velegnet. Derfor er hendelsestypen `is due in` tilgjengelig for dette feltet. For et felt som for eksempel **Kostsenter**, er imidlertid ikke en forfallsdatohendelse velegnet. Derfor er hendelsestypen `is due in` ikke tilgjengelig. I stedet er hendelsestypen `has changed` tilgjengelig.

## <a name="event-types"></a>Hendelsestyper

Tre typer hendelser kan oppstå:

- **Hendelser av opprett-type og slett-type** – Disse hendelsene utløser et varsel når en post opprettes eller slettes.
- **Hendelser av oppdater-type** – Disse hendelsene utløser et varsel når data i et bestemt felt endres.
- **Hendelser av forfallsdatotype** – Disse hendelsene utløser et varsel når en dato kommer.
    
Endringer kan startes av en annen bruker. En bruker endrer for eksempel leveringsdatoen for en bestilling. Det kan også forekomme endringer som en del av en prosess. Feltet **Status** på en side endres for eksempel til å gjenspeile livssyklusen til forskjellige prosesser i systemet.

## <a name="conditions"></a>Betingelser

I hurtigfanen **Varsle meg for** i dialogboksen **Opprett varslingsregel** kan du bruke betingelser til å kontrollere når du varsles om hendelser.

Du kan for eksempel angi at systemet skal varsle deg om endringer når statusen for bestillinger endres, men bare hvis statusen samsvarer med et bestemt sett med betingelser. Mer spesifikt ønsker du å bli varslet når statusen for en bestilling er satt til **Mottatt**. Denne endringen i statusen er hendelsen som utløser varselet.

Deretter må du bestemme hvilke bestillinger du ønsker å bli varslet om. Du kan for eksempel velge ett av følgende alternativer. Disse alternativene definerer betingelsene for varslingsregelen.

- **Gjeldende valgte post** – Du mottar et varsel når statusen for en bestemt bestilling endres til **Mottatt**.
- **Alle poster** – Du mottar et varsel når statusen for en bestilling endres for en vare på den aktive siden. Du kan bruke den avanserte filtreringen som er tilgjengelig på siden for å opprette regler for et bestemt sett med poster. Du kan for eksempel opprette et varsel som utløses for alle bestillingene for kundene i en bestemt kundegruppe.
    
## <a name="expiry-of-rule"></a>Utløp av regel

I hurtigfanen **Varsle meg inntil** i dialogboksen **Opprett varslingsregel** kan du angi hvor lenge varslingsregelen skal være aktiv.

## <a name="alert-contents"></a>Varselinnhold

I hurtigfanen **Varsle meg med** i dialogboksen **Opprett varslingsregel** kan du angi emneteksten og meldingsteksten som varslingsmeldingene skal bruke.

## <a name="user-id"></a>Bruker-ID

I hurtigfanen **Varsle meg med** i dialogboksen **Opprett varslingsregel** kan du angi hvilken bruker som skal motta varslene. Bruker-IDen er valgt som standard. Muligheten til å endre brukeren som mottar varselet, er begrenset til organisasjons administratorer.

## <a name="alerts-as-business-events"></a>Varsler som forretningshendelser

Du kan sende varsler eksternt ved hjelp av rammeverket for forretningshendelser. Når du oppretter et varsel, setter du **Hele organisasjonen** til **Nei** og **Send eksternt** til **Ja**. Når du har utløst varselet om forretningshendelsen, kan du utløse en flyt som er bygd i Power Automate ved hjelp av utløseren **Når en forretningshendelse oppstår** i Finance and Operations-koblingen, eller eksplisitt sende hendelsen til et sluttpunkt for forretningshendelser via **forretningshendelseskatalogen**.

## <a name="create-an-alert-rule"></a>Opprett en varslingsregel

0. Sikre at de satsvise varslingsjobbene kjører (se ovenfor).
1. Åpne siden som inneholder dataene du vil overvåke.
2. Velg **Opprett varslingsregel** i gruppen **Del** i fanen **Alternativer** i handlingsruten.
3. Velg feltet som skal overvåkes, i feltet **Felt** i dialogboksen **Opprett varslingsregel**.
4. Velg hendelsestypen i feltet **Hendelse**.
5. Velg ønsket alternativ i hurtigfanen **Varsle meg i**. Hvis du vil sende varslet som en forretningshendelse, setter du verdien for **Hele organisasjonen** til **Nei**.
6. Hvis varslingsregelen blir inaktiv på en bestemt dato, velger du en sluttdato i hurtigfanen **Varsle meg inntil**.
7. Godta standard emneoverskrift for e-postmeldingen eller skriv inn et nytt emne, i feltet **Emne** i hurtigfanen **Varsle meg med**. Teksten blir emneoverskrift for e-postmeldingen du mottar når det utløses et varsel. Hvis du vil sende varselet som en forretningshendelse, setter du **Send eksternt** til **Ja**.
8. Skriv inn en valgfri melding i feltet **Melding**. Teksten blir meldingen du mottar når det utløses et varsel.
9. Velg **OK** for å lagre innstillingene og opprette varslingsregelen.

## <a name="limitations-and-workarounds"></a>Begrensninger og midlertidige løsninger

### <a name="workaround-for-creating-alerts-for-the-secondary-data-sources-of-a-form"></a>Midlertidig løsning for oppretting av varsler for de sekundære datakildene i et skjema
Du kan ikke opprette varsler for enkelte sekundære datakilder i skjemaer. Når du for eksempel oppretter varsler i skjemaet for kunde- eller leverandørposteringsprofiler, er bare feltene i hodet (CustLedger eller VendLedger) tilgjengelige, og ikke dimensjonskontoene. Den midlertidige løsningen på denne begrensningen er å bruke **SysTableBrowser** til å åpne denne tabellen som hoveddatakilde. 
1. Åpne tabellen i **SysTableBrowser**-skjemaet.
    ```
        https://<EnvironmentURL>/?cmp=USMF&mi=SysTableBrowser&TableName=<TableName>
    ```
2. Opprett et varsel fra SysTableBrowser-skjemaet.

### <a name="change-based-alerts-do-not-work-for-batch-status-changes"></a>Endringsbaserte varsler fungerer ikke for endringer i satsvis status
Endringsbaserte varsler fungerer ikke med endringer i satsvis status fordi den er slått av av ytelseshensyn. I stedet bør du konfigurere funksjonen **Satsvise varsler**. Hvis du vil ha mer informasjon, kan du se [Konfigurere varsler for partiforbedrede skjemaer](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/sysadmin/alerts#set-up-alerts-for-batch-enhanced-forms).


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
