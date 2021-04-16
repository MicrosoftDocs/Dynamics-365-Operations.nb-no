---
title: Eksportere data for et datterselskap til filer
description: Dette emnet beskriver hvordan du forbereder å eksportere data fra Microsoft Dynamics 365 Finance og deretter importerer dem til en konsolidert juridisk enhet.
author: jinniew
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2018-5-31
ms.dyn365.ops.version: 8.0.1
ms.openlocfilehash: bae0a28c59f327e47378eef6392d5e304bbde9a8
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5826184"
---
# <a name="export-subsidiary-data-to-files"></a>Eksportere data for et datterselskap til filer

[!include [banner](../includes/banner.md)]

Du bruker siden **Eksport** (**Systemadministrasjon \> Arbeidsområder \> Importer/Eksporter**) til å forberede eksport av data fra datterselskapene til filer som deretter kan importeres til en konsolidert juridisk enhet. Hvis du vil ha mer informasjon om import- og eksportprosesser, se [Oversikt over dataimport- og -eksportjobber](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md).

1. Opprette en juridisk enhet for konsolideringsprosessen. Hvis du vil ha informasjon om hvordan du oppretter juridiske enheter, kan du se [Opprette en juridisk enhet](../../fin-ops-core/fin-ops/organization-administration/tasks/create-legal-entity.md). Hvis du vil ha mer informasjon, kan du se [Klargjøre en juridisk enhet for bruk i konsolideringsprosessen](prepare-company-for-consolidation.md), og [Definere en juridisk enhet for datterselskap for konsolidering](set-up-subsidiary-company-for-consolidation.md). 

2. Gå til **Konsolideringer \> Eksport av firmasaldoer**. På siden **Eksport av firmasaldoer**, i kategorien **Vilkår**, angir du detaljene for konsolideringen ved å angi følgende felt.

    | Felt                             | beskrivelse |
    |-----------------------------------|-------|
    | Hovedkonto                      | Angi kontoene som skal konsolideres. Hvis du vil inkludere alle kontoene, lar du dette feltet stå tomt. |
    | Bruke konsolideringskonto         | Hvis du har angitt konsolideringskontoer, setter du dette alternativet til **Ja**. |
    | Velg konsernkonto fra | Velg enten **Hovedkonto** eller **Konsolideringskontogruppe**. |
    | Konsernkontogruppe       | Velg en konsolideringskontogruppe for konsolideringskontoen som du valgte. |
    | Konsolideringsperiode              | Angi "fra"- og "til"-datoer for konsolideringen. |
    | Inkluder faktiske beløp            | Sett dette alternativet til **Ja** for å inkludere faktiske beløp. |
    | Inkluder budsjettbeløp            | Sett dette alternativet til **Ja** for å inkludere budsjettbeløp i konsolideringer. |
    | Budsjettmodeller                     | Angi budsjettmodellen som skal tas med. |

3. Angi detaljene for konsolideringen i kategorien **Finansdimensjoner**:

    - Angi finansdimensjonsinformasjonen som skal overføres fra transaksjonene i kontoene i datterselskapet, til transaksjonene i den konsoliderte juridiske enheten.
    - Velg finansdimensjonene i listen.
    - Identifiser riktig spesifikasjon for hver finansdimensjon som konsolideres. De tilgjengelige alternativene er **Dimensjon**, **Gruppedimensjon**, **Firmakontoer** og **Konto**.

        > [!NOTE]
        > Med alternativet for **Gruppedimensjon** kan du definere dimensjonsverdien som brukes av gruppen med firmaer som konsolideres.

    - Angi segmentrekkefølgen du vil konsolidere i.

4. I kategorien **Juridiske enheter** følger du disse trinnene for å angi den juridiske enheten du eksporterer:

    1. Velg **Ny**.
    2. I feltet **Kilde for juridisk enhet** angir du den juridiske enheten.

        Hvis de samme kriteriene gjelder for flere datterselskaper som er i samme databaser, kan du overføre data fra disse datterselskapene til separate eksportfiler i én enkelt operasjon.

        1. Opprett en linje for hver juridiske enhet for datterselskap med kontoer som skal eksporteres til filer. Disse filene vil senere bli importert til den konsoliderte juridiske enheten.
        2. Angi navnet på selskapet og navnet på eksportfilen som opprettes under eksportprosessen, for hvert datterselskap.

    3. I feltet **Kontotypen for konverteringsavvik** velger du **Resultat** eller **Balanse**.
    4. Angi et filnavn for eksportfilen som skal opprettes.

5. Velg **OK** for å kjøre eksporten.

Når eksporten er fullført, får du en melding som viser hvor mange poster som ble lagret i hver fil. Du kan deretter importere filene til den konsoliderte juridiske enheten.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]