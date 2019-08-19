---
title: Arbeidssteder og aktiva
description: Dette emnet beskriver arbeidssteder og aktiva i Aktivastyring. Aktivastyring er en avansert modul for håndtering av aktiva og vedlikeholdsjobber i Microsoft Dynamics 365 for Finance and Operations.
author: josaw1
manager: AnnBe
ms.date: 06/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 351e27dfbbd5227a9642f14a48afe194c447a0f3
ms.sourcegitcommit: 747bcd25ce7c6c20ce9eaa0027e730f74d4fd6aa
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/23/2019
ms.locfileid: "1783502"
---
# <a name="functional-locations-and-assets"></a>Arbeidssteder og aktiva

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Dette emnet beskriver arbeidssteder og aktiva i Aktivastyring. Aktivastyring er en avansert modul for håndtering av aktiva og vedlikeholdsjobber i Microsoft Dynamics 365 for Finance and Operations.

## <a name="overview"></a>Oversikt

Asset Management er integrert sømløst med flere moduler i Finance and Operations. Illustrasjonen nedenfor viser grensesnittene med andre moduler.

![Figur 1](media/01-overview-image.png)

Med Aktivastyring kan du effektivt administrere og utføre alle oppgaver som er knyttet til administrasjon og vedlikehold av mange typer utstyr i firmaet. Dette utstyret omfatter maskiner, produksjonsutstyr og kjøretøyer. Aktivastyring støtter også løsninger på tvers av en rekke bransjer.

Illustrasjonen nedenfor viser en oversikt over de viktigste funksjonene som dekkes av Aktivastyring.

![Figur 2](media/02-overview-image.png)

## <a name="functional-locations-and-assets"></a>Arbeidssteder og aktiva

Arbeidssteder brukes til å administrere aktiva på steder. Denne administrasjonen inkluderer sporing av aktivakostnader på arbeidssteder. Arbeidssteder er strukturert hierarkisk, og steder kan ha underordnede steder. Strukturen til arbeidssteder er statisk. Med andre ord, steder kan ikke endre plass. Aktiva kan installeres på arbeidssteder, og etter behov kan de installeres på andre arbeidssteder senere.

Aktivakostnader følger alltid plasseringen av aktivumet. Med andre ord, hvis du installerer et aktivum på et nytt arbeidssted, bruker aktivumet automatisk finansdimensjonene som er knyttet til det nye arbeidsstedet. Derfor er aktivakostnader alltid knyttet til arbeidsstedet som aktivumet er installert på. Denne automatiske håndteringen av finansdimensjoner bidrar til å sikre fullstendig sporing av kostnader når firmaet utfører prosjektkontroll og rapportering på arbeidssteder.

Måten du bygger hierarkiet av arbeidssteder på, avhenger av firmaets krav for å opprettholde internt utstyr eller betjene kundeutstyr. Den følgende illustrasjonen viser et eksempel på arbeidssteder som er basert på geografiske lokasjoner.

![Figur 3](media/03-overview-image.png)

Den følgende illustrasjonen viser et eksempel på arbeidssteder som er basert på kunder.

![Figur 4](media/04-overview-image.png)
