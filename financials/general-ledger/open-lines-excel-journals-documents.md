---
title: Publisere journallinjer og dokumenter fra Excel
description: "Dette emnet forklarer hvordan du angir og publiserer linjer for økonomijournaler fra Microsoft Excel. Det inneholder informasjon om de ulike malene du kan bruke, avhengig av hvilken type transaksjoner som du skriver inn."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerJournalTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 62213
ms.assetid: 211874a7-4bf0-4a0c-96c2-fa05042777d3
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: 1fed8d162a37736883365fa765a059e5beff06be
ms.contentlocale: nb-no
ms.lasthandoff: 06/13/2017

---

# <a name="publish-journal-lines-and-documents-from-excel"></a>Publisere journallinjer og dokumenter fra Excel

[!include[banner](../includes/banner.md)]


Dette emnet forklarer hvordan du angir og publiserer linjer for økonomijournaler fra Microsoft Excel. Det inneholder informasjon om de ulike malene du kan bruke, avhengig av hvilken type transaksjoner som du skriver inn.

Brukere kan angi og publisere linjer for finansjournaler fra Microsoft Excel. Når en bruker oppretter en journal, viser knappen **Åpne linjer i Excel** malene som er tilgjengelige. Malene er utformet for å støtte bestemte scenarier, men ikke alle kombinasjoner av kontotypen støttes i journalen. Tabellen nedenfor viser malene som er tilgjengelige og kontotypene som de støtter.
|                          |                                                                                                                         |                                                                                         |
|--------------------------|-------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| **Mal**             | **Støttede kontotyper**                                                                                             | **Få tilgang til malen**                                                          |
| Finansjournallinjer     | Konto: Finans, Kunde, Leverandør, Bank motkonto: Finans, Kunde, Leverandør, Bank konsernintern støttes.       | Økonomijournal                                                                         |
| Ankomstregistrering         | Konto: Motkonto leverandør: Finans konsernintern støttes ikke.                                                    | AP-fakturaregister                                                                     |
| Fakturajournal          | Kontoer: Motkonto leverandør: Finans konsernintern støttes.                                                      | AP-fakturajournal                                                                      |
| Leverandørfaktura           |                                                                                                                         | Leverandørfaktura                                                                          |
| Kundefakturajournal | Konto: Motkonto kunde: Finans konsernintern støttes.                                                     | Økonomijournal                                                                         |
| Fritekstfaktura        |                                                                                                                         | På siden **Fritekstfaktura** klikker du **Åpne i Excel** (Microsoft Office-ikonet). |
| Anleggsmiddeljournal     | Aktiva til finans, bank, kunde eller leverandør. Konsernintern støttes ikke.                                               | Anleggsmiddeljournal                                                                     |
| Leverandørbetalingsjournal   | Konto: Motkonto leverandør: Bank konsernintern støttes.                                                 | Leverandørbetalingsjournal                                                                  |
| Kundebetalingsjournal | Konto: Motkonto kunde: Finans, Bank konsernintern støttes.                                               | Kundebetalingsjournal                                                                |
| Prosjektutgiftsjournal  | Konto: Prosjekt, Finans, Kunde, Leverandør, Motkonto leverandør: Prosjekt, Finans, Kunde, Leverandør, Leverandør konsernintern støttes. | Økonomijournal Utgift (under prosjektstyring og regnskap)                       |

Når linjene er publisert, valideres de for å sikre at de overholder reglene som er definert i finansjournaler. Når linjene er publisert, kan brukere redigere eller postere bilagene fra Enterprise-utgaven av Microsoft Dynamics 365 for Operationos. 

Hvis du vil legge til finansdimensjoner i en mal, kreves det ytterligere endringer. For mer informasjon, se [Legge til dimensjoner i Microsoft Excel-malen](/dynamics365/unified-operations/dev-itpro/financial/add-dimensions-excel-templates). Etter dimensjoner blir lagt til enheten, er de tilgjengelige i Excel designer og kan legges til i malen.






