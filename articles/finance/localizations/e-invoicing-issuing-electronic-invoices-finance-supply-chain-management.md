---
title: Utstede elektroniske fakturaer i Finance og Supply Chain Management
description: Dette emnet beskriver hvordan du utsteder elektroniske fakturaer i Microsoft Dynamics 365 Finance og Dynamics 365 Supply Chain Management via Elektronisk fakturering-tillegget.
author: gionoder
manager: AnnBe
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 187f5a20d088b4fcd7af2a6576357a69c2efc2c6
ms.sourcegitcommit: e88c96d1cb817a22db81856cadb563c095ab2671
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/02/2021
ms.locfileid: "5104419"
---
# <a name="issue-electronic-invoices-in-finance-and-supply-chain-management"></a>Utstede elektroniske fakturaer i Finance og Supply Chain Management

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

Dette emnet beskriver hvordan du utsteder elektroniske fakturaer i Microsoft Dynamics 365 Finance og Dynamics 365 Supply Chain Management via Elektronisk fakturering-tillegget.


## <a name="feature-activation"></a>Funksjonsaktivering

For å starte utstedelse av elektroniske fakturaer via tillegget for Elektronisk fakturering er det nødvendig å aktivere funksjonsreferansen i Finance og Supply Chain Management.

Hver funksjonsreferanse tilsvarer en bestemt elektronisk faktureringsfunksjon som er i samsvar med de elektroniske faktureringskravene fra et land/område.

Følgende tabell viser listen listen over funksjonsreferanser som tillegget for Elektronisk fakturering støtter.

| Funksjonsreferanse | Navn                                              | Land/område |
|-------------------|---------------------------------------------------|----------------|
| BR-00053          | NF-e føderal – elektronisk faktura for Brasil       | Brasil         |
| BR-00095          | Brasilianske elektroniske fakturaer for NFS-e               | Brasil         |
| DK-00001          | E-fakturering til offentlig sektor (OIOUBL) – DK    | Danmark        |
| EG-00008          | E-fakturering for Egypt                             | Egypt          |
| ES-00025          | Elektronisk faktura for offentlig sektor           | Spania          |
| EUR-00023         | Den europeiske union, e-fakturering til den offentlige sektor       | Europa         |
| ITA-00036         | IT - E-fakturering til offentlig sektor (FatturaPA) | Italia          |
| MX-00010          | E-fakturering av CFDI                                  | Mexico         |
| MX-00016          | E-fakturering CFDI – annulleringsprosess           | Mexico         |

I tilfeller der det er en eldre funksjon for elektronisk fakturering, som støttes av landets lokaliseringsområde, gjør aktiveringen av funksjonsreferansen det mulig å utstede elektroniske fakturaer via tillegget for Elektronisk fakturering, og slår av den tidligere funksjonen.

## <a name="submit-electronic-documents"></a>Send elektroniske dokumenter

Prosessen med å sende elektroniske dokumenter representerer det eneste kommunikasjonspunktet mellom Finance og Supply Chain Management og tillegget for Elektronisk fakturering. Under hver innsendingshendelse flyter kommunikasjonen i begge retninger:

- **Fra Finance og Supply Chain Management til tillegget for Elektronisk fakturering** – Finance og Supply Chain Management sender de abstrakte fakturaene til tillegget for Elektronisk fakturering. Etter behov sender de også innholdet med variabler som ble konfigurert som en del av funksjonene for elektronisk fakturering.
- **Fra Finance og Supply Chain Management til tillegget for Elektronisk fakturering** – Avhengig av funksjonen for Elektronisk fakturering mottar Finance og Supply Chain Management oppdateringer fra tillegget for Elektronisk fakturering om behandlingsresultatene til fakturaer som tidligere ble sendt inn. De mottar også innholdet med variabler som ble konfigurert som en del av funksjonene for Elektronisk fakturering.

Hvis du vil sende elektroniske dokumenter til tillegget for Elektronisk fakturering, går du til Finance og Supply Chain Management og deretter **Organisasjonsadministrasjon &gt; Periodisk &gt; Elektroniske dokumenter &gt; Send elektroniske dokumenter**.

Utgangspunktet er en postert faktura. Denne fakturaen kan komme fra ulike opprinnelser, for eksempel salgsordrer, prosjektfakturaer eller fritekstfakturaer.

Innsendingsprosessen kan kjøres manuelt eller i bakgrunnen.

- **Manuell kjøring** – For manuell kjøring må du bruke alternativet **Filter** for å definere intervallet av dokumenter som må sendes. På siden **Filtre** kan du konfigurere din egen spørring til å velge de posterte fakturaene som må sendes. Når valget er gjort, må du manuelt starte kjøringen av behandlingen og vente til den er fullført. Når behandlingen er fullført, viser en melding i handlingssenteret antall elektroniske dokumenter som er sendt.
- **Bakgrunnskjøring** – Bakgrunnskjøring kjører uten at du må logge deg på eller holde sendingsdialogboksen åpen. Du kan planlegge at prosessen skal kjøre og definere kjøringsfrekvensen.

## <a name="view-the-submission-logs"></a>Vise sendelogger

I Finance og Supply Chain Management kan du bruke sendeloggene til å vise resultatene av å behandle sendingen til tillegget for Elektronisk fakturering. Gå til **Organisasjonsstyring &gt; Periodisk &gt; Elektroniske dokumenter &gt; Elektronisk dokumentsending**, og deretter, i **Dokumenttype**-feltet, velger du en verdi for å filtrere fakturatypene som loggene viser.

Det finnes tre mulige innsendingsstatuser:

- **Planlagt** – Tillegget for Elektronisk fakturering har mottatt sendingen fra Finance and Supply Chain Management, og behandling av funksjonen for Elektronisk fakturering pågår.
- **Fullført** – Tillegget for Elektronisk fakturering har behandlet den elektroniske faktureringsfunksjonen slik den ble konfigurert til kjøre den.
- **Mislykket** – Tillegget for Elektronisk fakturering fant en feil eller ble stoppet av et unntak under behandling av funksjonen for Elektronisk fakturering.

> [!IMPORTANT]
> Sendestatusen viser til statusen for behandlingen som tillegget for Elektronisk fakturering behandler i forbindelse med funksjonen for Elektroniske fakturering. Den refererer ikke til den endelige statusen til selve den elektroniske fakturaen.
>
> Hvis for eksempel en elektronisk faktura må sendes til en ekstern webtjeneste for godkjenning, kan innsendingsstatusen være **Fullført**, men statusen for den elektroniske fakturaen kan være **Avvist**. I dette tilfellet kunne tillegget for Elektronisk fakturering behandle den elektroniske faktureringsfunksjonen slik den ble konfigurert til kjøre den. Den elektroniske fakturaen ble imidlertid avvist fordi den ikke oppfyller kriteriene som webtjenesten fastsatte for fakturagodkjenning.

Sendeloggene inneholder følgende tilleggsfunksjoner:

- **Innsendingsdetaljer** – Vis detaljene for hovedinnsendingen. Visualiseringen viser den fullstendige utførelsesloggen for handlingene som er konfigurert i funksjonen for Elektronisk fakturering. Det gjør det også mulig for brukere å laste ned filene som opprettes under behandlingen. I scenarier der fakturaen må godkjennes av en ekstern webtjeneste, er det mulig for brukere å vise statusen til fakturaen.
- **Relaterte innsendinger** – Vis detaljene for underordnede innsendinger.
- **Avbryt innsendinger** – Denne funksjonen aktiverer en spesiell innsendingsprosess i scenarier der den elektroniske fakturaen må godkjennes av en ekstern webtjeneste. Den instruerer tillegget for Elektronisk fakturering om å sende webtjenesten en bestemt melding som skal avbryte statusen til en godkjent elektronisk faktura i webtjenestedatabasen.
- **Send dokumenter på nytt** – Sender et elektronisk dokument på nytt som allerede er sendt til tillegget for Elektronisk fakturering. Det opprettes en helt ny logg på siden for **Innsendingsdetaljer**.
- **Send relatert innsending**
