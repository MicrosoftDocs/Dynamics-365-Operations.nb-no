---
title: Antall ikke gyldig for plukking av arbeid med flere LPer
description: Antallet er ikke gyldig for ea-enheten når det er et plukkarbeid som har flere nummerskilter på ett sted. Kontroller at følgende felt er riktige.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 5b245f71e80339fee3e42cfffa0396078a56926e
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477159"
---
# <a name="quantity-not-valid-when-theres-picking-work-with-multiple-lps-in-one-location"></a>Antall ugyldig når det er plukkingsarbeid med flere nummerskilt på én lokasjon

## <a name="symptoms"></a>Symptomer

Når det er et plukkarbeid som har flere nummerskilter på ett sted, er ikke antallet gyldig for *ea*-enheten, og du får denne feilmeldingen:

> Antallet er ikke gyldig for enheten 1%.

## <a name="resolution"></a>Løsning

Kontroller at feltene **Sekvensgruppe-ID for enhet** og **Enhetskonverteringer** i frigitt produkt eller produktvariant er riktig angitt.

Legg merke til at feilmeldingen er forbedret i versjon 10.0.15 10.0.15 for å vise det forventede antallet (se [KB 4581627](https://fix.lcs.dynamics.com/Issue/Details/?bugId=486531)). Den nye feilmeldingen er:

> Antallet er ikke gyldig. Forventet %1 %2.
