---
title: Problemer med dataavstemming av en Z-rapport
description: Denne artikkelen beskriver problemer som brukere kan oppleve med dataavstemming av en Z-rapport i Commerce headquarters. Den beskriver også mulige rotårsaker og løsninger som kan forhindre fremtidige tilfeller.
author: Shajain
ms.date: 12/06/2022
ms.topic: Troubleshooting
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: shajain
ms.search.validFrom: 2021-01-31
ms.openlocfilehash: 9803134c4c77233e565525e96fd82af293d4c829
ms.sourcegitcommit: 0c927fcb3afd34d870391f05b5393a4673d916e5
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/08/2022
ms.locfileid: "9832135"
---
# <a name="issues-with-the-data-reconciliation-of-a-z-report"></a>Problemer med dataavstemming av en Z-rapport

[!include [banner](../../includes/banner.md)]

Denne artikkelen inneholder feilsøkingsveiledning som kan hjelpe deg hvis du oppdager problemer med dataavstemming av en Z-rapport i Microsoft Dynamics 365 Commerce headquarters. Den beskriver problemer som brukere kan oppleve med dataavstemming, mulige rotårsaker og løsninger som kan forhindre fremtidige forekomster.

## <a name="description"></a>Beskrivelse

- Det er en uoverensstemmelse mellom beløpene som vises i Z-rapporten og totalene som vises på det beregnede utdraget.
- Transaksjonen i headquarters har feil antall linjeelementer, eller det er en uoverensstemmelse mellom linjetotalen og totalen for transaksjonen.
- Antallet transaksjoner som vises i et skift i headquarters, er mindre enn antall transaksjoner i Z-rapporten.
- Utdragspostering mislyktes av en av de forrige årsakene.

### <a name="root-cause"></a>Rotårsak

Den vanligste rotårsaken til symptomene som beskrives tidligere, er genereringen av dupliserte transaksjons-ID-er i kanaldatabasen. Dupliserte transaksjons-ID-er kan genereres av følgende årsaker:

- Den lokale databaselagringen av Modern Point of Sale (MPOS) er ødelagt.
- MPOS har noen transaksjoner i frakoblet modus, og aktiveres på nytt ved å bruke en konto som ikke har tilgang til den frakoblede databasen.
- Det er et problem med tilpasning som er knyttet til genereringen av transaksjons-ID-er.

## <a name="resolution"></a>Løsning

Vanligvis er Commerce avhengig av en nummerserie for å generere sekvensielle transaksjons-ID-er. Hvis systemet ikke kan fastslå at en nummerserie ble bruk av en hvilken som helst årsak, genereres en duplisert transaksjons-ID. 

Hvis du vil korrigere problemet med duplisert transaksjons-ID, oppretter du en støtteforespørsel for å kontrollere om transaksjonsdataene kan korrigeres. I noen tilfeller, for eksempel når det ikke er tap av data i headquarters, er det ikke mulig eller nødvendig å korrigere data.

For å forhindre dette problemet i fremtiden må du aktivere **Aktiver ny transaksjons-ID for å unngå dupliserte transaksjons-ID-er** i headquarters. Denne funksjonen ble innført i Commerce versjon 10.0.19. Det forhindrer at det opprettes sekvensielle transaksjons-ID-er ved å sørge for at det opprettes en unik transaksjons-ID for hver transaksjon. Hvis du vil ha mer informasjon om denne funksjonen, kan du se [Forhindre dupliserte transaksjons-ID-er](../channel-setup-retail.md#ensure-unique-transaction-ids).
