---
title: Kan ikke flytte nummerskiltet hvis Tom avgang og Tom kvittering er tillatt
description: Du kan ikke flytte et nummerskilt hvis serienummeret har Tom avgang og Tom kvittering tillatt. Dette løses ved å gjøre serienummerfeltet valgfritt.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 0047f79aa417c8fc910447505f07963d014f54e7
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477192"
---
# <a name="cant-move-license-plate-if-serial-number-has-blank-issue-and-blank-receipt-allowed"></a>Kan ikke flytte et nummerskilt hvis serienummeret har Tom avgang og Tom kvittering tillatt

## <a name="symptoms"></a>Symptomer

Du kan ikke flytte et nummerskilt ved hjelp av et **Flytting**-menyelement hvis serienummeret har innstillinger for *Tom avgang tillatt* og *Tomt mottak tillatt* på sporingsdimensjonsgruppen, og hvis det er flere nummerskilter på samme sted, kan noe av disse ha serienumre og noen av dem ikke ha det.

## <a name="resolution"></a>Løsning

Dette problemet vil løses ved hjelp av endringer som er distribuert i [KB 4571546](https://fix.lcs.dynamics.com/Issue/Details?kb=4571546&bugId=467880&dbType=3&qc=5b46d7faa9cc326cebfe9854cb30be8ea30b21ef33d3572c325fbb21202de687). Disse endringene gjør **Serienummer**-feltet valgfritt når det er tillatt med tomt mottak og tom avgang.
