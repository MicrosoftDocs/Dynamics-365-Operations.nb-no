---
title: Forbedringer for kontanttransaksjoner
description: Dette emnet beskriver forbredringer for kontanttransaksjoner i POS for Dynamics 365 Commerce.
author: anpurush
ms.date: 05/21/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-05-21
ms.dyn365.ops.version: ''
ms.openlocfilehash: f878f39e8e9913edbe1da192e199090139a88adb6b7ed9a1e9b779c5748171b5
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6735660"
---
# <a name="cash-management-improvements"></a>Forbedringer for kontanttransaksjoner

[!include [banner](includes/banner.md)]


Kontanttransaksjoner er en nøkkelfunksjon for forhandlere i fysiske butikker. Forhandlere vil at butikkene skal ha systemer som kan hjelpe dem med å gi fullstendig sporing og ansvarlighet for kontanter og bevegelsen på tvers av de forskjellige kassene og kassererne i en butikk. De må kunne avstemme eventuelle forskjeller og bestemme ansvarlighet.


Microsoft Dynamics 365 Commerce har kontanttransaksjonsfunksjoner i salgsstedsapplikasjonen. I versjoner av Retail som er tidligere enn versjon 10.0.3, er imidlertid ikke kontanttransaksjonsfunksjonaliteten robust nok til å gi fullstendig sporing av kontantbevegelser i butikker. Selv om forhandlere kan avstemme kontanter for en butikk, kan de ikke nøyaktig bestemme ansvarlighet ved kontantavvik.


I Retail-versjon 10.0.3 og nyere vil forhandlerne oppnå sporinger for kontanthåndtering. Som en del av denne sporingen vil forhandlere kunne angi safer, foreta tosidige kontanttransaksjoner og avstemme kontantstyringstransaksjoner.

## <a name="set-up-traceability-and-define-safes"></a>Konfigurere sporingen og angi safer

For å definere den nye kontantstyringsfunksjonaliteten følger du denne fremgangsmåten for å konfigurere funksjonalitetsprofilen for butikker.

1. Gå til **Retail og Commerce \> Kanaloppsett \> Salgsstedsoppsett \> Salgsstedsprofiler \> Funksjonsprofiler**, og velg en funksjonalitetsprofil som er knyttet til butikkene der du vil gjøre endringene for kassastyring tilgjengelig.
2. I hurtigfanen **Funksjoner** i funksjonalitetsprofilen, under **Avansert kassastyring**, setter du **Aktiver sporing av kontanter** til **Ja**.
3. For å angi safer, gå til **Retail og Commerce \> Kanaler \> Butikker** \> Alle butikker, og velg en butikk.
4. På **Butikker**-siden, i handlingsruten i kategorien **Oppsett** i gruppen **Oppsett**, velg **Safer**. Ved hjelp av dette alternativet kan du definere og vedlikeholde flere safer for en butikk.
4. Før funksjonaliteten kan brukes må du kjøre distribusjonsplanjobben **1070-kanalkonfigurasjon** for å synkronisere disse konfigurasjonene med kanaldatabasen.

## <a name="additional-cash-management-changes"></a>Flere kontantstyringsendringer

I Retail versjon 10.0.3 og senere er følgende funksjoner knyttet til kontanttransaksjoner også tilgjengelige:

- En bruker som blir bedt om å angi "rapporter startbeløp", må oppgi kontantkilden. Brukeren kan søke etter de tilgjengelige safene som er definert i butikken, og velge safen som kontantene tas ut av, slik at de kan settes inn i kassen.
- En bruker som utfører operasjonen "fjerning av betalingsmidler", blir bedt om å velge, i en liste over åpne "flytoppføring"-transaksjoner, transaksjonen som operasjonen utføres mot. Hvis den tilsvarende flytoppføringen ikke finnes i systemet, kan brukeren opprette en transaksjon for ikke-koblet betalingsmiddelfjerning.
- En "flytoppføringen"-operasjon ber en bruker om å velge, i en liste over åpne "fjerning av betalingsmidler"-transaksjoner, transaksjonen som flytoppføringen utføres mot. Hvis den tilsvarende betalingsmiddelfjerningen ikke finnes i systemet, kan brukeren opprette en transaksjon for ikke-koblet flytoppføring.
- En bruker som foretar en "deponering til safe", blir bedt om å velge safen hvor kontanter skal deponeres.
- For safer som er definert i en butikk, kan brukere administrere operasjoner som å angi startbeløp, gjøre en flytoppføring, foreta en betalingsmiddelfjerning og gjøre en bankdeponering.
- For brukere som har riktige brukerrettigheter, viser "behandle skift"-operasjonene kontantsaldoene for aktive, deaktiverte og blinde, usporede skift.
- Hvis du vil avstemme kontanttransaksjoner innen et skift eller på tvers av skift, velger du skift for å avstemme og deretter **Avstem**. Visningen som åpnes, viser listen over avstemte og ikke-avstemte transaksjoner i separate kategorier. Fra denne visningen kan brukere enten velge ikke-avstemte transaksjoner og avstemme dem, eller velge tidligere avstemte transaksjoner og fjerne avstemmingen av dem.
- Hvis den valgte transaksjonen ikke balanseres under avstemming, må brukeren angi en beskrivelse av årsaken til at den ikke er avstemt. Brukere kan velge en enkelttransaksjon og avstemme den mot relevant årsaksbeskrivelse.
- Brukere kan fortsette å avstemme og fjerne avstemming av transaksjoner til skiftet er lukket. Når et skift er lukket, kan ikke transaksjonene være uavstemt.
- Når en bruker velger å lukke et skift, validerer Commerce at det ikke er noen uavstemte kontantstyringstransaksjoner i skiftet. Brukere kan ikke lukke et skift hvis det finnes uavstemte transaksjoner.


[!INCLUDE[footer-include](../includes/footer-banner.md)]