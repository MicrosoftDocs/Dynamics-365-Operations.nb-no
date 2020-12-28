---
title: Etterfylling med uttak – Kanbaner
description: Dette emnet beskriver hvordan kanban for uttak brukes til etterfylling av materialer til produksjonsaktiviteter.
author: johanhoffmann
manager: tfehr
ms.date: 06/16/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanBoardTransferJob, KanbanFlow, KanbanRules, WHSKanbanWaveTable, WHSKanbanWaveTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d0caa0020083138f702e4a1fda457b7075a9c87e
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4434724"
---
# <a name="replenishment-with-withdrawal-kanbans"></a>Etterfylling med uttak – Kanbaner

[!include [banner](../includes/banner.md)]

Dette emnet beskriver hvordan kanban for uttak brukes til etterfylling av materialer til produksjonsaktiviteter.

## <a name="workflow-for-material-replenishment-that-uses-the-withdrawal-kanban"></a>Arbeidsflyt for etterfylling av materialer som bruker kanban for uttak
-------------------------------------------------------------------

Kanban for uttak kan brukes til å flytte en kanban for en enkelt vare mellom lagre og produksjonslokasjoner der materialene forbrukes. Kanban for uttak støtter en pull-basert løsning for etterfylling av materialer, der et pull-signal er nødvendig for å utløse forsyning for et bestemt behov. 

Følgende scenario viser et pull-baserte etterfyllingssystem der et pull-signal utløser opprettelsen av en kanban for å etterfylle materialer for en produksjonsprosess. 

[![Pull-signal utløser opprettelsen av en kanban for å etterfylle materiale for en produksjonsprosess](./media/material-replenishment-with-withdrawal-kanban.png)](./media/material-replenishment-with-withdrawal-kanban.png)

1.  Uttak Kanban
2.  Kanban "fra"-lokasjon og plasseringsgslokasjon for lagerarbeid
3.  Kanban "til"-lokasjon og produksjonsinnleveringssted
4.  Produksjonsprosess
5.  Lagerarbeid for kanban-plukking
6.  Lagerlokasjoner for råvarer
7.  Materiallager
8.  Produksjonslager

I dette scenarietbruker en produksjonsprosess (4) materialer fra et produksjonsinnleveringssted (3) i produksjonslageret (8). Når en håndteringsenhet av materialet (kanban) er brukt, registreres den som tom. Et etterfyllingssignal blir opprettet for varens opprinnelsen, og det opprettes en ny kanban (1). I så fall består varens opprinnelsen av lokasjonene i materiallageret (7). Materialet for kanbanen plukkes og settes på en lokasjon (2) i det samme lageret. Når materialet er plukket, kan det overføres fra lokasjon 2 til produksjonsinnleveringsstedet (3) i produksjonslageret (8).

## <a name="configure-warehouse-work-for-kanban-picking-for-the-withdrawal-kanban"></a>Konfigurere lagerarbeid for kanban-plukking for uttaks-kanban

Hvis du vil aktivere råvareplukking for uttaks-kanban, konfigurerer du bølgemaler, arbeidsmaler og lokasjonsdirektiver for arbeidsordretypen **Kanban-plukking**. Denne ordretypen støtter ikke bare plukkprosessen for uttaks-kanban. Den støtter også plukkprosessen for produksjons-kanban. Du kan imidlertid konfigurere en egen plukkprosess for hver type kanban ved å skille bølgemaler, arbeidsmaler og lokasjonsdirektiver. Hvis du vil skille bølgemaler, maler for arbeid og lokasjonsdirektiver, må du angi vilkår på aktivitetstypen (**prosess** eller **overføring**) i spørringene for disse enhetene.

## <a name="configure-the-withdrawal-kanban"></a>Konfigurere uttaks-kanban

Overføringsaktiviteten som brukes for uttaks-kanban er konfigurert som en del av en aktivert aktivitetsplan i en Lean-produksjonsflyt. Som en del av konfigurasjonen av overføringsaktiviteten kan du angi "fra"- og "til"-lokasjoner for overføringen. Når du har konfigurert overføringsaktiviteten, kan du tilordne den til en kanban-regel for **uttak**-type. Kanban-regelen angir policyer og konfigurasjoner for uttaks-kanban. Kanbanens antall definerer hvor mange enheter av håndteringsenheten kanbanen bærer under overføringsprosessen. Fast kanban-antall brukes når fast etterfyllingsstrategi er valgt. Dette antallet angir hvor mange Kanbaner som kreves for å forhindre at lager eller beholdning går tomt ved behovskilden. Fast antall kan beregnes basert på faktisk etterspørsel, historisk etterspørsel og servicenivåer. Følgende to scenarier beskriver hvordan du kan administrere etterfylling av materialer som bruker uttaks-kanban.

## <a name="scenario-1-replenish-a-production-input-location-by-using-a-fixed-withdrawal-kanban"></a>Scenario 1: Etterfylle et produksjonsinnleveringssted ved å bruke en fast uttaks-kanban

En produksjonsprosess bruker et innkjøpt råmateriale fra et produksjonsinnleveringssted som er på produksjonslageret. Når råvaren mottas fra leverandøren, lagres den i lokasjoner på materiallageret. Fordi behovet for materialet anses stabilt i en periode, er det angitt til å forsyne produksjonen i en kanban-flyt med fast antall. Når en kanban forbrukes ved produksjonsinnleveringsstedet, registreres et tomt-signal, og en ny kanban av samme type legges til i flyten. 

Tomt-signalet kan konfigureres til å skje automatisk når en kanban er fullført. Alternativt kan tomt-signalet kan defineres som en manuell samhandling som gis enden fra Kanban-overføringstavlen eller fra en meny på den håndholdte enheten. Kanban-overføringstavlen er arbeidsområdet hvor alle aktiviteter i kanban-livssyklusen administreres. 

Når kanbanen opprettes, blir en bølgelinje for råvarer lagt til en kanban-bølge for materiallageret. I plukklistedelen av kanban-overføringstavlen kan statusen for materialer og tilknyttede lagerprosesser overvåkes fra bølgeopprettelse til arbeidsopprettelse, til materialet finnes på lokasjonen "Overfør fra" og er klart til å overføres til produksjonsinnleveringsstedene. Kanbanen kan fullføres fra Kanban-overføringstavlen eller en meny på den håndholdte enheten. 

I så fall behandles plukkarbeidet på materiallageret som én aktivitet. Overføringsaktiviteten mellom materiallageret og produksjonslageret behandles som en separat aktivitet. Denne fremgangsmåten kan være nyttig hvis det for eksempel er en fysisk stor avstand mellom de to lagrene. I så fall kan kanban-overføringsaktiviteten representere en trucklast. 

Hvis avstanden mellom lagerlokasjoner og produksjonsinnleveringsstedet er liten, kan det være mer effektivt å ta med overføringsaktiviteten i plukkprosessen. Deretter, når materialet er plukket, kan det bli plassert direkte til produksjonsinnleveringsstedet. For å støtte denne prosessen, konfigurerer du overføringsaktiviteten slik at den fylles ut automatisk når plukkarbeidet for uttaks-kanbanen behandles.

## <a name="scenario-2-automatically-complete-the-transfer-activity-when-kanban-picking-work-is-processed"></a>Scenario 2: Fullfør automatisk overføringshandlingen når kanban-plukkarbeidet er behandlet

I dette scenariet, er overføringsaktiviteten for uttaks-kanbanen konfigurert til å overføre mellom to steder i det samme lageret. Overfør aktiviteten for uttaks-kanbanen slik at den blir fylt ut automatisk. 

[![Overføringsaktiviteten fullføres automatisk når kanban-plukkarbeidet er behandlet](./media/transfer-activities-when-processing-kanban-picking.png)](./media/transfer-activities-when-processing-kanban-picking.png)

1.  Delt lager for råvarer og produksjon
2.  Lagerlokasjoner for råvarer
3.  Kanban "fra"-lokasjon og plasseringsgslokasjon for lagerarbeid
4.  Uttak Kanban
5.  Produksjonsinnleveringssted
6.  Produksjonsprosess

Når en kanban er forbrukt ved produksjonsinnleveringsstedet, rapporteres kanbanen som tom, og en ny kanban legges til i flyten. Når kanbanen opprettet, legges en bølgelinje til i en kanban-bølge. Når kanban-bølgen er beahandlet, opprettes det lagerarbeid for kanban-plukking. Lagermedarbeideren behandler arbeidet for kanban-plukking og blir ledet av arbeidet til å plukke materialer for kanbanen i en lagerlokasjon. Når denne lagermedarbeideren bekrefter plukkingen, blur kanbanen automatiak fullført, og lagerarbeideren blir ledet til å plassere materialet på produksjonsinnleveringsstedet.

