---
title: Parametere for styring av teknisk endring
description: Dette emnet forklarer hvordan du konfigurerer funksjoner for behandling av teknisk endring for Microsoft Dynamics 365 Supply Chain Management.
author: t-benebo
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: dbe51e9e44cbdbf71d02e84c3a8634750f45ffa13b213fc1306a1047fb9e0b63
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6725752"
---
# <a name="engineering-change-management-parameters"></a>Parametere for styring av teknisk endring

[!include [banner](../includes/banner.md)]

Siden **Parametere for behandling av teknisk endring** inneholder konfigurasjonsparametere som endrer standard virkemåte som er knyttet til frigivelsesproduktstrukturen og prosessene for behandling av teknisk endring.

## <a name="open-the-engineering-change-management-parameters-page"></a>Åpne siden Åarametere for behandling av teknisk endring

Hvis du vil åpne siden **Parametere for behandling av teknisk endring**, kan du gå til **Behandling av teknisk endring \> Oppsett \> Parametere for behandling av teknisk endring**. Du kan deretter angi feltene som beskrevet i resten av delene i dette emnet.

## <a name="release-control-tab"></a>Fanen Frigi kontroll

Følgende tabell beskriver feltene som er tilgjengelige i fanen **Frigivelseskontroll** på siden **Parametere for behandling av teknsik endring**. Disse feltene påvirker prosessen for frigivelseproduktstrukturen.

| Felt | beskrivelse |
|---|---|
| Regel for varenummer | Velg hvordan varenummeret skal defineres når produktet frigis til en juridisk enhet. Velg *Teknisk produktnummer* hvis produktnummeret i den mottakende juridiske enheten skal samsvare med produktnummeret i det tekniske firmaet. Velg *Lokal varenummersekvens* hvis produktet skal ta det neste nummeret i nummersekvensen for produktnumre i den mottakende juridiske enheten. |
| Regel for stykklistenavn | Velg hvordan navnet på stykklisten defineres når produktet mottas (frigis) i en juridisk enhet. Velg enten *Teknisk navn* eller *Mottak av varenummer*. |
| Regel for rutenavn | Velg hvordan rutenavnet skal defineres når ruten til et produkt mottas (frigis) i en juridisk enhet. Velg enten *Teknisk navn* eller *Mottak av varenummer*. |
| Kjør stykklistekontroll | Velg om en stykklistekontroll skal kjøres når produktet mottas (frigis) i en juridisk enhet. |
| Frigi virkemåte for inaktiv stykkliste | Velg om et produkt kan frigis hvis det har en inaktiv stykkliste. Velg *Godta*, *Bare advarsel* eller *Ikke tillatt*. |
| Frigi virkemåte for inaktiv rute | Velg om et produkt kan frigis hvis det har en inaktiv rute. Velg *Godta*, *Bare advarsel* eller *Ikke tillatt*.|
| Produktgodkjenning | Velg om det kreves et tilleggstrinn for godkjenning før produktet kan frigis i den juridiske enheten. Velg *Manuell* for å legge til godkjenningstrinnet. I dette tilfellet viser siden **Åpne produktfrigivelser** produktene. Velg *Automatisk* for å vise produktet direkte på siden **Frigitte produkter** i den juridiske målenheten rett etter at produktet er frigjort sammen med frigivelsesproduktstrukturen. |

## <a name="engineering-change-management-tab"></a>Fanen Behandling av teknisk endring

Følgende tabell beskriver feltene som er tilgjengelige i fanen **Behandling av teknisk endring** på siden **Parametere for behandling av teknsik endring**. Disse innstillingene påvirker prosessen for behandling av teknisk endring.

| Felt | beskrivelse |
|---|---|
| Kategori | Standardkategorien som skal brukes når det opprettes en forespørsel om teknisk endring. |
| Prioritet | Standardprioriteten som skal brukes når det opprettes en forespørsel om teknisk endring. |
| Regel for alvorsgrad | Velg hvordan alvorsgraden for en ordre om teknisk endring skal etableres. Velg *Manuell* hvis brukeren forventes å angi en verdi i feltet **Alvorsgrad**. Velg *Beregn* for å få systemet til å beregne verdien i feltet **Alvorsgrad** når du velger **Beregn alvorsgrad** i handlingsruten i ordren om teknisk endring. I dette tilfellet vil systemet bruke reglene for alvorsgrad som er definert på siden **Regelsett for alvorsgrad**. Velg *Beregn automatisk* hvis du vil at verdien i feltet **Alvorsgrad** beregnes og fylles ut automatisk i henhold til regelsettene for alvorsgrad. |
| Frigi berørte produkter på nytt | Dette feltet brukes når du frigir produkter på nytt via en ordre om teknisk endring. Du kan velge om alle produkter eller bare de berørte produktene skal foreslås i dialogboksen **Frigivelser**. |
| Stykklistenivåer som skal frigis | Dybden på stykklistenivået som skal frigis. Hvis stykklisten har flere nivåer (det vil si hvis den er dypere) enn verdien som er angitt her, vil bare nivåene opp til og med den angitte verdien bli frigjort. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]