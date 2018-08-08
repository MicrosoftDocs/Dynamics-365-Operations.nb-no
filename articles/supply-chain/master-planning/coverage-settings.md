---
title: Dekningsinnstillinger
description: "Hovedplanlegging bruker dekningsinnstillinger til å beregne varebehov."
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
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
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 858328ec60e0ffa5ca46a98b365fb0fc599ae1f0
ms.contentlocale: nb-no
ms.lasthandoff: 05/08/2018

---

# <a name="coverage-settings"></a>Dekningsinnstillinger

[!include [banner](../includes/banner.md)]

Hovedplanlegging bruker dekningsinnstillinger til å beregne varebehov. 

Du kan angi dekningsinnstillinger på flere måter:

-   Angi dekningsinnstillinger for en dekningsgruppe. Du kan opprette en dekningsgruppe som inneholder innstillinger for alle produkter som er koblet til dekningsgruppen. Klikk **Hovedplanlegging &gt; Oppsett &gt; Dekning &gt; Dekningsgrupper** for å opprette en dekningsgruppe. Du kan koble en dekningsgruppe til et produkt. Hvis koblingen er spesifikk for et område, lager eller produktdimensjon, kan du bruke **Dekningsgruppe**-feltet på **Varedekning**-siden. Hvis koblingen er generisk, uavhengig av produktdimensjonene, bruker du **Dekningsgruppe** i **Plan**-hurtigkategorien på **Produktdetaljer**-siden. Hvis du ikke kobler en dekningsgruppe til et produkt, bruker hovedplanlegging den **generelle dekningsgruppen** som er angitt på siden **Hovedplanleggingsparametere**, som standard.

-   Angi dekningsinnstillinger for et produkt. Du kan opprette dekningsinnstillinger for et bestemt produkt. Klikk **Behandling av produktinformasjon &gt; Produkter &gt; Frigitte produkter**. Velg produktet. I **handlingsruten**, i kategorien **Plan** i **Dekningsgruppen**, klikker du **Varedekning** for å åpne **Varedekning**-siden. Hvis produktet allerede er koblet til en dekningsgruppe, kan du overstyre innstillingene for dekningsgruppen ved å bruke **Overstyr**-feltet. Dekningsinnstillingene på **Varedekning**-siden har prioritet over innstillingene på **Dekningsgruppe**-siden.

<!-- -->

-   Angi dekningsinnstillinger for et produkt ved hjelp av en veiviser. Veiviseren gir deg trinnvise instruksjoner om hvordan du definerer primære dekningsparametere. På **Varedekning**-siden klikker du **Veiviser** for å åpne **Varedekningsveiviseren**.

<!-- -->

- Angi dekningsinnstillinger for en dimensjonsgruppe. Klikk **Behandling av produktinformasjon &gt; Felles &gt; Frigitte produkter**. På **Detaljer om frigitt produkt**-siden, i kategorien **Generelt** i **Administrasjon**-gruppen, klikker du koblingen **Lagringsdimensjonsgruppe**. På **Lagringsdimensjonsgruppe**-siden velger du feltet **Dekningsplanlegg etter dimensjon** for å opprette dekningsinnstillinger for en dimensjon i lagringsdimensjonsgruppen. Alle produktdimensjoner, for eksempel konfigurasjon, farge, størrelse, stil, må ha feltet **Dekningsplanlegg etter dimensjon** valgt.



<a name="additional-resources"></a>Tilleggsressurser
--------

[Hovedplaner](master-plans.md)




