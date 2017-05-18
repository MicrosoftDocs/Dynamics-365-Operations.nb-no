---
title: Materialerstatning i produksjon
description: "Dette emnet beskriver hvordan du kan erstatte materialer i løpet av produksjonsprosessen."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ProdBOM
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 70171
ms.assetid: ce3b11ef-550e-49b7-8942-2607c2ec3c5c
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 6936f75cac04dc20d4e14e7635f6ab86454c092b
ms.contentlocale: nb-no
ms.lasthandoff: 04/25/2017


---

# <a name="material-substitution-in-manufacturing"></a>Materialerstatning i produksjon

[!include[banner](../includes/banner.md)]


Dette emnet beskriver hvordan du kan erstatte materialer i løpet av produksjonsprosessen. 

Det finnes tre metoder for å erstatte materialer i løpet av produksjonsprosessen:

-   Etter dato, når ett materiale erstattes met et annet etter en bestemt dato
-   Under hovedplanlegging, når et materiale i en formel erstattes med et annet materiale, fordi det er utsolgt
-   Under produksjonen, når et materiale uventet blir utsolgt og blir erstattet med et annet materiale

## <a name="substituting-material-by-date"></a>Erstatte materiale etter dato
Vurder følgende scenario: En maskin som et selskap produserer inneholder en komponent som utgår fra leverandørens katalog om to måneder. Fra utløpsdatoen og fremover tilbyr leverandøren en ny komponent som kan erstatte den gamle komponenten. Fra og til-gyldighetsdatoer defineres på stykklistelinjer. I dette eksemplet kan du sette opp den gamle komponenten til å utløpe ved å angi utløpsdatoen i **Til dato**-feltet. I stykklisten du deretter sette opp den nye erstatningskomponenten slik at den er gyldig fra dagen etter at den gamle komponenten er utløpt. Du gjør dette ved å angi startdatoen i **Fra dato**-feltet.

## <a name="substituting-material-by-planning"></a>Erstatte materiale etter planlegging
Du kan erstatte materialer under planlegging bare når du bruker formler, ikke når du bruker en stykkliste. Vurder følgende scenario: Et matproduksjonsfirma lager en saus fra en formel som inneholder 20 ingredienser. Én ingrediens i formelen kan erstattes av én av to andre ingredienser. Fordi disse to ingrediensene er dyrere enn den foretrukne ingrediensen, brukes erstatning imidlertid bare hvis den foretrukne ingrediensen ikke finnes på lager. Materialet som kan erstattes, kalles A, mens de to materialene som kan erstatte det, kalles B og C. Materialerstatning ved planlegging styres av feltene **Planleggingsgruppe** og **Prioritet** i formellinjer. I dette eksemplet oppretter du formellinjer for de tre materialene og knytter formellinjene til den samme planleggingsgruppen. Formellinjen for materiale A har høyest prioritet (laveste tall), formellinjen for materiale C har laveste prioritet og formellinjen for materiale B har prioriteten mellom prioriteten for de to andre linjene i oppsettet. Hvis du har etterspørsel etter den ferdige varen, bestemmer hovedplanleggingen først om etterspørselen etter materiale A kan dekkes. Hvis etterspørselen ikke kan dekkes, ser hovedplanlegging på materialer B og C, i prioritert rekkefølge. Hvis materiale B er på lager, brukes det når en planlagt partiordre er autorisert for formelen. Hvis ingen av materialene er tilgjengelige, oppretter hovedplanleggingen en planlagt bestilling for materiale A. **Obs:** Når du definerer formellinjer i en planleggingsgruppe, bør du bare angi et antall på materialet som har høyest prioritet. Dette antallet brukes til å beregne etterspørselen av alle materialer i planen, også materialene som har lavere prioritet. Du kan ikke angi forskjellige antall for varer på lavere prioritet i planleggingsgruppen.

## <a name="substituting-material-during-production"></a>Erstatte materiale under produksjon
Tenk deg følgende: en metallplate er nødvendig for en sveiseoperasjon. Under operasjonen informerer en lagermedarbeider maskinoperatøren om at platen ikke finnes på lager. Det er imidlertid besluttet at platen kan bli erstattet med en plate som er litt tykkere. På denne måten kan operasjonen fullføres. Materiale kan legges til i stykklisten for en åpen produksjonsordre. Hvis produksjonsordren har statusen **Startet**, blir brukere bedt om å beregne ordren på nytt når de legger til en ny vare i produksjonsstykklisten. Når materialet er lagt til, du kan opprette en ny plukkliste for den nye varen. Du trenger ikke legge til det nye materialet i produksjonsstykklisten. I stedet kan du legge den direkte til produksjonsplukklisten. Deretter, når plukklisten posteres, vil systemet legge til materialet i produksjonsstykklisten.




