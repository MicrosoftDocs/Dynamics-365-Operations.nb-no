---
title: Opprette Internett-kanal og definere kanalattributter
description: Denne prosedyren hjelper med å opprette en ny Internett-kanal og legge den til i organisasjonshierarkiet.
author: jashanno
manager: AnnBe
ms.date: 06/04/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailSPOnlineStoreDetailPage, SysLookupMultiSelectGrid, DimensionLookup, OMHierarchyManager, HierarchyDesigner, OMNodeSelection, HierarchyPublishAndCloseForm
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f15b035c01801041d637a2d315d8a3ddcc9d6540
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4414697"
---
# <a name="create-online-channel-and-define-channel-attributes"></a>Opprette Internett-kanal og definere kanalattributter

[!include [banner](../includes/banner.md)]

Denne prosedyren hjelper med å opprette en ny Internett-kanal og legge den til i organisasjonshierarkiet. Før du kan opprette en ny Internett-kanal, må du opprette organisasjonshierarkiet. Denne prosedyren bruker demonstrasjonsdatafirmaet USRT.


## <a name="create-a-new-online-channel"></a>Opprette en ny Internett-kanal
1. Gå til Detaljhandel og handel > Kanaler > Nettbutikker.
2. Klikk Ny.
3. Skriv inn en verdi i Navn-feltet.
4. Angi eller velg en verdi i feltet Lager.
5. Velg et alternativ i feltet Tidssone for butikk.
6. Angi eller velg en verdi i Standardkunde-feltet.
7. Angi eller velg en verdi i feltet Adressebok for kunde.
8. Angi eller velg en verdi i Betalingsbetingelser-feltet.
9. Angi eller velg en verdi i Betalingsmåte-feltet.
10. Angi eller velg en verdi i feltet Profil for e-postvarsling.
11. Vis delen Finansdimensjoner.
12. Angi eller velg en verdi i BusinessUnit-feltet.
    * Angi verdien for alle andre standarddimensjoner på samme måte.  
13. Klikk Lagre.

## <a name="add-the-online-channel-to-organization-hierarchy"></a>Legge til Internett-kanalen i organisasjonshierarkiet
1. Lukk siden.
2. Gå til Organisasjonsstyring > Organisasjoner > Organisasjonshierarkier.
3. Finn og velg ønsket post i listen.
4. Klikk Vis.
5. Klikk Rediger.
    * Du kan velge en hierarkinode der du vil sette inn den nye kanalen.  
6. Klikk Sett inn.
7. Klikk på Handelskanal.
8. Klikk OK.
9. Klikk Publiser for å åpne nedtrekksdialogen.
10. Angi dato og klokkeslett i feltet Gyldighetsdato.
11. Klikk Publiser.

## <a name="configure-orders-for-near-real-time-notification"></a>Konfigurere ordrer for varsling i nær sanntid
1. Gå til Detaljhandel og handel > Hovedkvarteroppsett > Parametere > Handelsparametere.
2. Sett bruk sanntid-tjenesten for eCommerce-ordreoppretting til "Ja".
3. Kjør distribusjonsplanen 1070 for å synkronisere endringer i kanaldatabasen. 




[!INCLUDE[footer-include](../../includes/footer-banner.md)]