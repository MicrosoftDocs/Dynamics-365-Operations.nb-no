---
title: Sende en ordre fra en annen butikk
description: Dette emnet beskriver sendefunksjonen Tillegg.
author: ashishmsft
manager: AnnBe
ms.date: 10/10/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Core, Retail
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2017-10-10
ms.dyn365.ops.version: Retail Version
ms.translationtype: HT
ms.sourcegitcommit: 986ec7835dac52c326085c47313205d08b1bafa8
ms.openlocfilehash: d217bc31ad9d93c5440e5329f7b7327d089137f4
ms.contentlocale: nb-no
ms.lasthandoff: 10/10/2017

---

# <a name="ship-an-order-from-a-different-store"></a>Sende en ordre fra en annen butikk

Med sendefunksjonen Tillegg i Dynamics 365 for Retail kan kundeordrer registreres i én butikk og sendes fra en annen butikk. Kundeordrer i salgsstedsklienten støtter flere fullføringsalternativer. Eksempler på fullføringsalternativer:
-   Henting fra samme butikk på en annen dato.
-   Henting fra en annen butikk på samme eller en annen dato.
-   Sending fra standard leveringslager som er tilordnet til butikken, og levering på en bestemt dato.

Sendefunksjonen Tillegg bruker følgende POS-operasjoner: Lever alle produkter og lever valgte produkter. Dette lar butikkbetjeningen velge "send fra"-lokasjon som ordren eller ordrelinjen kan fullføres fra. Som standard er "send fra"-lokasjonen leveringslageret som er tilknyttet butikken. Butikkbetjeningen kan imidlertid endre denne lokasjonen og velge alle butikker som er definert i butikklokatorgruppen som er tilordnet butikken. 

Muligheten til å velge "send til"-adresser forblir uendret. 

Leveringsmetodene som kan brukes til å tilfredsstille ordrelinjen, er basert på konfigurasjonen av gyldig leveringsmåter for produkter og adresser. Fordi reglene om gyldig av leveringsmåter vedlikeholdes i Detaljhandel hovedkontor, utfører POS-klienten kall i sanntid for å hente de gyldige leveringsmåtene for en leveringslinje. 


