---
title: Publisere kladdelinjer og dokumenter fra Excel
description: "Dette emnet forklarer hvordan du angir og publiserer linjer for økonomijournaler fra Microsoft Excel. Den inneholder informasjon om de ulike malene du kan bruke, avhengig av hvilken type transaksjoner som du skriver inn."
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

# <a name="publish-journal-lines-and-documents-from-excel"></a>Publisere kladdelinjer og dokumenter fra Excel

Dette emnet forklarer hvordan du angir og publiserer linjer for økonomijournaler fra Microsoft Excel. Den inneholder informasjon om de ulike malene du kan bruke, avhengig av hvilken type transaksjoner som du skriver inn.

Brukere kan angi og publisere linjer for finansjournaler fra Microsoft Excel. Når en bruker oppretter en journal, den **åpner linjer i Excel** knappen vises maler som er tilgjengelige. Malene er utformet for å støtte bestemte scenarier, men ikke alle kombinasjoner av kontotypen støttes i journalen. Tabellen nedenfor viser malene som er tilgjengelige og kontotypene som de støtter.
|                          |                                                                                                                         |                                                                                         |
|--------------------------|-------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| **Template**             | **Støttede kontotypene**                                                                                             | **Få tilgang til malen**                                                          |
| Finansjournallinjer     | : Finans, kunde, leverandør, Bank forskyvning konto: finans, kunde, leverandør, Bank konserninterne støttes.       | Økonomijournal                                                                         |
| Ankomstregistrering         | Kontoen: Motkonto leverandør: finans konserninterne støttes ikke.                                                    | AP ankomstregistrering                                                                     |
| Fakturajournal          | Kontoer: Motkonto leverandør: finans konserninterne støttes.                                                      | AP-fakturajournal                                                                      |
| Leverandørfaktura           |                                                                                                                         | Leverandørfaktura                                                                          |
| Kundefakturajournal | Kontoen: Motkonto kunde: finans konserninterne støttes.                                                     | Økonomijournal                                                                         |
| Fritekstfaktura        |                                                                                                                         | På den **fritekstfaktura** klikker du **åpne i Excel** (Microsoft Office-ikonet). |
| Anleggsmiddeljournal     | Anleggsmidler til finans, bank, kunde eller leverandør. Konserninterne støttes ikke.                                               | Anleggsmiddeljournal                                                                     |
| Leverandørbetalingsjournal   | Kontoen: Motkonto leverandør: finans, Bank konserninterne støttes.                                                 | Leverandørbetalingsjournal                                                                  |
| Kundebetalingsjournal | Kontoen: Motkonto kunde: finans, Bank konserninterne støttes.                                               | Kundebetalingsjournal                                                                |
| Prosjektutgiftsjournal  | Konto: Prosjekt, finans, kunde, leverandør forskyvning konto: Project, finans, kunde, leverandør konserninterne støttes. | Finanskladd utgifter (under prosjektstyring og regnskap)                       |

Når linjene er publisert, valideres for å sikre at de overholder reglene som er definert i i finansjournaler. Når linjene er publisert, kan brukere redigere eller postere bilagene fra Microsoft Dynamics 365 for operasjoner. 

Hvis du vil legge til økonomiske dimensjoner i en mal, kreves det ytterligere endringer. Hvis du vil ha mer informasjon, se [Legg til dimensjoner i Microsoft Excel-malen](\dev-itpro\financial-dimensions\add-dimensions-excel-templates). Etter dimensjoner blir lagt til enheten, de er tilgjengelige i Excel designer og kan legges til i malen.




