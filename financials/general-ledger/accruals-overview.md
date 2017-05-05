---
title: Oversikt over avsetninger
description: Denne artikkelen beskriver avsetninger og gir informasjon om hvordan du konfigurerer dem og opprette transaksjoner.
author: RobinARH
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: LedgerAccuralTable
audience: Application User
ms.reviewer: RobinARH
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 14131
ms.assetid: 0489b59a-37a7-4a78-87bf-4b597e9efad9
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 328a4a7bef32ee8634e4a9f4854ebe78fcc99f6d
ms.lasthandoff: 03/31/2017


---

# <a name="accruals-overview"></a>Oversikt over avsetninger

[!include[banner](../includes/banner.md)]


Denne artikkelen beskriver avsetninger og gir informasjon om hvordan du konfigurerer dem og opprette transaksjoner.

Avsetninger brukes i avsetningsmetoden til å spore omsetning som gjenkjennes i perioden den er opptjent i, ikke når betaling mottas, og til å spore utgifter (kostnader) som gjenkjennes når de forekommer, ikke når betalingen foretas.

## <a name="accrual-schemes"></a>Avsetningsplaner
Avsetningsplaner brukes til å definere utsatte inntekter og kostnader, og samme avsetningsplan kan brukes til både inntekter og kostnader. Finansavsetninger omfordeler kostnadene eller inntektene på en journallinje slik at kostnadene og inntektene gjenkjennes i de riktige periodene. På **Avsetningsplaner**-siden angir du debet- og kreditkontoer som skal brukes når avsetningsplanen brukes.

-   **Debet** – Hovedkontoen du definerer, erstatter debethovedkontoen på journalbilagslinjen. Denne kontoen brukes også til tilbakeføring av henvisningen, basert på finansavsetningstransaksjoner.
-   **Kredit** – Hovedkontoen du definerer, erstatter kredithovedkontoen på journalbilagslinjen. Denne kontoen brukes også til tilbakeføring av henvisningen, basert på finansavsetningstransaksjoner.

Når du avgjør hvilke kontoer som skal brukes, kan du angi hvordan bilagsnummeret skal opprettes når avsetningstransaksjoner opprettes. Du kan også angi hvor ofte transaksjonene skjer, hvor mange ganger transaksjonene er opprettet, og når transaksjonene posteres. Når avsetningsplanen er opprettet, kan du bruke den i noen av journalene ved hjelp av funksjonen Finansavsetninger.

## <a name="ledger-accruals"></a>Finansavsetninger
Når du registrerer en journal, kan du klikke **Finansavsetninger** på **Funksjoner**-menyen. Når du deretter velger avsetningsplanen, vises grunnlagsbeløpet fra journalen som fordeles over perioden i henhold til avsetningsplanen. Hvis du for eksempel betaler en ansatts forsikring for hele året i januar, og beløpet er 120 000, må du gjenkjenne denne utgiften hver måned. Du kan velge startdatoen. Du kan også angi om det påløpte beløpet er basert på kontoen eller motkontoen. Når du har foretatt valgene, klikker du **Transaksjoner** for å vise alle transaksjonene som er opprettet basert på avsetningsplanen. Hvis du for eksempel fordeler 120 000 i forsikringsutgifter på hele året, ser du 10 000 for hver måned. Når du har postert journalen, kan du vise transaksjonene ved hjelp av forespørselssiden **Bilagstransaksjoner**. Hvis en avsetningsplan ikke kan brukes (for eksempel når en salgsordrefaktura eller bestillingsfaktura er involvert), kan du kreditere det forskuddsbetalte beløpet og debitere utgiftsbeløpet. Deretter kan du velge **Motregn** når du bruker avsetningsplanen.



