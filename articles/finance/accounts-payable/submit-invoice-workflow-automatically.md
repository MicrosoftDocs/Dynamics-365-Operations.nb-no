---
title: Sende fakturaer til arbeidsflytsystemet og samsvare produktkvitteringslinjer (forhåndsversjon)
description: Dette emnet beskriver prosessen for å sende leverandørfakturaer til arbeidsflytsystemet og automatisk samsvare posterte produktkvitteringslinjer med leverandørfakturaer.
author: abruer
manager: AnnBe
ms.date: 09/08/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.assetid: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2017-09-08
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: cde164ee89b542d769d81d8d483049fb7ca001c4
ms.sourcegitcommit: 3387595e41fb03e98bb437588f6de78794ae383f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/02/2020
ms.locfileid: "3930925"
---
# <a name="submit-invoices-to-the-workflow-system-and-match-product-receipt-lines-preview"></a>Sende fakturaer til arbeidsflytsystemet og samsvare produktkvitteringslinjer (forhåndsversjon)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Dette emnet beskriver prosessen for å sende leverandørfakturaer til arbeidsflytsystemet og automatisk samsvare posterte produktkvitteringslinjer med leverandørfakturaer.

## <a name="submitting-imported-vendor-invoices-to-the-workflow-system-and-matching-posted-product-receipt-lines-to-pending-vendor-invoice-lines"></a>Sende importerte leverandørfakturaer til arbeidsflytsystemet og samsvare posterte produktkvitteringslinjer til ventende leverandørfakturalinjer

Som en del av en berøringsfri faktureringsprosess for leverandører, kan du få systemet til automatisk å sende en importert faktura til arbeidsflytsystemet. Du kan konfigurere prosessen med å sende importerte fakturaer til arbeidsflytsystemet i kategorien **Automatisering av leverandørfaktura** på siden **Leverandørparametere** ( **Leverandør \> Oppsett \> Leverandørparametere** ). Prosessen for sending til arbeidsflyt vil kjøre i bakgrunnen med en angitt hyppighet (enten hver time eller daglig).

Når du sender fakturaer automatisk til arbeidsflytsystemet, må du begynne med en importert faktura. Hvis du vil sikre at fakturaen kan behandles fra start til slutt uten manuell behandling, må du inkludere en automatisk posteringsoppgave i arbeidsflytkonfigurasjonen. Fakturaer som er knyttet til bestillinger og fakturaer som inneholder en ikke-bestillingsinnkjøpskategori og ikke-lagerførte linjer, kan sendes automatisk til arbeidsflytsystemet. Fakturaer som registreres manuelt, må sendes manuelt til arbeidsflytsystemet.

Verdien **Innsendte av** i arbeidsflyten er bruker-ID-en som ble angitt for bakgrunnsoppgaven **Send leverandørfakturaer til arbeidsflyt** på siden **Prosessautomatisering** . Brukeren med denne bruker-ID-en kan tilbakekalle fakturaen fra arbeidsflytsystemet etter behov.

## <a name="matching-posted-product-receipts-to-invoice-lines-that-have-a-three-way-matching-policy"></a>Samsvare posterte produktkvitteringer med fakturalinjer som har en treveis kontrollpolicy

Som en del av en berøringsfri faktureringsprosess, kan systemet automatisk samsvare posterte produktkvitteringer med fakturalinjer. Det må defineres et treveis kontrollpolicy for denne oppgaven. Denne funksjonen er tilgjengelig hvis funksjonen **Automatisering av leverandørfaktura** er aktivert på siden **Funksjonsbehandling** .

Prosessen vil kjøre til det samsvarende produktkvitteringsantallet er lik fakturaantallet. Som en del av denne prosessen kan du angi det maksimale antall ganger som systemet skal prøve å samsvare produktkvitteringer med en fakturalinje før prosessen mislykkes. Prosessen kjøres i bakgrunnen, enten hver time eller hver dag. Du kan kjøre den automatiserte samsvarsprosessen som en del av prosessen for å sende fakturaer til arbeidsflytsystemet. Du kan også kjøre den som en frittstående prosess. Innstillingene for prosessen for samsvaring av produktkvittering med fakturalinjer konfigureres i kategorien **Automatisering av leverandørfaktura** på siden **Leverandørparametere** ( **Leverandør \> Oppsett \> Leverandørparametere** ).

Fakturalinjer som har en treveis kontrollpolicy, der det samsvarende mottaksantallet er mindre enn fakturaantallet, blir inkludert i den automatiske mottaksprosessen.

Hvis du vil vise **Siste treff** -statusen for fakturaer som ikke er en del av den automatiserte prosessen for sending til arbeidsflyt, åpner du fakturaen fra siden **Leverandørfakturaer** . Når du viser fakturaen, oppdateres den samsvarende valideringsinformasjonen.

En fakturalinje vil bli utelatt fra den automatiserte behandlingen hvis en av følgende betingelser er oppfylt:

- Verdien **Status for automatisert kvitteringssamsvar** for fakturalinjen **Mislyktes** .
- Fakturaen er i bruk.
- Fakturaen er i arbeidsflytsystemet.
