---
title: Spore genererte rapportresultater og sammenligne dem med basisverdier
description: Dette emnet gir informasjon om hvordan du kan sammenligne resultatene av genererte ER-rapporter med basisrapportverdier.
author: NickSelin
manager: AnnBe
ms.date: 05/25/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.translationtype: HT
ms.sourcegitcommit: 2fc887668171175d436b9eb281a35c1c9d089591
ms.openlocfilehash: 1a598d0bd053c60c3f8df6b05ecb7ff15addfaa3
ms.contentlocale: nb-no
ms.lasthandoff: 08/09/2018

---

# <a name="trace-generated-report-results-and-compare-them-with-baseline-values"></a>Spore genererte rapportresultater og sammenligne dem med basisverdier

[!include[banner](../includes/banner.md)]

Du kan spore resultatene av ER-formater som genererer utgående elektroniske dokumenter. Når sporingsgenerering er aktivert (ER-brukerparameteren **Kjør i feilsøkingsmodus**), genereres en ny post i ER-formatkjøringsloggen hver gang en ER-rapport kjøres. Følgende detaljer er lagret i hvert spor som er generert:

- Alle advarsler som ble generert av valideringsregler
- Alle feil som ble generert av valideringsregler
- Alle genererte filer som lagres som vedlegg i oppføringensposten

Du kan lagre individuelle basisprogramfiler for et hvilket som helst ER-format. Filer regnes som basisfiler når de beskriver de forventede resultatene av rapporter som kjøres. Hvis en basisfil er tilgjengelig for et ER-format som ble utført mens spor generering ble aktivert, lagrer sporingen, i tillegg til detaljene som ble nevnt tidligere, resultatet av sammenligningen av det genererte elektroniske dokumentet til basisfilen. Med ett klikk finner du også det genererte elektroniske dokumentet og basisfilen i en enkelt zip-fil. Deretter kan du også gjøre detaljert sammenligning ved hjelp av et eksterne verktøy, for eksempel Windiff.

Du kan vurdere sporingen for å analysere om de elektroniske dokumentene som genereres, inkluderer det forventede innholdet. Du kan gjøre denne evalueringen i en testemiljø for brukeraksept (UAT) når kodegrunnlaget endres (for eksempel når du overførte til en ny forekomst av programmet, installerte hurtigreparasjonspakker eller distribuerte endringer i koden). På denne måten kan du kontrollere at evalueringen ikke påvirker utførelsen av ER-rapporter som brukes. For mange ER-rapporter kan du gjøre evalueringen i uovervåket modus.

Hvis du vil vite mer om denne funksjonen, kan du spille av oppgaveveiledningene **ER Generere rapporter og sammenligne resultater (del 1)** og **ER Generere rapporter og sammenligne resultater (del 2)**, som er del av **7.5.4.3 Teste IT-tjenester/-løsninger (10679)**-forretningsprosessen og kan lastes ned fra [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684). Disse oppgaveveiledningene forklarer deg hvordan du konfigurere ER-rammeverket for å bruke basisfiler for å evaluere genererte elektroniske dokumenter.

