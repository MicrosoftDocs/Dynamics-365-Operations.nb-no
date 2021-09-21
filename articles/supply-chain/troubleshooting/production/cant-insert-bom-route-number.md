---
title: Kan ikke sette inn aktiv versjon av stykkliste- og rutenumre
description: Hvis standardområdet og -lageret allerede er definert for et valgt produkt, blir du ikke bedt om å sette inn den aktive versjonen av stykkliste- og rutenumre.
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 241618d70f01c85df946a48493f5d84e0964218e
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477153"
---
# <a name="cant-insert-bill-of-material-and-route-when-creating-a-new-production-order"></a>Kan ikke sette inn stykkliste og rute ved oppretting av en ny produksjonsordre

## <a name="symptoms"></a>Symptomer

Når du oppretter en ny produksjonsordre etter at du har angitt varenummeret, settes feltene **Område** og **Lager** automatisk til standardområdet og -lageret som er definert på siden **Standard ordreinnstillinger** for ferdigvarer. I tillegg angis det aktive stykklistenummeret og rutenummeret automatisk, slik at du ikke får følgende melding som spør deg om disse verdiene:

> Vil du sette inn aktiv versjon for stykkliste og rute?

## <a name="resolution"></a>Løsning

Du blir ikke bedt om å sette inn stykkliste- og rutenumre hvis du velger et produkt som et område eller et lager allerede er definert for, på siden **Standard ordreinnstillinger**. Du vil bare bli spurt hvis disse verdiene ikke er definert for det valgte produktet.
