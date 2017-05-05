---
title: Publisere journallinjer og dokumenter fra Excel
description: "Dette emnet forklarer hvordan du angir og publiserer linjer for økonomijournaler fra Microsoft Excel. Det inneholder informasjon om de ulike malene du kan bruke, avhengig av hvilken type transaksjoner som du skriver inn."
author: twheeloc
manager: AnnBe
ms.date: 2017-04-04
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: LedgerJournalTable
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 62213
ms.assetid: 211874a7-4bf0-4a0c-96c2-fa05042777d3
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ef99caf4570969d2b920cec8b53669ce2094965
ms.openlocfilehash: 087339cb3002b42bcb985c2ccfc2d97c752a817c
ms.lasthandoff: 03/31/2017


---

# <a name="publish-journal-lines-and-documents-from-excel"></a>Publisere journallinjer og dokumenter fra Excel

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

Når linjene er publisert, valideres de for å sikre at de overholder reglene som er definert i finansjournaler. Når linjene er publisert, kan brukere redigere eller postere bilagene fra Microsoft Dynamics 365 for Operationos. 

Hvis du vil legge til finansdimensjoner i en mal, kreves det ytterligere endringer. For mer informasjon, se [Legge til dimensjoner i Microsoft Excel-malen](\dev-itpro\financial-dimensions\add-dimensions-excel-templates). Etter dimensjoner blir lagt til enheten, er de tilgjengelige i Excel designer og kan legges til i malen.



