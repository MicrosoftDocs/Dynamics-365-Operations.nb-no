---
title: Definere anleggsmidler
description: Dette emnet gir en oversikt over oppsettet av anleggsmiddelmodulen.
author: moaamer
ms.date: 06/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 13771
ms.assetid: 8be64197-fea1-4a34-8af2-d939919c28b1
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9c26b45fc94d9983157eef9af5c0af6845d24056
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/06/2021
ms.locfileid: "6356757"
---
# <a name="set-up-fixed-assets"></a>Definere anleggsmidler

[!include [banner](../includes/banner.md)]

Dette emnet gir en oversikt over oppsettet av **Anleggsmiddel**-modulen. 

Parametere kontrollerer den generelle virkemåten i anleggsmidler. Med anleggsmiddelgrupper kan du gruppere aktiva og angi standardattributter for hvert anleggsmiddel som er tilordnet til en gruppe. Tablåer er tilordnet til anleggsmiddelgrupper. Tablåer sporer den økonomiske verdien av et anleggsmiddel over tid med avskrivningskonfigurasjonen som er definert i avskrivningsprofilen.

Anleggsmidler blir tilordnet til en gruppe når de opprettes. Som standard tilordnes deretter tablåer som er tilordnet anleggsmiddelgruppen, til anleggsmidlet. Tablåer som er konfigurert til å postere til økonomimodulen, er tilknyttet en posteringsprofil. Finanskontoer er definert for hvert tablå i posteringsprofilen, og brukes ved postering av anleggsmiddeltransaksjoner.

![Anleggsmiddelkomponenter.](./media/FAComponents_Updated.png)

## <a name="depreciation-profiles"></a>Avskrivningsprofiler

Du bør først definere avskrivningsprofiler. I avskrivningsprofilen kan du konfigurere hvordan en anleggsmiddelverdi avskrives over tid. Du må definere metoden for avskrivning, avskrivningsåret (kalenderår eller regnskapsår) og frekvensen for avskrivning. Hvis du vil ha mer informasjon, kan du se [Definere og opprette avskrivningsprofiler](tasks/set-up-depreciation-profiles.md).

## <a name="books"></a>Tablåer

Etter at du har definert avskrivningsprofiler, må du opprette de nødvendige tablåene for anleggsmidlene. Hvert tablå sporer en uavhengig økonomisk livssyklus for et anleggsmiddel. Tablåer kan konfigureres til å postere tilknyttede transaksjoner til økonomimodulen. Denne konfigurasjonen er standardinnstillingen, fordi den brukes vanligvis for firmaets finansrapportering. Tablåer som ikke posterer til økonomimodulen, posterer bare til underfinansjournalen for anleggsmiddel, og brukes vanligvis for skatteformål.

En primær avskrivningsprofil er tilordnet til hvert tablå. Tablåer har også en alternativ avskrivningsprofil, hvis denne typen profil brukes. Hvis du vil inkludere anleggsmiddeltablået i avskrivninger automatisk, må du aktivere alternativet **Beregner avskrivning**. Hvis dette alternativet ikke er aktivert for et anleggsmiddel, hopper avskrivningsforslaget over anleggsmidlet.

Du kan også sette opp avledede tablåer. De angitte avledede transaksjonene blir postert mot de avledede tablåene som en nøyaktig kopi av den primære transaksjonen. Derfor defineres avledede transaksjoner vanligvis for anskaffelse og salg, ikke for avskrivningstransaksjoner. Hvis du vil ha mer informasjon, kan du se [Definere verdimodeller](tasks/set-up-value-models.md).

Du kan bruke et alternativ på siden **Parametere for anleggsmidler** til å aktivere eller deaktivere låsefunksjonaliteten. Du kan aktivere denne funksjonen i **Arbeidsområde for funksjonsbehandling**.

## <a name="fixed-asset-posting-profiles"></a>Posteringsprofiler for anleggsmidler

Når du har definert tablåer, kan du opprette posteringsprofilen. Posteringsprofilen må defineres av tablået, men den kan også defineres på et mer detaljert nivå. Du kan for eksempel definere posteringsprofilen for kombinasjonen av et tablå og en anleggsmiddelgruppe, eller til og med for et enkelt anleggsmiddeltablå. Som standard brukes finanskontoene som er definert, for transaksjoner for anleggsmidler.

Du må definere finanskontoene som skal brukes ved avhending, både avhendingssalg eller avhendingssvinn. Tidligere posterte anleggsmiddeltransaksjonene tilbakeføres ut av de opprinnelige kontoene ved avhending. Nettobeløpet flyttes deretter til riktig konto for fortjeneste og tap for avhending av anleggsmidler. For å garantere at transaksjoner tilbakeføres på riktig måte, må du definere kontoer for hver transaksjonstype som du bruker i firmaet. Hovedkontoen skal være den opprinnelige hovedkontoen du angir i posteringsprofilen for transaksjonstypen, og motkontoen skal være avhendingskontoen for fortjeneste og tap. Unntaket er netto bokført verdi. I så fall skal både hovedkontoen og motkontoen settes til avhendingskontoen for fortjeneste og tap. Hvis du vil ha mer informasjon, kan du se [Definere posteringsprofiler for anleggsmidler](tasks/set-up-fixed-asset-posting-profiles.md).

## <a name="fixed-asset-groups"></a>Anleggsmiddelgrupper

**Anleggsmiddelgruppe**-feltet er det eneste obligatorisk feltet når du oppretter et anleggsmiddel. Verdien i dette feltet angir standardverdien for flere informasjonsfelt for anleggsmidlet. Tablåer settes opp slik at et standardtablå er tilordnet til hvert anleggsmiddel i en gruppe. På denne måten kan attributter som du angav for tablåene, være spesifikke for en gruppe anleggsmidler. Disse attributtene omfatter levetiden og avskrivningskonvensjonen.

Du kan også definere særskilte avskrivningsfradrag eller bonusavskrivning for en bestemt kombinasjon av en anleggsmiddelgruppe og et tablå. Du må tilordne en prioritet til det særskilte avskrivningsfradraget for å angi rekkefølgen som fradrag beregnes i når flere fradrag er tilordnet til et tablå. Hvis du vil ha mer informasjon, kan du se [Definere anleggsmiddelgrupper](tasks/set-up-fixed-asset-groups.md).

## <a name="journal-names"></a>Journalnavn

På **Journalnavn**-siden må du opprette journalnavnene som skal brukes til anleggsmiddeljournalen. Du må sette **Journaltype**-feltet til **Poster anleggsmidler**. Angi **Bilagsserie**-feltet slik at journalnavnene blir brukt til anleggsmiddeljournalen. Anleggsmiddeljournaler bør ikke bruke **Bare ett bilagsnummer**-innstillingen fordi et unikt bilagsnummer er obligatorisk for flere automatiserte prosesser, for eksempel overføringer og delinger.

## <a name="fixed-asset-parameters"></a>Parametere for anleggsmidler

Det siste trinnet er å oppdatere parameterne for anleggsmidler.

Feltet **Kapitaliseringsterskel** bestemmer hvilke anleggsmidler som avskrives. Hvis en innkjøpslinje er merket som et anleggsmiddel, men den ikke oppfyller den angitte kapitaliseringsterskelen, opprettes og oppdateres likevel et anleggsmiddel, men alternativet **Beregn avskrivning** er satt til **Ingen**. Anleggsmidlet avskrives derfor ikke automatisk som en del av avskrivningsforslagene.

Ett viktig alternativ heter **Opprett automatisk avskrivningsjusteringsbeløp med avhending**. Når du setter dette alternativet til **Ja**, justeres anleggsmiddelavskrivningen automatisk, basert på innstillingene for avskrivning ved avhending av anleggsmidler. Et annet alternativ lar deg trekke fra kontantrabatt fra anskaffelsesbeløpet når du kjøper anleggsmidler ved hjelp av en leverandørfaktura.

Parameteren **Lås aktivatablåer i en avskrivningsjournal** lar deg låse aktivatablåer i en avskrivningsjournal. Når avskrivningstransaksjoner posteres, kontrollerer systemet at det samme aktivatablået ikke er lagt til i flere enn én avskrivningsjournal. Hvis det er det, låses aktivatablået, og posteringen stopper. Hvis en aktivatablå-ID er i en låst journal, låses den automatisk opp når posteringen er fullført for den originale journalen. Du kan også låse opp journalen manuelt. 

I hurtigfanen **Bestillinger** kan du konfigurere hvordan du vil at anleggsmidlene skal opprettes som en del av innkjøpsprosessen. Det første alternativet heter **Tillat anleggsmiddelanskaffelse fra innkjøp**. Hvis du setter dette alternativet til **Ja**, oppstår anleggsmiddelanskaffelsen når fakturaen posteres. Hvis du setter dette alternativet til **Nei**, kan du fremdeles plassere et anleggsmiddel på en bestilling og faktura, men anskaffelsen posteres ikke. Postering må gjøres fra anleggsmiddeljournalen som et separat trinn. Med **Opprett anleggsmiddel under postering av mottaksseddel eller faktura**-alternativet kan du opprette nye aktiva "på direkten" under posteringen. Derfor trenger ikke anleggsmiddelet defineres som et anleggsmiddel før transaksjonen. Det siste alternativet, **Søk etter opprettelse av anleggsmidler under linjeregistrering**, gjelder bare for innkjøpsrekvisisjoner.

Du kan konfigurere årsakskoder til å være nødvendige for endringer av et anleggsmiddel eller for bestemte anleggsmiddeltransaksjoner.

Til slutt definerer du nummerserier for anleggsmidler i kategorien **Nummerserier**. **Anleggsmiddel**-nummerserien kan overstyres av **Anleggsmiddelgruppe**-nummerserien hvis det er angitt.

Hvis du vil ha mer informasjon, kan du se [Opprette et anleggsmiddel](tasks/create-fixed-asset.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
