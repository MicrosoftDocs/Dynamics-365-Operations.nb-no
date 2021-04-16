---
title: Sende fakturaer til arbeidsflytsystemet og avstemme produktkvitteringslinjer
description: Dette emnet beskriver prosessen for å sende leverandørfakturaer til arbeidsflytsystemet og automatisk samsvare posterte produktkvitteringslinjer med leverandørfakturaer.
author: abruer
ms.date: 09/08/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.assetid: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2017-09-08
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 84699746349024854a4eeb9cee62960ec38bc338
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5827824"
---
# <a name="submit-invoices-to-the-workflow-system-and-match-product-receipt-lines"></a>Sende fakturaer til arbeidsflytsystemet og avstemme produktkvitteringslinjer

[!include [banner](../includes/banner.md)]

Dette emnet beskriver prosessen for å sende leverandørfakturaer til arbeidsflytsystemet og automatisk samsvare posterte produktkvitteringslinjer med leverandørfakturaer.

## <a name="submitting-imported-vendor-invoices-to-the-workflow-system-and-matching-posted-product-receipt-lines-to-pending-vendor-invoice-lines"></a>Sende importerte leverandørfakturaer til arbeidsflytsystemet og samsvare posterte produktkvitteringslinjer til ventende leverandørfakturalinjer

Som en del av en berøringsfri faktureringsprosess for leverandører, kan du få systemet til automatisk å sende en importert faktura til arbeidsflytsystemet. Du kan konfigurere prosessen med å sende importerte fakturaer til arbeidsflytsystemet i kategorien **Automatisering av leverandørfaktura** på siden **Leverandørparametere** (**Leverandør \> Oppsett \> Leverandørparametere**). Prosessen for sending til arbeidsflyt vil kjøre i bakgrunnen med en angitt hyppighet (enten hver time eller daglig).

Når du sender fakturaer automatisk til arbeidsflytsystemet, må du begynne med en importert faktura. Hvis du vil sikre at fakturaen kan behandles fra start til slutt uten manuell behandling, må du inkludere en automatisk posteringsoppgave i arbeidsflytkonfigurasjonen. Fakturaer som er knyttet til bestillinger og fakturaer som inneholder en ikke-bestillingsinnkjøpskategori og ikke-lagerførte linjer, kan sendes automatisk til arbeidsflytsystemet. Fakturaer som registreres manuelt, må sendes manuelt til arbeidsflytsystemet.

Verdien **Innsendte av** i arbeidsflyten er bruker-ID-en som ble angitt for bakgrunnsoppgaven **Send leverandørfakturaer til arbeidsflyt** på siden **Prosessautomatisering**. Brukeren med denne bruker-ID-en kan tilbakekalle fakturaen fra arbeidsflytsystemet etter behov.

## <a name="matching-posted-product-receipts-to-invoice-lines-that-have-a-three-way-matching-policy"></a>Samsvare posterte produktkvitteringer med fakturalinjer som har en treveis kontrollpolicy

Som en del av en berøringsfri faktureringsprosess, kan systemet automatisk samsvare posterte produktkvitteringer med fakturalinjer. Det må defineres et treveis kontrollpolicy for denne oppgaven. Denne funksjonen er tilgjengelig hvis funksjonen **Automatisering av leverandørfaktura** er aktivert på siden **Funksjonsbehandling**.

Samsvarsprosessen vil kjøre til det samsvarende produktkvitteringsantallet er lik fakturaantallet. Hvis det imidlertid finnes flere produktmottak for én enkelt fakturalinje, må du kjøre prosessen flere ganger for å oppnå samsvarende antall. Du kan angi det maksimale antall ganger som systemet skal prøve å samsvare produktkvitteringer med en fakturalinje før prosessen mislykkes. Prosessen kjøres i bakgrunnen, enten hver time eller hver dag. 

Du kan kjøre den automatiserte samsvarsprosessen som en del av prosessen for å sende fakturaer til arbeidsflytsystemet. Du kan også kjøre den som en frittstående prosess. Innstillingene for prosessen for samsvaring av produktkvittering med fakturalinjer konfigureres i kategorien **Automatisering av leverandørfaktura** på siden **Leverandørparametere** (**Leverandør \> Oppsett \> Leverandørparametere**).

Fakturalinjer som har en treveis kontrollpolicy, der det samsvarende mottaksantallet er mindre enn fakturaantallet, blir inkludert i den automatiske mottaksprosessen.

Hvis du vil vise **Siste treff**-statusen for fakturaer som ikke er en del av den automatiserte prosessen for sending til arbeidsflyt, åpner du fakturaen fra siden **Leverandørfakturaer**. Når du viser fakturaen, oppdateres den samsvarende valideringsinformasjonen. Statusen **Siste treff** kan oppdateres automatisk ved hjelp av bakgrunnsoppgaven **Valider fakturakontroll**. Du kan konfigurere prosessen med automatisk oppdatering av status **Siste treff** i kategorien **Bakgrunnsprosesser** på siden **Prosessautomatiseringer** (**Systemadministrasjon\> Oppsett\> Prosessautomatiseringer**).

En fakturalinje vil bli utelatt fra den automatiserte behandlingen hvis en av følgende betingelser er oppfylt:

- Verdien **Status for automatisert kvitteringssamsvar** for fakturalinjen **Mislyktes**.
- Fakturaen er i bruk.
- Fakturaen er i arbeidsflytsystemet.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
