---
title: Aktivere forsinket avgiftsberegning i journaler
description: Denne artikkelen beskriver hvordan du aktiverer funksjonen Forsinket avgiftsberegning for å forbedre ytelsen for avgiftsberegning når det er svært mange journallinjer.
author: EricWang
ms.date: 09/18/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2019-09-18
ms.dyn365.ops.version: 10.0.7
ms.openlocfilehash: 02a038318d4c0fb44b6fcc4bb159ea87c2e9368a
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8887926"
---
# <a name="enable-delayed-tax-calculation-on-journals"></a>Aktivere forsinket avgiftsberegning i journaler
[!include [banner](../includes/banner.md)]


Denne artikkelen beskriver hvordan du kan forsinke beregning av merverdiavgift på journaler. Denne funksjonen bidrar til å forbedre ytelsen til avgiftsberegninger når det er mange journallinjer.

Som standard beregnes mva-beløp på journallinjer når avgiftsrelaterte felt blir oppdaterte. Disse feltene inkluderer feltene for mva-grupper for salg og mva-grupper for varer. Eventuelle oppdateringer til en journallinje fører til at avgiftsbeløp omberegnes for alle journallinjer. Selv om denne virkemåten hjelper brukeren å se avgiftsbeløp beregnet i sanntid, kan det også påvirke ytelsen hvis antall journallinjer er svært stort.

Funksjonen for forsinket mva-beregning gjør at du kan forsinke mva-beregningen på journaler og dermed bidra til å løse ytelsesproblemer. Når denne funksjonen er aktivert, beregnes bare avgiftsbeløp når brukeren velger **Merverdiavgift** eller posterer journalen.

Du kan forsinke beregningen av merverdiavgift på tre nivåer:

- Juridisk enhet
- Journalnavn
- Journalhode

Systemet gir prioritet til innstillingen for journalhodet. Som standard hentes denne innstillingen fra journalnavnet. Som standard hentes innstillingen for journalnavnet fra innstillingen på siden **Parametere for økonomimodul** når journalnavnet opprettes. De følgende delene forklarer hvordan du aktiverer forsinket avgiftsberegning for juridiske enheter, journalnavn og journalhoder.

## <a name="turn-on-delayed-tax-calculation-at-the-legal-entity-level"></a>Aktivere forsinket mva-beregning på nivået for juridisk enhet

1. Gå til **Økonomimodul \> Finansoppsett \> Parametere for økonomimodul**.
2. I kategorien **Merverdiavgift** i hurtigfanen **Generelt** angir du alternativet **Forsinket avgiftsberegning** til **Ja**.

![Parametere for økonomimodul-bildet.](media/delayed-tax-calculation-gl.png)

## <a name="turn-on-delayed-tax-calculation-at-the-journal-name-level"></a>Aktivere forsinket mva-beregning på journalnavnnivå

1. Gå til **Økonomimodul \> Journaloppsett \> Journalnavn**.
2. I hurtigfanen **Generelt** i delen **Merverdiavgift** angir du alternativet **Forsinket avgiftsberegning** til **Ja**.

![Journalnavnbilde.](media/delayed-tax-calculation-journal-name.png)

## <a name="turn-on-delayed-tax-calculation-at-the-journal-header-level"></a>Aktivere forsinket mva-beregning på journalhodenivå

1. Gå til **Økonomimodul \> Journaloppføringer \> Økonomijournaler**.
2. Velg **Ny**.
3. Velg et journalnavn.
4. I kategorien **Oppsett** setter du alternativet for **Forsinket avgiftsberegning** til **Ja**.

![Bilde av økonomijournalsiden.](media/delayed-tax-calculation-journal-header.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
