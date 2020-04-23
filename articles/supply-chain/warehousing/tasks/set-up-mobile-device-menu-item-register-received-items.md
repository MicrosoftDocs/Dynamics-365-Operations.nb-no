---
title: Definere et menyelement for mobilenhet for å registrere mottatte varer
description: Dette emnet fokuserer på oppsettet for et menyelement for mobil enhet.
author: ShylaThompson
manager: tfehr
ms.date: 08/16/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFMenuItem, WHSRFMenu
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 146eb0822566a9bae59d486e39c8227938eb2375
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/02/2020
ms.locfileid: "3216856"
---
# <a name="set-up-a-mobile-device-menu-item-to-register-received-items"></a>Definere et menyelement for mobilenhet for å registrere mottatte varer

[!include [banner](../../includes/banner.md)]

Dette emnet fokuserer på oppsettet for et menyelement for mobil enhet. Dette menyelementet brukes til registrering av mottak av varer som er bestilt via bestillinger. 

Du kan bruke denne veiledningen i USMF-demodatafirmaet. Denne fremgangsmåten er ment for lagersjef.


## <a name="create-a-mobile-device-menu-item"></a>Opprette et menyelement for mobilenhet
1. I navigasjonsruten går du til **Moduler > Lagerstyring > Oppsett > Mobilenhet > Menyelementer på mobilenheten**.
2. Velg **Ny**.
3. Skriv inn en verdi i feltet **Menyelementnavn**. Dette er den unike identifikatoren for dette menyelementet for mobil enhet. Du kan for eksempel skrive inn `My PO registration`.  
4. Skriv inn en verdi i **Tittel**-feltet. Dette er tittelen som skal vises for brukeren på den mobile enheten. Du kan for eksempel skrive inn `PO registration`.  
5. Velg **Arbeid** i feltet **Modus**. Registrering av lagerbeholdningsantall mottatt for en bestillingslinje oppretter arbeid for å flytte varene fra mottaksområdet til lageret. Arbeid opprettes ikke før varene er registrert. La derfor alternativet **Bruk eksisterende arbeid** være satt til **Nei**.
6. Velg **Mottak av bestillingsvare** i feltet **Arbeidsopprettelsesprosess** i delen **Generelt**.
    - En bestillingslinje må identifiseres unikt før beholdningen kan registreres i lageret. I dette scenarioet registrerer mobilenheten bestillingsnummeret og varenummeret, og det gjør at systemet kan identifisere bestillingslinjen. Plasseringsarbeidet blir opprettet og kan plukkes opp en annen arbeider. Arbeidsopprettingsmetoden du velger, bestemmer hvilke felt som blir tilgjengelige i hurtigkategorien **Generelt**.  
    - Hvis du velger alternativet **Bruk standarddata**, aktiveres knappen **Standarddata**. Her kan du velge felt for å vise data som en arbeider vanligvis trenger i arbeidet, slik at disse verdiene vises på den mobile enheten.  
    - Parameteren **Gruppering av nummerskilt** fungerer sammen med sekvensgruppe for enhet som er tilordnet til varen som blir mottatt. Du kan angi om mottak av mindre enn eller flere enn én pall skal grupperes i ett nummerskilt eller deles inn i et eget nummerskilt for hver enhet.  
    - Hvis du velger alternativet **Generer nummerskilt**, genereres et unikt nummerskilt basert på valget av nummerserie.  
    - Du kan velge malen som skal brukes når arbeid opprettes. Hvis du for eksempel registrerer en vare for en bestilling, blir plasseringsarbeidet generert basert på arbeidsmalen. Hvis du ikke velger arbeidsmal her, vil systemet tilordne en mal basert på spørringskriteriene som er knyttet til malene.  
    - Hvis disposisjonskoder vises på den mobile enheten, kan arbeidere evaluere statusen eller kvaliteten på varene, og velge den aktuelle koden. Reglene for disposisjonskoden bestemmer om varene blir tilgjengelige for andre lagerprosesser. Reglene bestemmer også hvilket lokasjonsdirektiv som brukes for arbeid som er opprettet.   
    - Hvis du velger alternativet **Partidisposisjonskoder,** kan arbeidere evaluere statusen eller kvaliteten på et parti, og velge den aktuelle disposisjonskoden. Reglene som angis for partidisposisjonskoden, bestemmer om partiet blir tilgjengelig for andre lagerprosesser.  
    - Hvis du velger alternativet **Skriv ut etiketter**, vil en nummerskiltetikett bli skrevet ut automatisk når varene mottas.  
7. Velg **Lagre**.
8. Lukk siden.

## <a name="add-the-menu-item-to-a-mobile-device-menu"></a>Legge til menyelementet på en meny for mobilenhet
1. I navigasjonsruten går du til **Moduler > Lagerstyring > Oppsett > Mobilenhet > Meny på mobilenheten**.
2. Bruk **hurtigfilteret** til å filtrere på **Navn**-feltet med en verdi lik `inbound`.
3. Velg **Rediger**.
4. Velg menyelementet som du har opprettet før, i treet med tilgjengelige menyer og elementer.
5. Velg pilen som peker mot høyre.
6. Velg **Lagre**.
7. Lukk siden.

