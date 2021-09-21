---
title: Lagereier er ikke tillatt ved behandling av bevegelser
description: Du kan få feilmeldingen "Lagereieren %1 er ikke tillatt." For øyeblikket støtter Warehouse Management-prosesser bare lager som eies av den juridiske enheten.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 4ee29cfc7bad990cd1ee5deaa98fca217af772ed
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477176"
---
# <a name="inventory-owner-not-allowed-when-processing-movements-in-the-warehouse-app"></a>Lagereier er ikke tillatt ved behandling av bevegelser i lagerappen

## <a name="symptoms"></a>Symptomer

Når du behandler bevegelser i Warehouse Management-mobilappen, kan du få denne feilmeldingen:

> Lagereieren %1 er ikke tillatt i denne prosessen.

## <a name="cause"></a>Årsak

Dette skjer fordi **Eier**-sporingsdimensjonen mangler når mobilappen Warehouse Management-mobilappen brukes til å lage bevegelser. En vanlig lageroverføringsjournal fra Supply Chain Management-klienten ser ut til å fungere som tiltenkt og kan bare posteres hvis **Eier**-dimensjonen er fylt ut.

## <a name="resolution"></a>Løsning

Microsoft har evaluert dette problemet og har funnet ut at det er en funksjonsbegrensning. For øyeblikket støtter lagerstyringsprosesser bare lager som eies av den juridiske enheten.
