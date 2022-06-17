---
title: Endre eller tildel en finanskalender på nytt
description: Denne artikkelen beskriver hvordan du endrer kalenderen som for øyeblikket er tildelt finans, og hvordan du tildeler en ny kalender til finans.
author: kweekley
ms.date: 05/07/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2021-5-07
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 751954e0dc5f682b99ab7fe349cd505dc9da7858
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8848613"
---
# <a name="change-or-reassign-a-ledger-calendar"></a>Endre eller tildel en finanskalender på nytt

[!include [banner](../includes/banner.md)]

Denne artikkelen beskriver hvordan du endrer kalenderen som for øyeblikket er tildelt finans, og hvordan du tildeler en ny kalender til finans.

## <a name="issue"></a>Problem

Noen ganger må firmaer enten endre den eksisterende kalenderen som er tilordnet finans, eller tilordne en ny kalender.

## <a name="resolution"></a>Løsning

Det finnes to scenarioer for endring eller ny tilordning av en finanskalender. Det første scenarioet omfatter endring av en eksisterende kalender som allerede er tilordnet finans. Det andre scenarioet omfatter oppretting av en ny kalender og tilordning av den til finans. Begge endringene kan utføres når som helst, også etter at transaksjoner er postert til finans.

### <a name="change-an-existing-fiscal-calendar"></a>Endre en eksisterende regnskapskalender

Hvis du vil endre en eksisterende kalender som er tilordnet finans, kan du gå til **Økonomimodul \> Finansoppsett \> Finans** og velge koblingen for regnskapskalenderen for å åpne siden **Finanskalendere**.

Det er begrensninger på hvilke endringer som kan gjøres i en kalender. Du kan for eksempel endre start- og sluttdatoene for *periodene* i et år, men du kan ikke endre start- og sluttdatoene for et *år* i kalenderen.

Hvis du vil endre periodene i et år, velger du riktig kalender og år. Først bruker du knappen **Slett periode** til å slette noen av eller alle de eksisterende driftsperiodene. Alle driftsperioder, bortsett fra den første, kan slettes. Deretter kan du bruke knappen **Del opp periode** til å dele opp gjenstående periode eller perioder i nye perioder ved å angi en passende startdato for den neste perioden.

Når du har endret periodene i en kalender, må du kjøre prosessen **Beregn finansperioder på nytt** i hver juridiske enhet (firma) som kalenderen er tilordnet. Selv om ingen advarsel påminner deg om å fullføre dette trinnet, er omberegningsprosessen nødvendig for å oppdatere perioden som er tilordnet hver posterte transaksjon i økonomimodulen. Hvis du vil kjøre omberegningsprosessen, velger du **Beregn finansperioder på nytt** på siden **Finansoppsett** i hvert firma.

Hvis omberegningsprosessen ikke kjøres, kan det hende at transaksjonssaldoer på en råbalanse eller i regnskapsoppgjør er feilaktig tatt med i perioder. I dette tilfellet kan du når som helst rette opp saldoene ved å kjøre omberegningsprosessen.

### <a name="assign-a-new-fiscal-calendar"></a>Tilordne en ny regnskapskalender

Hvis du vil tilordne en ny regnskapskalender, kan du gå til **Økonomimodul \> Finansoppsett \> Finans** og velge **Rediger** for å sette siden **Finans** i redigeringsmodus. Velg deretter en ny regnskapskalender i feltet **Regnskapskalender**.

Når du har endret regnskapskalenderen for finans, må du kjøre **Beregn finansperioder på nytt**. Når du tilordner en ny regnskapskalender til finans, får du en melding som minner deg på å fullføre dette trinnet. Selv om meldingen kan indikere at omberegningsprosessen er valgfri, så er den ikke det. Det er nødvendig å oppdatere perioden som er tilordnet hver posterte transaksjon i økonomimodulen. Hvis du vil kjøre omberegningsprosessen, velger du **Beregn finansperioder på nytt** på siden **Finansoppsett**.

Hvis omberegningsprosessen ikke kjøres, kan det hende at transaksjonssaldoer på en råbalanse eller i regnskapsoppgjør er feilaktig tatt med i perioder. I dette tilfellet kan du når som helst rette opp saldoene ved å kjøre omberegningsprosessen.
