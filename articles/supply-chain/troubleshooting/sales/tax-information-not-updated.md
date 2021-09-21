---
title: Avgiftsinformasjon ikke oppdatert hvis lokasjonen i et salgsordre endres
description: Hvis område-, lager- eller leveringsadressen endres på et salgsordrehode, oppdateres ikke skatteinformasjonen for saken automatisk på linjene. Dette må du gjøre manuelt.
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 77a73a787ff8a174c575f3b4f75694ded45d5712
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477204"
---
# <a name="tax-information-isnt-updated-if-location-on-a-sales-order-header-is-changed"></a>Avgiftsinformasjon ikke oppdatert hvis lokasjonen i et salgsordrehode endres

## <a name="symptoms"></a>Symptomer

Hvis område-, lager- eller leveringsadressen endres på et salgsordrehode, oppdateres ikke skatteinformasjonen for saken automatisk på linjene.

## <a name="resolution"></a>Løsning

Denne virkemåten er standard. Problemet oppstår fordi leveringsadressen, området og lageret ikke automatisk blir endret på linjenivået. Du må oppdatere dem manuelt.
