---
title: Vise gjelds-, aktiva- og utgiftstransaksjoner
description: Denne artikkelen forklarer hvordan du viser transaksjoner for en leid eiendel. Disse transaksjonene omfatter leieforpliktelsestransaksjoner og fullbyrdelsesutgiftstransaksjoner som er postert.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SysQueryForm
audience: Application User
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 552b5a6044950c4dd7547a5239c1b3f7d355dbce
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8906420"
---
# <a name="view-liability-asset-and-expense-transactions"></a>Vise gjelds-, aktiva- og utgiftstransaksjoner

[!include [banner](../includes/banner.md)]

Denne artikkelen forklarer hvordan du viser transaksjoner for en leid eiendel. Disse transaksjonene omfatter leieforpliktelsestransaksjoner og fullbyrdelsesutgiftstransaksjoner som er postert. De bærende verdiene for gjeld og bruksrettseiendel brukes i flere rapporter. De brukes også til å beregne justeringsverdier.

## <a name="liability-transactions"></a>Gjeldstransaksjoner

Hvis du vil vise leieforpliktelsestransaksjoner, velger du en leieavtale på siden **Leiesammendrag**, og deretter velger du **Tablåer** for å åpne tablåene som er knyttet til leieposten. Etter at en opprinnelig gjenkjenning, en faktura eller en rentejournal er postert, velger du **Gjeldstransaksjoner**.

Siden **Gjeldstransaksjoner** viser transaksjonene som enten øker eller reduserer leieforpliktelsen. Negative beløp på denne siden representerer kredittransaksjoner i standardprogrammet. Eventuelle renteavsetninger vises som negative verdier, og øker de totale leieforpliktelsene. Eventuelle leiejusteringer vises som positive eller negative verdier, avhengig av leietablåets natur og virkning. Gjeldende nettototalsaldo for leieforpliktelsen for den valgte leien vises nederst til venstre på siden.

## <a name="asset-transactions"></a>Aktivatransaksjoner

Hvis du vil vise leieaktivatransaksjoner, velger du en leieavtale på siden **Leiesammendrag**, og deretter velger du **Tablåer** for å åpne leietablåene som er knyttet til leieposten. Velg deretter **Leietransaksjoner**.

Siden **Aktivatransaksjon** viser transaksjonene som enten øker eller reduserer leieaktivaet og akkumulerte avskrivningskontoer. Debet vises som positive verdier, og kredit vises som negative verdier, som på **Gjeldstransaksjoner**-siden. Den posterte opprinnelige gjenkjenningen og den neste akkumulerte avskrivningen vises nederst til venstre på siden som anleggsmiddelsaldoen. 

## <a name="expenses-transactions"></a>Utgiftstransaksjoner

Hvis du vil vise leieutgiftstransaksjoner, velger du en leieavtale på siden **Leiesammendrag**, og deretter velger du **Tablåer** for å åpne leietablåene som er knyttet til leieposten. Deretter velger du **Utgiftstransaksjoner**.

Siden **Utgiftstransaksjoner** viser alle utgifter som er postert mot leieavtalen, for eksempel renteutgifter, avskrivningsutgifter og eventuelle fullbyrdelseskostnader.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
