---
title: Feil når status endres fra Ferdigmeldt til Slutt
description: Du kan få en feilmelding når status for en produksjonsordre endres fra Ferdigmeldt til Slutt. Denne siden beskriver hvordan du kan løse problemet.
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 744637f5cccffe44b85f77c1a9df2034012fac40
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477206"
---
# <a name="error-when-changing-status-of-production-order-from-reported-as-finished-to-end"></a>Feil når status for produksjonsordre endres fra Ferdigmeldt til Slutt

## <a name="symptoms"></a>Symptomer

Når statusen for en produksjonsordre endres fra Ferdigmeldt til Slutt, får du en av følgende feilmeldinger:

> Oppdateringskonflikt. Standardkostnaden samsvarer ikke med den økonomiske lagerverdien etter oppdateringen.

> Det har oppstått en kritisk feil i funksjonen InventCostMovement.checkVariance.

## <a name="cause"></a>Årsak

Dette problemet oppstår fordi de underliggende dataene ble endret av en annen prosess. Prosessen vil prøve å oppdatere dataene opptil fem ganger. Hvis konflikten fremdeles finnes etter fem forsøk, får du en av meldingene over.

## <a name="resolution"></a>Løsning

Denne virkemåten er standard. Du kan redusere problemet ved å gjenoppta den satsvise jobben. Den skal slutte å kjøre.

Hvis den satsvise jobben ikke fungerer etter at du har gjenopptatt den, må du kontrollere at avrundingspresisjonen for finansstandardvalutaen er kompatibel med avrundingen som brukes på verdier i InventSum-tabellen. Hvis avrundingspresisjonen er endret til en ikke-kompatibel verdi, må du sannsynligvis endre den tilbake til en kompatibel verdi. Se etter **ModifiedDateTime**. I dette tilfellet vil verdien vanligvis vise at avrundingspresisjonen nylig ble endret.
