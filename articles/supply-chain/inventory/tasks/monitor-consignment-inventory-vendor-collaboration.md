---
title: Overvåke forsendelseslager ved hjelp av leverandørsamarbeid
description: Denne fremgangsmåten viser hvordan du bruker leverandørsamarbeid til å se informasjon om lagernivået for produktet som du har plassert i forsendelse hos en kunde.
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ConsignmentProductReceiptLines, PurchVendorPortalConfirmedOrders, DefaultDashboard, ConsignmentVendorPortalOnhand
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: dfbe5e9de7b700d991e0826fb4387de416ce242a
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/01/2019
ms.locfileid: "1845402"
---
# <a name="monitor-consignment-inventory-using-vendor-collaboration"></a>Overvåke forsendelseslager ved hjelp av leverandørsamarbeid

[!include [task guide banner](../../includes/task-guide-banner.md)]

Denne fremgangsmåten viser hvordan du bruker leverandørsamarbeid til å se informasjon om lagernivået for produktet som du har plassert i forsendelse hos en kunde. Du kan også overvåke forbruket av lageret når kunden blir eier av lageret. Du kan bruke prosedyren i USMF-demodatafirmaet. Denne fremgangsmåten gjelder for en funksjon som ble lagt til i Dynamics 365 for Operations, versjon 1611.


## <a name="view-consumed-inventory"></a>Vise brukt beholdning
1. Gå til Leverandørsamarbeid > Forsendelseslager > Produkter mottatt fra forsendelseslager.
    * Listen viser mottaksseddellinjene som ble generert da eierskap av forsendelseslageret ble endret fra leverandøren til kunden. Du må kanskje gå til høyre for å se antall og annen informasjon. Du kan bruke informasjonen i denne listen til å generere fakturaer for kunden. Du kan også eksportere dataene til Microsoft Excel.   
2. Klikk Vis bestilling.
3. Vis seksjonen Linjedetaljer.
    * Linjen er merket som Forsendelse, og topptekstdelen viser at bestillingen har statusen Mottatt.  
4. Lukk siden.

## <a name="view-on-hand-inventory"></a>Vise lagerbeholdning
1. Gå til Leverandørsamarbeid > Forsendelseslager > Forsendelseslager for beholdning.
    * Siden Forsendelseslager for beholdning viser lageret du eier på kundens lager. Du kan vise flere dimensjoner, for eksempel område og lager, ved å klikke kategorien Visningsdimensjoner.   

