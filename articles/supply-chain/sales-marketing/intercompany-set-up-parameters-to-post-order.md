---
title: Definere parametere for å postere en konsernintern ordre
description: Denne artikkelen forklarer hvordan du definerer parametere for å postere en konsernintern ordre
author: Henrikan
ms.date: 09/01/2021
ms.topic: article
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 97ea0061d57beede6350eecfd497c12dd37aea31
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8900803"
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
