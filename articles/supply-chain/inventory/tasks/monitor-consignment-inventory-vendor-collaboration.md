---
title: Overvåke forsendelseslager ved hjelp av leverandørsamarbeid
description: Denne fremgangsmåten viser hvordan du bruker leverandørsamarbeid til å se informasjon om lagernivået for produktet som du har plassert i forsendelse hos en kunde.
author: sherry-zheng
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ConsignmentProductReceiptLines, PurchVendorPortalConfirmedOrders, DefaultDashboard, ConsignmentVendorPortalOnhand
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: chuzheng
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7cca89917148f782a67c80fc47ac1af0582c79d19337dd1093965c87a4c9a42e
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6755329"
---
# <a name="monitor-consignment-inventory-using-vendor-collaboration"></a>Overvåke forsendelseslager ved hjelp av leverandørsamarbeid

[!include [banner](../../includes/banner.md)]

Denne fremgangsmåten viser hvordan du bruker leverandørsamarbeid til å se informasjon om lagernivået for produktet som du har plassert i forsendelse hos en kunde. Du kan også overvåke forbruket av lageret når kunden blir eier av lageret. Du kan bruke prosedyren i USMF-demodatafirmaet. Denne fremgangsmåten gjelder for en funksjon som ble lagt til i Dynamics 365 for Operations, versjon 1611.


## <a name="view-consumed-inventory"></a>Vise brukt beholdning
1. Gå til Leverandørsamarbeid > Forsendelseslager > Produkter mottatt fra forsendelseslager.
    * Listen viser mottaksseddellinjene som ble generert da eierskap av forsendelseslageret ble endret fra leverandøren til kunden. Du må kanskje gå til høyre for å se antall og annen informasjon. Du kan bruke informasjonen i denne listen til å generere fakturaer for kunden. Du kan også eksportere dataene til Microsoft Excel.   
2. Klikk på Vis bestilling.
3. Vis seksjonen Linjedetaljer.
    * Linjen er merket som Forsendelse, og topptekstdelen viser at bestillingen har statusen Mottatt.  
4. Lukk siden.

## <a name="view-on-hand-inventory"></a>Vise lagerbeholdning
1. Gå til Leverandørsamarbeid > Forsendelseslager > Forsendelseslager for beholdning.
    * Siden Forsendelseslager for beholdning viser lageret du eier på kundens lager. Du kan vise flere dimensjoner, for eksempel område og lager, ved å klikke fanen Visningsdimensjoner.   



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]