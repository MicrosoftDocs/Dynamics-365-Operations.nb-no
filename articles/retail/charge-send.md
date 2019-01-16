---
title: Sende ordrer fra et annet lager ved hjelp av sendefunksjonen Tillegg
description: Dette emnet beskriver sendefunksjonen Tillegg.
author: ashishmsft
manager: AnnBe
ms.date: 10/10/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2017-10-10
ms.dyn365.ops.version: Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 190d0b59ad2e232b33b3c0d1700cbaf95c45aeca
ms.openlocfilehash: e5351086c56d13ef98937aec066be00cdf88fd37
ms.contentlocale: nb-no
ms.lasthandoff: 01/04/2019

---

# <a name="ship-orders-from-another-store-by-using-the-charge-send-feature"></a>Sende ordrer fra et annet lager ved hjelp av sendefunksjonen Tillegg

[!include [banner](includes/banner.md)]

Med sendefunksjonen Tillegg i Dynamics 365 for Retail kan kundeordrer registreres i én butikk og sendes fra en annen butikk.

Kundeordrer i salgsstedsklienten støtter flere fullføringsalternativer. Eksempler på fullføringsalternativer:

- Henting fra samme butikk på en annen dato.
- Henting fra en annen butikk på samme eller en annen dato.
- Sending fra standard leveringslager som er tilordnet til butikken, og levering på en bestemt dato.

Sendefunksjonen Tillegg bruker følgende POS-operasjoner: Lever alle produkter og lever valgte produkter. Dette lar butikkbetjeningen velge "send fra"-lokasjon som ordren eller ordrelinjen kan fullføres fra. Som standard er "send fra"-lokasjonen leveringslageret som er tilknyttet butikken. Butikkbetjeningen kan imidlertid endre denne lokasjonen og velge alle butikker som er definert i butikklokatorgruppen som er tilordnet butikken.

Muligheten til å velge "send til"-adresser forblir uendret.

Leveringsmetodene som kan brukes til å tilfredsstille ordrelinjen, er basert på konfigurasjonen av gyldig leveringsmåter for produkter og adresser. Fordi reglene om gyldig av leveringsmåter vedlikeholdes i Detaljhandel hovedkontor, utfører POS-klienten kall i sanntid for å hente de gyldige leveringsmåtene for en leveringslinje.

