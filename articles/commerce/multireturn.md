---
title: Returner varer på tvers av flere kunder, ordrer og fakturaer
description: Denne artikkelen beskriver funksjonen for aktivering av returer på tvers av flere ordrer fra kunder og fakturaer i Dynamics 365 Commerce.
author: josaw1
ms.date: 08/27/2020
ms.topic: index-page
ms.prod: ''
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
ms.openlocfilehash: 65ef700db5a81c49a962fd388af54e7811c088d2
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8890328"
---
# <a name="return-items-across-multiple-customer-orders-and-invoices"></a>Returner varer på tvers av flere kunder, ordrer og fakturaer

[!include [banner](includes/banner.md)]


Returer kan utføres på tvers av flere ordrer og fakturaer. 

## <a name="configure-commerce-to-support-returns-across-multiple-customer-order-and-invoices"></a>Konfigurere Commerce til å støtte returer på tvers av flere kundeordrer og fakturaer

1. Gå til **Handelsparametere \> Kundeordrer**.
1. Aktiver parameteren **Aktiver returer for flere ordrer**. 

## <a name="process-returns"></a>Behandle returer

Når parameteren er aktivert og endringene synkronisert til butikkene, kan kassereren i butikken velge flere salgsordrer for en kunde for kundens retur.

Når ordrene er valgt, vises det en liste over alle returnerbare produkter på tvers av alle fakturaene for ordrene. Kassereren kan deretter velge produktene som skal returneres. Én returordre opprettes for alle de valgte produktene.
