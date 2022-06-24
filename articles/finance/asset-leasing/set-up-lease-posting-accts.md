---
title: Definere leieposteringskontoer
description: Denne artikkelen viser posteringskontoene som kreves for aktivaleietransaksjoner, og forklarer hvordan du definerer posteringskontoer på siden for parametere for leiepostering.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeasePostingAccounts
audience: Application User
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 6e3a0d8dd3bb3e58ca10b2efce0cc88a2f48d2de
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8859921"
---
# <a name="set-up-lease-posting-accounts"></a>Definere leieposteringskontoer

[!include [banner](../includes/banner.md)]

Denne artikkelen viser posteringskontoene som kreves for aktivaleietransaksjoner, og forklarer hvordan du definerer posteringskontoer på siden for **Parametere for leiepostering**.

For å overholde Accounting Standards Codification-emne 842 (ASC 842) og International Financial Reporting standard 16 (IFRS 16), må du kanskje opprette kontoer i kontoplanen. Alle kontoer du oppretter for å overholde ASC- og IFRS-standarder, er imidlertid ikke anleggsmiddelkontoer. Under ASC 842 blir det registrert en bruksrettseiendel for både økonomi og gjeldende leie. Disse leieavtalene er atskilte fra anleggsmidler. (Du kan fremdeles vedlikeholde en bruksrettseiendel ved å bruke anleggsmidler.)

Hvis du vil ha informasjon om hvordan du opprette kontostrukturer, kan du se [Opprette kontostrukturer](../general-ledger/tasks/create-account-structures.md). Hvis du vil ha informasjon om hvordan du oppretter en hovedkonto, kan du se [Opprette en hovedkonto](../general-ledger/tasks/create-main-account.md).

Følgende tabell viser eksempler på kontoer du må opprette for transaksjoner for leide eiendeler, hvis de ikke allerede er opprettet. Under IFRS 16 blir gjeldende leie-relasjoner fremdeles brukt for leieavtaler med lav verdi eller kortsiktige leieavtaler.

| Finanskontonummer | Kontotype  | Kontonavn                                          |
|-----------------------|---------------|-------------------------------------------------------|
| 180150                | Objekt         | Bruksrettseiendel for kjøretøy                                     |
| 180160                | Objekt         | Bruksrettseiendel for bygning                                    |
| 180250                | Objekt         | Akkumulert avskrivning – kjøretøyer                   |
| 180260                | Objekt         | Akkumulert avskrivning – bygninger                  |
| 222300                | Gjeld     | Kortsiktig forpliktelse – finansiell leie                |
| 222310                | Balanse | Kortsiktig forpliktelse – gjeldende leie              |
| 250200                | Gjeld     | Fakturagjeld                                         |
| 250601                | Balanse | Langsiktig forpliktelse – finansiell leie                 |
| 250602                | Balanse | Langsiktig forpliktelse – gjeldende leie               |
| 250606                | Balanse | Utsatt leie                                         |
| 300160                | Balanse | Tilbakeholdt overskudd                                     |
| 604500                | Expense       | Leieutgift                                         |
| 604501                | Expense       | Utgift for gjeldende leie for kjøretøy – rentetillegg  |
| 604502                | Expense       | Utgift for gjeldende leie for kjøretøy – nedbetaling        |
| 605200                | Expense       | Utgift for gjeldende leie for bygning – rentetillegg |
| 605201                | Expense       | Utgift for gjeldende leie for bygning – nedbetaling       |
| 607101                | Expense       | Utgift for leieamortisering for kjøretøy                    |
| 607102                | Expense       | Utgift for leieamortisering for bygning                   |
| 607103                | Expense       | Verdiforringelsesutgift – finansiell leie                   |
| 607104                | Expense       | Verdiforringelsesutgift – gjeldende leie                 |
| 618910                | Expense       | Leieutgift – finansiell leie                        |
| 618920                | Expense       | Variable betalinger – finansiell leie                    |
| 618930                | Expense       | Variable betalinger – gjeldende leie                  |
| 800600                | Expense       | Renteutgift for leie for kjøretøy                        |
| 800601                | Expense       | Renteutgift for leie for bygning                       |
| 801201                | Balanse | Fortjeneste/tap – endring av leie                      |

## <a name="configure-posting-accounts"></a>Konfigurere posteringskontoer

Hvis du vil tilordne kontoer til leietablåer og -grupper som er opprettet, må du konfigurere parametere for aktivaleie.

1. Gå til **Aktivaleie \> Oppsett \> Parametere for leiepostering**.
2. I kategorien **Kontoer** åpner du hurtigfanen for **Leiekontoer**. Fastsett hovedkontoene for finansiell og gjeldende leie til tilsvarende **Posteringstype**. Den foregående tabellen viser kontoene som er knyttet til finansiell og gjeldende leie.

    > [!NOTE]
    > Dette trinnet krever at du definerer separate kontoer for både gjeldende og finansiell leie for hver posteringstype, unntatt **Motpost for leieutgift** og **Økning/reduksjon av leie**. Firmaer som følger IFRS 16-regnskapsrammeverket, må legge til en hovedkonto for gjeldende leie. Men systemet vil ikke bruke denne kontoen selv om det er et obligatorisk felt, fordi alle leieavtaler under IFRS 16 klassifiseres som finansielle leieavtaler.
    >[!NOTE]
    > **Økning/reduksjon av leie** vil bli brukt som posteringstype for ytterligere aktivabetraktninger, inkludert **opprinnelig direkte kostnad, leieinsentiver, forskuddsbetaling av leie og avviklingskostnader**, men posteres til hovedkonto for bruksrettseiendeler som er **Leieaktiva** som standard.        
    
3. Hvis du vil velge en bestemt leiegruppe som tilsvarer hovedkontoen, velger du **Gruppe** i feltet **Kontokode**. I feltet **Konto-/gruppenummer** velger du leiegruppe for å tilordne til hovedkontoen.
4. Hvis du vil tilordne kontokoder til administrative kostnader som er definert i systemet, går du til hurtigfanen for **fullbyrdelseskostnader** og velger en utgift i feltet **Utgiftstype**. Deretter tilordner du økonomi- og driftskontoer som skal brukes for hver bok.

    > [!NOTE]
    > Den valgte økonomi- eller driftskontoen blir debitert når fakturaen for den planlagte utgiften posteres.
    > **Motpost for leieutgift** blir brukt som posteringstype for fullbyrdelseskostnadstransaksjoner, men posteres til angitt **Motkonto** i **betalingsplanlinjer for fullbyrdelseskostnader** i leiedetaljer eller leietablåskjema.   


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
