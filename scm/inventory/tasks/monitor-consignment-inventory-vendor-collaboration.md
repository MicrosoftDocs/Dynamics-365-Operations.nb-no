--- 
title: "Overvåke forsendelseslager ved hjelp av leverandørsamarbeid"
description: "Denne fremgangsmåten viser hvordan du bruker leverandørsamarbeid til å se informasjon om lagernivået for produktet som du har plassert i forsendelse hos en kunde."
author: mkirknel
manager: AnnBe
ms.date: 10/13/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 9b947a02be981155053e33a4ef20e19bf2a194a5
ms.openlocfilehash: ad4868991226aef21a0410860e3f98d11901ffbb
ms.contentlocale: nb-no
ms.lasthandoff: 07/27/2017

---
# <a name="monitor-consignment-inventory-using-vendor-collaboration"></a>Overvåke forsendelseslager ved hjelp av leverandørsamarbeid

[!include[task guide banner](../../includes/task-guide-banner.md)]

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


