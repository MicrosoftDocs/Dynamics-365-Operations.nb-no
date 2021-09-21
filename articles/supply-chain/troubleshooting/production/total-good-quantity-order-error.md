---
title: Totalt antallsfeil for varer når du forsøker å avslutte en ordre
description: Når du prøver å avslutte en produksjonsordre og ferdigmelde den, kan du få en totalt antallsfeil for varer. Denne siden beskriver hvorfor og hvordan du kan løse problemet.
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 5f0c2c2ca64ada9d72c0ebd04e7de561aaa52039
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477190"
---
# <a name="total-good-quantity-error-when-trying-to-end-a-production-order"></a>Totalt antallsfeil for varer når du forsøker å avslutte en produksjonsordre

## <a name="symptoms"></a>Symptomer

Når du prøver å postere en rapport som ferdigmeldingsjournal på en produksjonsordre, får du følgende feilmelding:

> Totalt antall korrekte som ferdigmeldes for produksjonen, blir %1. På siste operasjon er det i alt tilbakemeldt 0,00.

## <a name="cause"></a>Årsak

Dette problemet oppstår hvis antallet som ble postert i de siste operasjonene, var feil. Hvis for eksempel produksjonen startes, men antallet som må startes, ikke er tilordnet, posteres rutekortjournalen uten linjer. Hvis du vil bekrefte situasjonen, åpner du produksjonsordren, og deretter velger du **Rutekort** i handlingsruten i fanen **Vis**.

## <a name="resolution"></a>Løsning

Du kan løse dette problemet ved å postere flere journaler for operasjonene som journalene ikke var riktig postert for. Start produksjonsordren på nytt, og velg om du vil postere tilleggsjournalene. Denne handlingen vil ikke starte produksjonsordren, men den vil postere journalene. Deretter skal rutekortet vise antallet som ble postert, og du skal kunne avslutte produksjonsordrene.
