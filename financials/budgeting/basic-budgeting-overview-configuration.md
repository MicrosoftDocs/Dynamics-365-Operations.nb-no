---
title: Oversikt over budsjettering
description: "Nesten alle selskap som bruker finansfunksjonaliteten i Microsoft Dynamics 365 for Operations, må være i stand til å opprette rapporter for budsjett i forhold til faktisk. Denne artikkelen forklarer minimumskonfigurasjonen som er nødvendig for å opprette budsjetter i Dynamics 365 for Operations eller laste dem ned fra et tredjepartsprogram."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 60113
ms.assetid: 28a9793e-d376-47af-a345-69046bad17df
ms.search.region: global
ms.author: sigitac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: a4f9c99b8d74e20fbadc6cd9617451cfbfc06ba4
ms.contentlocale: nb-no
ms.lasthandoff: 05/25/2017


---

# <a name="budgeting-overview"></a>Oversikt over budsjettering

[!include[banner](../includes/banner.md)]


Nesten alle selskap som bruker finansfunksjonaliteten i Microsoft Dynamics 365 for Operations, må være i stand til å opprette rapporter for budsjett i forhold til faktisk. Denne artikkelen forklarer minimumskonfigurasjonen som er nødvendig for å opprette budsjetter i Dynamics 365 for Operations eller laste dem ned fra et tredjepartsprogram.

<a name="overview"></a>Oversikt
--------

Det godkjente budsjettet for en juridisk enhet vedlikeholdes i et dokument som kalles en *budsjettregisteroppføring*. Linjene i et dokument for budsjettregisteroppføring er kjent som *budsjettkonto*-oppføringer, og inneholder informasjon om finansdimensjoner, datoer og beløpene for det godkjente budsjettet. Budsjettregisteroppføringsdokumentet er integrert med grunnleggende finansrapporter og forespørselssider der faktiske finansbeløp sammenlignes med budsjetterte beløp. 

Det finnes flere metoder for å opprette budsjettregisteroppføringer i Dynamics 365 for Operations:

-   Manuelt registrere dokumentinformasjon på siden **Budsjettregisteroppføringer**.
-   Bruke Microsoft Excel-malen som du kan åpne ved å klikke **Åpne i Excel**-knappen på siden **Budsjettregisteroppføringer**.
-   Bruk dataenheten **Budsjettkontooppføringer** i Databehandling for å importere budsjettregisteroppføringer. Du bør vurdere å bruke denne metoden og aktivere **parameteren **Settbasert** **behandling når du må importere mange budsjettkontooppføringer i systemet.
-   Hvis firmaet bruker funksjonaliteten for planlegging av budsjett til å klargjøre budsjettdata, kan du bruke den periodiske prosessen **Generer budsjettregisteroppføring**.

Budsjettregisteroppføringen anses som fullført når budsjettsaldoene har blitt oppdatert. På siden **Budsjettregisteroppføringer** klikker du **Oppdater budsjettsaldoer** for den valgte budsjettregisteroppføringer eller flere oppføringer. Når du har oppdatert budsjettsaldoene, endres statusen for budsjettregisteroppføringen til **Fullført**. Fullført budsjettregisteroppføring kan ikke åpnes for redigering igjen. Hvis budsjettdataene må justeres, må du derfor opprette en ny budsjettregisteroppføring i stedet for å rette data i en fullført budsjettregisteroppføring.

## <a name="configuration"></a>Konfigurasjon
Når du konfigurerer budsjettering, starter du på siden **Budsjetteringsparametere**. Du må definere budsjettjournalen, nummerserien for budsjettregisteroppføringer og standard virkemåte i arbeidsområdene på denne siden.

Hvis det finnes policyer som styrer godkjenningen av budsjettregistreringsoppføringer, basert på budsjettype (for eksempel overføringer eller endringer), må du deretter opprette arbeidsflyter for budsjettregisteroppføringer på siden **Budsjetteringsarbeidsflyter**. Hvis det finnes situasjoner der overføringer kan være tillatt uten godkjenning av arbeidsflyt, kan du definere regler for budsjettoverføring for å støtte disse scenariene. 

På siden **Budsjetteringsdimensjoner** må du velge finansdimensjonene som er brukt for budsjettering, basert på dimensjonene som brukes i kontoplanen. Du kan velge alle finansdimensjoner eller et delsett av dem for budsjettering.

Definer en *budsjettmodell *som samsvarer med alle eller noen av budsjettene. Du kan bruke en enkelt budsjettmodell for alle budsjettregisteroppføringer. Du kan også opprette egne modeller som er basert på budsjettypen, den geografiske plasseringen eller en annen måte som et budsjett kan klassifiseres på. 

> [!NOTE] 
> Hvis budsjettkontroll brukes, kan du knytte bare én budsjettmodell til et bestemt tidsrom for budsjettsyklus. 

Opprett *budsjettkoder *som identifiserer typen budsjettransaksjoner som skal registreres og eventuell tilknyttet arbeidsflyt. Budsjettkoder kan støtte følgende budsjettyper:

-   Opprinnelig budsjett
-   Overføring
-   Revisjon
-   Disposisjon
-   Forhåndsdisposisjon
-   Overført budsjett

Med budsjettkoder kan du ha et revisjonsspor for godkjente budsjettendringer gjennom utviklingen av budsjettsyklusen. Hvis en arbeidsflyt er knyttet til en budsjettkode, aktiveres arbeidsflyten for alle budsjettregisteroppføringer som bruker denne budsjettkoden, og trinn i arbeidsflyten må være fullført før budsjettregisteroppføringen kan nå stadiet **Fullført**.  

Du kan også sette opp *regler for budsjettoverføring*. Hvis du vil bruke regler for budsjettoverføring, velger du **Bruk regler for budsjettoverføringer** på **Budsjettparametere**-siden. Når regler for budsjettoverføring brukes, hvis en bruker oppretter et dokument ved hjelp av en budsjettkode av typen **overføring**, vil ikke budsjettsaldoer bli oppdatert hvis reglene for budsjettoverføring er brutt. Du kan for eksempel tillate budsjettoverføringsdokumenter der utgiftsbudsjettet overføres mellom hovedkontoene for avdelingen for salg og markedsføring, men du kan hindre at budsjettet blir overført fra eller til denne avdelingen med mindre arbeidsflytgodkjenning er gitt for denne typen budsjettkontooppføring.

## <a name="using-workspaces-and-inquiry-pages-to-track-budget-vs-actuals"></a>Bruke arbeidsområder og forespørselssider til å spore budsjett i forhold til faktisk
Budsjettlederen kan gå gjennom gjeldende tilstand for et budsjett i arbeidsområdet **Finansbudsjetter og prognoser**. Kategoriene for **utgifter over budsjett** og **omsetning under budsjett** gir en rask oversikt over kombinasjonene av finansdimensjoner der budsjettmål ikke oppfylles, eller er nærmer seg terskelen. Du kan tilpasse budsjetterskelprosenten og finansdimensjonssettene som brukes i disse kategoriene ved å klikke **Konfigurer mitt arbeidsområde**. Kan du klikke **Enhetsledere** for å se arbeidere som er ansvarlige for bestemte finansdimensjonskombinasjoner som er valgt i disse kategoriene. Hvis du for eksempel ser at Utgiftsbudsjett for driftsavdelingen overskrider budsjetterskelen, kan du enkelt finne og kontakte lederen for driftsavdelingen for å diskutere saken. 

> [!NOTE] 
> Feltet **Avdelingsleder på siden** på siden **Organisasjonsenheter** bestemmer hvilke ledere som støtter bestemte finansdimensjonskombinasjoner. Klikk **Se mer** nederst i kategorien for å åpne forespørselssiden **Budsjett i forhold til faktisk** for mer informasjon om budsjettbeløp kontra faktiske beløp. 

Forespørselssiden **Faktisk i forhold til budsjett** lar deg drille ned til detaljene for budsjettbeløp kontra faktiske beløp. Velg en linje på forespørselssiden, og klikk deretter **Periodesaldoer** for å se budsjettbeløp og faktiske beløp som er spredt over regnskapsperioder. Siden **Budsjettkontooppføringer** inneholder gjennomgang til detaljene for budsjettbeløpet i budsjettregisteroppføringer. Siden **Økonomijournaloppføringer** åpner finanstransaksjonene som er inkludert i det beregnede **faktiske** beløpet. 

Et firma som bruker funksjonaliteten for budsjettplanlegging, kan opprette og bruke *budsjettprognoser* i arbeidsområdet **Finansbudsjetter og prognoser**.




