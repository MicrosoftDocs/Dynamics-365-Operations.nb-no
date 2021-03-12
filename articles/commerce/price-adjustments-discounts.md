---
title: Prisjusteringer og rabatter
description: Denne artikkelen inneholder informasjon om prisjusteringer og rabatter i Dynamics 365 Commerce.
author: scott-tucker
manager: AnnBe
ms.date: 11/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailParameters, RetailPeriodicDiscount
audience: Application User
ms.reviewer: josaw
ms.custom: 15891
ms.assetid: bab5adf3-ddf0-4c22-a2eb-b4d25b88de99
ms.search.region: global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: f29e90e1c61792c70d4d6eaeee7758676bf193b2
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "4972496"
---
# <a name="price-adjustments-and-discounts"></a>Prisjusteringer og rabatter

[!include [banner](includes/banner.md)]

Denne artikkelen inneholder informasjon om prisjusteringer og rabatter i Dynamics 365 Commerce.

I Commerce kan du justere prisene for produkter, og du kan også definere rabatter som gjelder for en linjevare eller en transaksjon på salgsstedet, i en salgsordre via et telefonsenter eller i en elektronisk ordre. Både prisjusteringer og rabatter kan knyttes til prisgrupper. Du kan angi én enkelt startdato og sluttdato eller en regelmessig periode, en rabattkode og noen ytterligere attributter for både prisjusteringer og rabatter. 

Prisjusteringer og rabatter kan brukes på produkter, varianter eller hierarkier. Hvis mer enn én rabatt gjelder for et produkt, kan en kunde få enten en av rabattene eller en kombinert rabatt, avhengig av konfigurasjonen av rabatten. Commerce bruker automatisk rabatten eller kombinasjon av rabatter som gir den beste prisen til kunden. Når du definerer en prisjustering eller rabatt, må du bekrefte at prisgrupper tilordnes til riktige kanaler, kataloger, tilknytninger eller fordelsprogrammer som du vil at rabatten skal gjelde for. Hvis du i tillegg vil generere rabatt-ID-en automatisk, kan du definere nummerserier på **Handelsparametere**-siden før du definerer en ny rabatt eller prisjustering.

> [!NOTE]
> Du kan slette en prisjustering eller rabatt. Statistisk informasjon går imidlertid tapt.

## <a name="types-of-discounts"></a>Rabattyper

Det finnes mange typer rabatter:

- **Enkel rabatt** – en enkelt prosent eller et enkelt beløp.
- **Kvantumsrabatt** – en rabatt som brukes når to eller flere varer som kjøpes.
- **Samlerabatt** – en rabatt som brukes ved kjøp av en bestemt kombinasjon av produkter.
- **Terskelrabatt** – en rabatt som brukes når totalen for transaksjonen er mer enn et bestemt beløp.
- **Betalingsmiddelbasert rabatt** – En rabatt som brukes når totalen for transaksjonen er mer enn et bestemt beløp, og en bestemt betalingstype (for eksempel kontant, kredit- eller debetkort) brukes til betaling.
- **Leveringsrabatt** – En rabatt som brukes når totalen for transaksjonen er mer enn et bestemt beløp og en bestemt leveringsmåte (for eksempel forsendelse på to dager eller over natten) brukes på ordren.

Både prisjusteringer og rabatter kan knyttes til prisgrupper. Prisgrupper kan deretter knyttes til kanaler, kataloger, tilknytninger og fordelsprogrammer.
