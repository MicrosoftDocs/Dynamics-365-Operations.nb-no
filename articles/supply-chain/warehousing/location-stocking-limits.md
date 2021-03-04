---
title: Lokasjon – lagringsgrenser
description: Dette emnet beskriver funksjonaliteten til lagringsgrenser for lokasjon.
author: perlynne
manager: tfehr
ms.date: 11/11/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLocationLimit
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-11-11
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 208662f38b06b1f230bdde5247946a9fefd57cea
ms.sourcegitcommit: d2dea9ce480f35d0c0b10615c18862695e107d55
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/23/2020
ms.locfileid: "4607285"
---
# <a name="location-stocking-limits"></a>Lokasjon – lagringsgrenser

[!include [banner](../includes/banner.md)]

Du kan bruke siden **Lagringsgrenser for lokasjon** (**Lagerstyrings \> Oppsett \> Lager \> Lagringsgrense for lokasjon**) til å kontrollere lastkapasiteten på lagringslokasjoner uten å måtte bruke de mer avanserte prosessene for volumberegninger av fysiske produkter.

Formålet med lagringsgrensen for lokasjon er å evaluere det maksimale antallet en lokasjon kan inneholde. Du kan definere funksjonen på et av tre nivåer, der hvert har sin egen kategori på siden **Lagringsgrense for lokasjon**:

- Produkter
- Produktvarianter
- Beholdertyper

For hvert nivå kan du definere forskjellige feltverdier. Systemet vil da evaluere kapasiteten til en bestemt lokasjon, basert på verdiene for **antall** og **enhet** for hver rad. Den vil velge den mest detaljerte samsvarende posten først. En rad som har en verdi i feltet **Lokasjonsprofil-ID**, vurderes for eksempel før en rad som har en verdi bare i **Lager**-feltet. Den gjenstående kapasiteten vil også bli evaluert, basert på **Antall**-verdien for posten til lagringsgrense for lokasjon som brukes.

I **Produkter**-delen på siden kan du definere følgende feltverdier for søk etter lagringsgrenser for lokasjon:

- Lager
- Profil-ID for lokasjon
- Lokasjon
- IDen for kategorien for pakkestørrelse
- Varenummer
- Enhet

> [!NOTE]
> Du trenger ikke definere en **enhetsverdi** for post for lagringsgrense for lokasjon. Lokasjonskapasitetsberegningene blir basert på lagerenhetsantallet. Hvis ingen enhetskonvertering er definert for en verdi som brukes, hoppes det over posten for lagringsgrense for lokasjon, som om verdien **Varenummer** er definert for den.

## <a name="example--purchase-order-receiving"></a>Eksempel – Mottak av bestilling

Dette eksemplet er basert på et rent *USMF*-demonstrasjonsdatasett, der følgende verdier angis i fanen **Produktvarianter** på siden **Lagringsgrenser for lokasjon**.

| Lager | Profil-ID for lokasjon | Varenummer | Størrelse | Antall | Enhet |
|-----------|---------------------|-------------|------|----------|------|
| 24        | GULV               | D0013       | M    | 300      | Hver   |
| 24        | GULV               | D0013       | L    | 240      | Hver   |
| 24        | GULV               | D0013       | L    | 360      | Hver   |

Ulike enhetsproduktvarianter defineres for produktene. Disse variantene justeres med lagringsgrensen for lokasjon for tre paller (PL):

- **Størrelse M:** 1 pl = 100 per stykk (Ea)
- **Størrelse L:** 1 pl = 80 Ea
- **Størrelse S:** 1 pl = 120 Ea

Derfor kan alle lokasjoner der verdien **Lokasjonsprofil-ID** er satt til *GULV* kan bære *3* *pl* av varenummer *D0013*.

### <a name="prepare-for-the-example"></a>Forberede for eksemplet

I dette eksemplet skal du kjøre en bestillingsmottaksflyt for to linjer. Du må imidlertid først oppdatere demodataene på følgende måte for å sikre at lokasjonene tillater at blandede varer utføres, bare de tomme lokasjonene *FL-002* til *FL-004* brukes, og det ikke er noe åpent innkommende arbeid.

1. For lokasjon *FL-001* endrer du verdien for feltet **Lokasjonsprofil** fra *GULV* til *GULV-05*.
1. For *GULV*-lokasjonsprofilen setter du alternativet **Tillat blandede varer** til *Ja*.
1. Opprett en bestillingslinje som har følgende to linjer.

    | Lager | Varenummer | Størrelse | Antall | Enhet |
    |-----------|-------------|------|----------|------|
    | 24        | D0013       | L    | 4        | PL   |
    | 24        | D0013       | L    | 4        | PL   |

### <a name="process-the-example"></a>Behandle eksemplet

Du vil først motta et antall på *4* av enheten *PL* i størrelse *S*, og se over plasseringslinjelokasjonene for arbeidet som opprettes. Du vil deretter motta et antall på *4* av enheten *PL* i størrelse *L*, og se over plasseringslinjelokasjonene for arbeidet som opprettes.

1. I lagerappen logger du deg på ved å bruke *24* som bruker-ID og *1* som passord.
1. Velg **Inngående** \> **Kjøpsmottak**.
1. Motta *4* *PL* av varenummer *D0013* i størrelse *S*.
1. Se gjennom det plasseringsarbeidet som ble opprettet. Du skal se følgende resultat:

    - 3 PL -\> FL-002
    - 1 PL -\> FL-003

1. Motta *4* *PL* av varenummer *D0013* i størrelse *L*.
1. Se gjennom det plasseringsarbeidet som ble opprettet. Du skal se følgende resultat:

    - 1 PL -\> FL-003
    - 3 PL -\> FL-004

Basert på resultatene kan du kanskje anta at systemet ikke kunne tildele riktige plasseringslokasjoner. Hvis ikke hvorfor førte systemet bare *1* *PL* av størrelse *L* til lokasjon *FL-003* i siste trinn, ikke *2* *PL*? Det vil si hvorfor er det ikke totalt *3* *PL* for plassering til denne lokasjonen?

Hvis du vil forklare denne tydelige feilen, må du forstå utvalgskriteriene for lagringsgrensene for lokasjon. Systemet velger den mest detaljerte samsvarende posten. I dette eksemplet er den mest detaljerte samsvarende posten linjen der **Størrelse**-verdien er *L*, **Antall**-verdien er *240*, og **Enhet**-verdien er *Ea*. Siden du allerede har åpent arbeid fra forrige mottak av et antall på *120* *Ea* av størrelse *S*, er den gjenstående kapasiteten beregnet som *240* – *120* = *120* *Ea*. Derfor kan gjenstående kapasitet bare bære *1* *PL* av *80* *Ea*.

> [!NOTE]
> Du kan ikke bruke lagringsgrenser for lokasjon til å styre for eksempel etterfylling av varer som har ulike antall på samme lokasjon. I dette tilfellet bruker du en *etterfyllingsmal*.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]