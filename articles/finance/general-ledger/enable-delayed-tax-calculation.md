---
title: Aktivere forsinket avgiftsberegning på journal
description: Dette emnet beskriver hvordan du bruker funksjonen **Aktivere forsinket avgiftsberegning på journal** til å forbedre ytelsen for avgiftsberegning når det er svært mange journallinjer.
author: ericwang
manager: Ann Beebe
ms.date: 09/18/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2019-09-18
ms.dyn365.ops.version: 10.0.7
ms.openlocfilehash: 5a8ae30a007d3e2b8b7a9bc9eb7786f6e58246d0
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/27/2019
ms.locfileid: "2179180"
---
# <a name="enable-delayed-tax-calculation-on-journal"></a>Aktivere forsinket avgiftsberegning på journal
[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Dette emnet beskriver hvordan du bruker funksjonen **Aktivere forsinket avgiftsberegning på journal** til å forbedre ytelsen for avgiftsberegning når det er svært mange journallinjer.

Gjeldende virkemåte for avgiftsberegning for journalen utløses i sanntid når brukeren oppdaterer avgiftsrelaterte felt, for eksempel mva-gruppe/mva-gruppe for vare. Alle oppdateringer på journallinjenivå vil beregne avgiftsbeløp på nytt på alle journallinjer. Den hjelper brukeren med å se sanntidsberegnet avgiftsbeløp, men det kan også føre til ytelsesproblemer hvis det er svært mange journallinjer.

Denne funksjonen gir mulighet til å forsinke avgiftsberegningen for å løse ytelsesproblemer. Hvis denne funksjonen er aktivert, beregnes bare avgiftsbeløp når brukeren klikker på kommandoen Merverdiavgift eller posterer journalen.

Brukeren kan aktivere/deaktivere parameteren på tre nivåer:
- Etter juridisk enhet
- Etter journalnavn
- Etter journalhode

Systemet vil bruke parameterverdien i journalhodet som endelig. Parameterverdien i journalhodet hentes som standard fra journalnavn. Parameterverdi i journalnavn blir som standard opprettet fra økonomimodulparameteren når journalnavnet opprettes.

Feltene Faktisk mva-beløp og Beregnet mva-beløp i journalen, skjules hvis denne parameteren er aktivert. Formålet kan ikke forvirre brukeren fordi verdien av disse to feltene alltid viser 0 før brukeren utløser avgiftsberegningen.

## <a name="enable-delayed-tax-calculation-by-legal-entity"></a>Aktivere forsinket avgiftsberegning etter juridisk enhet

1. Gå til **Økonomimodul > Finansoppsett > Parametere for økonomimodul**.
2. Klikk på **Merverdiavgift**.
3. I hurtigfanen **Generelt** finner du parameteren **Forsinket avgiftsberegning** og aktiverer/deaktiverer den

![](media/delayed-tax-calculation-gl.png)



## <a name="enable-delayed-tax-calculation-by-journal-name"></a>Aktivere forsinket avgiftsberegning etter journalnavn

1. Gå til **Økonomimodul > Journaloppsett > Journalnavn**.
2. I hurtigfanen **Generelt** finner du parameteren **Forsinket avgiftsberegning** og aktiverer/deaktiverer den

![](media/delayed-tax-calculation-journal-name.png)

## <a name="enable-delayed-tax-calculation-by-journal"></a>Aktivere forsinket avgiftsberegning etter journal

1. Gå til **Økonomimodul > Journaloppføringer > Økonomijournaler**
2. Klikk på **Ny**
3. Velg et journalnavn
4. Klikk på **Oppsett**
5. Finn parameteren **Forsinket avgiftsberegning** og aktiverer/deaktiverer den

![](media/delayed-tax-calculation-journal-header.png)
