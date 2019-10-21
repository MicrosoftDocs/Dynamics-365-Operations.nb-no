---
title: Prisjusteringer og rabatter
description: Denne artikkelen inneholder informasjon om prisjusteringer og rabatter i Dynamics 365 Retail.
author: scott-tucker
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailParameters, RetailPeriodicDiscount
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 15891
ms.assetid: bab5adf3-ddf0-4c22-a2eb-b4d25b88de99
ms.search.region: global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 9461496cf5334ff0a25361b9b426cacc0aa1f88c
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/24/2019
ms.locfileid: "2025247"
---
# <a name="price-adjustments-and-discounts"></a>Prisjusteringer og rabatter

[!include [banner](includes/banner.md)]

Denne artikkelen inneholder informasjon om prisjusteringer og rabatter i Dynamics 365 Retail.

I Retail kan du justere prisene for produkter, og du kan også definere rabatter som gjelder for en linjevare eller en transaksjon på salgsstedet, i en salgsordre via et telefonsenter eller i en elektronisk ordre. Både prisjusteringer og rabatter kan knyttes til prisgrupper. Du kan angi én enkelt startdato og sluttdato eller en regelmessig periode, en rabattkode og noen ytterligere attributter for både prisjusteringer og rabatter. Prisjusteringer og rabatter kan brukes på produkter, varianter eller hierarkier. Hvis mer enn én rabatt gjelder for et produkt, kan en kunde få enten en av rabattene eller en kombinert rabatt, avhengig av konfigurasjonen av rabatten. Retail bruker automatisk rabatten eller kombinasjon av rabatter som gir den beste prisen til kunden. Når du definerer en prisjustering eller rabatt, må du bekrefte at prisgrupper tilordnes til riktige kanaler, kataloger, tilknytninger eller fordelsprogrammer som du vil at rabatten skal gjelde for. Hvis du i tillegg vil generere rabatt-ID-en automatisk, kan du definere nummerserier på **Detaljhandelsparametere**-siden før du definerer en ny rabatt eller prisjustering.

> [!NOTE]
> Du kan slette en prisjustering eller rabatt. Statistisk informasjon går imidlertid tapt.

## <a name="types-of-discounts"></a>Rabattyper

Det finnes fire typer detaljhandelsrabatter:

- **Enkel rabatt** – en enkelt prosent eller et enkelt beløp.
- **Kvantumsrabatt** – en rabatt som brukes når to eller flere varer som kjøpes.
- **Samlerabatt** – en rabatt som brukes ved kjøp av en bestemt kombinasjon av produkter.
- **Terskelrabatt** – en rabatt som brukes når totalen for transaksjonen er mer enn et bestemt beløp.

Både prisjusteringer og rabatter kan knyttes til prisgrupper. Prisgrupper kan deretter knyttes til kanaler, kataloger, tilknytninger og fordelsprogrammer.
