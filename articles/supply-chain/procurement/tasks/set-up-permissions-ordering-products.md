---
title: Definere tillatelser for bestilling av produkter på vegne av andre
description: Denne artikkelen forklarer hvordan du gir arbeidere tillatelse til å klargjøre innkjøpsrekvisisjoner på vegne av andre arbeidere.
author: GalynaFedorova
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: PurchReqAuthorization, HcmWorkerLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3053f28fdf97637b1da5f644f64676bfd10fb6a0
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8854217"
---
# <a name="set-up-permissions-for-ordering-products-on-behalf-of-someone-else"></a>Definere tillatelser for bestilling av produkter på vegne av andre

[!include [banner](../../includes/banner.md)]

Denne artikkelen forklarer hvordan du gir arbeidere tillatelse til å klargjøre innkjøpsrekvisisjoner på vegne av andre arbeidere. Med andre ord kan en innkjøpsrekvisisjonsklargjører opprette en rekvisisjon for en annen "bestiller". Prosedyren viser også hvordan du kan gi arbeidere tillatelse til å bestille varer og tjenester i andre juridiske enheter eller driftsenheter. Disse oppgavene utføres vanligvis av en innkjøpssjef. Du kan bruke denne fremgangsmåten i demonstrasjonsdatafirmaet USMF eller på dine egne data.


## <a name="grant-permission-to-enter-purchase-requisitions-on-behalf-of-another-worker"></a>Gi tillatelser til å registrere innkjøpsrekvisisjoner på vegne av en annen arbeider
1. I navigasjonsruten går du til **Moduler > Innkjøp og leverandører > Oppsett > Policyer > Innkjøpsrekvisisjonstillatelser**. Kontroller at feltet **Gjeldende visning** er satt til **Etter klargjører**. Listen i ruten til venstre, viser personene som kan gis tillatelse til å klargjøre rekvisisjoner på vegne av andre.  
2. Velg personen som skal gis tilgang (klargjøreren).
3. Velg **Legg til**.
4. Finn og velg personen som skal legges til som en bestiller.
    - Bestilleren er personen som klargjøreren kan opprette rekvisisjoner på vegne av.  
    - I feltet **Autorisasjon**, velger du **Bestemte** hvis klargjøreren skal kunne opprette innkjøpsrekvisisjoner på vegne av den valgte arbeideren. Velg **Rapportering** hvis klargjøreren også skal kunne opprette innkjøpsrekvisisjoner på vegne av alle arbeidere som rapporterer til denne arbeideren.  
5. Angi en dato i **Gyldig**-feltet.
6. Angi en dato i **Utløp**-feltet.

## <a name="view-preparers-who-have-permission-to-create-purchase-requisitions-for-a-selected-worker"></a>Vise klargjørerne som har tillatelse til å opprette innkjøpsrekvisisjoner for en valgt arbeider
1. Velg **Etter bestiller** i feltet **Gjeldende visning**. Denne visningen viser en liste over klargjørere som er gitt tillatelse til å opprette innkjøpsrekvisisjoner på vegne av en valgt arbeider.  
2. Bruk dette hurtigfilteret til å finne arbeideren som du nettopp la til som bestiller.
3. Velg bestilleren. Klargjørerlisten viser personene som har tillatelse til å bestille varer på vegne av bestilleren, som er valgt i ruten til venstre.  Du kan legge til flere klargjørerne her. Denne visningen lar deg også gi bestilleren tillatelse til å opprette rekvisisjoner i juridiske enheter og driftsenheter som ikke er primær juridisk enhet eller driftsenhet for den aktuelle personen.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]