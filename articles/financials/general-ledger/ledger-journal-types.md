---
title: Finansjournaltyper
description: Dette emnet beskriver journaltypene som du kan definere for finansjournaler.
author: ShylaThompson
manager: AnnBe
ms.date: 10/10/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalSetup
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 15631
ms.assetid: 81613b31-bc3c-43a0-8474-e01c9a482c40
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0e344cfbcb1b3d034a1d36cbead8133ba47af8cc
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/01/2019
ms.locfileid: "1839045"
---
# <a name="ledger-journal-types"></a>Finansjournaltyper

[!include [banner](../includes/banner.md)]

Dette emnet beskriver journaltypene som du kan definere for finansjournaler. Bruk **Journalnavn**-siden til å definere journaler som du kan bruke i Microsoft Dynamics 365 for Finance and Operations.

| Journaltype                      | Formål                       | Angi transaksjoner på denne siden                                |
|-----------------------------------|-------------------------------|----------------------------------------------------------------|
| Tilordning                        | Opprett fordelingstransaksjoner i en fordelingsjournal. Før du kan opprette en fordelingjournal, må du opprette en fordelingsregel på siden **Fordelingsregel finans**.      | Behandle tildelingsforespørsel             |
| Godkjenning                          | Poster leverandørfakturaer som er godkjent, til de riktige finanskontoene.  | Fakturagodkjenningsjournal                                       |
| Annullering av banksjekk               | Tilbakefør en postert sjekk. Hvis du vil bruke denne journaltypen, merker du av for alternativet **Bruk vurderingsprosess for betalingsannulleringer** på siden **Parametere for kontant- og bankbehandling**.   | Sjekkannulleringer, Betalingsannullering                   |
| Annullering av bankbetalingsbilag    | Annuller et betalingsbilag. Hvis du vil bruke denne journaltypen, merker du av for alternativet **Bruk vurderingsprosess for betalingsannulleringer av betalingsbilag** på siden **Parametere for kontant- og bankbehandling**.   | Annullering av betalingsbilag            |
| Budsjett                            | Behandle budsjettbevilgninger. Hvis du vil bruke denne journaltypen, merker du av for alternativet **Aktiver budsjettbevilgning** på siden **Parametere for økonomimodul**. Budsjettjournaloppføringene inneholder informasjonen som er basert på finanskontoer som er definert på siden **Posteringsdefinisjoner**.                                                        |                                                                |
| Kundeaksept veksel  | Opprette kundegodkjenningstransaksjoner for veksler.             | Journal for vekseltrekking, Journal for ny vekseltilbaketrekking |
| Kunde: bankremisse          | Opprett en veksel som kan sendes til organisasjonens bank. Hvis du vil bruke denne journaltypen, fjerner du merket for alternativet **Automatisk utligning** på siden **Kontoer** **Kundeparametere**.            | Remittering                                                     |
| Kunde: trekk veksel    | Oprette transaksjoner for kunde: trekk veksel. Hvis du vil bruke denne journaltypen, fjerner du merket for alternativet **Opprett og poster trekkjournal automatisk ved postering av fakturaer** på siden **Betalingsmåter – kunder**.   | Journal for vekseltrekking                                  |
| Kundebetaling                  | Opprett kundebetalingstransaksjoner.                             | Betalingsjournal             |
| Kundeprotest veksel | Opprett transaksjoner for kundeprotest veksel.                    | Journal for vekselprotest                               |
| Kundens tilbaketrekking av veksel  | Oprette transaksjoner for kunde: trekk tilbake veksel.                     | Journal for ny vekseltilbaketrekking                                |
| Kunde: avregn veksel  | Opprett transaksjoner for kunde: avregn veksel.                       | Vekselavregningsjournal                                |
| Daglig                             | Opprett daglige transaksjoner i en økonomijournal.                          | Økonomijournal                                                |
| Eliminering                       | Opprett elimineringstransaksjoner i en elimineringsjournal. Hvis du vil bruke denne journaltypen, merker du av for alternativene **Brukes til finanseliminering** og **Bruk for finanskonsolideringsprosess** på siden **Juridiske enheter**. Før du kan bruke denne journaltypen, må du opprette en finanselimineringsregel på siden **Elimineringsregel, finans**. | Eliminering                                                    |
| Anleggsmiddelbudsjett                | Opprett budsjettregisterposter for anleggsmidler.                                                                                                                                                                                                                                                                                                                 | Anleggsmiddelbudsjett                                             |
| Ankomstregistrering                  | Registrer grunnleggende informasjon om leverandørfakturaer.                                                                                                                                                                                                                                                                                                           | Ankomstregistrering                                               |
| Lønnsutbetaling              | Utsted betalinger som er basert på lønnsoppgaver. Du kan ikke angi transaksjoner manuelt i denne journalen. Du må generere lønnsoppgaver og deretter sende de uttrykkene for betaling.                                                                                                                                                              |                                                                |
| Tidsbestemt                          | Opprett periodiske transaksjoner for den periodiske journalen.                                                                                                                                                                                                                                                                                                      | Periodiske journaler                                              |
| Poster anleggsmidler                 | Poster anleggsmiddeltransaksjoner.                                                                                                                                                                                                                                                                                                                              | Anleggsmidler                                                   |
| Prosjekt - utgifter                | Opprett utgiftstransaksjoner i prosjekt.                                                                                                                                                                                                                                                                                                                        | Expense                                                        |
| Justering for rapporteringsvaluta     | Opprett justeringer i rapporteringsvalutaen for saldoer på finanskontoer.               | Justeringsjournaler for rapporteringsvaluta                         |
| Statistikktransaksjoner            | Opprette statistiske transaksjoner.                                                                                                                                                                                                                                                                                                                            |                                                                |
| Leverandør: bankremisse            | Opprett en remitteringsfil for egenveksel som kan sendes til organisasjonens bank.                                                                                                                                                                                                                                                                      | Remitteringsjournal                                             |
| Leverandørbetaling               | Opprette transaksjoner for leverandørbetaling.                                                                                                                                                                                                                                                                                                                    | Betalingsjournal                                                |
| Leverandørtrekking egenveksel       | Trekke leverandøregenveksler som betalingsmåte. Hvis du vil bruke denne journaltypen, fjerner du merket for alternativet **Opprett og poster trekkjournal automatisk ved postering av fakturaer** på siden **Betalingsmåter – leverandører**.                                                                                                                                          | Journal for egenvekseltrekking                                   |
| Pulje for leverandørfakturaer ekskl. postering | Opprett leverandørfakturatransaksjoner som ennå ikke er postert til en midlertidig ankomstkonto.                                                                                                                                                                                                                                                             | Leverandørfakturapulje uten posteringsdetaljer                  |
| Leverandørfakturapulje               | Opprett transaksjoner for leverandørfakturapulje.                                                                                                                                                                                                                                                                                                                    |                                                                |
| Registrering av leverandørfaktura          | Poster leverandørfakturaer som er i en journal.                                                                                                                                                                                                                                                                                                                 | Fakturajournal                                                |
| Leverandørtilbaketrekking egenveksel     | Trekk tilbake en egenveksel som tidligere er innfridd av organisasjonens bank.                                                                                                                                                                                                                                                                      | Journal for egenvekseltilbaketrekking                                 |
| Leverandøravregning egenveksel     | Opprett transaksjoner for leverandøravregning egenveksel.                                                                                                                                                                                                                                                                                                          | Journal for egenvekselavregning                                 |





