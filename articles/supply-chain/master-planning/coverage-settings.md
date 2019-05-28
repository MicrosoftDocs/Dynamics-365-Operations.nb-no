---
title: Dekningsinnstillinger
description: Dette emnet inneholder informasjon om dekningsinnstillingene som hovedplanlegging bruker til å beregne varebehov.
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqGroup, ReqItemTable, ReqItemTableWizard
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2494
ms.assetid: 5a95ae4f-ca75-47d9-a1c3-68c97b42f166
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 99e094a7131b6d3a299fc72abd0141529908ddd2
ms.sourcegitcommit: 9e50bee6a67f0fe2fa6f86e02c7e8de16d0e2482
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/08/2019
ms.locfileid: "1538900"
---
# <a name="coverage-settings"></a>Dekningsinnstillinger

[!include [banner](../includes/banner.md)]

Hovedplanlegging bruker dekningsinnstillinger til å beregne varebehov.

Du kan angi dekningsinnstillinger på flere måter:

- Angi dekningsinnstillinger for en dekningsgruppe.

    Du kan opprette en dekningsgruppe som inneholder innstillinger for alle produkter som er koblet til dekningsgruppen. Hvis du vil opprette en dekningsgruppe, går du til **Hovedplanlegging &gt; Oppsett &gt; Dekning &gt; Dekningsgrupper**. Du kan koble en dekningsgruppe til et produkt. Hvis koblingen er spesifikk for et område, lager eller produktdimensjon, kan du bruke **Dekningsgruppe**-feltet på **Varedekning**-siden. Hvis koblingen er generisk, uavhengig av produktdimensjonene, bruker du **Dekningsgruppe**-feltet i **Plan**-hurtigkategorien på **Produktdetaljer**-siden. Hvis du ikke kobler en dekningsgruppe til et produkt, bruker hovedplanlegging som standard den generelle dekningsgruppen som er angitt på siden **Hovedplanleggingsparametere**.

- Angi dekningsinnstillinger for et produkt.

    Du kan opprette dekningsinnstillinger for et bestemt produkt. Gå til **Behandling av produktinformasjon &gt; Produkter &gt; Frigitte produkter**. Velg produktet. I handlingsruten, i kategorien **Plan** i **Dekning**-gruppen, velger du **Varedekning** for å åpne **Varedekning**-siden. Hvis produktet allerede er koblet til en dekningsgruppe, kan du overstyre innstillingene for dekningsgruppen ved å bruke **Overstyr**-feltet. Dekningsinnstillingene på **Varedekning**-siden har prioritet over innstillingene på **Dekningsgruppe**-siden.

- Angi dekningsinnstillinger for et produkt ved hjelp av en veiviser.

    Veiviseren fører deg gjennom prosessen med å definere de primære varedekningsparameterne. På **Varedekning**-siden i handlingsruten velger du **Veiviser** for å åpne **Varedekningsveiviseren**.

- Angi dekningsinnstillinger for en dimensjonsgruppe.

    Gå til **Behandling av produktinformasjon &gt; Produkter &gt; Frigitte produkter**. På **Detaljer om frigitt produkt**-siden, i hurtigfanen **Generelt** i **Administrasjon**-delen, velger du koblingen i feltet **Lagringsdimensjonsgruppe**. På **Lagringsdimensjonsgrupper**-siden merker du av for **Dekningsplanlegg etter dimensjon** for å opprette dekningsinnstillinger for en dimensjon i lagringsdimensjonsgruppen. Feltet **Dekningsplanlegg etter dimensjon** må være valgt for alle produktdimensjoner, for eksempel konfigurasjon, farge, størrelse og stil.

## <a name="additional-resources"></a>Tilleggsressurser

[Hovedplaner](master-plans.md)
