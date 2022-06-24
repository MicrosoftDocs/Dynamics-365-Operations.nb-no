---
title: Sende ordrer fra et annet lager ved hjelp av sendefunksjonen Tillegg
description: Denne artikkelen beskriver sendefunksjonen Tillegg.
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
ms.openlocfilehash: d73a21bfe9a284bd6e222e73bb0250648912b230
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8863519"
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