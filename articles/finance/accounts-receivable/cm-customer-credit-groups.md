---
title: Kundekredittgrupper
description: Dette emnet gir informasjon om kundekredittgrupper.
author: JodiChristiansen
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: roschloma
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: c8a007dcaaa9e10ab36dd3a7d0f80dd49b8e4d63
ms.sourcegitcommit: 408786b164b44bee4e16ae7c3d956034d54c3f80
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/05/2021
ms.locfileid: "7753856"
---
# <a name="customer-credit-groups"></a>Kundekredittgrupper

[!include [banner](../includes/banner.md)]

Du kan definere grupper med kunder som har en delt kredittgrense. Den individuelle kredittgrensen som er definert på kundefakturakontoen, tas også hensyn til.

Medlemmer av en kundekredittgruppe kan velges fra ulike juridiske enheter. Når du legger til en kunde i listen over kunder i kundekredittgruppen, endres utløpsdatoen for kredittgrensen for hver kunde til utløpsdatoen som er tilordnet gruppen.

Du kan definere kundekredittgrupper på siden **Kundekredittgrupper** (**Kredittbehandling \> Kundekredittgrupper \> Kundekredittgrupper**).

1. I feltene **Gruppenummer** og **Beskrivelse** angir du en ID for og en beskrivelse av gruppen.
2. I feltene **Kredittgrense** og **Valuta** angir du kredittgrensen og valutaen som skal brukes når systemet kontrollerer kredittgrensen for medlem av gruppen.
3. I feltet **Kredittgrense til dato** angir du datoen da kredittgrensen utløper. Kundekredittgrupper må ha en utløpsdato.

Når du er ferdig med å definere en kundekredittgruppe, kan du legge til kunder i den ved å angi deres juridiske enhet og kundekonto-ID. Når du legger til en ny kunde i en kundekredittgruppe, søker systemet etter den samme kundekontoen på tvers av alle juridiske enheter og ber deg om å legge den til i kundekredittgruppen.

Bruk menyen **Aldersfordelte saldoer** til å vise detaljer for aldersfordelingssaldoen for alle fakturakunder i en kundekredittgruppe. Siden **Aldersfordelingssaldo** viser et sammendrag av de aldersfordelte saldoene for fakturakundekontoene.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
