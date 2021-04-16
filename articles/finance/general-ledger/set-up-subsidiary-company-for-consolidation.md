---
title: Definere en juridisk enhet for datterselskap for konsolidering
description: Dette emnet beskriver hvordan du arbeider med kontoplaner for konsolideringsfirmaer.
author: jinniew
ms.date: 10/30/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2020-10-31
ms.dyn365.ops.version: 8.0.1
ms.openlocfilehash: 15050310f355ece683b00a00be9552d32aded17b
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5832856"
---
# <a name="set-up-a-subsidiary-legal-entity-for-consolidation"></a>Definere en juridisk enhet for datterselskap for konsolidering

[!include [banner](../includes/banner.md)]

Metoden du bruker for å forberede underordnede kontoer for konsolidering, er delvis avhengig av i hvilken grad strukturen i kontoplanen i den underordnede juridiske enheten reflekterer kontoplanen i den konsoliderte juridiske enheten.

Før du begynner en konsolidering som del av en periodeavslutning, må du utføre de forberedende aktivitetene for periodeavslutningen, men ikke avslutte underkontoene før konsolideringen er fullført. Hvis du vil ha mer informasjon om periodeavslutning, kan du se [Lukke økonomimodulen ved periodeslutt](close-general-ledger-at-period-end.md) og [Avslutte regnskapsåret](tasks/close-fiscal-year.md).

> [!NOTE]
>  Vi anbefaler at du bruker Management Reporter for Microsoft Dynamics 365 Finance til å kombinere de økonomiske resultatene for flere juridiske enheter i et konsolidert format. Management Reporter lar deg opprette konsoliderte finansrapporter på tvers av juridiske enheter, bruke Excel til å importere konsolideringsdata fra andre kilder og omsette beløp til et hvilket som helst antall rapporteringsvalutaer uten å måtte kjøre konsolideringsprosessen i Dynamics 365 Finance.

## <a name="map-subsidiary-main-accounts-to-consolidated-main-accounts"></a>Tilordne underordnede hovedkontoer til konsoliderte hovedkontoer

Hvis den kontoplanen i den underordnede juridiske enheten ikke følger kontoplanen i den konsoliderte juridiske enheten, kan du tilordne hovedkontoene i den underordnede til hovedkontoene i den konsoliderte juridiske enheten.

1. I den *juridiske enheten* går du til **Økonomimodul \> Oppsett** \> **Kontoplan \> Kontoplan**.
2. Velg en kontoplan. I hurtigfanen **Hovedkontoer** velger du en hovedkonto, og deretter velger du **Rediger**.
3. Velg hver underordnede hovedkonto som skal tilordnes til en konsoliderte hovedkonto. På hurtigfanen **Generelt** i **Konsolidert konto**-feltet, angir du kontoen i den konsoliderte juridiske enheten som saldoen eller transaksjonene i den aktuelle underordnede hovedkontoen skal overføres til. Du kan angi den samme konsoliderte hovedkontoen for flere underordnede kontoer.

    > [!NOTE]
    > Hvis hovedkontotypene til underkontoene som tilordnes, er forskjellige fra hovedkontotypene til kontoene i den konsoliderte juridiske enheten, overskrives verdiene på kontoer av hovdekontotypen **Total** under konsolidering.

4. Klargjør rapporter og regnskapsoppgjør for den konsoliderte juridiske enheten som er basert på finansdimensjoner. Følg denne fremgangsmåten for å tilordne finansdimensjonene som brukes i underkontoene, til finansdimensjonene i den konsoliderte juridiske enheten:

    1. I den *juridiske enheten for datterselskaper* går du til **Økonomimodul \> Oppsett \> Finansdimensjoner \> Finansdimensjoner**, velger en finansdimensjon og velger deretter **Finansdimensjonsverdier**.
    2. Velg finansdimensjonsverdien du vil tilordne til en annen finansdimensjonsverdi i den konsoliderte juridiske enheten.
    3. Angi finansdimensjonen i den konsoliderte juridiske enheten i hurtigfanen **Generelt** i feltet **Gruppedimensjon**. Under konsolidering tilordnes denne finansdimensjonen til transaksjoner og saldoer som bruker den valgte finansdimensjonen i den underordnede juridiske enheten. Finansdimensjonene du angir her, må være i bruk i den konsoliderte juridiske enheten. Du kan tilordne finansdimensjonen som brukes som gruppefinansdimensjonen for flere underordnede finansdimensjoner.

5. Hvis du gjør en online konsolidering, følger du fremgangsmåten nedenfor for å sikre at overføringene skjer slik du har til hensikt å gjøre:

    1. I den *konsoliderte juridiske enheten* går du **Økonomimodul \> Periodisk \> Konsolider \> Konsolider \[Eksporter til\]** for å åpne siden **Konsolider \[Online\]**.
    2. I kategorien **Vilkår** merker du av for **Bruk konsolideringskonto**.
    3. Velg de riktige finansdimensjonene i kategorien **Finansdimensjoner**.
    4. For hver finansdimensjon du velger, angir du et nummer i feltet **Segmentrekkefølge** for å angi rekkefølgen dimensjonene skal vises i.

## <a name="maintain-the-same-chart-of-accounts-in-the-subsidiary-and-consolidated-legal-entities"></a>Opprettholde samme kontoplan i de underordnede og konsoliderte juridiske enhetene

Hovedkontoene i den underordnede juridiske enheten kan ha samme kontonumre og samme struktur for kontoplanen som hovedkontoene i den konsoliderte juridiske enheten. I dette tilfellet trenger du ikke å tilordne hovedkontoene i den underordnede til hovedkontoene i den konsoliderte juridiske enheten manuelt.

Følg denne fremgangsmåten før du starter konsolideringen.

1. I den *konsoliderte juridiske enheten* går du **Økonomimodul \> Periodisk \> Konsolider \> Konsolider \[Eksporter til\]** for å åpne siden **Konsolider \[Online\]**.
2. Merk av for **Bruk konsolideringskonto**. Under konsolidering overføres transaksjoner og saldoer automatisk til rett konto.

> [!NOTE]
> Hvis kontoene ikke samsvarer, stopper konsolideringen, og du får en melding.

## <a name="create-a-chart-of-accounts-for-the-consolidated-legal-entity-based-on-an-existing-chart-of-accounts"></a>Opprette en kontoplan for den konsoliderte juridiske enheten på grunnlag av en eksisterende kontoplan

Du kan utføre konsolideringen selv om det ikke er opprettet kontoplan i den konsoliderte juridiske enheten enda.

- Hvis du har planlagt kontostrukturen som skal brukes i den konsoliderte juridiske enheten, kan du tilordne de underordnede kontoene til denne strukturen.
- Hvis du ikke tilordner underordnede kontoer, opprettes kontoene i den konsoliderte juridiske enheten automatisk når underordnet data overføres til den konsoliderte juridiske enheten. Disse kontoene er basert på hovedkontoen. Etterfølgende data samles i kontoer i den konsoliderte juridiske enheten som har samme kontonummer som de underordnede kontoene.

Uavhengig av om du har tilordnet kontoer eller ei, fjerner du merket i avmerkingsboksen **Bruk konsolideringskonto** på siden **Konsolider** i den konsoliderte juridiske enheten før du kjører denne typen konsolidering.

> [!NOTE]
> Du kan bruke denne metoden til å opprette en kontoplan i den konsoliderte juridiske enheten fra kontoplanen i en av de underordnede juridiske enhetene. (Hvis du vil ha mer informasjon, kan du se [Konsolideringskontogrupper og ekstra konsolideringskontoer](../budgeting/consolidation-account-groups-consolidation-accounts.md).) Tilordne deretter et passende konsolideringsomregningsprinsipp til hver konsoliderte hovedkonto, og kjør konsolideringen for alle juridiske enheter for datterselskaper.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]