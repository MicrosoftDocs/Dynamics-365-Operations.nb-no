---
title: Integrering av anleggsmidler
description: Anleggsmidler kan integreres med økonomi, lagerstyring, kunder og leverandører. Du kan også konfigurere Anleggsmidler slik at det integreres med bestillinger.
author: ShylaThompson
manager: AnnBe
ms.date: 03/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 3501
ms.assetid: f0639053-d99c-432a-8ead-5c26e0d4eaec
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2023d68a1455c6bb5ec569b6ae19fc3268f8769d
ms.sourcegitcommit: 065d9fab832b6bcc88c00dc78ac1ae854c762ec7
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/06/2019
ms.locfileid: "778161"
---
# <a name="fixed-assets-integration"></a>Integrering av anleggsmidler

[!include [banner](../includes/banner.md)]

Anleggsmidler kan integreres med økonomi, lagerstyring, kunder og leverandører. Du kan også konfigurere Anleggsmidler slik at det integreres med bestillinger.

<a name="general-ledger"></a>Økonomimodul
--------------

I Økonomimodul summeres vanligvis verdien for alle anleggsmidler i flere hovedkontoer som er nødvendige for finansrapportering. På **Anleggsmidler**-siden kan du imidlertid opprette mange anleggsmiddelposter. Disse oppføringene kan inneholde informasjon som anskaffelsespris, avskrivning og vurdering. Hver gang du posterer en transaksjon for et anleggsmiddel, oppdateres de riktige hovedkontoene. Hovedkontoene for anleggsmidler viser alltid den oppdaterte verdien for anleggsmidlene.

På **Posteringsprofiler for anleggsmidler**-siden kan du definere hovedkontoene som anleggsmiddeltablåtransaksjoner posteres i. Du angir også hvilke typer anleggsmiddeltransaksjoner som skal posteres til hver hovedkonto. Du kan opprette ulike kombinasjoner av hovedkontoer for anleggsmidler, avhengig av hvor mange detaljer du vil ha for anleggsmidler i økonomimodulen. Hovedkontoer kan være basert på transaksjonstyper, tablåer og andre hovedkontoer.

## <a name="inventory-management"></a>Lagerstyring
I lagerjournalen for anleggsmidler kan du angi anskaffelsen av anleggsmidler som den juridiske enheten har produsert eller bygd for seg selv. Du kan deretter overføre varer på lager til anleggsmidler som en anskaffelse eller som en del av en anskaffelse. 

Du kan også anskaffe anleggsmidler ved hjelp av bestillinger. Når bestillinger inneholder lagervarer som er angitt som anleggsmidler, avgjør innstillingen for **Tillat anleggsmiddelanskaffelse fra innkjøp** på siden **Parametere for anleggsmidler** om en anskaffelse posteres for anleggsmidlet når fakturaen posteres. Én kjøpslinje oppretter bare ett anleggsmiddel, uavhengig av antallet. Effekten anskaffelsen av anleggsmidler har på lager, er avhengig av definisjonen av den juridiske enheten. 

Når en lagervare blir en anleggsmiddelanskaffelse via lagerjournalen, en bestilling eller et anskaffelsesforslag, opprettes en anskaffelsestransaksjon for tablå for anleggsmiddel. Hvis en tablåanskaffelse inkluderer et avledet tablå, opprettes det også en anskaffelsestransaksjon for det avledede tablået. 

Posteringsregler som defineres på siden **Postering** i Lagerstyring, styrer reduksjonen i lager når en anskaffelse posteres. Du reduserer imidlertid ikke alltid lageret når du posterer fakturaer som er knyttet til anleggsmidler. I noen tilfeller kan anleggsmidlene være anskaffet til intern bruk. Et eksempel er en bærbar datamaskin som er kjøpt for salgsavdelingen. Når du arbeider med bestillinger, kan du bruke varer som er definert både for videresalg og intern bruk. 

Hvis du bruker spesifikke avgangs- og tilgangskontoer i varegrupper for anleggsmidler, kan du bruke den samme lagervaren både for interne innkjøp og som lager for videresalg. 

Anleggsmidler som er til intern bruk, settes opp slik at de har kontotypen **Anleggsmiddelmottak**. Denne kontotypen brukes til å spore mottaket av anleggsmidlet. Når du posterer en leverandørfaktura, bruker du tilgangskontoen for anleggsmiddel hvis en av følgende betingelser er oppfylt:

-   Fakturalinjen inneholder et eksisterende anleggsmiddel til interne formål.
-   Avmerkingsboksen **Nytt anleggsmiddel?** er merket av for produktkvitteringslinjen som posteres.
-   Avmerkingsboksen **Opprett et nytt anleggsmiddel** er merket for leverandørfakturalinjen.

Denne kontoen er som regel en utgiftskonto. Du kan definere kontotypen **Anleggsmiddelmottak** for enten en varegruppe eller en enkelt vare ved å bruke kategorien **Bestilling** på siden **Varegruppe** eller **Postering**.

På samme måte kan anleggsmidler som er til intern bruk, settes opp slik at de har kontotypen **Anleggsmiddelfrigivelse**. Denne kontotypen brukes til å spore sending av et anleggsmiddel til mottakeren. Når det bes om et anleggsmiddel ved hjelp av en bestilling, vil avgangskontoen for anleggsmiddelet motkontere debetkontoen for anleggsmiddelet. Anleggsmiddelanskaffelsen kan enten posteres når du posterer en leverandørfaktura, eller når du posterer anleggsmiddelanskaffelsen i Anleggsmidler-journalen, eventuelt ved hjelp av et anskaffelsesforslag. Du kan definere kontotypen **Anleggsmiddelfrigivelse** for enten en varegruppe eller en enkelt vare ved å bruke kategorien **Beholdning** på siden **Varegruppe** eller **Varepostering**. 

I siste instans fastsettes hovedkontoene som skal brukes for postering av alternativene for finansintegrering, som er angitt for lagermodellgruppen. I tillegg varierer hovedkontoene som brukes, avhengig av om et anleggsmiddel er tilordnet bestillingslinjen. Kontoene avledes av posteringsprofilen for hver varegruppe. 
**Obs!** Hvis det finnes en lagerreservasjon når produktkvitteringer posteres, kan du ikke tilordne et anleggsmiddel eller opprette et anleggsmiddel fra linjen. 

Kontoer som anleggsmiddeltransaksjoner posteres til, avhenger av to faktorer: om aktivaene kjøpes inn eller bygges av den juridiske enheten og av transaksjonstypen for anleggsmiddelet. 

Transaksjonstypen kobler lagertransaksjonen til posteringsprofilen i Anleggsmidler. Siden posteringsprofilen i Anleggsmidler definerer hvilke kontoer som oppdateres, er valget av en transaksjonstype for et anleggsmiddel også indirekte valget av hovedkontoene som transaksjonen posteres til. For både bygde og innkjøpte anleggsmidler er transaksjonstypen vanligvis **Anskaffelse** eller **Anskaffelsesjustering**.

## <a name="accounts-receivable"></a>Kundereskontro
Integrering av Anleggsmidler med Kunder bruker posteringsprofiler som er definert i anleggsmidler. Disse posteringsprofilene aktiveres når et anleggsmiddel, et tablå og en anleggsmiddeltransaksjon velges for en kundefaktura før kundefakturaen posteres. Siden anleggsmidler ikke er en del av Lagerstyring, må du bruke siden **Fritekstfaktura** når du selger et anleggsmiddel. 

Hvis tablået inkluderer et avledet tablå, opprettes det avledede tablåtransaksjon når du posterer kundefakturaen.

## <a name="accounts-payable"></a>Leverandører
Anleggsmidler skaffes vanligvis fra eksterne leverandører. Du kan bruke siden **Parametere for anleggsmidler** til å angi om anleggsmiddelanskaffelser alltid skal posteres når du posterer leverandørfakturaer, eller om anleggsmiddelanskaffelser bare kan posteres fra Anleggsmidler. Hvis du tillater at anleggsmiddelanskaffelser posteres fra Leverandører, oppdateres alltid anleggsmiddelkontoer når en leverandørfaktura for en anleggsmiddelanskaffelse posteres. 

Hvis systemet er konfigurert slik at det posterer en anleggsmiddelanskaffelse når en faktura posteres, posteres transaksjonen i henhold til posteringsprofilene som er definert i Anleggsmidler for de forskjellige transaksjonstypene for anleggsmiddel. Posteringen styres av anleggsmiddelet, tablået og transaksjonstypen for anleggsmiddel som er valgt på **Bestilling**-siden før leverandørfakturaen posteres. 

Hvis tablået inkluderer et avledet tablå, opprettes det avledede tablåtransaksjon når du posterer leverandørfakturaen.

Integreringen for hver ordrelinje aktiveres i kategorien **Anleggsmidler** på hurtigfanen **Linjedetaljer** på **Bestilling**-siden. Du kan sende en bestilling for et anleggsmiddel til leverandøren. Anleggsmidler og hovedkontoer oppdateres imidlertid bare når du posterer leverandørfakturaen, etter at anleggsmiddelet er mottatt. Siden bestillinger kan bare inneholde lagervarer, er effekten som anskaffelsen av anleggsmidler har på lager, avhengig av definisjonen av den juridiske enheten.

## <a name="project-management-and-accounting"></a>Prosjektstyring og regnskap
Du kan knytte et prosjekt til et anleggsmiddel som påvirkes av prosjektet. Du kan også knytte hver fase, oppgave eller underprosjekt til et annet anleggsmiddel. Ett anleggsmiddel kan være knyttet til hver prosjektpost. Du kan opprette tilordningen når du registrerer et anleggsmiddelnummer i **Anleggsmiddel**-nummerfeltet på **Prosjekter**-siden. Prosjekttypen må være enten **Intern** eller **Kostnadsprosjekt**. 

Du kan også bruke **Prosjekter**-siden til å vise detaljer om anleggsmidler som er knyttet til prosjekter. Hvis du vil vise anleggsmiddelposten, klikker du anleggsmiddelkoblingen i hurtigfanen **Konfigurer** for å åpne **Anleggsmidler**-siden. Klikk deretter **Prosjekter** &gt; **Alle prosjekter** for å vise prosjektene som er knyttet til anleggsmidlet. 

Du knytter vanligvis anleggsmidler til prosjekter når prosjektene er knyttet til arbeid, vedlikehold eller forbedringer av anleggsmidlet. Når prosjektet er fullført, blir det ikke automatisk opprettet en oppskrivingsjustering for anleggsmidlet. Derfor må du opprette oppskrivingsjusteringen manuelt, hvis det kreves en oppskrivning. 

Hvis du vil slette tilordningen mellom et prosjekt og et anleggsmiddel, fjerner du merket i feltet **Anleggsmiddelets nummer** på **Prosjekter**-siden. 

Du kan også angi et anleggsmiddel du oppretter eller produserer i forbindelse med et estimatprosjekt. Når estimatprosjektet avsluttes, kan du automatisk postere en anleggsmiddelanskaffelsestransaksjon.

Hvis du vil ha mer informasjon, se [Skaffe anleggsmidler ved hjelp av innkjøp](acquire-assets-procurement.md)



