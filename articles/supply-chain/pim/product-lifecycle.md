---
title: Oversikt over tilstand for produktlivssyklus
description: Livssyklustilstand for produkter dokumenterer livssyklustilstanden til et frigitt produkt eller produktvariant.
author: cvocph
manager: tfehr
ms.date: 01/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductLifecycleState, EcoResReleasedProductLifecycleStateChanges
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: conradv
ms.dyn365.ops.version: 7.2999999999999998
ms.search.validFrom: 2017-12-31
ms.openlocfilehash: 7889f1d21bf38a9063fff6a64da50febd15df5d6
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/02/2020
ms.locfileid: "3209450"
---
# <a name="product-lifecycle-state-overview"></a>Oversikt over tilstand for produktlivssyklus

[!include [banner](../includes/banner.md)]

Livssyklustilstand for produkter dokumenterer livssyklustilstanden til et frigitt produkt eller produktvariant. Produktlivssyklustilstander defineres av brukeren, vanligvis produktsjefen eller ansvarlig for produktstandarddata. Bestemte forretningsprosesser, for eksempel hovedplanlegging, kan påvirkes av en bestemt livssyklustilstand.   

Et frigitt produkt eller produktvariant kan knyttes til en produktlivssyklustilstand som dokumenterer hvilken livssyklustilstand et bestemt produkt eller en variant befinner seg i. Du kan definere antall produktlivssyklustilstander ved å tilordne statusnavn og beskrivelse. Du kan velge én livssyklustilstand som standardinnstilling for nye frigitte produkter. Frigitte produktvarianter arver produktlivssyklustilstanden fra deres frigitte produktstandard ved oppretting. Når du endrer livssyklustilstanden for en frigitt produktstandard, kan du velge å oppdatere alle eksisterende varianter som har samme opprinnelige tilstand.  

## <a name="create-a-new-product-lifecycle-state"></a>Opprette en ny livssyklustilstand for produkt 

- Hvis du vil opprette en ny produktlivssyklustilstand, spiller eller leser du oppgaveveiledningen **Opprette en ny livssyklustilstand for produkt**. 

-  Hvis du vil opprette en standard produktlivssyklustilstand, spiller eller leser du oppgaveveiledningen **Opprette en standard livssyklustilstand for produkt**.   

## <a name="associate-product-lifecycle-states-to-released-products"></a>Knytte produktlivssyklustilstander til frigitte produkter  

Det finnes flere måter å knytte en produktlivssyklustilstand til frigitte produkter og produktvarianter.

-  Ved oppretting av et nytt frigitt produkt tilordnes standard **livssyklustilstand for produkt** automatisk. 
-  Ved frigivelse av et produkt til en juridisk enhet tilordnes standard **livssyklustilstand for produkt** automatisk. 
-  Ved frigivelse av en produktvariant til en juridisk enhet tilordnes **livssyklustilstanden for produkt** som er knyttet til den frigitte produktstandarden i denne juridiske enheten, automatisk til den nye varianten. 

Du kan oppdatere produktlivssyklustilstanden manuelt ved hjelp av: 

-    **Frigitte produkter**-listesiden eller **Detaljvisning**. 
-  **Frigitte produktvarianter**-listesiden eller **Detaljvisning**. 
-  Finn utdaterte produkter eller produktvarianter basert på behov og tilknytt en livssyklustilstand.  

Hvis du vil ha mer informasjon om hvordan du tilknytter produktlivssyklustilstander, spiller du av eller leser følgende to oppgaveveiledninger.

-  Hvis du vil knytte en produktlivssyklustilstand til en frigitt produktstandard, spiller du av eller leser oppgaveveiledningen **Tilordne en produktlivssyklustilstand til en frigitt produktstandard**. 

-  Hvis du vil knytte en produktlivssyklustilstand til et frigitt produkt, spiller du av eller leser oppgaveveiledningen **Tilordne en produktlivssyklustilstand til et frigitt produkt**. 

## <a name="impact-on-master-planning"></a>Påvirkning på hovedplanlegging 

Produktlivssyklustilstanden har bare ett kontrollflagg: **Er aktiv for planlegging**. Som standard er dette satt til **Ja** for alle opprettede produktlivssyklustilstander, men det kan endres til **Nei**. Hvis du angir **Nei**, er de tilknyttede frigitte produktene eller frigitte produktvariantene: 

-  Utelatt fra hovedplanlegging. 
-  Ekskludert fra beregning av stykklistenivå. 

Hvis du vil ha mer informasjon om hvordan du bruker produktlivssyklustilstand for å utelate produkter fra hovedplanlegging og stykklistenivåberegning, spiller du av eller leser oppgaveveiledningen **Opprette en produktlivssyklustilstand for å utelukke produkter fra hovedplanlegging**.

> [!NOTE]
> Av hensyn til ytelsen anbefales det å knytte alle foreldede frigitte produkter eller produktvarianter, spesielt når du arbeider med ikke-gjenbrukbare produktkonfigurasjonsvarianter, til en produktlivssyklustilstand som er deaktivert for hovedplanlegging.  

## <a name="default-migration-import-and-export"></a>Standard overføring, import og eksport 

Produktlivssyklustilstandene støttes ikke av dataenheter, og livssyklustilstanden kan settes til variabel tilstand via den frigitte produktdataenheten eller den frigitte variantdataenheten.

## <a name="find-obsolete-products-and-products-variants"></a>Finn foreldede produkter og produktvarianter 

Du kan kjøre en simuleringsanalyse for å finne de foreldede frigitte produktene eller produktvariantene og deretter oppdatere produktlivssyklusstatusen deres. Hvis du vil finne utdaterte produkter, kan du spille av eller lese oppgaveveiledningen **Finne utdaterte produktvarianter og tilordne en produktlivssyklustilstand**. Denne oppgaveveiledningen viser hvordan du finner foreldede frigitte produkter og produktvarianter og hvordan du knytter en produktlivssyklustilstand til de foreldede produktene. Den viser også hvordan du viser simuleringsresultatene og vurderer hvor mange produkter og produktvarianter som skal være tilknyttet en ny produktlivssyklustilstand når du kjører oppdateringen uten simulering.  

Ved å kjøre analysen i simuleringsmodus vises produktene og produktvariantene som er identifisert som foreldede, i et bestemt skjema, der de kan lett kan gjennomgås. Analysen søker etter transaksjoner og bestemte hoveddata for å identifisere produkter som ikke har etterspørsel i en variabel periode, og ingen hoveddata som kan føre til etterspørsel. Ny frigitte produkter i en variabel periode kan utelates fra analysen. Når analysesimuleringen returnerer det forventede resultatet, kan brukeren kjøre analysen og angi en ny produktlivssyklustilstand for alle produkter som er identifisert som foreldede i analysen.  

> [!NOTE]
> Vær oppmerksom på at alle analyser og oppdateringer må gjøres innenfor samme juridiske enhet.  

## <a name="criteria-to-select-and-update-released-products-or-product-variants"></a>Kriterier for å velge og oppdatere frigitte produkter og produktvarianter 

Bruk følgende kriterier for å velge og oppdatere de frigitte produktene og produktvariantene: 

-    Produktlivssyklustilstanden for produktet eller produktvarianten må være forskjellig fra den nye ønskede tilstanden. 
-  Produktet eller produktvarianten ble opprettet for noen dager siden basert på antallet dager du angir i dialogboksen for valg. 
-  Det finnes ingen åpne produksjonsordrer (= status < avsluttet) for produktet eller produktvarianten. 
-  Det finnes ingen åpne lagertransaksjoner (= status problem ReservPhysical til QuotationIssue eller status mottak Registrered til QuotationReceipt) for produktet eller produktvarianten. 
-  Det finnes ingen lagertransaksjoner i løpet av de siste antall dagene for produktet eller produktvarianten. 
-  Det finnes ikke noe fremtidig behov eller forsyningsprognose for produktet eller produktvarianten.  
-  Minimumsnivå for lager er ikke angitt i varedekning for produktet eller produktvarianten. 
-  Ingen aktiv kanban-regel for fast antall for produktet eller produktvarianten.  
-  Ingen serviceordrelinje for produktet eller produktvarianten. 
-  Ingen aktive eller fremtidige salgs- eller kjøpsavtalelinjer for produktet eller produktvarianten. 
-  Produktet eller produktvarianten brukes ikke i en stykkliste som er knyttet til en ikke-utløpt godkjent stykklisteversjon for et produkt eller en variant som er aktivert for planlegging.

## <a name="related-topics"></a>Relaterte emner

-  [Opprette en ny livssyklustilstand for produkt](tasks/new-product-lifecycle-state.md)
-  [Opprette en standard livssyklustilstand for produkt](tasks/default-product-lifecycle-state.md)
-  [Tilordne en tilstand for produktlivssyklus til en utgitt produktstandard](tasks/product-lifecycle-state-released-product-master.md)
-  [Tilordne en tilstand for produktlivssyklus til et utgitt produkt](tasks/product-lifecycle-state-released-product.md)
-  [Finne utdaterte produktvarianter og tilordne en produktlivssyklustilstand](tasks/obsolete-product-variants.md)
-  [Opprette en produktlivssyklustilstand for å utelukke produkter fra hovedplanlegging](tasks/exclude-products-master-planning.md)
