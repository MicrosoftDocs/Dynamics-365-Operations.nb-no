---
title: Oversikt over avsetninger
description: Denne artikkelen beskriver avsetninger og gir informasjon om hvordan du konfigurerer dem og opprette transaksjoner.
author: aprilolson
manager: AnnBe
ms.date: 01/11/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerAccuralTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14131
ms.assetid: 0489b59a-37a7-4a78-87bf-4b597e9efad9
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4b97055f7eac12e3e82d028a0097ca926e5c355a
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4446356"
---
# <a name="accruals-overview"></a>Oversikt over avsetninger

[!include [banner](../includes/banner.md)]

Denne artikkelen beskriver avsetninger og gir informasjon om hvordan du konfigurerer dem og opprette transaksjoner.

Avsetninger brukes i avsetningsmetoden til å spore omsetning som gjenkjennes i perioden den er opptjent i, ikke når betaling mottas, og til å spore utgifter (kostnader) som gjenkjennes når de forekommer, ikke når betalingen foretas.

## <a name="accrual-schemes"></a>Avsetningsplaner
Avsetningsplaner brukes til å definere utsatte inntekter og kostnader, og samme avsetningsplan kan brukes til både inntekter og kostnader. Finansavsetninger omfordeler kostnadene eller inntektene på en journallinje slik at kostnadene og inntektene gjenkjennes i de riktige periodene. På **Avsetningsplaner**-siden angir du debet- og kreditkontoer som skal brukes når avsetningsplanen brukes.

-   **Debet** – Hovedkontoen du definerer, erstatter debethovedkontoen på journalbilagslinjen. Denne kontoen brukes også til tilbakeføring av henvisningen, basert på finansavsetningstransaksjoner.
-   **Kredit** – Hovedkontoen du definerer, erstatter kredithovedkontoen på journalbilagslinjen. Denne kontoen brukes også til tilbakeføring av henvisningen, basert på finansavsetningstransaksjoner.

Når du avgjør hvilke kontoer som skal brukes, kan du angi hvordan bilagsnummeret skal opprettes når avsetningstransaksjoner opprettes. Du kan også angi hvor ofte transaksjonene skjer, hvor mange ganger transaksjonene er opprettet, og når transaksjonene posteres. Når avsetningsplanen er opprettet, kan du bruke den i noen av journalene ved hjelp av funksjonen Finansavsetninger.

## <a name="ledger-accruals"></a>Finansavsetninger
Når du registrerer en journal, kan du klikke **Finansavsetninger** på **Funksjoner**-menyen. Når du deretter velger avsetningsplanen, vises grunnlagsbeløpet fra journalen som fordeles over perioden i henhold til avsetningsplanen. Hvis du for eksempel betaler en ansatts forsikring for hele året i januar, og beløpet er 120 000, må du gjenkjenne denne utgiften hver måned. Du kan velge startdatoen. Du kan også angi om det påløpte beløpet er basert på kontoen eller motkontoen. Når du har foretatt valgene, klikker du **Transaksjoner** for å vise alle transaksjonene som er opprettet basert på avsetningsplanen. Hvis du for eksempel fordeler 120 000 i forsikringsutgifter på hele året, ser du 10 000 for hver måned. Når du har postert journalen, kan du vise transaksjonene ved hjelp av forespørselssiden **Bilagstransaksjoner**. Hvis en avsetningsplan ikke kan brukes (for eksempel når en salgsordrefaktura eller bestillingsfaktura er involvert), kan du kreditere det forskuddsbetalte beløpet og debitere utgiftsbeløpet. Deretter kan du velge **Motregn** når du bruker avsetningsplanen.


Hvis du vil ha mer informasjon, se [Opprette avsetningsplaner](tasks/create-accrual-schemes.md) og [Opprette finansavsetningstransaksjoner](tasks/create-ledger-accrual-transactions.md).
