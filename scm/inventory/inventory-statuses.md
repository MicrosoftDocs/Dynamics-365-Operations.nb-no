---
title: Beholdningsstatuser
description: "Denne artikkelen beskriver hvordan du kan bruke lagerstatusene til å kategorisere og holde orden på lager."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: EcoResStorageDimensionGroup, WHSInventStatus
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 21331
ms.assetid: b35f495f-de4f-48a0-9d09-4d06781d7650
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: f77012e7b64b7f153103e9bbe91e8ded202b509a
ms.openlocfilehash: 1fcdf262ee1e7e1fbbdd0a5fed46fb1867f8d8fd
ms.lasthandoff: 03/31/2017


---

# <a name="inventory-statuses"></a>Beholdningsstatuser

[!include[banner](../includes/banner.md)]


Denne artikkelen beskriver hvordan du kan bruke lagerstatusene til å kategorisere og holde orden på lager.

Du kan bruke lagerstatuser til å kategorisere beholdning. Du kan deretter utføre aktuelle handlinger, for eksempel etterfylling eller plasseringsarbeid. 

Her er noen eksempler på hvordan du kan bruke lagerstatuser:

-   Opprett lagerstatuser for lagerbeholdning, innkommende transaksjoner og utgående transaksjoner.
-   Angi en standard lagerstatus for lagertransaksjoner.
-   Endre en beholdningsstatus for varer før ankomst, under ankomst, eller når varene plasseres under lagerbevegelse.
-   Bruk en lagerstatus til å prissette varer som returneres, og til å planlegge varedekning under hovedplanlegging.

En beholdningsstatus er én av dimensjonene i lagringsdimensjonsgruppen. Lagerstatuser kan kategoriseres som tilgjengelige eller utilgjengelige, og du kan bruke parameteren **Lagerblokkering** til å blokkere varer som har en tilgjengelig lagerstatus. Varer som har en blokkert status, regnes som aktuell beholdning og kan ikke brukes i produksjonsordrer, salgsordrer, overføringsordrer eller utgående transaksjoner. 

Du kan bruke lagervarer som har enten tilgjengelig eller utilgjengelig lagerstatus for innkommende arbeid. La oss si at du for eksempel oppretter en tilgjengelig status kalt **Klar**, en utilgjengelig status kalt **Skadet**, og en blokkert status kalt **Sperret**. Hvis du oppretter en bestilling for mottatte eller returnerte varer og eventuelle varer er skadet eller ødelagt, kan du endre lagerstatusen for disse varene til **Skadet** på bestillingslinjen. Etter at disse varene er mottatt, settes statusen automatisk til **Sperret**. Hvis du skanner de skadede varene med en mobil enhet, kan Microsoft Dynamics 365 for Operations bruke lokasjonsdirektiver og arbeidsmaler til å vise informasjon om en passende lokasjon eller et lokasjonsområde der du kan plassere disse varene. Når det gjelder returnerte varer, opprettes avgangstypen **Reservering** på **Lagertransaksjoner**-siden. 

Når det gjelder utgående arbeid, bruker du varer som har en tilgjengelig lagerstatus. Hvis du har varer med statusen **Brutt** og hovedplanlegging kjøres på disse varene, regnes de som manglende, og beholdningen etterfylles automatisk. 

Når du har definert beholdningsstatuser, kan du angi standard beholdningsstatus for et område, en vare og et lager. Du kan også angi en standardstatus for salg, overføring og bestillinger. Standardstatus for salgsordrer og utgående overføringsordre kan ikke ha alternativet **Lagerblokkering** satt til **Ja**. Lagerstatusen som arves fra standardinnstillingene for område, lager, vare, bestilling, overføringsordre eller salgsordre, kan endres ved hjelp av den mobile enheten, eller på bestillings-, salgsordre- eller overføringsordrelinjen. 

Hvis du planlegger dekning for varer som har en tilgjengelig lagerstatus, velger du alternativet **Dekningsplanlegg etter dimensjon** for en lagringsdimensjon på siden **Lagringsdimensjonsgrupper**. Når du åpner veiviseren **Varedekning**, vises varer som har en tilgjengelig status, på **Status**-siden. Hvis du vil opprette dekningsinnstillinger for disse varene, velger du IDen for lagerstatus for de tilgjengelige lagerstatusene. Basert på dekningsinnstillingene kan du beregne varebehovene og forhåndsberegne forsyning og behov for tilgjengelige varer under hovedplanlegging. Du kan ikke opprette et oppsett av varedekning som har en blokkert lagerstatus. Bruk i stedet **Varedekning**-siden til å opprette eller endre varedekningsparameterne.




