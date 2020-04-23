---
title: Leverandørforespørselskonfigurasjoner
description: Dette emnet beskriver feltene som må fylles ut i en ny leverandørforespørsel.
author: mkirknel
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendProspectiveVendorRegistrationConfig
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2017-12-31
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: d78aa7c14ed2a2a5097f6f80c946c6ae4ed8bb94
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/02/2020
ms.locfileid: "3208092"
---
# <a name="vendor-request-configurations"></a>Leverandørforespørselskonfigurasjoner
[!include [banner](../includes/banner.md)]

For å fullføre en leverandørforespørsel må en kontaktperson for leverandøren fullføre veiviseren for registrering av potensiell leverandør.

I skjemaet **Leverandørforespørselskonfigurasjoner** kan du opprette profiler som angir obligatoriske felt og synlige felt i veiviseren for registrering av potensiell leverandør.

Registreringsveiviseren for leverandører starter ved å spørre den potensielle leverandørbruker om hvilket land/region som leverandøren gjør forretninger i. Denne informasjonen bestemmer den aktuelle konfigurasjonen. Hvis ingen bestemt konfigurasjon er definert for et land/region, brukes en standardkonfigurasjon.

### <a name="set-up-a-vendor-request-configuration"></a>Definere en konfigurasjon av leverandørforespørsel

Som standard finnes det en leverandørkonfigurasjon i skjemaet Leverandørforespørselskonfigurasjoner.

Det er ikke mulig å velge land/regioner for standardkonfigurasjonen, så delen **Land/regioner** kan ikke endres.

1. Klikk **Innkjøp og leverandører** > **Oppsett** > **Leverandører**, og klikk deretter på **Leverandørforespørselskonfigurasjoner**.
2. Klikk på **Felt**-fanen for å sette statusen til de oppførte feltene.
3. Skjult (ikke synlige)
4. Vises (synlige, men ikke obligatoriske)
5. Obligatorisk (synlig og obligatorisk)
6. Klikk på **Innhold**-fanen for å angi om teksten skal vises i veiviseren, og om det skal være en bekreftelse som den potensielle leverandørbrukeren må godta før neste trinn i veiviseren. Det vil bli bedt om bekreftelse for alle vilkårene som brukeren må godta for å fortsette.

Du kan også angi en bekreftelsesmelding som skal vises når veiviseren er ferdig, og du kan legge til ett eller flere spørreskjemaer.

### <a name="create-a-vendor-configuration-for-a-specific-countryregion"></a>Opprette en leverandørkonfigurasjon for et bestemt land/område
1.  Klikk **Innkjøp og leverandører** > **Oppsett** > **Leverandører**, og klikk deretter på **Leverandørforespørselskonfigurasjoner**.
2.  Klikk på **Ny** for å opprette en ny konfigurasjon, og angi et navn for konfigurasjonen.
3.  Klikk **Lagre**.
4.  Åpne fanen **Land/regioner** for å velge landet/regionen som skal brukes for konfigurasjonen.
5.  Fullfør konfigurasjonen ved å følge retningslinjene for standardkonfigurasjonen.

