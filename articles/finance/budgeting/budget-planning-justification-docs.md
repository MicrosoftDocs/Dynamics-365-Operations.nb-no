---
title: Dokumenter for budsjettplanleggingsjusteringer
description: Justeringsdokumenter gir en narrativ beskrivelse for dem som ber om et budsjett for å forklare hvorfor et bestemt budsjett er nødvendig.
author: panolte
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BudgetPlanJustificationTemplate
audience: Application User
ms.reviewer: roschlom
ms.custom: 259594
ms.assetid: 52576fad-32b9-48f2-8197-c11ec313fc29
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 9ca0c291b5d446325f6be6b6bed612bd26e7c640
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/16/2021
ms.locfileid: "5019209"
---
# <a name="budget-planning-justification-documents"></a>Dokumenter for budsjettplanleggingsjusteringer

[!include [banner](../includes/banner.md)]

Justeringsdokumenter gir en narrativ beskrivelse for dem som ber om et budsjett for å forklare hvorfor et bestemt budsjett er nødvendig. 

En budsjettplanmal opprettes av budsjettansvarlig i Microsoft Word og tilordnes den gjeldende budsjettplanleggingsprosessen. Budsjetteierne kan deretter åpne malen og la data fylles ut automatisk i Word basert på budsjettforespørselen. De kan deretter legge til ekstra tekst eller data før de lagrer og knytter det personlige justeringsdokumentet til budsjettplanen.

##### <a name="set-up-microsoft-dynamics-office-add-in-for-microsoft-word"></a>Konfigurere Microsoft Dynamics Office-tillegget for Microsoft Word

1.  Åpne et nytt Microsoft Word-dokument.
2.  Klikk **Sett inn** på båndet, og klikk **Butikk**.
3.  Søk etter Microsoft Dynamics Office-tillegg, og klikk **Legg til**.
4.  Klikk **Legg til serverinformasjon** i den høyre ruten i Word.
5.  Skriv inn eller lim inn URL-adressen for serveren, og klikk **OK**.

##### <a name="define-the-justification-template-in-microsoft-word"></a>Definere justeringsmalen i Microsoft Word

1.  Klikk **Utforming** i Microsoft Dynamics Office-tillegget etter at du har logget på.
2.  For hodeinformasjon bruker du **Legg til felt**-knappen.
3.  Velg datakilden for enhet for BudgetPlanJustification, og klikk **Neste**. **Merk:** Denne enheten er nødvendig for alle justeringsdokumenter. Andre enheter kan brukes, men opplastingen tilbake til Microsoft Dynamics 365 Finance mislykkes hvis denne enheten ikke er inkludert.
4.  Legg til etikettene og verdiene for BudgetPlanName, BudgetPlanPreparer, ResponsibilityCenter og DocumentNumber i Word-dokumentet. **Merk:** Du kan bruke egendefinerte etiketter i stedet for standardetikettene, hvis nødvendig.
5.  Klikk **Utført** for å fullføre topptekstdelen.
6.  For linjenivådetaljer for budsjettplanbeløp klikker du **Legg til tabell**.
7.  Velg igjen datakilden for enhet for BudgetPlanJustification, og klikk **Neste**.
8.  Legg til felt for EffectiveDate, ScenarioName, AccountDisplayValue og AccountingCurrencyExpenseAmount. **Merk:** Hvis det finnes kommentarer som kan legges til i individuelle budsjettplanlinjer, kan de legges til i tabellen her.
9.  Legg til eventuelle instruksjoner til sluttbrukeren, og angi nødvendig formatering eller stiler i dokumentet.
10. Lagre dokumentet på den lokale datamaskinen, og lukk filen før du fortsetter.

##### <a name="set-up-the-budget-planning-process-to-use-the-justification-template"></a>Konfigurere budsjettplanprosessen for å bruke justeringsmalen

1.  Gå til **Budsjettering** &gt; **Oppsett** &gt; **Budsjettplanlegging** &gt; **Maler for justeringsdokument**.
2.  Klikk **Ny**, og bla til det nylig opprettede Microsoft Word-dokumentet.
3.  Angi et malvisningsnavn og en beskrivelse. Klikk **OK**.
4.  Gå til **Budsjettering** &gt; **Oppsett** &gt; **Budsjett** **planlegging** &gt; **Budsjettplanleggingsprosess**.
5.  Velg prosessen der justeringsmalen skal brukes, og klikk **Rediger**.
6.  I feltet **Mal for justeringsdokument** velger og lagrer du den relevante malen.

##### <a name="edit-and-save-personalized-justification-documents"></a>Redigere og lagre tilpassede justeringsdokumenter

1.  Opprett en ny budsjettplan, eller åpne en eksisterende.
2.  På **Justering**-rullegardinmenyen velger du **Opprett ny justering**.
3.  Når du har fylt ut detaljene, velger du å laste opp det egendefinerte dokumentet fra **Justering**-rullegardinmenyen.




