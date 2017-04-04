---
title: Definere anleggsmidler
description: Dette emnet gir en oversikt over oppsett av anleggsmiddelmodulen.
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 13771
ms.assetid: 8be64197-fea1-4a34-8af2-d939919c28b1
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: b41901d573e977a89fcd1a7c1ebf7185e162c654
ms.openlocfilehash: dde8053df96d03c8c8e52fa6d2fdf7f74e95ec92
ms.lasthandoff: 03/31/2017


---

# <a name="set-up-fixed-assets"></a>Definere anleggsmidler

Dette emnet gir en oversikt over oppsett av anleggsmiddelmodulen.

<a name="overview"></a>Oversikt
--------
Parametere kontrollerer den generelle virkemåten i anleggsmidler.

Med anleggsmiddelgrupper kan du gruppere aktiva og angi standardattributter for hvert anleggsmiddel som er tilordnet til en gruppe. Tablåer er tilordnet til anleggsmiddelgrupper. Tablåer sporer den økonomiske verdien av et anleggsmiddel over tid med avskrivningskonfigurasjonen som er definert i avskrivningsprofilen.

Anleggsmidler blir tilordnet til en gruppe når de opprettes. Som standard tilordnes deretter tablåer som er tilordnet anleggsmiddelgruppen, til anleggsmidlet. Tablåer som er konfigurert til å postere til økonomimodulen, er tilknyttet en posteringsprofil. Finanskontoer er definert per tablå i posteringsprofilen, og brukes ved postering av anleggsmiddeltransaksjoner. 

![Bilde av komponenter for anleggsmiddel](./media/FAComponents_Updated.png)

## <a name="depreciation-profiles"></a>Avskrivningsprofiler
Du bør definere avskrivningsprofiler først. I avskrivningsprofilen kan du konfigurere hvordan en anleggsmiddelverdi avskrives over tid. Du må definere metoden for avskrivning, avskrivningsåret (kalenderår eller regnskapsår) og frekvensen for avskrivning.

## <a name="books"></a>Tablåer
Etter at du har definert avskrivningsprofiler, må du opprette de nødvendige tablåene for anleggsmidlene. Hvert tablå sporer en uavhengig økonomisk livssyklus for et anleggsmiddel. Tablåer kan konfigureres til å postere tilknyttede transaksjoner til økonomimodulen. Denne konfigurasjonen er standardinnstillingen, fordi den brukes vanligvis for bedrifts finansrapportering. Bøker som ikke postere til finans poster bare for anleggsmiddel-underfinansjournal og brukes vanligvis for mva-rapporteringsformål.

En primær avskrivningsprofil er tilordnet til hvert tablå. Tablåer har også en alternativ avskrivningsprofil, hvis denne typen profil brukes. Hvis du vil inkludere anleggsmiddeltablået i avskrivninger automatisk, må du aktivere alternativet Beregner avskrivning. Hvis dette alternativet ikke er valgt for et anleggsmiddel, hopper avskrivningsforslaget aktivaet.

Du kan også sette opp avledede tablåer. De angitte avledede transaksjonene blir postert som en nøyaktig kopi av den primære transaksjonen mot de avledede tablåene. Derfor defineres avledede transaksjoner vanligvis for anskaffelse og salg, ikke for avskrivningstransaksjoner.

## <a name="fixed-asset-posting-profiles"></a>Posteringsprofiler for anleggsmidler
Når du har definert tablåer, kan du opprette posteringsprofilen. Posteringsprofilen må defineres av tablået, men den kan også defineres på et mer detaljert nivå. Du kan for eksempel definere posteringsprofilen for kombinasjonen av et tablå og en anleggsmiddelgruppe, eller til og med for et enkelt anleggsmiddeltablå. Som standard brukes finanskontoene som er definert, for transaksjoner for anleggsmidler.

Du må definere finanskontoene som skal brukes ved avhending, både avhendingssalg eller avhendingssvinn. Tidligere posterte anleggsmiddeltransaksjonene tilbakeføres ut av de opprinnelige kontoene ved avhending, og nettobeløpet flyttes til riktig konto for fortjeneste og tap for avhending av anleggsmidler. For å garantere at transaksjoner tilbakeføres på riktig måte, må du definere kontoer for hver transaksjonstype som du bruker i firmaet. Hovedkontoen skal være den opprinnelige hovedkontoen du angir i posteringsprofilen for transaksjonstypen, og motkontoen skal være avhendingskontoen for fortjeneste og tap. Unntaket er netto bokført verdi. I så fall skal både hovedkontoen og motkontoen settes til avhendingskontoen for fortjeneste og tap.

## <a name="fixed-asset-groups"></a>Anleggsmiddelgrupper
Anleggsmiddelgruppe er det eneste obligatorisk feltet når du oppretter et anleggsmiddel. Verdien i dette feltet angir standardverdien for flere informasjonsfelt for anleggsmidlet. Tablåer settes opp slik at et standardtablå er tilordnet til hvert anleggsmiddel i en gruppe. Du kan deretter angi attributter for tablåer som er spesifikke for en gruppe anleggsmidler, for eksempel Levetid og Avskrivningskonvensjon.

Du kan også definere særskilte avskrivningsfradrag eller bonusavskrivning for en bestemt kombinasjon av en anleggsmiddelgruppe og et tablå. Du må tilordne en prioritet til det særskilte avskrivningsfradraget for å angi rekkefølgen som fradrag beregnes i når flere fradrag er tilordnet til et tablå.

## <a name="fixed-asset-parameters"></a>Parametere for anleggsmidler
Det siste trinnet er å oppdatere parameterne for anleggsmidler.

Feltet Kapitaliseringsterskel bestemmer hvilke anleggsmidler som avskrives. Hvis en innkjøpslinje er merket som et anleggsmiddel, men den ikke oppfyller de angitte kapitaliseringsterskelen, et anleggsmiddel opprettes eller oppdateres fortsatt, men alternativet Beregn avskrivning er satt til Nei. Anleggsmidlet avskrives ikke derfor automatisk som en del av avskrivningsforslagene.

Ett viktig alternativ er Opprett automatisk avskrivningsjusteringsbeløp med avhending. Når du setter dette alternativet til Ja, justeres anleggsmiddelavskrivningen automatisk, basert på innstillingene for avskrivning ved avhending av anleggsmidler. Et annet alternativ lar deg trekke fra kontantrabatt fra anskaffelsesbeløpet når du kjøper anleggsmidler ved hjelp av en leverandørfaktura.

I hurtigfanen Bestillinger kan du konfigurere hvordan du vil at anleggsmidlene skal opprettes som en del av innkjøpsprosessen. Det første alternativet er Tillat anleggsmiddelanskaffelse fra innkjøp. Hvis du setter dette alternativet til Ja, oppstår anleggsmiddelanskaffelsen når fakturaen posteres. Hvis du setter dette alternativet til Nei, kan du fremdeles plassere et aktiva på en bestilling (Inngående) og en faktura, men posteres ikke anskaffelsen. Postering må gjøres fra anleggsmiddeljournalen som et separat trinn. Opprett aktivaet under produktet mottaksseddel eller faktura alternativet kan du opprette et nytt aktivum "på sparket" under postering, slik at den ikke har kan defineres som et anleggsmiddel før transaksjonen. Det siste alternativet, Søk etter opprettelse av anleggsmidler under linjeregistrering, gjelder bare for innkjøpsrekvisisjoner.

Du kan konfigurere årsakskoder til å være nødvendige for endringer av et anleggsmiddel eller for bestemte anleggsmiddeltransaksjoner.

Til slutt definerer du nummerserier for anleggsmidler i kategorien Nummerserier. Anleggsmiddelnummerserien kan overstyres av gruppenummersekvensen for anleggsmiddelet hvis det er angitt.


