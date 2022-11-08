---
title: Oversikt over sammenslåing av Dynamics 365 Human Resources-infrastruktur
description: Denne artikkelen beskriver sammenslåingen av Microsoft Dynamics 365 Human Resources-infrastruktur.
author: twheeloc
ms.date: 10/24/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-10-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: f79ef3ed5db7583eb44b99e49c010778ce8524d1
ms.sourcegitcommit: 088a7b5eb9a3b68710dfe012abf4c24776978750
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/01/2022
ms.locfileid: "9733473"
---
# <a name="dynamics-365-human-resources-infrastructure-merge"></a>Sammenslåing av Dynamics 365 Human Resources-infrastruktur 

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]
[!include [preview banner](../includes/preview-banner.md)]

## <a name="dynamics-human-resources-365"></a>Dynamics Human Resources 365

Microsoft Dynamics 365 Human Resources tilbyr verktøy som hjelper personalgrupper med å øke organisasjonsmessig fleksibilitet, transformere erfaringen til de ansatte og optimalisere personalprogrammer for å skape en arbeidsplass der mennesker og bedrift kan trives. Hvis du vil vite mer om Dynamics 365 Human Resources, kan du se [Dynamics 365 Human Resources](https://dynamics.microsoft.com/human-resources/overview/).

- **Transformer de ansattes opplevelse.** Behold de beste aktørene ved å gi ledere og ansatte muligheten til å bruke tilkoblede selvbetjeningsopplevelser som driver engasjement og vekst.
- **Optimalisere personalprogrammer.** Bidra til å redusere driftskostnadene, og opprett programmer for håndtering av permisjon og fravær, arbeidstid, fordeler og kompensasjon med folk i sentrum.
- **Øk den organisasjonsmessige fleksibiliteten.** Sørg for at personalavdelingen kan operere med fleksibiliteten som virksomheten krever, ved å bruke Dataverse og Microsoft Power Platform til å sentralisere persondata og enkelt utvide Dynamics 365 Human Resources.
- **Oppdag innsikt i arbeidsstyrken.** Ta datadrevne beslutninger gjennom evnen til å analysere og visualisere persondata på rike instrumentbord som er tilgjengelige på alle enheter.

## <a name="human-resources-infrastructure-merge"></a>Human Resources-infrastruktursammenslåing

Dynamics 365 Human Resources er et frittstående program som for øyeblikket bruker en annen infrastruktur enn andre økonomi- og driftsapper, for eksempel Dynamics 365 Finance eller Dynamics 365 Supply Chain Management. Sammenslåingen av infrastrukturen bringer Dynamics 365 Human Resources inn i den samme infrastrukturen som andre økonomi- og driftsapper.

Hvis du vil vite mer om sammenslåingen av Human Resources-infrastrukturen, kan du se [Sammenslåing av HR-tilbud](https://cloudblogs.microsoft.com/dynamics365/it/2021/09/15/merging-of-hr-offerings-brings-capabilities-together-for-customers/). Hvis du vil ha svar på vanlige spørsmål, kan du se [Vanlige spørsmål om sammenslåing av Human Resources-infrastruktur](./hr-infrastructure-merge-faq.md).

## <a name="customer-migration-vs-customer-merge"></a>Kundeoverføring i forhold til kundesammenslåing

Alle funksjonene i Human Resources-programmet er gjort tilgjengelige i økonomi- og driftsmiljøer som en del av sammenslåingen av infrastruktur. Kunder kan overføre Human Resources-miljøet ved hjelp av overføringsverktøyet som er tilgjengelig i Microsoft Dynamics Lifecycle Services. De kan også eventuelt slå sammen dataene sine med det eksisterende økonomi- og driftsmiljøet. 

Kundeoverføring og kundesammenslåing er ulike på følgende måte:

- **Kundeoverføring** – Det automatiserte overføringsverktøyet brukes til å utføre en «løft-og-flytt-overføring» (flytting) av kundedatabasen fra Human Resources-infrastrukturen til økonomi- og driftsinfrastrukturen. Resultatet er et nytt økonomi- og driftsmiljø som bruker kundens Human Resources-database. 
- **Kundesammenslåing** – Dette ytterligere trinnet kreves ikke av Microsoft. Kunden avgjør om dette skal gjøres, og eventuelt når det skal gjøres. I dette trinnet flyttes kundedata til et eksisterende miljø, for eksempel et Finance-miljø eller et Project Operations-miljø. Dette er for det meste en manuell oppgave og kan gjøres ved hjelp av DMF-dataenheter (Data Management Framework). 

## <a name="planning-a-human-resources-environment-migration"></a>Planlegging av overføring av et Human Resources-miljø

Alle kunder må overføre sine eksisterende Human Resources-miljøer fra den frittstående infrastrukturen som en del av sammenslåingen av infrastrukturen. For å støtte denne prosessen anbefaler vi at du bruker det automatiserte overføringsverktøyet i Lifecycle Services til å flytte gjeldende miljøer til den nye infrastrukturen. 

De følgende delene gir mer detaljert informasjon om hvordan du bruker Lifecycle Services-verktøy til å overføre et frittstående Human Resources-miljø. 

Kunder som planlegger en overføring, kan forvente seg følgende:

- Alle kunder må overføre et sandkassemiljø før produksjonsmiljøet kan overføres. 
- Overføringsverktøy tillater bare overføring fra sandkasse til sandkasse og fra produksjon til produksjon. Miljøtypen avgjør derfor hvilket miljø som kan overføres på riktig måte. 
- Kunder kan overføre så mange sandkasser som nødvendig før de overfører produksjonsmiljøet, så lenge en målsandkasseplass er tilgjengelig. Kunder kan også slette en overført sandkasse og overføre på nytt flere ganger. 
- Hvis en sandkasseoverføring mislykkes eller du vil starte på nytt, kan du slette et miljø i økonomi- og driftsinfrastrukturen og overføre det samme miljøet på nytt.
- Nettadressen til Human Resources-miljøet er en annen etter overføringen.
- Planlegg en passende mengde nedetid for overføringen av produksjonsmiljøet. Den estimerte tidsrammen for fullføring av den automatiserte overføringen er tre til fire timer. Tidsrammen varierer avhengig av organisasjonens data. Du bør bekrefte hvor lang tid du trenger til overføring av sandkassemiljøene, og beregne ekstra tid til eventuelle manuelle tilleggsoppgaver som må fullføres.

> [!IMPORTANT] 
> Når et produksjonsmiljø er vellykket overført til økonomi- og driftsinfrastrukturen, slettes det frittstående kildeproduksjonsmiljøet automatisk. Du må ikke slette det overførte produksjonsmiljøet. 

Prosessen for overføringen er for det meste automatisk. Forretningsbrukerne må imidlertid utføre noen manuelle trinn og valideringer etter overføringen.

De følgende manuelle trinnene må fullføres:

- Opprett et nytt Lifecycle Services-prosjekt for overføringen.
- Endre eventuelle integreringer i det gamle miljøet til det nye miljøet ved å peke integreringen mot den nye nettadressen / de nye sluttpunktene, basert på hver integreringskonfigurasjon.
- Oppdater datalageret for innebygde Power BI-rapporter.
- Oppdater dataenhetslisten fra DMF-arbeidsområdet.
- Koble til Lifecycle Services for hjelp.
- Opprett regnskapskalendere.

Under den automatiske prosessen fullføres følgende handlinger, som bør valideres:

- Data:

    - Konfigurasjoner
    - Sikkerhetsroller (inkludert egendefinerte roller)
    - Arbeidsflyter
    - Tilpassinger og lagrede visninger
    - Transaksjoner
    - Tilpassede felter
    - Vedlegg

- Dataadministrasjon – Vise din egen database (BYOD).
- Funksjonsbehandling – Aktiver/deaktiver funksjoner.
- Innebygd Power Apps.
- Miljø knyttet til administrasjonssenteret for Power Platform (bare produksjon).
- Satsvise jobber.
- En tom finansmodul opprettes for hver juridiske enhet. Standard valutakurstype og regnskapsvalutaen for hver finansmodul angis.
- En ny kontoplan opprettes automatisk og knyttes til **Finans**-siden i hver juridiske enhet. Finansdimensjonene som er konfigurert i Human Resources-miljøet, blir automatisk lagt til i en ny kontostruktur og koblet til finansmodulen. 

> [!NOTE]
> En finansmodul er nødvendig i økonomi- og driftsinfrastrukturen som en del av Dynamics 365 Finance-produktet. Den egendefinerte dimensjonskontrolleren som fantes i det frittstående Dynamics 365 Human Resources-programmet, er ikke tilgjengelig. Den sammenslåtte infrastrukturen for Human Resources er avhengig av finanslogikken for å vise finansdimensjoner i **Human Resources**-modulen. Hvis du vil vite mer om kontoplanen og finansdimensjoner, kan du se [her](../finance/general-ledger/plan-chart-of-accounts.md). 

## <a name="considerations"></a>Hensyn

- Overføring til miljøer skjer alltid i den nyeste allment tilgjengelige versjonen. Hvis overføringsvalideringen for sandkassemiljøer var i en annen versjon, anbefaler vi at du validerer en sandkasseoverføring i samme versjon som produksjonsmiljøet, avhengig av planen din for overføring og testing. 
- Under overføringen plasseres de overførte miljøene i det samme området som de frittstående Human Resources-miljøene.

## <a name="licensing"></a>Lisensiering

Det finnes ingen endringer i lisensiering for Dynamics 365 Human Resources i følgende områder: 

- **Minstekrav til kjøp av lisens**
- **Lisenser til et produksjons- og sandkassemiljø** – Hvis du har eksisterende frittstående Human Resources-lisenser som gir deg ett produksjonsmiljø og ett sandkassemiljø, er samme antall lisenser tilgjengelige i økonomi- og driftsinfrastrukturen uten ekstra kostnad.
- **Flere sandkasselisenser** – Hvis du har kjøpt flere sandkasselisenser for det frittstående Human Resources-programmet, er det samme antallet sandkasselisenser tilgjengelig for et standard godkjenningstestmiljø (sandkasse) i økonomi- og driftsinfrastrukturen uten ekstra kostnad. 
