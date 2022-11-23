---
title: Importer datterselskapsdata fra filer
description: Denne artikkelen beskriver hvordan du klargjør data fra eksterne systemer, slik at de kan importeres til Microsoft Dynamics 365 Finance.
author: jinniew
ms.date: 10/09/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2020-12-01
ms.dyn365.ops.version: 8.0.1
ms.openlocfilehash: 494f6396d5e6fab6fef9404ad473566b02b1b9ab
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/16/2022
ms.locfileid: "9780103"
---
# <a name="import-subsidiary-data-from-files"></a>Importer datterselskapsdata fra filer

[!include [banner](../includes/banner.md)]

Denne artikkelen beskriver hvordan du klargjør data fra eksterne systemer, slik at de kan importeres til Microsoft Dynamics 365 Finance. Du bruker siden **Konsolider med import** (**Konsolideringer \> Konsolider med import**) til å forberede overføringen av data for datterselskap fra eksterne systemer.

1. Opprett en juridisk enhet for datterselskap for konsolideringen. Hvis du vil ha informasjon om hvordan du oppretter juridiske enheter, kan du se [Opprette en juridisk enhet](../../fin-ops-core/fin-ops/organization-administration/tasks/create-legal-entity.md). Hvis du vil ha mer informasjon, kan du se [Klargjøre en juridisk enhet for bruk i konsolideringsprosessen](prepare-company-for-consolidation.md), og [Definere en juridisk enhet for datterselskap for konsolidering](set-up-subsidiary-company-for-consolidation.md).

2. Klargjør en fil som skal inneholde dataene som importeres. Hvis du vil ha mer informasjon om importprosessen, se [Oversikt over dataimport- og -eksportjobber](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md).
3. Eksporter data til en fil ved å følge trinnene i fremgangsmåten "Prosess for dataimport/-eksport" i [Oversikt over dataimport- og -eksportjobber](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md). Du kan bruke denne fremgangsmåten til å konsolidere data fra en annen forekomst av Dynamics 365 Finance eller fra Dynamics 365 Business Central. Hvis du importerer data fra eksterne systemer, må data være i formatet som beskrives under [Eksportere datterselskapdata til filer](export-subsidiary-data-to-file.md).
4. Gå til **Konsolideringer \> Konsolider med import**. På siden **Konsolider med import**, i kategorien **Vilkår**, angir du detaljene av rapporten og/eller importen ved å angi følgende felt.

| Felt                                 | Verdi for rapporten | Verdi for importen |
|---------------------------------------|----------------------|----------------------|
| **beskrivelse**                      | Gjelder ikke | Angi en beskrivelse for å identifisere importen. |
| **Hovedkonto**    | Definer kontoområdet som rapporten skal inkludere. Hvis du ikke definerer et område, blir alle kontoene tatt med. | Definer kontoområdet som importen skal inkludere. Hvis du ikke definerer et område, blir alle kontoene tatt med. |
    | **Konsolideringsperiode**                  | Definer datoområdet som skal konsolideres. | Definer datoområdet som skal konsolideres. |
    | **Inkluder faktiske beløp**                | Sett dette alternativet til **Ja** for å inkludere faktiske data. | Sett dette alternativet til **Ja** for å inkludere faktiske data. |
| **Inkluder budsjettbeløp** | Sett dette alternativet til **Ja** for å inkludere budsjettbeløp i konsolideringer. | Sett dette alternativet til **Ja** for å inkludere budsjettbeløp i konsolideringer. |
| **Bygge saldoer på nytt i løpet av konsolidering** | Sett dette alternativet til **Ja** hvis gjenoppbyggingsprosessen skal fjerne saldoen og nye poster helt, og opprett saldoen på nytt fra starten. | Sett dette alternativet til **Ja** hvis gjenoppbyggingsprosessen skal fjerne saldoen og nye poster helt, og opprett saldoen på nytt fra starten. |
| **Budsjettmodeller**                         | Gjelder ikke | Hvis du har valgt å importere budsjettbeløp, kan du angi budsjettmodellene som skal konsolideres. |
    | **Budsjettsatstype**                      | Gjelder ikke | Angi typen budsjettvalutakurs. |

6. Hvis du har andre regnskapsvalutaer, bruker du feltene i kategorien **Valutaveksling** til å konfigurere oversettelsen som gjøres i løpet av konsolidering.

    | Felt                      | beskrivelse |
    |----------------------------|-------------|
 | **Kilde for juridisk enhet**        | Velg den juridiske enheten du importerer fra. |
 | **Regnskapsvaluta for kilde** | Denne standardvalutaen er valutaen som er knyttet til den juridiske kildeenheten du valgte i feltet **Kilde for juridisk enhet**. |
 | **Fra**- og **Til-kontoer**       | Definer kontointervallet som skal importeres fra den juridiske kildeenheten. |
    | **Valutakurstype**         | Velg valutakurstype. Valutakurstyper tilordnes når du oppretter en hovedkonto. Hvis du vil ha mer informasjon, kan du se [Opprette en hovedkonto](tasks/create-main-account.md). |
| **Bruk valutakurs fra**   | Angi en dato for å bruke valutakursen som gjelder på denne datoen. Du kan eventuelt angi verdien som skal brukes som valutakurs. |
| **Valutakurs**  | Standardverdien avhenger av typen valutakurs som du valgte i feltet **Type valutakurs**. Hvis du har angitt en brukerdefinert valutakurs, kan du definere en kurs. |

7. Angi alternativet **Kjør i bakgrunnen** til **Ja** for å gjøre det mulig å kjøre importprosessen i bakgrunnen.
8. Sett alternativet **Satsvis behandling** til **Ja** for å kjøre konsolideringen som en satsvis jobb på et bestemt tidspunkt. Hvis du vil kjøre konsolideringen umiddelbart, velger du **OK**. 

Transaksjonene og saldoene som ble angitt for konsolidering i datterselskapene, blir lagt til de aktuelle kontoene i den konsoliderte juridiske enheten.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
