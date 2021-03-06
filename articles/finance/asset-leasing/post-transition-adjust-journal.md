---
title: Postere journaloppføringer for overgangsjustering i aktivaleie
description: Dette emnet beskriver funksjonaliteten som lar deg overføre en leieavtaleportefølje til de nye regnskapsstandardene for leieavtaler, Accounting Standards Codification-emne 842 (ASC 842) og International Financial Reporting Standard 16 (IFRS 16).
author: moaamer
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: ea61a0d6e30695a2ef6b93529fcf3d21882c9cd2
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5819776"
---
# <a name="post-transition-adjustment-journal-entries-in-asset-leasing"></a>Postere journaloppføringer for overgangsjustering i aktivaleie

[!include [banner](../includes/banner.md)]

Dette emnet beskriver funksjonaliteten som lar deg overføre en leieavtaleportefølje til de nye regnskapsstandardene for leieavtaler: Accounting Standards Codification-emne 842 (ASC 842), som er standard i Generally Accepted Accounting Principles i USA (US GAAP), og International Financial Reporting Standard 16 (IFRS 16).

Hvis du vil ha informasjon om hvordan du definerer et tablå for overgangen til de nye standardene, kan du se [Definere leietablåer](set-up-lease-books.md).

Når du oppretter en journaloppføring for overgangsjustering, genereres det en journaloppføring. Denne oppføringen gjenspeiler balansevirkningen for registrering av leieavtalen i henhold til de nye standardene på denne datoen. Den relevante aktivakontoen debiteres for det indirekte beløpet på denne datoen, og gjeldskontoen krediteres. Differansen blir enten debitert eller kreditert til opptjente midler.

Hvis du vil postere en overgangsjustering i samsvar med de nye regnskapsstandardene, følger du disse trinnene.

1. På siden **Leiesammendrag** velger du leieavtalen, og deretter velger du **Tablåer**.
2. I tablået velger du **Betalingsplan**.
3. I dialogboksen **Betalingsplan** velger du **Bekreft**. Lukk deretter dialogboksen.
4. Velg **Overgangsjustering**.

    > [!NOTE]
    > En overgangsjustering kan bare opprettes for leietablåer som er tilordnet til et tablå der feltet for **overgangstablå** er tilgjengelig. Hvis verdien i feltet for **leieavtalestart** er senere enn overgangsdatoen, vil ikke verdien i feltet for **Overgangsjustering** oppdateres.

5. Du viser journaloppføringen ved å velge **Journaler for leie av anleggsmidler**.
6. Velg den nye journalen, og velg deretter **Poster**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]