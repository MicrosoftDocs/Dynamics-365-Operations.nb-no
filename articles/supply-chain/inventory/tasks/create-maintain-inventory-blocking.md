---
title: Opprette og vedlikeholde en lagerblokkering
description: Denne fremgangsmåten viser hvordan du forhindrer at fysisk lagerbeholdning blir reservert av andre utgående kildedokumenter ved å bruke lagerblokkeringen.
author: perlynne
manager: tfehr
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventBlocking, InventItemIdLookupSimple, InventLocationIdLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b5fb3c7fc5dbeb6263357113d2a9348afc5b1ac9
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5212753"
---
# <a name="create-and-maintain-an-inventory-blocking"></a>Opprette og vedlikeholde en lagerblokkering

[!include [banner](../../includes/banner.md)]

Denne fremgangsmåten viser hvordan du forhindrer at fysisk lagerbeholdning blir reservert av andre utgående kildedokumenter ved å bruke lagerblokkeringen. Du kan kjøre prosedyren i demonstrasjonsdatafirmaet USMF med eksempelverdiene som vises. Du må ha en vare med fysisk lagerbeholdning tilgjengelig før du starter denne fremgangsmåten.


## <a name="create-an-inventory-blocking"></a>Opprette en lagerblokkering
1. I **navigasjonsruten** går du til **Moduler > Lagerstyring > Periodiske oppgaver > Lagerblokkering**.
2. Klikk på **Ny**.
3. Klikk på rullegardinknappen i **Varenummer**-feltet for å åpne oppslaget.
4. Velg varen du vil bruke, i listen. Velg et varenummer med fysisk lagerbeholdning som du vil blokkere. Hvis du bruker USMF, kan du velge vare M9201.  
5. Angi et tall i **Antall**-feltet. Hvis du bruker varen M9201, må du velge mindre enn 200.
6. Vis hurtigfanen **Lagerdimensjoner**.
7. Klikk på rullegardinknappen i **Lager**-feltet for å åpne oppslaget.
8. Finn og velg ønsket post i listen. Hvis du bruker vare M9201, kan du velge lager 51.  
9. Klikk på **Lagre**.

## <a name="update-the-conditions-of-the-inventory-blocking"></a>Oppdatere betingelsene for lagerblokkeringen
1. Angi et tall i hurtigfanen **Generelt** i feltet **Antall**. Oppdater lagerantall-feltet for å gjenspeile antallet som skal blokkeres.  
2. Angi en dato i feltet **Forventet dato**. Du kan angi når den blokkerte lagertransaksjonen forventes å bli tilgjengelig for reservasjon, ved å tilordne en forventet dato. Hvis alternativet Forventede mottak er valgt for lagerblokkeringen, som den er som standard når du manuelt oppretter en blokkering, vises denne datoen på den forventede transaksjonen.  
3. Klikk på **Lagre**.

## <a name="remove-the-inventory-blocking"></a>Fjerne lagerblokkeringen
1. Klikk på **Slett** i **handlingsruten**.
2. Klikk på **Ja**.
3. Lukk siden.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]