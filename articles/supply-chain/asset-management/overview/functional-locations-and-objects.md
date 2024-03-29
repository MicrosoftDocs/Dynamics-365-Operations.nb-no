---
title: Arbeidssteder og aktiva
description: Denne artikkelen beskriver arbeidssteder og aktiva i Aktivastyring. Aktivastyring er en avansert modul for håndtering av aktiva og vedlikeholdsjobber i Dynamics 365 Supply Chain Management.
author: johanhoffmann
ms.date: 06/24/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0d8d155b8bbf981408f6f15e914fc3bb1da25c9c
ms.sourcegitcommit: 6781fc47606b266873385b901c302819ab211b82
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/02/2022
ms.locfileid: "9111084"
---
# <a name="functional-locations-and-assets"></a>Arbeidssteder og aktiva

[!include [banner](../../includes/banner.md)]

 

Denne artikkelen beskriver arbeidssteder og aktiva i Aktivastyring. Aktivastyring er en avansert modul for håndtering av aktiva og vedlikeholdsjobber i Dynamics 365 Supply Chain Management.

## <a name="overview"></a>Oversikt

Aktivastyring er integrert sømløst med flere moduler i andre økonomi- og driftsapper. Illustrasjonen nedenfor viser grensesnittene med andre moduler.

![Diagram som viser hvordan Aktivastyring har grensesnitt til andre moduler.](media/01-overview-image.png)

Med Aktivastyring kan du effektivt administrere og utføre alle oppgaver som er knyttet til administrasjon og vedlikehold av mange typer utstyr i firmaet. Dette utstyret omfatter maskiner, produksjonsutstyr og kjøretøyer. Aktivastyring støtter også løsninger på tvers av en rekke bransjer.

Illustrasjonen nedenfor viser en oversikt over de viktigste funksjonene som dekkes av Aktivastyring.

![Diagram som viser hovedfunksjonaliteten i Aktivastyring.](media/02-overview-image.png)

## <a name="functional-locations-and-assets"></a>Arbeidssteder og aktiva

Arbeidssteder brukes til å administrere aktiva på steder. Denne administrasjonen inkluderer sporing av aktivakostnader på arbeidssteder. Arbeidssteder er strukturert hierarkisk, og steder kan ha underordnede steder. Strukturen til arbeidssteder er statisk. Med andre ord, steder kan ikke endre plass. Aktiva kan installeres på arbeidssteder, og etter behov kan de installeres på andre arbeidssteder senere.

Aktivakostnader følger alltid plasseringen av aktivumet. Med andre ord, hvis du installerer et aktivum på et nytt arbeidssted, bruker aktivumet automatisk finansdimensjonene som er knyttet til det nye arbeidsstedet. Derfor er aktivakostnader alltid knyttet til arbeidsstedet som aktivumet er installert på. Denne automatiske håndteringen av finansdimensjoner bidrar til å sikre fullstendig sporing av kostnader når firmaet utfører prosjektkontroll og rapportering på arbeidssteder.

Måten du bygger hierarkiet av arbeidssteder på, avhenger av firmaets krav for å opprettholde internt utstyr eller betjene kundeutstyr. Den følgende illustrasjonen viser et eksempel på arbeidssteder som er basert på geografiske lokasjoner.

![Diagram som viser arbeidssteder basert på geografiske steder.](media/03-overview-image.png)

Den følgende illustrasjonen viser et eksempel på arbeidssteder som er basert på kunder.

![Diagram som viser arbeidssteder basert på kunder.](media/04-overview-image.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
