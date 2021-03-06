---
title: Global kildeskatt
description: Dette emnet gir informasjon om global funksjonalitet for kildeskatt og hvordan du definerer det. Global kildeskattfunksjonalitet er utvidet for leverandør- og kundetransaksjoner, slik at kildeskatt beregnes på varenivå.
author: roschlom
ms.date: 01/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2020-01-12
ms.dyn365.ops.version: AX 10.0.16
ms.openlocfilehash: 9a73d34fb4fbf007cbb5a996cfa6e9719532869c
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5826672"
---
# <a name="global-withholding-tax"></a>Global kildeskatt

[!include [banner](../includes/banner.md)]

Dette emnet gir informasjon om global funksjonalitet for kildeskatt og forklarer hvordan du definerer det. Den nye funksjonen er tilgjengelig i versjon 10.0.17 og senere.

Global kildeskattfunksjonalitet er utvidet for leverandør- og kundetransaksjoner, slik at kildeskatt beregnes på varenivå. Saldoen på kildeskattkontoen fra kjøpstransaksjoner kan utlignes ved å kjøre betalingsjobben for kildeskatt mot utligningskontoen for kildeskatt.

> [!NOTE]
> Global kildeskatt støtter ikke funksjonen **Vedlikehold tillegg** på bestillings-, leverandørfaktura- og salgsordresidene.

## <a name="turn-on-global-withholding-tax"></a>Slå på global kildeskatt

1. I **Funksjonsbehandling**-arbeidsområdet velger du **Global kildeskatt**, og deretter velger du **Aktiver nå**.
2. Gå til **Avgift \> Oppsett \> Parametere \> Parametere for økonomimodul** og deretter, i kategorien **Kildeskatt**, setter du alternativet **Aktiver global kildeskatt** til **Ja**.
3. Velg **Lagre**.
4. Oppdatere siden i webleseren.

> [!NOTE]
> Global kildeskattfunksjonalitet kan ikke aktiveres for land/områder der det allerede finnes lokale kildeskattløsninger. Disse områdene omfatter, men er ikke begrenset til India, Brasil, Thailand, Saudi-Arabia, Irland, Storbritannia og USA.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]