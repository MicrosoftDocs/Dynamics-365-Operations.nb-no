---
title: "Skaffe aktiva ved hjelp av innkjøp"
description: "Dette emnet beskriver hvordan du kan sette opp integrering mellom anleggsmidler og leverandører, slik at anleggsmidler opprettes automatisk fra bestillinger eller leverandørfakturaer, eller automatisk postere anskaffelses- og anskaffelsesjusteringstransaksjoner for anleggsmidler."
author: twheeloc
manager: AnnBe
ms.date: 10/27/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetParameters
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 3481
ms.assetid: d4e73a3f-633b-48b2-b8db-7a4a59a4d7ec
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 1e9b1dc6297f33ea25ca498895740596ebd020b8
ms.contentlocale: nb-no
ms.lasthandoff: 11/03/2017

---

# <a name="acquire-assets-through-procurement"></a>Skaffe aktiva ved hjelp av innkjøp

[!include [banner](../includes/banner.md)]

Dette emnet beskriver hvordan du kan sette opp integrering mellom anleggsmidler og leverandører, slik at anleggsmidler opprettes automatisk fra bestillinger eller leverandørfakturaer, eller automatisk postere anskaffelses- og anskaffelsesjusteringstransaksjoner for anleggsmidler.

 Følgende metoder er tilgjengelige for integrering av Anleggsmidler og Leverandører, og du må bruke den samme metoden for alle anleggsmidler:
-   Du må opprette et anleggsmiddel manuelt før du legger til anleggsmiddelnummeret i linjen på bestillingen eller leverandørfakturaen. En anskaffelsestransaksjon posteres automatisk for et anleggsmiddel når du posterer leverandørfakturaen. Dette er standardverdien.
-   Du må opprette et anleggsmiddel manuelt før du legger til anleggsmiddelnummeret i linjen på bestillingen eller leverandørfakturaen. Det posteres ingen anskaffelsestransaksjon for et anleggsmiddel når du posterer leverandørfakturaen.
-   Et anleggsmiddel opprettes automatisk når du posterer en produktkvittering eller leverandørfaktura der det er merket av for Opprett et nytt anleggsmiddel. En anskaffelsestransaksjon posteres automatisk for et anleggsmiddel når du posterer leverandørfakturaen.
-   Et anleggsmiddel opprettes automatisk når du posterer en produktkvittering eller leverandørfaktura der det er merket av for Opprett et nytt anleggsmiddel. Det posteres ingen anskaffelsestransaksjon for et anleggsmiddel når du posterer leverandørfakturaen.

Velg en av de to første metodene hvis du foretrekker å opprette anleggsmidler manuelt, og tilordne deretter anleggsmiddelnummeret til bestillingen eller leverandørfakturaen. Velg en av de to siste metodene hvis du foretrekker en mer fleksibel tilnærming: Noen ganger ønsker du kanskje å opprette anleggsmidler manuelt, men du vil også ha muligheten til å opprette et anleggsmiddel automatisk, basert på anleggsmiddelinformasjonen i linjevareopplysningene. 

Uansett om du oppretter anleggsmidler manuelt eller bruker en mer fleksibel tilnærming, må du også velge om du vil at en anskaffelsestransaksjon bare kan posteres i Anleggsmidler, eller om den også kan posteres når du posterer en leverandørfaktura. Noen organisasjoner foretrekker at brukere oppretter anskaffelser og anskaffelsestransaksjoner i Anleggsmidler ved hjelp av manuelle journaloppføringer eller forslag. 

I dette emnet beskrives detaljene i hver metode.

## <a name="methods-for-manually-creating-fixed-assets"></a> Metoder for manuell oppretting av anleggsmidler
Når du posterer en leverandørfaktura som har et anleggsmiddelnummer angitt i linjene, og det er merket av for Tillat anleggsmiddelanskaffelse fra innkjøp på siden Parametere for anleggsmidler, vil anskaffelsen posteres automatisk, og anleggsmiddelets status endres til Åpen. 

Hvis en anskaffelse ikke kan posteres, kan du enten registrere en anskaffelsestransaksjon manuelt i Anleggsmidler, eller du kan bruke et anskaffelsesforslag i anleggsmiddeljournalen til å opprette flere anskaffelsestransaksjoner på en gang.

> [!NOTE]                                                                                                                              
> Hvis Anleggsmidler er satt opp til å begrense postering av anskaffelsestransaksjoner til en bestemt brukergruppe, må du være medlem i denne gruppen for å postere anskaffelsestransaksjoner fra fakturaer.

## <a name="methods-for-automatically-creating-fixed-assets"></a> Metoder for automatisk oppretting av anleggsmidler
Når du posterer en produktkvittering som har alternativet Opprett et nytt anleggsmiddel valgt for en linje, blir et nytt anleggsmiddel opprettet som har statusen Ennå ikke anskaffet. Deretter, når du posterer en leverandørfaktura med et nytt anleggsmiddel, posteres en anskaffelsestransaksjon for det nye aktiva og anleggsmiddelets status endres til Åpen hvis anleggsmidler er konfigurert til å tillate anleggsmiddelanskaffelser fra leverandører, og du er medlem av en brukergruppe som kan postere anskaffelsestransaksjoner. 

Hvis alternativet Nytt anleggsmiddel? ikke ble valgt på innkjøpslinjen da du posterte produktkvitteringen, men det var merket da du posterte leverandørfakturaen, blir det nye anleggsmiddelet opprettet og anskaffet med status Åpen hvis anleggsmidler er definert for oppretting og anskaffelse. Et aktiva i tillegg opprettes ikke når du posterer en leverandørfaktura hvis ett allerede ble opprettet da du posterte produktkvitteringen.

### <a name="capitalization-threshold"></a>Kapitaliseringsterskel

Når du bruker en metode der aktiva opprettes og anskaffes automatisk, kan du sette opp systemet til å kontrollere om anleggsmiddelets innkjøpsbeløp er i samsvar med en angitt kapitaliseringsterskel for avskrivning av aktiva. I så fall vil det være merket av for alternativet Avskrivning i tablåene for anleggsmiddelet når det opprettes fra Leverandører. 

En kapitaliseringsterskel er et valutabeløp som bestemmer om anleggsmidler avskrives hvis de oppfyller det angitte beløpet. Hvis du for eksempel kjøper et anleggsmiddel og innkjøpsbeløpet er mindre enn kapitaliseringsterskelen, defineres anleggsmiddelet som ikke avskrivbart. Hvis innkjøpsbeløpet oppfyller eller overskrider terskelen, defineres anleggsmiddelet som avskrivbart. 

Du kan definere kapitaliseringsterskelen på siden Anleggsmiddelgrupper.

## <a name="scenario"></a>Scenario
Dette scenariet beskriver hele syklusen for integrering mellom Anleggsmidler og Leverandører. Et eksempeloppsett vises, og bruken av anskaffelsesforslag beskrives også. 

I dette scenariet er systemet satt opp slik:

-   Aktiva opprettes automatisk når produktkvittering eller leverandørfaktura posteres, men Anleggsmidler er satt opp til å hindre postering av anskaffelsestransaksjoner fra Leverandører.
-   Kontoer er angitt i Kontotype-feltet for typene Anleggsmiddelmottak og Anleggsmiddelfrigivelse på siden Varegrupper.
-   Kapitaliseringsterskelen for anleggsmiddelgruppen Datamaskiner (COMP) er 1 500.
-   Din oppgave er å registrere en bestilling av en ny bærbar datamaskin som en ansatt skal bruke, postere bestillingen, kontrollere at spedisjonsassistenten posterer en produktkvittering, postere leverandørfakturaen og til slutt kontrollere at regnskapsføreren oppdaterer status for aktivaet bærbar datamaskin til Åpen.

Det første du må gjøre, er å bruke siden Bestilling til å registrere opplysninger om den bærbare datamaskinen, som koster 1 600. Du velger alternativet Nytt anleggsmiddel? i hurtigkategorien Anleggsmidler i bestillingslinjene, velger COMP som anleggsmiddelgruppen, og lagrer bestillingen. 

Når den bærbare datamaskinen mottas, registrerer og posterer en spedisjonsassistent en produktkvittering for å registrere mottaket av den bærbare datamaskinen. Den bærbare datamaskinen opprettes og har statusen Ennå ikke anskaffet. Beløpet overskrider kapitaliseringsterskelen. Derfor er alternativet Avskrivning valgt i tablåene for aktivaet bærbar datamaskin. Følgende transaksjoner skjer:

| Beskrivelse                               | Konto             | Debet    | Kreditt   |
|-------------------------------------------|---------------------|----------|----------|
| Innkjøp, produktkvitteringsinnkjøp        | Ikke fakturerte mottak | 1 600,00 |          |
| Innkjøp, motkonto for produktkvitteringsinnkjøp | Påløpte innkjøp   |          | 1 600,00 |

I neste omgang posterer du leverandørfakturaen for den bærbare datamaskinen. Den bærbare datamaskinens status endres ikke fordi Anleggsmidler er konfigurert til å hindre at aktivatransaksjoner posteres når en leverandørfaktura posteres. Alternativet Opprett et nytt anleggsmiddel ble valgt da leverandørfakturaen ble postert. Derfor ble kontoen Anleggsmiddelmottak brukt. Kontoen for anleggsmiddelfrigivelse ble ikke brukt fordi ingen anskaffelse ble postert. Den skal brukes senere når organisasjonens regnskapsfører posterer en anskaffelsestransaksjon i Anleggsmidler ved hjelp av anskaffelsesforslag. 

Følgende transaksjoner skjer:

| Beskrivelse                               | Konto             | Debet    | Kreditt   |
|-------------------------------------------|---------------------|----------|----------|
| Innkjøp, motkonto for produktkvitteringsinnkjøp | Påløpte innkjøp   | 1 600,00 |          |
| Leverandørsaldo                            | Leverandører    |          | 1 600,00 |
| Innkjøp, Anleggsmiddelmottak             | Datamaskinutgifter    | 1 600,00 |          |
| Innkjøp, produktkvitteringsinnkjøp        | Ikke fakturerte mottak |          | 1 600,00 |

Til slutt går regnskapsføreren gjennom alle anleggsmidler som har statusen Ennå ikke anskaffet. Derfor blir det nye anleggsmiddelet bærbar datamaskin gjennomgått. Regnskapsføreren åpner deretter siden Anskaffelsesforslag fra Journallinjer for anleggsmidler, og oppretter anskaffelsestransaksjoner for alle aktiva som har en faktura, men fortsatt har statusen Ennå ikke anskaffet. Når journalen posteres, endres statusen for aktivaet bærbar datamaskin til Åpen. Kontoen for anleggsmiddelfrigivelse krediteres, og kontoen for aktivaanskaffelse debiteres. 

Nedenfor vises noen varianter av dette scenariet:

-   Hvis Anleggsmidler er satt opp for å tillate at aktivaanskaffelsestransaksjoner posteres når leverandørfakturaer posteres, behøver ikke regnskapsføreren å bruke anskaffelsesforslag i Anleggsmidler, fordi anskaffelsestransaksjonen allerede er opprettet. Dessuten oppdateres andre kontoer når du posterer leverandørfakturaen. I stedet for Datamaskinutgifter, debiteres beholdningskontoen for anleggsmiddelmottak, og ytterligere to transaksjoner skjer: kontoen for anleggsmiddelanskaffelse debiteres og beholdningskontoen for anleggsmiddelfrigivelse krediteres.
-   Hvis alternativet Opprett et nytt anleggsmiddel ikke er merket når produktkvitteringen posteres, opprettes ingen aktiva på dette tidspunktet. Hvis du velger alternativet Opprett et nytt anleggsmiddel før du posterer leverandørfakturaen, opprettes anleggsmiddelet og har statusen Ennå ikke anskaffet, eller statusen Åpen hvis du også posterer anskaffelsestransaksjoner når leverandørfakturaer posteres.
-   Hvis den bærbare datamaskinen koster 1 400 i stedet for 1 600, nås ikke kapitaliseringsterskelen. Derfor blir anleggsmiddelet opprettet og alternativet for avskrivning fjernes.
-   Hvis ankomstregistrering brukes, bruker du siden Fakturagodkjenningsjournal etter at ankomstregistrering posteres til å hente frem bilaget, knytte bestillingen til fakturaen, merke av for Opprett et nytt anleggsmiddel, og deretter postere fakturaen. Hvis du er medlem i en brukergruppe som kan opprette anskaffelsestransaksjoner, opprettes anskaffelsen og anleggsmiddelet får statusen Åpen.
-   Hvis bare et delvis antall mottas, opprettes ingen aktivaanskaffelse for den første leverandørfakturaen på grunn av brukergrupperestriksjoner. Det kan bare posteres en anskaffelse for den andre leverandørfakturaen som fullfører det bestilte antallet, hvis det allerede er registrert en anskaffelsestransaksjon for den første leverandørfakturaen, og hvis du er medlem i en brukergruppe som kan postere anskaffelser.


Hvis du vil ha mer informasjon, se [Integrering av anleggsmidler](fixed-asset-integration.md).




