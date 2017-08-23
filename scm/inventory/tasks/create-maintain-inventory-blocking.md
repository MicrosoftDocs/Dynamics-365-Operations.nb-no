--- 
title: Opprette og vedlikeholde lagerblokkering
description: "Denne fremgangsmåten viser hvordan du forhindrer at fysisk lagerbeholdning blir reservert av andre utgående kildedokumenter ved å bruke lagerblokkeringen."
author: perlynne
manager: AnnBe
ms.date: 12/02/2015
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bibis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 9b947a02be981155053e33a4ef20e19bf2a194a5
ms.openlocfilehash: 7d0834aa3a415e8e9b4eab745b680e22a680b6b6
ms.contentlocale: nb-no
ms.lasthandoff: 07/27/2017

---
# <a name="create-and-maintain-inventory-blocking"></a>Opprette og vedlikeholde lagerblokkering

[!include[task guide banner](../../includes/task-guide-banner.md)]

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


