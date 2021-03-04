---
title: Returnere varer på tvers av flere kunder, ordrer og fakturaer
description: Dette emnet beskriver funksjonen for aktivering av returer på tvers av flere ordrer fra kunder og fakturaer i Dynamics 365 Commerce.
author: josaw1
manager: AnnBe
ms.date: 08/27/2020
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-01-15
ms.dyn365.ops.version: 10
ms.openlocfilehash: ee4c863e617b9351e55e1fc652ea8905f17c8346
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "4976669"
---
# <a name="return-items-across-multiple-customer-orders-and-invoices"></a>Returnere varer på tvers av flere kunder, ordrer og fakturaer

[!include [banner](includes/banner.md)]


Denne artikkelen beskriver to funksjoner som optimaliserer kundeordrereturer via flere fakturaer. 

## <a name="enable-refunds-over-multiple-captures"></a>Aktiver refunderinger på tvers av flere registreringer

Denne funksjonen aktiverer flere sammenkoblede refusjoner mot samme kundeordre. 

1. Gå til arbeidsområdet **Funksjonsbehandling** og søk etter **Aktiver refusjoner over flere registreringer**.
2. Velg **Aktiver refusjoner over flere ordrer**, og klikk deretter **Aktiver**. 

## <a name="enable-proper-tax-calculation-for-returns-with-partial-quantity"></a>Aktiver riktig avgiftsberegning for returer med delvis antall

Denne funksjonen sikrer at når en ordre returneres ved hjelp av flere fakturaer, vil avgiften være lik avgiftsbeløpet som opprinnelig ble belastet. 

1. Gå til arbeidsområdet **Funksjonsbehandling** og søk etter **Aktiver riktig avgiftsberegning for returer med delvis antall**.
2. Velg **Aktiver riktig avgiftsberegning for returer med delvis antall**, og klikk deretter **Aktiver**. 


## <a name="process-returns"></a>Behandle returer

Når disse funksjonene er aktivert og endringene synkronisert til butikkene, kan kassereren i butikken velge flere salgsordrer for en kunde for kundens retur.

Når ordrene er valgt, vises det en liste over alle returnerbare produkter på tvers av alle fakturaene for ordrene. Kassereren kan deretter velge produktene som skal returneres. Én returordre opprettes for alle de valgte produktene.

Hvis ordren er fullstendig returnert, vil beløpet som returneres til kunden, være lik avgiftsbeløpet som opprinnelig ble belastet.



[!INCLUDE[footer-include](../includes/footer-banner.md)]