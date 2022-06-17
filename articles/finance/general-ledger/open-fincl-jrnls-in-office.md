---
title: Åpne finansjournalmaler i Office
description: Denne artikkelen beskriver problemer som kan oppstå når du oppretter egendefinerte finansjournaler ved hjelp av en Microsoft Excel-mal.
author: kweekley
ms.date: 05/14/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2020-05-14
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: a29ab1cb2980ebfed6c6fa6409538bc802849156
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8896354"
---
# <a name="open-financial-journal-templates-in-office"></a>Åpne finansjournalmaler i Office

[!include [banner](../includes/banner.md)]

Denne artikkelen beskriver problemer som kan oppstå når du oppretter egendefinerte finansjournaler ved hjelp av en Microsoft Excel-mal.

## <a name="symptom"></a>Symptom

Du har opprettet en egendefinert Excel-mal for finansjournaler, men den vises ikke på menyen **Åpne linjer i Excel**. Hvis det eventuelt vises i menyen, åpnes en annen mal, men når du velger den.

## <a name="resolution"></a>Løsning

Standardfunksjonen Åpne i Excel bruker rotdatakilden (tabell) på den gjeldende siden til å fastslå hvilke Office-maler eller dataenheter som skal vises som alternativer på menyen **Åpne i Excel**. Denne virkemåten er ikke en ideell funksjon for finansjournaler fordi finansjournaler bruker de samme tabellene (LedgerJournalTable og LedgerJournalTrans) som rotdatakilden for mange andre journaltyper.

For finansjournaler er Åpne linjer i Excel-funksjonen ment å vise maler som er utformet for journalen du for øyeblikket arbeider i sammenheng med, for eksempel økonomijournalen eller en betalingsjournal. En mal som for eksempel er ment å brukes med en leverandørbetalingsjournal, er utformet for å fremtvinge primærkontoen som en leverandørkonto.

Hvis du vil promotere en mal slik at den er tilgjengelig på menyene **Åpne linjer i Excel** og **Åpne i Excel**, er det en enkel utviklerfunksjon å implementere grensesnittet **LedgerIJournalExcelTemplate** og utvide klassen **DocuTemplateRegistrationBase**. Mange eksempler på denne fremgangsmåten er implementert i systemet. Et eksempel som kan brukes som referanse, er grensesnittet **LedgerDailyJournalExcelTemplate** som ble opprettet for økonomijournalen (eller den daglige journalen).

Når grensesnittet **LedgerIJournalExcelTemplate** er implementert for malen, filtrerer menyen **Åpne linjer i Excel** maler etter journaltypen til journalen din og viser bare malene som er tilgjengelige for den journalen. Grensesnittet gir også en valideringsmetode som sikrer at en mal ikke kan åpnes for en journal hvis den ikke oppfyller kontotypekravene. Du kan for eksempel angi at kontotypen må være av typen **Leverandør** eller **Finans**.

Hvis du vil ha mer informasjon om denne funksjonaliteten, kan du se [Legg til maler på menyen Åpne linjer i Excel](../../fin-ops-core/dev-itpro/user-interface/add-templates-open-lines-excel-menu.md).
