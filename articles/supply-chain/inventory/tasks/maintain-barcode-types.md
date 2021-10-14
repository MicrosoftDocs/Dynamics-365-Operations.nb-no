---
title: Opprettholde strekkodetyper
description: Denne fremgangsmåten viser hvordan du definerer en ny definisjon for strekkode som kan brukes som en del av plukklisterapporten.
author: yufeihuang
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: BarcodeSetup, InventParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b689d1fc85d59ac87efa1903fd7122ae5ff011da
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/29/2021
ms.locfileid: "7571119"
---
# <a name="maintain-bar-code-types"></a>Opprettholde strekkodetyper

[!include [banner](../../includes/banner.md)]

Denne fremgangsmåten viser hvordan du definerer en ny definisjon for strekkode som kan brukes som en del av plukklisterapporten. Du kan gå gjennom denne fremgangsmåten i demonstrasjonsselskapet USMF eller ved hjelp av dine egne data. Hvis du bruker USMF, kan du bruke eksempelverdiene som vises. Disse oppgavene vil vanligvis utføres av en lagersjef.

1. Gå til **Strekkoder**.
1. Velg **Ny**.
1. Skriv inn en verdi i feltet **Strekkodeoppsett**.
1. Skriv inn en verdi i **Beskrivelse**-feltet.
1. Velg et alternativ i **Strekkodetype**-feltet.
    * Hvis du bruker USMF, kan du velge "Kode 39".
1. I **Maske-ID**-feltet angir du IDen til strekkodemasken. Strekkodemasker brukes til å opprette strekkoder og raskt identifisere strekkoder som skannes inn på et salgsstedssystem. Hvis du vil ha mer informasjon, kan du se [Definere strekkodemasker](../../../commerce/set-up-bar-code-masks.md).
1. Angi et tall i feltet **Størrelse**.
1. Angi et tall i feltet **Maksimumslengde**.
1. Velg **Lagre**.
1. Lukk siden.
1. Gå til **Parametere for beholdnings- og lagerstyring**.
1. Angi eller velg en verdi i feltet **Strekkodeoppsett**.
    * Velg strekkodeoppsettet som du opprettet før, men Vær oppmerksom på at strekkodeformatet må samsvare med formatet for den unike identifikatoren for oppføringstypen som brukes i prosessen. For plukkruter bør for eksempel strekkodeformatet samsvare med formatet for plukkrutereferansen, som vanligvis er en nummerserie.  
1. Velg **Lagre**.
1. Lukk siden.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
