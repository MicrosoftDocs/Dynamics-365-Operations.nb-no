---
title: Opprette kundebetalingsmåte
description: Dette emnet forklarer hvordan du oppretter en betalingsmåte for kundebetalinger.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/31/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPaymMode, BankAccountTableLookUp
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4b9960c3fdf0d65be19e28dbb41913a310ae7530
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/18/2020
ms.locfileid: "3140220"
---
# <a name="establish-customer-method-of-payment"></a>Opprette kundebetalingsmåte

[!include [banner](../../includes/banner.md)]

Dette emnet forklarer hvordan du oppretter en betalingsmåte for kundebetalinger. Denne oppgaven bruker demonstrasjonsfirmaet USMF.

1. I navigasjonsruten går du til **Moduler > Kunder > Betalingsoppsett > Betalingsmåter**.
2. Velg **Ny**.
3. Angi en ID for betalingsmåten i feltet **Betalingsmåte**. Metoden for betalings-ID vises på fakturaer og betalinger, så gjør den beskrivende nok til å forstå hvilken type betaling som blir registrert, og for hvilken bankkonto.  
4. Angi en beskrivelse i **Beskrivelse**-feltet.
5. Velg hvilken betalingsstatus som er nødvendig for at betalinger som skal posteres. Når du oppretter en kundebetaling, kan den bare posteres når betalingsstatusen samsvarer med betalingsstatusen du definerer her.  
6. Velg hvordan betalinger for kunder skal opprettes for fakturaer. Dette alternativet brukes bare når du kjører et betalingsforslag. Et betalingsforslag kan brukes for kundebetalinger ved bruk av avtalegiro, og når du trekker penger fra kundenes bankkontoer.  
7. Velg betalingstypen. Betalingstypen vil hjelpe deg med å finne ut om noen validering utføres eller ikke i betalingen.  
8. Velg hvilken kontotype betalinger skal posteres til. Banken vil vanligvis være valgt for dette alternativet.  
9. Velg bankkontoen som denne betalingen blir registrert i.
10. Angi banktransaksjonstypen for å identifisere typen betaling som brukes av banken. Banktransaksjonstypen brukes under bankavstemmingsprosessen, og kan forenkle avstemming.  
11. Velg om denne betalingen skal posteres midlertidig til en mellomkonto. Hvis du vil prøve flyttidspunktet for en betaling som skal klares av banken, kan du bruke funksjonen mellompostering. Betalingen posteres midlertidig til en finanskonto før den klareres av banken, og betalingen flyttes da til bankkontoen du har definert her.  
12. Angi hovedkontoen som brukes for mellompostering. Dette er hovedkontoen som betalingen midlertidig posteres til hvis du bruker mellompostering.  
13. Bruk kategorien **Filformat** til å definere innstillinger for elektroniske betalinger.
14. Bruk kategorien **Betalingskontroll** til å definere felt som er obligatoriske. Hvis du for eksempel trenger at alle betalinger med denne betalingsmåten skal innbetales, kan du velge dette alternativet i denne kategorien.  
15. Bruk kategorien **Betalingsattributter** til å definere hvilke betalingsattributter du vil bruke for denne betalingsmåten.
16. Velg **Lagre**.

