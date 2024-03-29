---
title: Bonusavskrivning
description: Denne artikkelen gir en oversikt over funksjonaliteten for bonusavskrivning.
author: moaamer
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetBonus
audience: Application User
ms.reviewer: kfend
ms.custom: 3621
ms.assetid: 835ec594-744e-461c-a676-1b9abc094173
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 801747f06d16e70cd04b727787f0bfa6b6baefc0
ms.sourcegitcommit: 04e6c1c9400e1b582180cf3e0e4767434e736c26
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/05/2022
ms.locfileid: "8711152"
---
# <a name="bonus-depreciation"></a>Bonusavskrivning

[!include [banner](../includes/banner.md)]

Denne artikkelen gir en oversikt over funksjonaliteten for bonusavskrivning.

For bonusavskrivning kan du ta ekstra- eller bonusavskrivningsbeløp i det første året som anleggsmidlet brukes og avskrives. Bonusavskrivning må utføres før alle andre avskrivningsberegninger. Derfor er det best å bruke bonusavskrivning med tablåer der funksjonen Poster i økonomimodul er deaktivert. Du kan bruke alternativet **Slett transaksjoner som ikke er postert til økonomimodulen** for å slette historiske transaksjoner for tablåer som ikke posterer til økonomimodulen. Du kan deretter bruke bonusavskrivning senere i livssyklusen til aktiva ved å slette avskrivningstransaksjoner som allerede er postert. 

Du kan beregne bonusavskrivning ved hjelp av forslagsprosessen, eller du kan opprette manuelle bonusavskrivningstransaksjoner. Du kan ikke opprette bonusavskrivningstransaksjoner hvis det finnes avskrivningstransaksjoner eller avskrivningsjusteringstransaksjoner for dette tablået for anleggsmiddel.

Når du bruker forslagsprosessen til å beregne bonusavskrivning, inkluderes alle eksisterende bonustransaksjoner i beregningen av grunnlaget. Beregningen omfatter også alle tidligere bonusavskrivninger som du har angitt manuelt for anleggsmiddelet. 

Hvis mer enn én bonusavskrivning skal utføres for et anleggsmiddel, tas det hensyn til prioritet. Hver bonus reduserer anleggsmiddelgrunnlaget for den neste bonusen. Restverdien vurderes ikke i anleggsmiddelgrunnlaget for beregning av bonusavskrivning, og avskrivningskonvensjonen gjelder ikke for bonusavskrivning. 

I USA kvalifiserer noen eiendommer som Section 179-eiendom. Ved å bruke Section 179-fradraget kan du gjenopprette hele eller deler av kostnaden for noen eiendommer, opptil en grense. Du kan gjenopprette kostnaden ved å trekke det fra i året der du setter i drift eiendommen.

## <a name="example"></a>Eksempel
Følgende bonusavskrivninger er knyttet til et tablå for anleggsmiddel:

-   **Section 179:** 1 000,00, Prioritet 1
-   **Liberty Zone:** 30 prosent, prioritet 2

Kostnaden for anleggsmiddelanskaffelse er 5 000,00. Når bonusavskrivning beregnes, er det første bonusavskrivningsbeløpet 1 000,00 for Section 179-avskrivningen. 

Det neste bonusavskrivningsbeløpet for Liberty Zone-avskrvningen, beregnes som følger: 

Anskaffelseskostnad – 1 000 (Section 179-avskrivning) × 30 prosent = 1 200 

Hvis bonusavskrivningsbeløpet er større enn den gjenstående anskaffelseskostnaden, er bonusavskrivningsbeløpet resultatet av bonusavskrivningsberegningen eller den gjenværende anskaffelseskostnaden, eller det beløpet som er minst. 

Hvis den gjenstående anskaffelseskostnaden er 0 (null) eller mindre, genereres det ikke bonusavskrivningstransaksjoner. 

Når bonusavskrivning beregnes ved av forslagsprosessen, opprettes det en bonusavskrivningstransaksjon for alle bonusavskrivningspostene som er tilknyttet tablået for anleggsmiddel. 

Du kan opprette et ubegrenset antall bonusavskrivningsposter. Når du har tildelt disse postene til tablået for anleggsmiddelgruppe, brukes de for anleggsmiddeltablået. 

Bonusavskrivning angis som en prosent eller et fast beløp. Når du posterer avskrivningsforslag, posteres bonusavskrivningstransaksjoner til tablået som transaksjoner som er atskilte fra avskrivningstransaksjonene.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
