---
title: Kundeposter vises ikke i Commerce Headquarters
description: Denne artikkelen inneholder feilsøkingsveiledning som kan hjelpe når kundeposter ikke vises i Commerce Headquarters umiddelbart.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 5cdc96c9829be4d34e9346b2c99d300c2349bc41
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8876551"
---
# <a name="customer-records-dont-appear-in-commerce-headquarters"></a>Kundeposter vises ikke i Commerce Headquarters

[!include [banner](../../includes/banner.md)]

Denne artikkelen inneholder feilsøkingsveiledning som kan hjelpe når kundeposter ikke vises i Commerce Headquarters umiddelbart.

## <a name="description"></a>beskrivelse

Når du oppretter en ny kundepost ved hjelp av registreringsflyten i e-handelbutikken, vises ikke den tilsvarende kundeposten umiddelbart i Commerce Headquarters.

## <a name="resolution"></a>Oppløsning

### <a name="disable-customer-creation-in-async-mode"></a>Deaktivere kundeoppretting i Async-modus

> [!IMPORTANT]
> Hvis du deaktiverer oppretting av asynkron kunde, kan systemytelsen påvirkes, fordi oppretting av hver post vil føre til en forespørsel i sanntid til Commerce Headquarters. Hvis også Commerce Headquarters er nede (for eksempel under serviceflyt), vil det føre til feil hvis det opprettes nye flyter for kunde.

Følg denne fremgangsmåten for å deaktivere kundeoppretting i asynkron modus i Commerce Headquarters.

1. Gå til **Detaljhandel og handel \> Kanaloppsett \> Oppsett av nettbutikk \> Funksjonsprofiler**.
1. Hvis du ikke allerede bruker en funksjonsprofil for den nettbaserte kanalen, kan du opprette en.
1. Kontroller at alternativet **Opprett kunde i async-modus** er satt til **Nei**.
1. Gå til **Detaljhandel og handel \> Kanaler \> Nettbutikker**.
1. Velg den elektroniske butikken du vil deaktivere oppretting av asynkron kunde for.
1. I fanen **Generelt** kontrollerer du at feltet **Funksjonsprofil** er satt til funksjonsprofilen du bruker for den elektroniske kanalen.

## <a name="additional-resources"></a>Tilleggsressurser

[Konfigurere en B2C-leier i Commerce](../set-up-b2c-tenant.md)
