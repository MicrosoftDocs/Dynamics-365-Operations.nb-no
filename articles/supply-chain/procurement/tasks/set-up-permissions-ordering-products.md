--- 
title: "Definere tillatelser for bestilling av produkter på vegne av andre"
description: "Denne fremgangsmåten viser hvordan du gir arbeidere tillatelse til å klargjøre innkjøpsrekvisisjoner på vegne av andre arbeidere."
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PurchReqAuthorization, HcmWorkerLookUp
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 9e003f953c05facd5516e2bfa6d1c83ba6381c15
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-permissions-for-ordering-products-on-behalf-of-someone-else"></a>Definere tillatelser for bestilling av produkter på vegne av andre

[!include [task guide banner](../../includes/task-guide-banner.md)]

Denne fremgangsmåten viser hvordan du gir arbeidere tillatelse til å klargjøre innkjøpsrekvisisjoner på vegne av andre arbeidere. Med andre ord kan en innkjøpsrekvisisjonsklargjører opprette en rekvisisjon for en annen "bestiller". Prosedyren viser også hvordan du kan gi arbeidere tillatelse til å bestille varer og tjenester i andre juridiske enheter eller driftsenheter. Disse oppgavene utføres vanligvis av en innkjøpssjef. Du kan bruke denne fremgangsmåten i demonstrasjonsdatafirmaet USMF eller på dine egne data.


## <a name="grant-permission-to-enter-purchase-requisitions-on-behalf-of-another-worker"></a>Gi tillatelser til å registrere innkjøpsrekvisisjoner på vegne av en annen arbeider
1. Gå til Innkjøp og leverandører > Oppsett > Policyer > Innkjøpsrekvisisjonstillatelser.
    * Kontroller at feltet Gjeldende visning er satt til Etter klargjører.  Listen i ruten til venstre, viser personene som kan gis tillatelse til å klargjøre rekvisisjoner på vegne av andre.  
2. Velg personen som skal gis tilgang (klargjøreren).
3. Klikk Legg til.
4. Finn og velg personen som skal legges til som en bestiller.
    * Bestilleren er personen som klargjøreren kan opprette rekvisisjoner på vegne av.  
    * I feltet Autorisasjon, velger du Bestemte hvis klargjøreren skal kunne opprette innkjøpsrekvisisjoner på vegne av den valgte arbeideren. Velg Rapportering hvis klargjøreren også skal kunne opprette innkjøpsrekvisisjoner på vegne av alle arbeidere som rapporterer til denne arbeideren.  
5. Angi en dato i Gyldig-feltet.
6. Angi en dato i Utløp-feltet.

## <a name="view-preparers-who-have-permission-to-create-purchase-requisitions-for-a-selected-worker"></a>Vise klargjørerne som har tillatelse til å opprette innkjøpsrekvisisjoner for en valgt arbeider
1. Velg Etter bestiller i feltet Gjeldende visning.
    * Denne visningen viser en liste over klargjørere som er gitt tillatelse til å opprette innkjøpsrekvisisjoner på vegne av en valgt arbeider.  
2. Bruk dette hurtigfilteret til å finne arbeideren som du nettopp la til som bestiller.
3. Velg bestilleren.
    * Klargjørerlisten viser personene som har tillatelse til å bestille varer på vegne av bestilleren, som er valgt i ruten til venstre.   Du kan legge til flere klargjørerne her.   Denne visningen lar deg også gi bestilleren tillatelse til å opprette rekvisisjoner i juridiske enheter og driftsenheter som ikke er primær juridisk enhet eller driftsenhet for den aktuelle personen.  


