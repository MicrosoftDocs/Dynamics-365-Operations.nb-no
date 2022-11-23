---
title: Forskuddsbetalinger i Dynamics 365 Commerce
description: Denne artikkelen gir en oversikt over behandlingen for transaksjoner for forskuddsbetaling i Microsoft Dynamics 365 Commerce.
author: BrianShook
ms.date: 11/15/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2021-06-28
ms.openlocfilehash: 8262470f83481ef8840857a52948c0833d8b278e
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/16/2022
ms.locfileid: "9780364"
---
# <a name="prepayments-in-dynamics-365-commerce"></a>Forskuddsbetalinger i Dynamics 365 Commerce

[!include[banner](../includes/banner.md)]

Denne artikkelen gir en oversikt over behandlingen for transaksjoner for forskuddsbetaling i Microsoft Dynamics 365 Commerce.

Dynamics 365 Commerce behandler forskuddsbetalingstransaksjoner for følgende betalingstyper som brukes i Kunder eller Commerce:

- **Innbetaling på kundekonto** – En kunde betaler et innbetalingsbeløp ved salgsstedet (POS). Commerce behandler betalingen som en forskuddsbetalingstransaksjon. Når du posterer transaksjonen, opprettes og posteres en betalingsjournal på **Journalbilag**-siden i Commerce headquarters. Avmerkingsboksen **Journalbilag for forskuddsbetaling** i fanen **Betaling** velges automatisk for betalingsjournalen.. Hvis du vil ha mer informasjon, inkludert forskuddsbetaling og skattespesifikk informasjon som er relevant for målområdet, kan du se [det spesifikke hjelpinnholdet for Globaliseringsressurser – Land-/område](/dynamics365/fin-ops-core/dev-itpro/lcs-solutions/country-region?context=%2Fdynamics365%2Fcontext%2Ffinance#countryregion-specific-help-content).
- **Kundeordre som har et innbetalingsbeløp** – En kunde oppretter en kundeordre på salgsstedet. Kunden kan betale et innbetalingsbeløp for ordren, basert på standard innbetalingsprosent som er konfigurert på **Kundeordrer**-siden i Commerce headquarters (**Commerce-parametere \> – Kundeordrer**). Commerce behandler innbetalingen for kundeordren som en forskuddsbetalingstransaksjon. Når du posterer transaksjonen, opprettes og posteres en betalingsjournal på **Journalbilag**-siden. Avmerkingsboksen **Journalbilag for forskuddsbetaling** i fanen **Betaling** velges automatisk for betalingsjournalen.. Betalingen utlignes, og kundefakturaen utstedes automatisk når ordren plukkes eller leveres.
- **Telefonsenter-salgsordrer** - En kundeservicerepresentant for telefonsenter oppretter en salgsordre på vegne av en kunde, og attributtet for **forskuddsbetaling** settes til **Ja** i løpet av betalingsregistreringen.

Commerce utfører følgende oppgaver for å behandle en forskuddsbetaling:

- **Behandle en kundekontoinnbetaling** – En innbetaling som en kunde foretar, overføres til Commerce ved hjelp av en tjeneste som synkroniserer data. Commerce oppretter en detaljbetalingstransaksjon for betalingen. Når du posterer detaljhandelstransaksjonen, posteres det en kontantjournal eller en kundebetalingsjournal. Det merkes automatisk av for **Journalbilag for forskuddsbetaling** på fanen **Betaling** på siden **Journalbilag** i Commerce headquarters for betalingsjournalen. Forskuddsbetalinger kan ikke behandles hvis betalingsbeløpet er negativt.
- **Behandle en kundeordre eller salgsordre som har en innbetaling** – En kunde betaler et nødvendig innbetalingsbeløp for en kundeordre ved å bruke Commerce Data Exchange: Sanntidsservice. Commerce oppretter enten en kundebetalingsjournal eller en kontantjournal, avhengig av betalingsmåten som kunden bruker. Det merkes automatisk av for **Journalbilag for forskuddsbetaling** på fanen **Betaling** på siden **Journalbilag** for betalingsjournalen i Commerce headquarters. Hvis en kunde bruker flere betalingsmåter for å foreta delbetalinger, behandler Commerce hver delbetaling basert på betalingsmåten som ble brukt.

For kredittkort og for digitale hentinger som har underliggende kredittkortbetalingsmetoder, sender Commerce en "registrering"-forespørsel etter vellykket autorisasjon. (Midler registreres før salgsordren faktureres.)

Hvis du annullerer en kundeordre, blir forskuddsbetalingsbeløpet refundert, og en journal for refusjon blir postert for innbetalingsbeløpet. Refusjonsbeløpet blir beregnet og postert, basert på betalingsmåten du angav da du posterte refunderingsbetalingen. Commerce kan bruke en annulleringsavgift, basert på prosenten du angir på **Commerce-parameter** siden i Commerce Headquarters.

Hvis du returnerer en kundeordre, opprettes det en returordre og en journal for refusjonsbetaling. Når du posterer returordren, oppretter Commerce enten en kundebetalingsjournal eller en kontantjournal, avhengig av betalingsmåten som kunden brukte for den opprinnelige transaksjonen.
