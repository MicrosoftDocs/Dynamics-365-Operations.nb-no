---
title: "Satsvis utføring for varsler"
description: Dette emnet gir informasjon om satsvis behandling av varsler i Microsoft Dynamics 365 for Finance and Operations.
author: tjvass
manager: AnnBe
ms.date: 03/20/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application user
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2018-3-30
ms.dyn365.ops.version: Platform update 15
ms.translationtype: HT
ms.sourcegitcommit: 454368ab5a467002ebf973db97fd98e31885dfe0
ms.openlocfilehash: f4c874c148dc10ac658f659896009981962a5802
ms.contentlocale: nb-no
ms.lasthandoff: 03/23/2018

---

# <a name="batch-processing-for-alerts"></a>Satsvis behandling for varsler
[!INCLUDE [banner](../includes/banner.md)]

[!INCLUDE [banner](../includes/pre-release.md)]

Varsler behandles med funksjonaliteten for satsvis behandling i Microsoft Dynamics 365 for Finance and Operations. Du må konfigurere satsvis behandling før varsler kan leveres.

Finance and Operations støtter to typer hendelser:

- Hendelser som utløses av endringsbaserte hendelser. Disse hendelsene omtales også som Opprett/Slett- og Oppdater-hendelser.
- Hendelser som utløses av forfallsdatoer.

Du kan definere satsvis behandling for hver hendelsestype.
        
## <a name="batch-processing-for-change-based-events"></a>Satsvis behandling for endringsbaserte hendelser
Finance and Operations leser alle endringsbaserte hendelser som har inntruffet siden satsvis behandling ble utført sist. Endringsbaserte hendelser omfatter oppdateringer i felt, sletting av poster og opprettelse av poster. Disse hendelsene sammenlignes med betingelsene som er angitt i varslingsreglene. Når en hendelse samsvarer med betingelsene for regelen, genererer en satsvis behandling et varsel.

### <a name="frequency-for-change-based-events"></a>Hyppighet for endringsbaserte hendelser
For endringsbaserte hendelser kan du definere en satsvis jobb som utløser behandling av en hendelse rett etter at hendelsen er logget av systemet. Hvis du konfigurerer at den satsvise jobben skal gjentas oftere, får brukerne varslene sine tidligere når det oppstår endringer. En høy hyppighet for satsvis behandling kan imidlertid ha negativ innvirkning på systemets ytelse.

På den annen side kan en satsvis jobb som oppstår sjeldnere, og som er planlagt på tider når systembelastningen er lav, forbedre systemytelsen. En lav hyppighet for satsvis behandling kan imidlertid ikke oppfyller brukernes behov for betimelige varsler.

Når du konfigurerer hyppigheten for satsvis behandling for endringsbasert hendelser, må du derfor vurdere balansen mellom betimeligheten for varslene og ytelsen til hele systemet. Disse hensynene blir mer relevante jo større antall brukere som oppretter varslingsregler. Hyppigheten påvirker ikke hvor mange hendelser som må behandles. Hvis flere brukere imidlertid oppretter regler, må flere kontroller utføres. Denne typen datautveksling kan påvirke systemets ytelse.

#### <a name="the-risks-of-low-batch-frequency"></a>Faren for lav frekvens for satsvis behandling
Hvis du konfigurerer lav hyppighet for satsvis behandling for endringsbaserte hendelser, kan det hende data som er relevante for betingelsene i varslingsregler, blir endret før partiet er behandlet. Derfor kan du miste varsler.

En varslingsregel er for eksempel konfigurert til å utløse et varsel når **kundekontakten endres**, og betingelsen er at **kunden = BB**. Med andre ord, når kundekontakten for kunde BB endres, logges hendelsen. Systemet for satsvis behandling er imidlertid konfigurert slik at satsvis behandling forekommer sjeldnere enn dataregistrering. Hvis kundenavnet endres fra **BB** til **AA** før hendelsen behandles, oppfyller ikke dataene i databasen lenger betingelsen i regelen, **kunde = BB**. Når hendelsen behandles til slutt, genereres det derfor ikke noe varsel.

### <a name="set-up-processing-for-change-based-alerts"></a>Definere behandling av endringsbaserte varsler
1. Gå til **Systemadministrasjon** &gt; **Periodiske oppgaver** &gt; **Varsler** &gt; **Endringsbaserte varsler**.
2. I dialogboksen **Endringsbaserte varsler** angir du riktig informasjon.

## <a name="batch-processing-for-due-date-events"></a>Satsvis behandling for forfallsdatohendelser
Finance and Operations oppdager alle hendelser som forårsakes av forfallsdatoer, og disse hendelsene sammenlignes med betingelsene som er konfigurert i varslingsreglene. Den satsvise behandlingen genererer et varsel når en hendelse samsvarer med betingelsene i en regel.

### <a name="frequency-for-due-date-events"></a>Hyppighet for forfallsdatohendelser
For forfallsdatohendelser vil du kanskje angi satsvise jobber som utføres om natten eller på bestemte tider på dagen for å fordele belastningen på systemet. Det anbefales at du setter opp en satsvis jobb slik at den har kjørt i minst én gang per dag. Hvis du vil at varsler skal sendes ut så tidlig som mulig, må du konfigurere den satsvise behandlingen til å foregå umiddelbart etter at systemdatoen endres. Hvis du vil generere varsler for forfallsdatohendelser som skjer etter at en satsvis jobb allerede har behandlet varsler, kan du kjøre den satsvise jobben en gang til på samme dag.

En satsvis jobb er for eksempel kjørt på en bestemt dag. Du kan deretter opprette en bestilling med en forfallsdato som skal utløse et varsel samme dag. Hvis du vil bli varslet på nytt den dagen, må du kjøre den satsvise jobben på nytt etter at bestillingen er opprettet. Men hvis du ikke kjører den satsvise jobben på nytt den dagen, vil neste dags satsvise jobb registrere alle ikke-behandlede forfallsdatohendelser fra forrige dager.

> [!NOTE]
> Selv når den satsvise behandlingen kjøres mer enn én gang per dag, genereres det ikke varsler to ganger for samme forfallsdatohendelse og -betingelser. Varsler genereres bare for datoer som har forfall på grunn av endringer som skjedde i systemet etter at forrige satsvise jobb ble kjørt.

### <a name="batch-processing-window"></a>Vindu for satsvis behandling
Behandlingen av varslingsregler i et firma kan stoppes av flere årsaker. Disse årsakene omfatter ferier, systemfeil eller andre problemer som hindrer at de satsvise jobbene kjøres på en stund.

Hvis du vil hindre at varsler om forfallsdatoer blir foreldede fordi den satsvise jobben ikke er kjørt i flere dager, kan du definere et vindu for satsvis behandling. Et vindu for satsvis behandling kan brukes til å hindre at en satsvis jobb kjøres for et bestemt antall dager.

Hvis du setter opp et vindu for satsvis behandling, sendes det et varsel når varslingsregelen behandles, selv om varselet overskrider tidsgrensen som er definert i forfallsdatokriteriet. Et varsel fortsetter å bli sendt så lenge perioden som er definert av denne tidsgrensen, i tillegg til vinduet for satsvis behandling, ikke overskrides. Når perioden som er definert av tidsgrensen, i tillegg til vinduet for satsvis behandling, blir overskredet, sendes det imidlertid ikke lenger et varsel.

### <a name="set-up-processing-for-due-date-alerts"></a>Definere behandling av forfallsdatovarsler
1. Gå til **Systemadministrasjon** &gt; **Periodiske oppgaver** &gt; **Varsler** &gt; **Forfallsdatovarsler**.
2. I dialogboksen **Forfallsdatovarsler** angir du riktig informasjon.

