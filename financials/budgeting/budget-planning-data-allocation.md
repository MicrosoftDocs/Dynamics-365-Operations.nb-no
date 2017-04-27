---
title: Tildeling av data for budsjettplanlegging
description: Denne artikkelen beskriver de ulike tildelingsmetoder som er tilgjengelige i Microsoft Dynamics 365 for Operations, og hvordan de kan brukes.
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: BudgetPlanningConfiguration
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 15191
ms.assetid: 89a918e8-59a4-4711-a2e9-b41989ddd0f1
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 8e89a57dda8f2d392483ed13c686ea97b74926b0
ms.openlocfilehash: f717e9de361b5511ac4af360cddb1ea16ad4a1e2
ms.lasthandoff: 03/31/2017


---

# <a name="budget-planning-data-allocation"></a>Tildeling av data for budsjettplanlegging

[!include[banner](../includes/banner.md)]


Denne artikkelen beskriver de ulike tildelingsmetoder som er tilgjengelige i Microsoft Dynamics 365 for Operations, og hvordan de kan brukes.  

Du kan distribuere dataene i en budsjettplan på flere måter for å vise nøyaktig de forventede beløpene.

## <a name="allocation-methods"></a>Tildelingsmetoder
Tre tildelingsmetoder (tildele på tvers av perioder, tildele til dimensjoner og bruke finansfordelingsregler) kan opprette budsjettplanlinjer som er basert på linjene i den samme budsjettplanen. Tre andre metoder (aggregere, distribuere og kopiere fra budsjettplanen) kan opprette budsjettplanlinjer i andre budsjettplaner. Du kan angi målscenariet for alle seks tildelingsmetoder. Målscenariet kan være det samme som kildescenariet eller forskjellig fra kildescenariet. Du kan også angi om nye linjer legges til budsjettplanen eller erstatter gjeldende linjer i budsjettplanen.

[![Tildele på tvers av perioder](./media/allocateacrossperiods-300x259.png)](./media/allocateacrossperiods.png)
**Tildele på tvers av perioder** – En periodetildelingskategori brukes for å tildele budsjettplanlinjer fra kildebudsjettplanscenariet på tvers av perioder i målscenariet. Kildebeløpet tilordnes til flere linjer i målscenariet, basert på prosentdelen og datoen som er definert i periodetildelingsperioden.         

[![Tildele til dimensjoner](./media/allocatetodimensions.jpg)](./media/allocatetodimensions.jpg)
**Tildele til dimensjoner** – Budsjettplanlinjene tildeles fra kildebudsjettplanleggingsscenariet til én eller flere linjer i målscenariet, basert på prosentdelene og finansdimensjonene som er definert i en valgt budsjettfordelingsbetingelse.           

![Aggregere diagram](./media/aggregatechart-300x230.png)
**Aggregere** – Budsjettplanlinjene aggregeres fra kildebudsjettplanscenariet i de tilknyttede (underordnede) budsjettplanene til målscenariet i den overordnede budsjettplanen. Denne metoden gjør det mulig for budsjetterte beløp som er klargjort på et lavere nivå i organisasjonen, å konsolideres på et høyere nivå.          

[![Fordele diagram](./media/distributechart-300x230.png)](./media/distributechart.png)
**Fordele** – Budsjettplanlinjene fordeles fra kildebudsjettplanleggingsscenariet i den overordnede budsjettplanen, til målscenariet i de tilknyttede (underordnede) budsjettplanene, basert på finansdimensjonene for organisasjonsenhetene for de tilknyttede planene. Denne metoden gjør det mulig for budsjetterte beløp som er klargjort på et høyere nivå i organisasjonen, å spres ut for mer lokalisert gjennomgang.           

[![FInansfordelingsregler](./media/ledgerallocationrules-300x202.png)](./media/ledgerallocationrules.png)
**Bruk finansfordelingsregler** – Budsjettplanlinjene fordeles fra kildebudsjettplanscenariet i til målbudsjettplanleggingsscenariet basert på den valgte finansfordelingsregelen. 

[![Kopier fra budsjettplan](./media/copyfrombudgetplan-187x300.png)](./media/copyfrombudgetplan.png)
**Kopier fra budsjettplan** – Som i fordelingstildelingsmetoden, opprettes budsjettplanlinjer i målet, basert på linjene i en tilknyttet budsjettplan. For demme metoden trenger imidlertid ikke kildebudsjettplanen å være overordnet, men kan være på et høyere nivåer i budsjettplanhierarkiet. Denne tildelingsmetoden er nyttig hvis konsoliderte beløp opprinnelig budsjetteres på et mye høyere nivå og må overføres til et lavere nivå i organisasjonen for detaljert gjennomgang og justering, før vedkommende kan motta godkjenning på øverste nivå.          

## <a name="using-allocation-methods-in-a-budget-plan"></a>Bruke tildelingsmetoder i en budsjettplan
Hvis du vil utføre tildelinger på pudsjettplansiden, velger du linjene som skal tildele og klikker deretter **Tildel budsjett**.

[![AllocateBudgetButton](./media/allocatebudgetbutton-300x84.png)](./media/allocatebudgetbutton.png) 

Velg en tildelingsmetode. Deretter angis de gjenværende feltene i samsvar med metoden du har valgt. Disse feltene inneholder kilden og målet for budsjettplandataene og et alternativ som lar deg multiplisere kilden med en bestemt faktor når målbeløpene opprettes, for å forenkle samlet justering. Du kan også angi alternativet **Legg til i plan**. Velg **Nei** for å erstatte de eksisterende budsjettplanlinjene, eller velg **Ja** for å beholde de eksisterende budsjettplanlinjene og legge til nye linjer for de tilordnede beløpene.

## <a name="automating-allocations-during-a-workflow"></a>Automatisere tildelinger under en arbeidsflyt
En kraftig funksjon gjør det mulig å utføre tildelinger automatisk som en del av en arbeidsflyt for budsjettplanlegging. Når en budsjettplan flyttes gjennom arbeidsflyten, kan automatiserte oppgaver starte en tildeling på et bestemt budsjettplanleggingsstadium. 

Hvis du vil angi automatisk tildeling, må du først opprette en tildelingsplan på siden **Budsjettplanleggingskonfigurasjon**. Tildelingsplanen definerer tildelingsmetoden som skal brukes når den automatisk tildelingen kjøres, og verdiene for de ulike alternativene for tildeling (se avsnittet for beskrivelser). 

Deretter oppretter du en stadietildeling på siden **Budsjettplanleggingskonfigurasjon**. Stadietildelingen tildeler en tildelingsplan til arbeidsflyten for budsjettplanlegging og stadiet. 

Til slutt legger du til en automatisert oppgave for tildeling for budsjettplanleggingsstadiet på det aktuelle arbeidsflytstadiet. I eksemplet nedenfor er to tildelinger for budsjettplanleggingsstadiet (uthevet i rødt) satt inn i arbeidsflyten.

[![Tildelinger for budsjettplanleggingsstadium](./media/budgetplanningstageallocations-300x300.png)](./media/budgetplanningstageallocations.png)




