---
title: Kan ikke frigi en delvis levert last på nytt til lager
description: I tidligere versjoner kunne du ikke frigi en delvis levert last på nytt ved bruk av bestemte funksjoner med fullførte reserveringer. Problemet er løst.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 0380e1963a38f2be55b31e06b3845f935661eed2
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477217"
---
# <a name="cant-re-release-a-partially-shipped-load-to-the-warehouse"></a>Kan ikke frigi en delvis levert last på nytt til lageret

## <a name="symptoms"></a>Symptomer

Du kan ikke frigi en delvis levert last til lageret. Når du gjør frigivelsen til lageret, vises meldingen Operasjon fullført, men ingenting skjer ikke, og det opprettes ikke noe arbeid for restantallet. Dette problemet oppstår når du bruker funksjonalitet for transportlast, og det er en ufullstendig reservasjon.

## <a name="resolution"></a>Løsning

[KB-problem 470069](https://fix.lcs.dynamics.com/Issue/Details?kb=4574490&bugId=470069&dbType=3&qc=84ce1e09d7032d8b8ef86f5a0c68b86badf3dfaf29686c5ebbe97c53c0957b5f) (Delvis leverte laster kan bølges og behandles på nytt) er løst i [frigivelses 10.0.15](/dynamics365/supply-chain/get-started/whats-new-scm-10-0-15).
