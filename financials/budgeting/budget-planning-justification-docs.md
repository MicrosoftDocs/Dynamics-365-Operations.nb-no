---
title: Budsjett planleggingsdokumenter justering
description: "Justering-dokumenter gir en fortellende beskrivelsen for de ber om et budsjett til å forklare hvorfor et bestemt budsjett er nødvendig."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 259594
ms.assetid: 52576fad-32b9-48f2-8197-c11ec313fc29
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: c86d01fec3d8d7c210c7e73a034f4e9e384a0dcf
ms.lasthandoff: 03/31/2017


---

# <a name="budget-planning-justification-documents"></a>Budsjett planleggingsdokumenter justering

Justering-dokumenter gir en fortellende beskrivelsen for de ber om et budsjett til å forklare hvorfor et bestemt budsjett er nødvendig. 

En budsjettplanmal er opprettet av budsjettbehandling i Microsoft Word og tilordnet den gjeldende budsjettplanleggingsprosessen. Budsjett eierne kan deretter åpne malen og data fylles ut automatisk i Word basert på budsjettet forespørselen. De kan deretter legge til ekstra tekst eller data før du lagrer og legge sine personlige justeringsdokumentet til budsjettplanen.

##### <a name="set-up-microsoft-dynamics-office-add-in-for-microsoft-word"></a>Definer Microsoft Dynamics Office-tillegget for Microsoft Word

1.  Åpne et nytt Microsoft Word-dokument.
2.  Klikk **Sett inn** på båndet, og velg **Store**.
3.  Søke etter Microsoft Dynamics Office-tillegg, og klikk **Legg til**.
4.  Klikk i den høyre ruten i Word, **legge til informasjon om server**.
5.  Skriv inn eller lime inn URL-adressen for serveren, og klikk **OK**.

##### <a name="define-the-justification-template-in-microsoft-word"></a>Definere justering-malen i Microsoft Word

1.  Klikk **Design** i Microsoft Dynamics-kontor tillegget etter at du har logget på.
2.  For informasjon, kan du bruke den **legge til feltene** knappen.
3.  Velg datakilden for enhet for BudgetPlanJustification, og klikk **neste**. **Merk:** denne enheten er nødvendig for et dokument for justering. Andre enheter som kan brukes, men opplasting tilbake til Microsoft Dynamics 365 for operasjoner mislykkes hvis denne enheten ikke er inkludert.
4.  Legge til BudgetPlanName, BudgetPlanPreparer, ResponsibilityCenter og DocumentNumber etikettene og verdiene i Word-dokumentet. **Merk:** du kan bruke egendefinerte etiketter, i stedet for standard etikettene, hvis nødvendig.
5.  Klikk **gjort** å fullføre inndelingen for topptekst.
6.  For linje nivå detaljer av budsjettbeløp for planen, klikker du **Legg til tabell**.
7.  På nytt, velger du datakilden for enhet for BudgetPlanJustification, og klikk **neste**.
8.  Legge til felt for EffectiveDate, ScenarioName, AccountDisplayValue og AccountingCurrencyExpenseAmount. **Merk:** Hvis det finnes kommentarer til å legge til i individuelle budsjettplanlinjer, de kan legges til i tabellen her.
9.  Legg til eventuelle instruksjoner for å tilby sluttbrukeren, og utføre nødvendige formatering eller stiler i dokumentet.
10. Lagre dokumentet på den lokale datamaskinen, og lukk filen før du fortsetter.

##### <a name="set-up-the-budget-planning-process-to-use-the-justification-template"></a>Definere budsjettplanleggingsprosessen for å bruke malen for justering

1.  I Microsoft Dynamics 365 for operasjoner, kan du gå til **budsjettering**&gt;**Setup**&gt;**budsjettplanlegging**&gt;**begrunnelse dokumentmaler**.
2.  Klikk **ny**, og bla til det nylig opprettede Microsoft Word-dokumentet.
3.  Skriv inn et navn på mal for skjerm og en beskrivelse. Click **OK**.
4.  Gå til **budsjettering**&gt;**Setup**&gt;**budsjett****planlegging**&gt;**budsjett planleggingsprosessen**.
5.  Velg prosess der justeringsmal som skal brukes, og klikk **Rediger**.
6.  I den **begrunnelse dokumentmal** feltet, velg den relevante malen, og lagre.

##### <a name="edit-and-save-personalized-justification-documents"></a>Redigere og lagre tilpassede begrunnelse dokumenter

1.  Oppretter en ny budsjettplan i Dynamics 365 for operasjoner, eller åpne en eksisterende budsjettplan.
2.  I den **justering** -menyen, velg **opprette ny justering**.
3.  Fyll ut detaljene, kan du velge å laste opp egendefinerte dokumentet fra den **justering** -menyen.



