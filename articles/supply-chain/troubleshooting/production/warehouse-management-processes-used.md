---
title: Lagerstyringsprosesser brukes for øyeblikket
description: Når du reserverer eller frigir arbeid, kan du få en melding om at lagerstyringsprosesser er i bruk. Rett opp problemet med ett av disse trinnene.
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: bfda2fae824cdc64d722310d20cf16e6306d766c
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477152"
---
# <a name="cant-reserve-or-release-work-because-processes-are-currently-being-used"></a>Kan ikke reservere eller frigi arbeid fordi prosesser i øyeblikket brukes

## <a name="symptoms"></a>Symptomer

Mens du arbeider med atskilt produksjon, får du følgende feilmelding:

> Lagerstyringsprosesser brukes for øyeblikket. Hvis arbeidslinjer ennå ikke er registrert, kan du avbryte opprettet arbeid og eventuelle last- eller forsendelseslinjer, og deretter fortsette med plukkingen eller forsendelsen.

## <a name="cause"></a>Årsak

Dette problemet oppstår hvis du prøver å reservere eller frigi arbeid for en linje, men lagertransaksjonen har statusen *Plukket*, som indikerer at materialet er plukket.

## <a name="resolution"></a>Løsning

Følg en av fremgangsmåtene nedenfor for å løse problemet.

- Endre statusen for produksjonsordren tilbake til *Estimert* eller *Frigitt*.
- Åpne siden med detaljer for den relevante produksjonsordren. I handlingsruten i **Lager**-fanen i **Stopp**-gruppen velger du **Stopp og legg tilbake** for å oppheve plukking av alle plukkede transaksjoner. Velg deretter **Fjern stopp** for å behandle produksjonsordren.

Her er en forklaring på funksjonene *Legg tilbake* og *Stopp*:
  
- **Legg tilbake** – Denne funksjonen tilbakefører statusen for lagertransaksjoner for stykklistelinjer og formellinjer som har statusen *Plukket* via *I ordre*. Når arbeid for plukking av råvarer er fullført, settes statusen for linjene til *Plukket*. Denne statusen hindrer at produksjonsordren tilbakestilles til statusen *Opprettet*. I dette tilfellet kan du bruke *Legg tilbake*-funksjonen til å tilbakeføre transaksjonene fra statusen *Plukket*, og deretter tilbakestille produksjonsordren til statusen *Opprettet*.
- **Stopp** – Denne funksjonen angir et **Stoppet**-flagg på produksjonsordren for å hindre statusoppdateringer på ordren. Du finner **Stoppet**-flagget i hurtigfanen **Lager** på siden for produksjonsordredetaljer.

> [!NOTE]
>
> - Knappene vises bare når produksjonsordren opprettes for varer som er aktivert for lagerprosesser.
> - **Stopp**-gruppen vises bare i fanen **Lager** i handlingsruten på siden for detaljer om produksjonsordre. Den vises ikke i hurtigfanen **Lager** på listesiden **Produksjonsordrer**.
