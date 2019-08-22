---
title: Opprette og vedlikeholde en lagerblokkering
description: Denne fremgangsmåten viser hvordan du forhindrer at fysisk lagerbeholdning blir reservert av andre utgående kildedokumenter ved å bruke lagerblokkeringen.
author: perlynne
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventBlocking, InventItemIdLookupSimple, InventLocationIdLookup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 845d517ad10245df3b208874df61e235c199c7fe
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/01/2019
ms.locfileid: "1836413"
---
# <a name="create-and-maintain-an-inventory-blocking"></a>Opprette og vedlikeholde en lagerblokkering

[!include [task guide banner](../../includes/task-guide-banner.md)]

Denne fremgangsmåten viser hvordan du forhindrer at fysisk lagerbeholdning blir reservert av andre utgående kildedokumenter ved å bruke lagerblokkeringen. Du kan kjøre prosedyren i demonstrasjonsdatafirmaet USMF med eksempelverdiene som vises. Du må ha en vare med fysisk lagerbeholdning tilgjengelig før du starter denne fremgangsmåten.


## <a name="create-an-inventory-blocking"></a>Opprette en lagerblokkering
1. Gå til Lagerstyring > Periodiske oppgaver > Lagerblokkering.
2. Klikk Ny.
3. Klikk rullegardinknappen i Varenummer-feltet for å åpne oppslaget.
4. Velg varen du vil bruke, i listen. 
    * Velg et varenummer med fysisk lagerbeholdning som du vil blokkere. Hvis du bruker USMF, kan du velge vare M9201.  
5. Angi et tall i feltet Antall.
    * Hvis du bruker varen M9201, må du velge mindre enn 200.  
6. Aktiver utvidelsen av delen Lagerdimensjoner.
7. Klikk rullegardinknappen i Lager-feltet for å åpne oppslaget.
8. Finn og velg ønsket post i listen.
    * Hvis du bruker vare M9201, kan du velge lager 51.  
9. Klikk Lagre.

## <a name="update-the-conditions-of-the-inventory-blocking"></a>Oppdatere betingelsene for lagerblokkeringen
1. Angi et tall i feltet Antall.
    * Oppdater lagerantall-feltet for å gjenspeile antallet som skal blokkeres.  
2. Angi en dato i Forventet dato-feltet.
    * Du kan angi når den blokkerte lagertransaksjonen forventes å bli tilgjengelig for reservasjon, ved å tilordne en forventet dato. Hvis alternativet Forventede mottak er valgt for lagerblokkeringen, som den er som standard når du manuelt oppretter en blokkering, vises denne datoen på den forventede transaksjonen.  
3. Klikk Lagre.

## <a name="remove-the-inventory-blocking"></a>Fjerne lagerblokkeringen
1. Klikk Slett.
2. Klikk Ja.
3. Lukk siden.

