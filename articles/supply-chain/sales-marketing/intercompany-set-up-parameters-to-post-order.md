---
title: Definere parametere for å postere en konsernintern ordre
description: Dette emnet forklarer hvordan du definerer parametere for å postere en konsernintern ordre
author: GalynaFedorova
ms.date: 09/01/2021
ms.topic: article
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: c728f2f491948ae1c8550396ba4d72f76f46fe85
ms.sourcegitcommit: fcfd85a508c0de52cfe11d1986892219e39ef406
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/23/2021
ms.locfileid: "7548445"
---
# <a name="set-up-parameters-to-post-an-intercompany-order"></a>Definere parametere for å postere en konsernintern ordre

[!include [banner](../../includes/banner.md)]

Når en konsernintern kundefaktura posteres, kan du konfigurere den til å postere både den konserninterne bestillingen og den originale kundefakturaen automatisk.

> [!NOTE]
> Før du utfører denne fremgangsmåten, må du konfigurere utskriftsbehandlingen i organisasjonen til å peke til riktig fakturaskriver. Dette vil sikre at fakturaen for den opprinnelige salgsordren skrives ut på riktig skriver.

Du må konfigurere følgende parametre:

1. Gå til **Salg og markedsføring \> Salgsordrer \> Alle salgsordrer**. Velg salgsordren du vil arbeide med.
1. I handlingsruten i salgsordren velger du **Topptekstvisning**, og velger deretter hurtigfanen **Konserninterne innstillinger**, og åpner den.
1. Gå til handlingsruten i **Salgsordre**-kategorien, og velg **Rediger**.
1. Gå tilbake til hurtigfanen **Konserninterne innstillinger**, og velg **Direkte levering** for å aktivere direkte levering i hele den konserninterne kjeden (alle ordrer).
1. Velg **Lagre** for å lagre salgsordren med den nye innstillingen. Deretter velger du **Lukk** for å lukke salgsordren.
1. Gå til **Innkjøp og leverandører \> Leverandører \> Alle leverandører**. I kategorien **Generelt** velger du **Konsernintern**.
1. På siden **Konsernintern** velger du koblingen **Bestillingspolicyer**. I feltgruppen **Konsernintern bestilling (direktelevering)** velger du **Poster faktura automatisk** og fjerner merket i feltet **Skriv ut faktura automatisk**.
1. I feltgruppen **Opprinnelig salgsordre (direktelevering)** velger du feltet **Poster faktura automatisk** og feltet **Skriv ut faktura automatisk**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
