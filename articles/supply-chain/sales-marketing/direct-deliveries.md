---
title: Direkte leveringer
description: Denne artikkelen gir informasjon om direkte leveringer. Direkte leveringer er leveringer som sendes direkte fra leverandøren til kunden.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchCreateFromSalesOrder, SalesTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 9704
ms.assetid: 64c51384-8a4e-45d0-83c1-12cea22902f9
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d9c4a695c591865c52ad5ee6d37a515139f58bf8
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/15/2019
ms.locfileid: "1563466"
---
# <a name="direct-deliveries"></a>Direkte leveringer

[!include [banner](../includes/banner.md)]

Denne artikkelen gir informasjon om direkte leveringer. Direkte leveringer er leveringer som sendes direkte fra leverandøren til kunden.

Direkte leveringer sparer leveringstid og reduserer kostnadene som er knyttet til ha beholdning, fordi produktene ikke oppbevares i lageret før du sender dem til kunden.  

Du kan opprette direkte leveringer fra **Salgsordre**-siden. Opprett først en salgsordre og ordrelinjer. Velg deretter **Direkte levering** i **Salgsordre**-fanen i handlingsruten. Angi til slutt linjene som må behandles som en direkte levering. En kobling opprettes nå mellom salgsordrelinjene for direkteleverineng og de tilsvarende bestillingslinjene.  

**Obs!** Hvis en del av det bestilte antallet allerede er levert, må du dele det gjenstående antallet. Opprett en ny linje for antallet som må leveres direkte, og trekk dette antallet fra antallet på den opprinnelige linjen. Hvis det opprinnelige antallet var 15, og 5 er levert, må du for eksempel opprette en ny linje for det gjenværende antallet på 10 og deretter redusere det opprinnelige antallet med det beløpet.  

Når du har opprettet direkteleveringskoblingen mellom salgsordrelinjene og bestillingslinjene, kan du oppdatere salgsordren ved hjelp av en følgeseddel. Kjøre enten en følgeseddeloppdatering eller en fakturaoppdatering fra bestillingen. Du må fakturaoppdatere salgsordren fra **Salgsordre**-siden. En fakturaoppdatering kan ikke forårsake at antallet på salgsordren overskrider antallet som er registrert som mottatt. En salgsordrelinje har for eksempel 10 stykker, men bare 5 stykker fra salgsordrelinjen har blitt oppdatert ved hjelp av en følgeseddel. Hvis du velger **Alle** i **Antall**-listen når du foretar fakturaoppdatering av salgsordren, er det bare varene som er fysisk mottatt eller oppdatert ved hjelp av en følgeseddel, som blir fakturaoppdatert. Hele salgsordrelinjen oppdateres ikke.

## <a name="delivery-date"></a>Leveringsdato
Når du oppdaterer feltet **Ønsket mottaksdato** på salgsordelinjen, oppdateres også **Leveringsdato**-feltet på den tilhørende bestillingslinjen. Når du oppdaterer **Bekreftet**-feltet på bestillingslinjen, oppdateres også feltene **Bekreftet leveringsdato** og **Bekreftet forsendelsesdato** på de tilhørende salgsordrelinjene.

## <a name="delivery-address"></a>Leveringsadresse
Leveringsadressen for bestillinger er vanligvis firmaets adresse. Når du oppretter en direkte levering, angir du imidlertid kundens adresse som leveringsadresse. Hvis du endrer leveringsadressen på en bestillingslinje som har leveringstypen **Direkte levering**, oppdateres også leveringsadressen på den tilhørende salgsordrelinjen. Hvis du endrer leveringsadressen på salgsordrelinjen, oppdateres også leveringsadressen på bestillingslinjen.

## <a name="deleting-order-lines"></a>Slette ordrelinjer
Hvis du prøver å slette salgsordrelinjer som har leveringstypen **Direkte levering**, vises en meldingsboks der det står at bestillingslinjer er knyttet til linjen. Hvis salgsordrelinjen er delvis levert, kan du ikke slette salgsordrelinjen eller bestillingslinjene som er knyttet til den.

## <a name="warehouse"></a>Lager
Når du oppretter en direktelevering, ankommer varene du selger, aldri lageret. Du må imidlertid likevel angi et lager på salgsordrelinjen. På samme måte kan plukkbehov angis i varemodellgruppen for varen. Siden varene imidlertid aldri ankommer lageret, ignoreres disse behovene når salgsordren er en direktelevering.



