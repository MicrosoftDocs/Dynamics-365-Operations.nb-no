---
title: Oversikt over å planlegge laster ved hjelp av hubkonsolidering
description: Denne artikkelen beskriver funksjonen for konsolidering av forsendelser i en hub når du leverer varer fra forskjellige lagre til samme kunde, eller når du mottar varer fra flere leverandører på samme lager.
author: Weijiesa
ms.date: 07/25/2019
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: WHSLoadPlanningWorkbench, WHSHistory, WHSLoadTable, WHSLoadPlanningListPage, TMSParameters
audience: Application User
ms.reviewer: kamaybac
ms.custom:
- "92273"
- intro-internal
ms.assetid: d27b0926-a534-4caf-a2a3-acbc7c440bca
ms.search.region: Global
ms.search.industry: Distribution
ms.author: weijiesa
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 055d7c53b771e09002c84c643c45d3da9f71aca0
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/03/2022
ms.locfileid: "8676558"
---
# <a name="plan-loads-using-hub-consolidation-overview"></a>Oversikt over å planlegge laster ved hjelp av hubkonsolidering

[!include [banner](../includes/banner.md)]

Denne artikkelen beskriver funksjonen for konsolidering av forsendelser i en hub når du leverer varer fra forskjellige lagre til samme kunde, eller når du mottar varer fra flere leverandører på samme lager.

Det kan være nyttig å konsolidere forsendelser i en hub når du leverer varer fra forskjellige lagre til samme kunde, eller når varene leveres fra flere leverandører til samme lager.

## <a name="building-loads"></a>Planlegge laster
Før du kan bruke hubkonsolidering, må du aktivere alternativet **I transitt-planlegging** på siden **Parametere for transportstyring**. Du må også opprette huber der konsolidering vil utføres. Diagrammet nedenfor viser et eksempel på hubkonsolidering. I så fall vil salgsordrer fra forskjellige lagre sendes til samme kunde. Grunnleggende laster opprettes basert på salgsordrer på vanlig måte, ved hjelp av siden **Arbeidsområde for lastplanlegging**. Hvis du vil konsolidere to laster i en hub før de sendes til kunden, går du til siden **Arbeidsområde for lastplanlegging** og velger **Hubkonsolidering** i **Transport**-feltet. Når du velger riktig hub for hver last, vil lastene ha huben som plasseringsmål. Du har også to transportforespørselslinjer i delen **Forsyning og behov** på siden **Arbeidsområde for lastplanlegging**. Deretter kan du legge disse to linjene til en ny last. Denne nye lasten vil ha begge salgsordrelinjene, og den har også huben som plukkadressen og kunden A som plasseringsmål. De tre lastene er deretter klar til å bli vurdert og rutes på samme måte som andre laster. Du kan velge transportøren som systemet foreslår for hver Last. [![Hubkonsolidering.](./media/hubconsol.jpg)](./media/hubconsol.jpg) Du kan også bruke samme fremgangsmåte for å konsolidere laster for flere overføringsordrer. I så fall er kunden A i det forrige diagrammet, et lager. Du kan også konsolidere laster for flere bestillinger, der lastene leveres fra forskjellige leverandører til samme lager. Du kan ha mer enn én konsolideringshub, og du kan konsolidere i flere huber for flere laster som kommer fra forskjellige lagre. Når du bygger dine grunnleggende laster og bruker alternativet for hubkonsolidering, kan du bygge de nye lastene ved hjelp av linjer for konsoliderte transportforespørsel. Deretter vurderer og distribuerer du lastene.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]