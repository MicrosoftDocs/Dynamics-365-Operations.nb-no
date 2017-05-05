---
title: Administrere lagermedarbeidere
description: "Denne artikkelen beskriver hvordan du kan bruke Microsoft Dynamics AX for å kontrollere og overvåke arbeidet som utføres av ansatte i lagrene."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: HcmWorker, InventLocation, WHSLaborStandards, WHSWorker, WHSWorkTable, WHSWorkTableListPage
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 72891
ms.assetid: feaa6f15-49d2-41f5-9b87-453463c52e4e
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: f77012e7b64b7f153103e9bbe91e8ded202b509a
ms.openlocfilehash: b63ec70a7d02d23ccdc9fd295a65431ac6b012ba
ms.lasthandoff: 03/31/2017


---

# <a name="manage-warehouse-workers"></a>Administrere lagermedarbeidere

[!include[banner](../includes/banner.md)]


Denne artikkelen beskriver hvordan du kan bruke Microsoft Dynamics AX for å kontrollere og overvåke arbeidet som utføres av ansatte i lagrene.

Hvis du bruker funksjonaliteten i Lagerstyring, refereres alle lagerarbeideroperasjoner til som *arbeid*. Arbeid, for eksempel plukking, flytting og telling av lagerbeholdningen, registreres ved hjelp av mobilenheter. Før en lagermedarbeider kan utføre arbeidet må han eller hun være knyttet til en arbeider i Personale. Hver **arbeider**-konto kan ha flere lagerarbeidsbrukere tilknyttet. Disse arbeidsbrukerene kan arbeide i forskjellige lagre og kan ha ulike tilgangsnivåer til de ulike mobilenhetsmenyene. Du kan tenke på lagerarbeidsbrukerne som flere pålogginger for den valgte arbeideren. Hver arbeidsbruker har et standardlager, og bestemte arbeidsflyter vises av menyeelementene som er tilgjengelig for denne arbeidsbrukeren. 

For å opprette en ny arbeidsbruker velger du siden **Arbeidere**, kategorien **Generelt**, delen **Lagre** og klikker **Arbeider**. Du må angi en bruker-ID, et brukernavn, et standardlager og et menynavn. Denne menyen lastes inn når brukeren logger på portalen for lagermobilenheter og lar deg definere hvilke menyelementer brukeren har tilgang til. 

Som en del av oppsettet for hver arbeidsbruker kan du også definere bestemte prosessarbeidsflyter. Du kan for eksempel bruke feltet **Er en syklustellingsansvarlig** for å angi om brukeren kan behandle justeringer av syklustellingsavvik under en tellingsoperasjon eller om disse justeringene først må vurderes av en annen person.

## <a name="defining-labor-standards"></a>Definere arbeidsstandarder
Siden **Arbeidsstandarder** lar deg definere beregningsmetodene som systemet bruker til å beregne den estimerte tiden som en bestemt type arbeid skal kreve. Du kan angi denne definisjonen på et generelt nivå eller på et bestemt nivå. Du kan for eksempel definere tiden som er nødvendig for å behandle en salgsordreplukking per vekt for en bestemt enhetsdefinisjon når en bestemt plukkeprosess brukes. Samtidig kan du registrere tiden, basert på en annen beregningsmåte, for plasseringsoperasjonen for lagerbeholdningen som er plukket. 

Hvis du vil aktivere arbeidsstandardene som du har definert, må du velge alternativet **Tillat arbeidsstandarder** for hvert lager der arbeidsstandarder vil bli brukt.

## <a name="monitoring-and-controlling-warehouse-work"></a>Overvåke og kontrollere lagerarbeid
Siden **Alt arbeid** lar deg overvåke og vedlikeholde alt arbeid som er planlagt, pågår og fullført. Du kan oppdatere forskjellige prosesser, for eksempel tilordninger for lagerarbeidsbruker og arbeidsprioritet fra denne siden. Du kan også drille ned til detaljene som er knyttet til arbeidshodet og arbeidslinjene, for å få en forståelse av de forventede eller fullførte arbeidsprosessene. 

Hvis du aktiverer alternativet **Arbeidsstandarder**, kan du se den beregnede estimerte tiden for jobben. Deretter, når arbeidet er behandlet, vises også faktisk tid for hver arbeidsoperasjon. På denne måten kan du sammenligne beregningene av anslått tid med faktisk tid. 

Du kan også bruke den estimerte tiden i reglene for automatisk å dele opp arbeid under arbeidsopprettelse. På denne måten kan du belastningsfordele arbeid basert på forventet tid for å fullføre oppgavene. 

Analyse av tiden som brukes til å behandle arbeidselementer kan hjelpe oppnå forbedringer av lagermedarbeideres effektivitet. Følgende rapporter er tilgjengelige for å hjelpe deg med denne analysen:

-   **Arbeid etter bruker** – Denne rapporten viser arbeiderproduktivitet, basert på faktisk tid mot forventet tid.
-   **Arbeid etter arbeidstransaksjonstype** – Du kan bruke denne rapporten til å undersøke ineffektivitet i bestemte lagerprosesser. Anta for eksempel at du legger merke til at plukk for overføringsordrer tar lengre tid denne uken enn i tidligere uker. Du kan deretter bruke denne informasjonen for ytterligere undersøkelse.




