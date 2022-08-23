---
title: Kundeposter vises ikke i Commerce Headquarters
description: Denne artikkelen inneholder feilsøkingsveiledning som kan hjelpe når kundeposter ikke vises i Commerce Headquarters umiddelbart.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.custom: ''
ms.assetid: ''
ms.search.industry: Retail
ms.openlocfilehash: f1ad1f45abbc95cbf6d41b3c8681db781c6c9d23
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/12/2022
ms.locfileid: "9268845"
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
