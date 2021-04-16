---
title: Definere utgiftstyper
description: Dette emnet forklarer hvordan du definerer utgiftstyper i aktivaleie.
author: moaamer
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2019-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: b50f406c7411ff8ed990a312fde9c2fc0ba3c3db
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5819704"
---
# <a name="set-up-expense-types"></a>Definere utgiftstyper

[!include [banner](../includes/banner.md)]

Dette emnet forklarer hvordan du definerer utgiftstyper i aktivaleie. Kostnader som ikke representeres av betalingsplanen, kalles *utgiftskostnader*. Eksempler på disse kostnadene inkluderer eiendomsavgifter, vedlikeholdskostnader for vanlige områder og forsikringsutgifter.

## <a name="add-an-administrative-expense-type"></a>Legge til en administrativ utgiftstype

1. Gå til **Aktivaleie \> Oppsett \> Utgiftstyper**.
2. Velg **Ny**.
3. I de aktuelle feltene angir du den nye utgiftstypen og en beskrivelse.

## <a name="assign-accounts-to-administrative-costs"></a>Tilordne kontoer til administrative kostnader

Deretter bør du knytte kontoer til utgiftstypene. Disse kontoene blir debitert når utgiftsplanoppføringer posteres. Motkontoen angis på linjene for **betalingsplan for fullbyrdelseskostnad** på hver leieavtale.

1. Gå til **Aktivaleie \> Oppsett \> Parametere for aktivaleie**.
2. I kategorien **Kontoer** på hurtigfanen for **fullbyrdelseskostnad** i feltet **Utgiftstype** velger du utgiftstype.
3. Velg **Legg til**.
4. I feltet for **tablåtype** velger du tablåtypen for å koble til de administrative kostnadene.

    > [!NOTE]
    > Flere tablåtyper kan knyttes til den samme utgiftskontoen.

5. I **Kontokode**-feltet angir du hvilke leieavtaler tablået skal brukes på:

    - **Alle** – Bruk tablået på alle leieavtaler.
    - **Gruppe** – Bruk tablået på en bestemt gruppe leieavtaler.
    - **Tabell** – Bruk tablået på spesifikke leieavtaler.

6. Hvis du har valgt **Gruppe** eller **Tabell** i **Kontokode**, velger du et kontonummer eller gruppenummer i feltet **Konto-/gruppenummer**.
7. I de aktuelle feltene velger du hovedkonto for finansiell leie og hovedkonto for gjeldende leie.

Når du har fullført disse trinnene, kan du legge til utgifter ved hjelp av linjene i **betalingsplan for fullbyrdelseskostnad** på siden **Leiedetaljer** for en valgt leieavtale. Du kan også legge til utgifter når du oppretter en ny leieavtale.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]