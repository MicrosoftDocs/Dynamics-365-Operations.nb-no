---
title: Sende ordrer fra et annet lager ved hjelp av sendefunksjonen Tillegg
description: Dette emnet beskriver sendefunksjonen Tillegg.
author: ashishmsft
ms.date: 10/10/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2017-10-10
ms.dyn365.ops.version: Retail July 2017 update
ms.openlocfilehash: b9e0c4f55fd823bf7471edfe6ce1d424b0179d21
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5800477"
---
# <a name="ship-orders-from-another-store-by-using-the-charge-send-feature"></a>Sende ordrer fra et annet lager ved hjelp av sendefunksjonen Tillegg

[!include [banner](includes/banner.md)]

Med sendefunksjonen Tillegg i Commerce kan kundeordrer registreres i én butikk og sendes fra en annen butikk.

Kundeordrer i salgsstedsklienten støtter flere fullføringsalternativer. Eksempler på fullføringsalternativer:

- Henting fra samme butikk på en annen dato.
- Henting fra en annen butikk på samme eller en annen dato.
- Sending fra standard leveringslager som er tilordnet til butikken, og levering på en bestemt dato.

Sendefunksjonen Tillegg bruker følgende POS-operasjoner: Lever alle produkter og lever valgte produkter. Dette lar butikkbetjeningen velge "send fra"-lokasjon som ordren eller ordrelinjen kan fullføres fra. Som standard er "send fra"-lokasjonen leveringslageret som er tilknyttet butikken. Butikkbetjeningen kan imidlertid endre denne lokasjonen og velge alle butikker som er definert i butikklokatorgruppen som er tilordnet butikken.

Muligheten til å velge "send til"-adresser forblir uendret.

Leveringsmetodene som kan brukes til å tilfredsstille ordrelinjen, er basert på konfigurasjonen av gyldig leveringsmåter for produkter og adresser. Fordi reglene om gyldig av leveringsmåter vedlikeholdes i hovedkontoret, utfører POS-klienten kall i sanntid for å hente de gyldige leveringsmåtene for en leveringslinje.


[!INCLUDE[footer-include](../includes/footer-banner.md)]