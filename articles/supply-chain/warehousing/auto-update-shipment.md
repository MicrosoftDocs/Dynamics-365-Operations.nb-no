---
title: Automatiske oppdateringer av forsendelser
description: Dette emnet inneholder en oversikt over funksjonalitet som gir automatiske oppdateringer av forsendelser.
author: josaw1
ms.date: 11/04/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSWaveTemplateTable,SalesTableListPage,SalesTable,WHSWaveTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 69d20615eb72b036659fe99b140ca18b1fb529bf5ec03bf9390615ea315e9202
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6760256"
---
# <a name="shipment-auto-updates"></a>Automatiske oppdateringer av forsendelser

[!include [banner](../includes/banner.md)]

Funksjonen for automatisk oppdatering av forsendelse oppdaterer antall automatisk (både økninger og reduksjoner) på en lastlinje som er knyttet til en forsendelse, etter at lasten er frigitt til et lager. Denne funksjonaliteten forblir aktivert til lastlinjen til forsendelsen eller lasten behandles på en bølge. Når den brukes, kan ordreoppdateringer automatisk flyte gjennom til lageret, uten å kreve manuell inngripen, til det opprettes et lagerarbeid.

Når funksjonen for automatisk oppdatering av forsendelse ikke brukes, reduseres bare antallet automatisk til det opprettes et lagerarbeid. Brukere må manuelt oppdatere eller slette linjer, og de må deretter frigi linjene på nytt hvis ordreantall økes eller nye ordrelinjer blir lagt til. Ved hjelp av funksjonen for automatisk oppdatering av forsendelse kan bedrifter sømløst levere oppdateringer til lageret uten å måtte bekymre seg om at relaterte forsendelser og laster ikke gjenspeiler ordrelinjeoppdateringer.

Funksjonen for automatisk oppdatering av forsendelse gjelder både for salgsordrelinjer og overføringsordrelinjer, og den er aktivert for et bestemt lager. Firmaer kan derfor bruke forskjellige forsendelsespolicyer for automatisk oppdatering på tvers av lagre, slik de har behov for. Som standard brukes forsendelsespolicyen for automatisk oppdatering for reduksjon av antall for alle lagre som bruker lager lagerstyringsprosesser. Når denne standard policyinnstillingen brukes, reduseres bare antall automatisk flyt til en forsendelse og last til det opprettes et lagerarbeids. Denne virkemåten ligner på virkemåten som ble brukt før funksjonen for automatisk oppdatering av forsendelse ble innført.

## <a name="main-elements-of-the-functionality"></a>Hovedelementer i funksjonaliteten

Funksjonen for automatisk oppdatering av forsendelse er primært beregnet på forsendelsesstatusen for å fastslå om antallet på en lastlinje skal endres når en endring utføres på en salgsordrelinje eller overføringsordrelinje. Den er også hovedsakelig avhengig av forsendelsesstatusen for å fastslå når en ny lastlinje automatisk skal legges til i en eksisterende last. Når forsendelsesstatusen er **Bølget** eller høyere, utføres ingen automatisk oppdatering.

Bølgestatus blir også tatt hensyn til for automatiske oppdateringer. Når bølgen som er relatert til lastlinjen har statusen **Oppbevares**, **Utfører**, **Frigitt**, **Plukket** eller **Levert**, og hvis en bruker prøver å redusere antallet på en lastlinje (via en reduksjon av antall på salgsordrelinjen eller overføringsordrelinjen), vises følgende feilmelding: Kan ikke fjerne reservasjoner fordi det finnes opprettet arbeid som avhenger av reservasjonene. Når bølgen har en av de tidligere nevnte bølgestatusene, og hvis en bruker prøver å øke lastlinjeantallet ved å redusere øke på salgsordrelinjen eller overføringsordrelinjen, blir ikke antallet på lastlinjen økt automatisk. I dette tilfellet må lastlinjen oppdateres manuelt.

## <a name="scenarios"></a>Scenarier

Funksjonen for automatisk oppdatering av forsendelse støtter fire scenarier: legge til en ny ordrelinje, øke antallet på en ordrelinje, redusere antallet på en ordrelinje og fjerne en ordrelinje.

- **Legg til en ny ordrelinje** – Når feltet **Automatisk oppdatering av forsendelse** i hurtigfanen **Lager** på siden **Lagre** (**Lagerstyring \> Oppsett \> Lager \> Lagre**) er satt til **Alltid**, og hvis det finnes en forsendelse for ordren og en ny ordrelinje legges til en salgsordre eller overføringsordre etter at en last allerede er opprettet for salgsordren, oppdateres ikke den eksisterende lasten. En ny lastlinje som ikke har referanse til den eksisterende lasten, blir opprettet og tilknyttet den eksisterende forsendelsen. Den nye linjen legges til i lasten og frigitt.
- **Øk antallet på en ordrelinje** – Når feltet **Automatisk oppdatering av forsendelse** er satt til **Alltid**, og hvis det finnes en forsendelse for ordren og antallet på en eksisterende salgsordrelinje eller overføringsordrelinje blir økt etter at en last allerede er opprettet for salgsordren, økes lastlinjen med samme antall som ordrelinjen. Hvis lasten ble frigitt, men ikke det ikke ble opprettet arbeid, økes lastlinjen med samme antall som ordrelinjen.
- **Reduser antallet på en ordrelinje** – Når feltet **Automatisk oppdatering av forsendelse** er satt til **Alltid** eller **Ved reduksjon av antall**, og hvis det finnes en forsendelse for ordren og antallet på en eksisterende salgsordrelinje eller overføringsordrelinje reduseres etter at en last allerede er opprettet for salgsordren, oppdateres antallet på den tilknyttede lastlinjen slik at det samsvarer, med mindre antallet på lastlinjen allerede er lik eller mindre enn det nye antallet på ordrelinjen. I dette tilfellet påvirkes ikke lastlinjen. Hvis lasten ble frigitt, men det ikke ble opprettet arbeid, blir antallet på den tilknyttede lastlinjen oppdatert slik at det samsvarer, med mindre antallet på lastlinjen allerede er lik eller mindre enn det nye antallet på ordrelinjen. I dette tilfellet påvirkes ikke lastlinjen.
- **Fjern en ordrelinje** – Når feltet **Automatisk oppdatering av forsendelse** er satt til **Alltid** eller **Ved reduksjon av antall**, vises en feilmelding hvis brukeren prøver å fjerne en ordrelinje som det finnes en lastlinje for.

## <a name="example-scenario"></a>Eksempelscenario

For dette scenarioet må du ha demonstrasjonsdata installert, og du må bruke demonstrasjonsdataene for firmaet **USMF**.

### <a name="turn-on-the-auto-update-shipment-functionality"></a>Aktivere funksjonen for automatisk oppdatering av forsendelse

Følg fremgangsmåten nedenfor for å aktivere funksjonen for automatisk oppdatering av forsendelse.

1. Gå til **Lagerstyring \> Oppsett \> Lager \> Lagre**.
2. Velg lager **24**.
3. I hurtigfanen **Lager**, i feltet **Automatisk oppdatering av forsendelse**, endrer du verdien fra **Ved reduksjon av antall** til **Alltid**.

Når du har endret verdien til **Alltid**, blir eventuelle økninger eller reduksjoner i antallene på salgsordrelinjer og overføringsordrelinjer, og eventuelle tillegg av nye linjer, gjenspeilet på forsendelser og laster for det valgte lageret, gitt de tidligere nevnte oppdateringsbegrensningene.

### <a name="change-the-wave-template-so-that-load-lines-arent-automatically-processed"></a>Endre bølgemalen slik at lastlinjer ikke behandles automatisk

Følg fremgangsmåten nedenfor for å konfigurere bølgemalen slik at den ikke behandler lastlinjer automatisk.

1. Gå til **Lagerstyring \> Oppsett \> Bølger \> Bølgemaler**.
2. Velg bølgemalen **24 Standardforsendelse**.
3. Velg **Rediger**.
4. I hurtigfanen **Generelt** setter du alternativet **Automatiser oppretting av bølge** til **Ja**, og kontrollerer at alle andre alternativer er satt til **Nei**.

Det er viktig at arbeid ikke opprettes og frigis automatisk som en del av oppretting av bølge. Når arbeidet er opprettet for lastlinjen som ble opprettet for salgsordrelinjen, oppdateres ikke lastlinjen lenger automatisk hvis antallet på salgsordrelinjen endres.

### <a name="create-a-sales-order"></a>Opprette en salgsordre

Følg fremgangsmåten nedenfor for å opprette en salgsordre.

1. Gå til **Salg og markedsføring \> Salgsordrer \> Alle salgsordrer**.
2. Velg kunden **US-003**.
3. Opprett en linje for varenummer **A0001**.
4. Angi antallet **10**. (Kontroller at du bruker lageret **24**.)
5. Velg **Lagre**.
6. Velg **Frigi til lager** i gruppen **Handlinger** i fanen **Lager** i handlingsruten. Det opprettes en forsendelse og en bølge.

Det opprettes ikke last eller arbeid fordi du endret bølgemalen i forrige fremgangsmåten. Forsendelsesstatusen er **Åpen**, og bølgestatusen er **Opprettet.**

### <a name="decrease-the-quantity-on-a-sales-order-line"></a>Redusere antallet på en salgsordrelinje

Følg fremgangsmåten nedenfor for å redusere antallet på en salgsordrelinje.

1. Gå til **Salg og markedsføring \> Salgsordrer \> Alle salgsordrer**.
2. Velg salgsordren du akkurat har frigitt til lageret.
3. Velg salgsordrelinjen. I **Antall**-feltet endrer du verdien fra **10** til **8**.
4. Fra salgsordrelinjen velger du **Lager \> Forsendelsesdetaljer**. På siden **Forsendelsesdetaljer**, i hurtigfanen **Lastlinjer**, gjenspeiler antallet endringen på salgsordrelinjen.

### <a name="increase-the-quantity-on-a-sales-order-line"></a>Øke antallet på en salgsordrelinje

Følg fremgangsmåten nedenfor for å øke antallet på en salgsordrelinje.

1. Gå til **Salg og markedsføring \> Salgsordrer \> Alle salgsordrer**.
2. Velg salgsordren du tidligere har frigitt til lageret.
3. Endre linjeantallet fra **8** til **12**.
4. Velg **Lagre**.
5. Gå tilbake til siden **Alle salgsordrer**, og velg salgsordren på nytt.
5. Velg **FOrsendelsesdetaljer** i gruppen **Beslektet informasjon** i fanen **Lager** i handlingsruten. På siden **Forsendelsesdetaljer**, i hurtigfanen **Lastlinjer**, gjenspeiler antallet endringen på salgsordrelinjen.

Selv om antallet på lastlinjen økes fra 8 til 12, forblir bare åtte varer reservert med mindre automatisk reservering er aktivert. Fordi antallet som ble lagt til den eksisterende forsendelsen ikke reserveres, og hvis bølgen behandles på dette tidspunktet uten reservering, opprettes det bare arbeid for antallet som allerede er reservert.

> [!NOTE]
> Når antallet på en ordrelinje reduseres, påvirkes ikke antallet på lastlinjen hvis det allerede er lik eller mindre enn det nye antallet på ordrelinjen. Når antallet på en ordrelinje økes, økes lastlinjen med samme antall som ordrelinjen. Hvis antallet på ordrelinjen er forskjellig fra antallet på lastlinjen, forblir differansen den samme.

### <a name="add-a-sales-order-line"></a>Legge til en salgsordrelinje

Følg fremgangsmåten nedenfor for å legge til en salgsordrelinje.

1. Gå til **Salg og markedsføring \> Salgsordrer \> Alle salgsordrer**.
2. Velg salgsordren du tidligere har frigitt til lageret.
3. Opprett en linje for varenummer **A0002**.
4. I feltet **Antall** angi **10**. (Kontroller at du bruker lager **24**.) Den nye linjen legges automatisk til i den eksisterende forsendelsen.
5. Velg **Lagre**.
6. Gå tilbake til siden **Alle salgsordrer**, og velg salgsordren på nytt.
7. Velg **FOrsendelsesdetaljer** i gruppen **Beslektet informasjon** i fanen **Lager** i handlingsruten. Legg merke til den andre lastlinjen i hurtigfanen **Lastlinjer** på siden **Forsendelsesdetaljer**.

Fordi salgsordrelinjen du nettopp la til i den eksisterende forsendelsen, ikke er reservert, og hvis bølgen behandles på dette tidspunktet, opprettes det bare arbeid for antallet på den første salgsordrelinjen og den første lastlinjen.

### <a name="process-a-wave"></a>Behandle en bølge

Følg fremgangsmåten nedenfor for å behandle bølgen.

1. Gå til **Lagerstyring \> Utgående bølger \> Forsendelsesbølger \> Alle bølger**.
2. Velg bølgen du opprettet tidligere.
3. I handlingsruten, i fanen **Bølge**, i **Bølge**-gruppen, velger du **Behandle**.

Bølgen behandles og oppretter arbeid for de reserverte antallene på lastlinjene. Forsendelsesstatusen oppdateres **Åpen** til **Bølget**. Når forsendelsesstatusen oppdateres til **Bølget**, vil eventuelle endringer som oppstår, for eksempel reduksjon eller økning av linjeantallet eller tilføying av nye linjer i salgsordren, ikke påvirke de eksisterende lastlinjene som er knyttet til den bølgede forsendelsen.

Hvis en forsendelse har statusen **Bølget** eller høyere, vil ikke oppdateringer av antallet på en salgsordrelinje gjenspeiles på eller valideres mot en lastlinje som er knyttet til forsendelsen. Endringer i antallet på en lastlinje må gjøres direkte på lastlinjen.

Validering utføres etter at arbeid er opprettet for lastlinjen og det er gjort en reservering. En reduksjon av antallet på salgsordrelinjen blir deretter validert mot reservasjonen av arbeidslinjen.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]