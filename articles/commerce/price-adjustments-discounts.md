---
title: Prisjusteringer og rabatter
description: Denne artikkelen inneholder informasjon om prisjusteringer og rabatter i Dynamics 365 Commerce.
author: josaw1
ms.date: 06/11/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: global
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.custom: 15891
ms.assetid: bab5adf3-ddf0-4c22-a2eb-b4d25b88de99
ms.search.industry: Retail
ms.search.form: RetailParameters, RetailPeriodicDiscount
ms.openlocfilehash: ff90df814d6930b5cf92772e430625943e0ae983
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/12/2022
ms.locfileid: "9279096"
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

> [!NOTE]
> Samlerabatten og terskelrabatten har henholdsvis egenskapene «Regn med ikke-rabatterte produkter» og «Tell ikke-rabatterte produkter mot terskel». Hvis disse egenskapene er aktivert, kan en vare som ikke kvalifiserer for rabatt, likevel bidra til å kvalifisere en transaksjon for rabatten, men den ikke-kvalifiserte varen blir ikke rabattert. 
> 
> Hvis du for eksempel oppretter en samlerabatt med to linjer, A og B, der en kunde skal få 10 % rabatt på begge varene, men der det er merket av for Hindre alle rabatter for vare A, gjør dette vanligvis at vare A ikke blir tatt med i rabatten. Hvis egenskapen «Regn med ikke-rabatterte produkter» er aktivert, kan imidlertid vare A brukes til å kvalifisere for samlerabatten, men rabatten på 10 % brukes bare på vare B. En tilsvarende logikk gjelder for terskelrabatten. 
>
> Egenskapen «Tell ikke-rabatterte produkter mot terskel» har imidlertid en tilleggsfunksjon sammenlignet med egenskapen «Regn med ikke-rabatterte produkter» for samlerabatten. Hvis terskelrabatten er aktivert og det finnes en vare som har en eksisterende rabatt som gjør at andre rabatter ikke kan gjelde for varen, kvalifiserer prisen som betales for denne varen, mot terskelen, men tilleggsrabatten blir ikke gjeldende for denne varen.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
