---
title: Leiekonvensjoner for aktiva
description: Dette emnet beskriver konvensjoner for leide aktiva.
author: moaamer
ms.date: 1/14/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLease
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2021-1-28
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: e6450438a6e8c594590df3cc4502895913f50d01
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5842400"
---
# <a name="asset-leasing-conventions"></a>Leiekonvensjoner for aktiva

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Dette emnet beskriver konvensjoner for leide aktiva. Leiekonvensjoner brukes til å bestemme startdatoen for et leietablå. Hvis leiekonvensjonen er satt til **Ingen**, er startdatoen den samme som startdatoen for leien (det vil si verdien for **Startdato for leie**). Hvis leiekonvensjonen er satt til **Hele måneden**, er startdatoen den første dagen i måneden som startdatoen for leieavtalen faller på.

Startdatoen fastsetter startdatoen for perioden for planene for nedbetaling av gjeld og avskrivning av aktiva. Rente- og avskrivningsutgifter posteres på sluttdatoen for perioden i de gjeldende planene. Den første journaloppføringen for opprinnelig føring og justering posteres på startdatoen.

> [!NOTE]
> Funksjonen for leiekonvensjoner må aktiveres ved hjelp av Funksjonsbehandling. I arbeidsområdet for **Funksjonsbehandling** finner og velger du funksjonen for **Leiekonvensjon for aktivaleie**, og deretter velger du **Aktiver nå**.

Leiekonvensjoner tilordnes til oppsettet for et leieaktivatablå.

Følg denne fremgangsmåten for å vise eller tilordne leiekonvensjonen.

1. Gå til **Aktivaleie \> Oppsett \> Leietablåer**.
2. I feltet **Leiekonvensjon** velger du en av følgende verdier.

    | Leiekonvensjon | beskrivelse |
    |--------------------|-------------|
    | None               | Planene for nedbetaling av gjeld og avskrivning av aktiva starter på startdatoen for leieavtalen, fordi startdatoen er lik startdatoen for leieavtalen. Sluttdatoen er én måned senere. Denne leiekonvensjonen gir ingen garanti for at renten posteres på den siste dagen i hver måned. |
    | Hele måneden         | For leieavtaler med startdato når som helst i løpet av måneden, begynner planene for nedbetaling av gjeld og avskrivning av aktiva å avsette utgifter på den første dagen i denne måneden. Denne leiekonvensjonen sikrer at det avsettes rente på den siste dagen i hver måned for hele måneden. |

3. Velg **Lagre**.

Når det opprettes en leieavtale, angis startdatoen for hvert tablå automatisk basert på startdatoen som er angitt for leieavtalen og leiekonvensjonen som er angitt for tablået.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]