---
title: Returnere varer på tvers av flere kunder, ordrer og fakturaer
description: Dette emnet beskriver funksjonen for aktivering av returer på tvers av flere ordrer fra kunder og fakturaer i Dynamics 365 Commerce.
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
ms.openlocfilehash: c36fe4c8376ad0364516c0268965c798e20436c6
ms.sourcegitcommit: 3a9599e9b9458434c0e44d295eabd2304c5650be
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/02/2021
ms.locfileid: "6334431"
---
# <a name="return-items-across-multiple-customer-orders-and-invoices"></a>Returnere varer på tvers av flere kunder, ordrer og fakturaer

[!include [banner](includes/banner.md)]


Returer kan utføres på tvers av flere ordrer og fakturaer. 

## <a name="configure-commerce-to-support-returns-across-multiple-customer-order-and-invoices"></a>Konfigurere Commerce til å støtte returer på tvers av flere kundeordrer og fakturaer

1. Gå til **Handelsparametere \> Kundeordrer**.
1. Aktiver parameteren **Aktiver returer for flere ordrer**. 

## <a name="process-returns"></a>Behandle returer

Når parameteren er aktivert og endringene synkronisert til butikkene, kan kassereren i butikken velge flere salgsordrer for en kunde for kundens retur.

Når ordrene er valgt, vises det en liste over alle returnerbare produkter på tvers av alle fakturaene for ordrene. Kassereren kan deretter velge produktene som skal returneres. Én returordre opprettes for alle de valgte produktene.
