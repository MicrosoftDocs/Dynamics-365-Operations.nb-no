---
title: Oversikt over serviceobjekter
description: Denne artikkelen gir en oversikt over hvordan du jobber med serviceobjekter.
author: sorenva
ms.date: 07/25/2019
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServiceObjectTable
audience: Application User
ms.reviewer: kamaybac
ms.assetid: ''
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8150a94677fe38f4caa6f3e0b5fb5d1be5972eaf
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8862418"
---
# <a name="service-objects-overview"></a>Oversikt over serviceobjekter

[!include [banner](../includes/banner.md)]

Serviceobjekter er en kundes aktiva og produkter som du kan utføre en tjeneste for. Avhengig av servicetypen du tilbyr, kan objekter være materielle eller immaterielle:

-  Konkrete objekter er gjenstander, for eksempel en maskin eller en bygning, som du kan utføre en fysisk serviceoppgave på.

    Et materielt serviceobjekt kan også være en lagervare du oppretter i skjemaet Detaljer om frigitt produkt. Avhengig av lagerdimensjonsgruppen du har tilknyttet varen, kan du opprette et serviceobjektet på et detaljnivå som inneholder varens serienummer. Dette er nyttig når du må vite nøyaktig hvilken vare som serviceobjektet representerer.

    Et materielt serviceobjekt kan imidlertid også være en vare som ikke er direkte relatert til den direkte produksjonen eller forsyningskjeden til et firma. Et verktøysett som brukes til reparasjoner i en serviceordre kan for eksempel være et serviceobjekt som ikke er inkludert i lageret. I dette tilfellet registrere du den ikke som en lagervare.

-  Immaterielle objekter er ikke-fysiske ting, for eksempel et sett med kontoer eller et juridisk dokument, som du kan utføre serviceoppgaver på.

## <a name="example-of-an-intangible-service-object"></a>Eksempel på et immaterielt serviceobjekt

Firma A opprettholder finanspostene for flere små firmaer. En av kundene til firma A er det lokale fotballaget, og firma A fører ukentlig bokføring og årlig revisjon for klubbens kontoer. Lagets kontoer er definert i Serviceobjekter-skjemaet og angitt som objektet i serviceavtalen. Det er to serviceavtalelinjer for objektet. Linje 1 er ukentlig bokføring med et ukentlig intervall som er tilordnet til linjen, og linje 2 er årlig revisjon med et årlig intervall som er tilordnet.

## <a name="related-articles"></a>Relaterte artikler

[Opprette serviceobjekter](create-service-objects.md)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]