---
title: Opprette, beregne og postere utdrag for en detaljhandel
description: Denne artikkelen beskriver de manuelle trinnene for å opprette, beregne og postere et utdrag for en butikk.
author: jashanno
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: RetailChannelOperationsWorkspace, RetailStatementTable
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 740857e6a902e21588855eef5e36cac68e560898
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8873284"
---
# <a name="create-calculate-and-post-statements-for-a-retail-store"></a>Opprette, beregne og postere utdrag for en detaljhandel

[!include [banner](../includes/banner.md)]

Denne artikkelen beskriver de manuelle trinnene for å opprette, beregne og postere et utdrag for en butikk. Det finnes også satsvise jobber som kan konfigureres for de samme oppgavene. Du finner fremgangsmåten for å konfigurere og kjøre de satsvise jobbene i andre artikler. Hvis du vil fullføre denne prosedyren, må du ha transaksjoner som ble fullført i POS, og deretter overført til Dynamics 365 Commerce. Denne registreringen bruker firmaet USRT i demonstrasjonsdataene.

1. Velg **Finans for butikk** fra hjemmesiden.
2. Velg **Nytt utdrag**.
3. I **Butikknummer**-feltet velger du et alternativ fra rullegardinlisten.
4. Velg **OK**.
5. **Oppsett**-gruppen inneholder innstillingene som styrer hvilke transaksjoner som inkluderes i utdraget, og hvordan de grupperes i utdragslinjene. Du kan åpne **Oppsett**-gruppen og endre disse innstillingene, eller du kan bruke standardinnstillingene.  
    - Feltet **Utdragsmetode** angir hvordan utdragslinjene skal grupperes.  
    - Velg et stabsmedlem eller en kasse i feltet **Stab/kasse** hvis du vil beregne et utdrag bare for bestemte stabsmedlemmer eller kasser.  
6. Velg et alternativ i **Avslutningsmetode**-feltet.
7. Velg **Beregn utdrag** fra handlingsruten.
8. Velg **Ja**.
    - Når du har beregnet utdraget, skal det være opprettet linjer med totalbeløp for hver betalingsmåte og utdragsmetode som ble brukt.  
    - Angi et opptelt beløp i hver linje hvis den må angis eller oppdateres. Telt opp-feltet fylles ut med beløp fra kasseoppgjør i POS.  
9. Velg **Poster utdrag** fra handlingsruten.
10. Velg **Lukk**.
11. Lukk ruten.
12. Velg **Finans for butikk** på hjemmesiden.
13. Velg kategorien **Posterte utdrag**.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]