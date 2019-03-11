---
title: Serviceobjekter
description: Serviceobjekter er en kundes aktiva og produkter som du kan utføre en tjeneste for.
author: ShylaThompson
manager: AnnBe
ms.date: 02/21/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceObjectTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5641077de84b6702d2c5621edef74783f2f104fd
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/29/2019
ms.locfileid: "353408"
---
# <a name="service-objects"></a>Serviceobjekter 

[!include [banner](../includes/banner.md)]

Serviceobjekter er en kundes aktiva og produkter som du kan utføre en tjeneste for. Avhengig av servicetypen du tilbyr, kan objekter være materielle eller immaterielle:

-  Konkrete objekter er gjenstander, for eksempel en maskin eller en bygning, som du kan utføre en fysisk serviceoppgave på.

    Et materielt serviceobjekt kan også være en lagervare du oppretter i skjemaet Detaljer om frigitt produkt. Avhengig av lagerdimensjonsgruppen du har tilknyttet varen, kan du opprette et serviceobjektet på et detaljnivå som inneholder varens serienummer. Dette er nyttig når du må vite nøyaktig hvilken vare som serviceobjektet representerer.

    Et materielt serviceobjekt kan imidlertid også være en vare som ikke er direkte relatert til den direkte produksjonen eller forsyningskjeden til et firma. Et verktøysett som brukes til reparasjoner i en serviceordre kan for eksempel være et serviceobjekt som ikke er inkludert i lageret. I dette tilfellet registrere du den ikke som en lagervare.

-  Immaterielle objekter er ikke-fysiske ting, for eksempel et sett med kontoer eller et juridisk dokument, som du kan utføre serviceoppgaver på.

## <a name="example-of-an-intangible-service-object"></a>Eksempel på et immaterielt serviceobjekt

Firma A opprettholder finanspostene for flere små firmaer. En av kundene til firma A er det lokale fotballaget, og firma A fører ukentlig bokføring og årlig revisjon for klubbens kontoer. Lagets kontoer er definert i Serviceobjekter-skjemaet og angitt som objektet i serviceavtalen. Det er to serviceavtalelinjer for objektet. Linje 1 er ukentlig bokføring med et ukentlig intervall som er tilordnet til linjen, og linje 2 er årlig revisjon med et årlig intervall som er tilordnet.

## <a name="related-topics"></a>Relaterte emner

[Opprette serviceobjekter](create-service-objects.md)

