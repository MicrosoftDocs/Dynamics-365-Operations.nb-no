---
title: Definere en arbeidsmal for bestillinger
description: Denne artikkelen beskriver hvordan du definerer en enkel arbeidsmal som skal brukes når du plasserer mottatte varer.
author: Mirzaab
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WHSWorkTemplateTable, SysQueryForm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ee6bc896a979c326001e1596e4a463753005fabf
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8877370"
---
# <a name="set-up-a-work-template-for-purchase-orders"></a>Definere en arbeidsmal for bestillinger

[!include [banner](../../includes/banner.md)]

Denne artikkelen beskriver hvordan du definerer en enkel arbeidsmal som skal brukes når du plasserer mottatte varer. Arbeidsmaler bestemmer settet med instruksjoner som presenteres for lagermedarbeideren på en mobil enhet når de flytter varer fra mottaksområdet. Du kan bruke denne fremgangsmåten med data som er nevnt i demonstrasjonsdataselskapet USMF. Før du starter denne veiledningen kan du opprette en arbeidspulje-ID. I dette eksemplet brukes en arbeidpulje-ID kalt Innkommende. Denne fremgangsmåten er ment for lagersjef.

1. I navigasjonsruten går du til **Moduler > Lagerstyring > Oppsett > Arbeid > Arbeidsmaler**.
2. Velg **Bestillinger** i feltet **Arbeidsordretype**.

## <a name="create-a-work-template-header"></a>Opprette et arbeidsmalhode
1. Velg **Ny**.
2. Angi et nummer i **Sekvensnummer**-feltet. Dette er sekvensen der arbeidsmalene blir evaluert. Du kan endre rekkefølgen om nødvendig.  
3. Angi en verdi i feltet **Arbeidsmal**. Dette er den unike identifikatoren for denne malen.  
4. Skriv inn en verdi i feltet **Beskrivelse av arbeidsmal**.
    - Alternativet **Gyldig** kontrolleres ikke før du har fullført all informasjonen som kreves av malen og deretter har valgt **Lagre**.  
    - En arbeidsordre av typen **Bestilling** kan ikke kan behandles automatisk, så la alternativet **Behandle automatisk** være satt til **Nei**.  
5. Skriv inn en verdi i feltet **ID for arbeidsutvalg**. Arbeidspulje-ID-er gir deg muligheten til å organisere arbeidet i grupper. Verdien du angir her, blir standardverdien for arbeid som opprettes med denne malen.  
6. I **Arbeidsprioritet**-feltet angir du `1`. Dette indikerer viktigheten av arbeidet, og verdien du angir her, blir standard for alt arbeid som er opprettet ved hjelp av denne malen.  
7. Velg **Lagre**. Du må lagre arbeidsmalhodet før knappen **Rediger spørring** blir tilgjengelig.  

## <a name="set-up-the-query-for-the-work-template"></a>Konfigurere spørringen for arbeidsmalen
1. Velg **Rediger spørring**. Vi vil angi en begrensning slik at malen bare kan brukes i et bestemt lager.  
2. Velg **Legg til**.
3. Skriv inn `warehouse` i **Felt**-feltet i den nye raden.
4. Skriv inn en verdi i **Kriterier**-feltet.
5. Velg **OK**.
6. Velg **Ja**.

## <a name="set-work-template-details"></a>Angi arbeidsmaldetaljer
1. Velg **Ny**.
2. Velg **Plukk** i **Arbeidstype**-feltet.
3. Skriv inn `purchase` i feltet **Arbeidsklasse-ID**. Arbeidsklassen som du angir her, blir standard på alle arbeidslinjer av typen Plukk som opprettes ved hjelp av denne malen. Arbeidsklassen kan ikke overskrives fra arbeidsordrelinjene. Arbeidsklasser brukes til å styre og/eller begrense typen arbeidsordrelinjer som en lagermedarbeider kan behandle på en mobilenhet.  
4. Velg **Ny**.
5. Velg **Plasser** i **Arbeidstype**-feltet.
6. Skriv inn en verdi i feltet **Arbeidsklasse-ID**. Instruksjoner for plukking og plassering er et sett. Hvert plukk/plasser-sett må ha samme arbeidsklasse. Bruk samme arbeidsklasse som du har angitt for plukkinstruksjonen.  
7. Velg **Lagre**. Legg merke til at det nå merket av for **Gyldig**.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]