---
title: Kvalitetsstyringsprosesser
description: Denne artikkelen inneholder informasjon om kvalitetsstyringsprosessen for materiell med avvik. Det beskriver hvordan du kan bruke kvalitetskontrollfunksjonen, hvordan du definerer og vedlikeholder avvik og hvordan du håndterer korrigeringer.
author: perlynne
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventItemSampling, InventNonConformanceHistory, InventNonConformanceTable, InventQualityOrderLineResults, InventQualityOrderTable, InventTestCorrection, InventTestDiagnosticType, InventTestInstrument, InventTestReportSetup, InventTestTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 11574
ms.assetid: 5ac8a059-5cb4-4cb5-ba14-b944bd08dae9
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2ab3b886b9d5237e96e193d7369c6060f19516e5
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4434683"
---
# <a name="quality-management-processes"></a>Kvalitetsstyringsprosesser

[!include [banner](../includes/banner.md)]

Denne artikkelen inneholder informasjon om kvalitetsstyringsprosessen for materiell med avvik. Det beskriver hvordan du kan bruke kvalitetskontrollfunksjonen, hvordan du definerer og vedlikeholder avvik og hvordan du håndterer korrigeringer.

Kvalitetssikring omfatter produkttesting og håndtering av materiell med avvik. Kvalitetsstyringsprosesser bidrar til å sikre produktkvalitet på høyt nivå i forsyningskjeden. Disse prosessene bidrar også til å optimalisere forsyningskjedeprosesser og øke kundetilfredsheten. Kvalitetsstyring kan hjelpe deg med å administrere behandlingstiden når du håndterer produkter med avvik, uavhengig av opprinnelsespunktet for disse produktene. Du kan koble diagnoseresultater til korrigeringsoppgaver. Systemet kan planlegge aktiviteter for å løse problemer og dermed forhindre gjentakelser av disse problemene i fremtiden. Kvalitetsstyring lar deg også spore problemer (inkludert interne problemer) etter problemtype, og lar deg angi løsninger som kortsiktige eller langsiktige. Statistikk om nøkkelytelsesindikatorer (KPI-er) gir innsikt i avviksproblemer som har oppstått tidligere, og løsninger som ble brukt til å rette feilene. Du kan bruke historiske data for å undersøke effektiviteten til kvalitetstiltak som er iverksatt tidligere, og bestemme nødvendige tiltak som skal brukes i fremtiden.

## <a name="controlling-the-quality-management-process"></a>Styre kvalitetstyringssprosessen
Her er noen måter du kan styre kvalitetstyringssprosessen på:

-   Opprett kvalitetsordrer som er basert på utløserpunkter som for eksempel "ved produktmotta" for innkommende operasjoner eller "ved produktplukking" for utgående operasjoner.
-   Dokumenter testresultater, og bestem om resultatene oppfyller de etablerte testkriteriene og de akseptable kvalitetsnivåene.
-   Bruk dokumentbehandling for detaljerte produktspesifikasjoner og brukerspesifikke notater som en del av rapporteringen under inspeksjonsprosessen.
-   Vedlikehold produkter med avvik, og samsvar disse produktene med ytterligere avviksinformasjon for å spore den opprinnelige årsaken til et problem.
-   Dokumenter kostnaden ved administrasjon av et avvik. Denne kostnaden kan omfatte varene (for eksempel reservedeler), diverse tillegg og arbeidstimene på timelistene som er nødvendige for å korrigere avviket.
-   Planlegg feilrettelsesprosesser ved å bruke rettelseshåndtering som er koblet til kvalitetsordrer.

[![Kvalitetsstyringsprosess](./media/quality-management-process-diagram.png)](./media/quality-management-process-diagram.png)  

## <a name="product-testing-and-quality-orders"></a>Produkttesting og kvalitetsordrer
Produkttesting kalles ofte kvalitetskontroll og bruker kvalitetsordrer. Ved hjelp av funksjonen for kvalitetskontroll kan du gjøre følgende:

-   Definere tester som må utføres på materialer. Disse testene inkluderer kvalitetsspesifikasjonene, det relevante testinstrumentet, dokumenter som beskriver testen, en prøveplan og de akseptable kvalitetsnivåene (AQL).
-   Opprette en kvalitetsordre som identifiserer testene som må utføres for en bestemt ordre, for eksempel en bestilling eller produksjonsordre, eller for et bestemt lagerantall. Du kan opprette en kvalitetsordre manuelt, eller du kan automatisk generere en kvalitetsordre basert på kvalitetsretningslinjer.
-   Definere kvalitetsretningslinjer som er knyttet til innkjøp, karantene, produksjon eller salgsordrer i hver forretningsprosess, slik at en kvalitetsordre kan genereres automatisk som identifiserer testkrav for innkommende og utgående materialer.
-   Registrere testresultatene i en kvalitetsordre, vurdere testresultatene mot akseptabelt kvalitetsnivå og skrive ut et analysesertifikat med testresultatene.

## <a name="nonconformance"></a>Avvik
Et avvik beskriver en vare som har et kvalitetsproblem. Avviksprosessen lar deg opprette en avviksordre som beskriver antallet materiell med avvik, problemkilde, problemtype og en utdypende forklaring. Du kan definere en klassifikasjon av problemtyper for å gjøre analysen av materialene med avvik enklere. Du kan også skrive ut en avviksbrikke og en avviksrapport til veiledning for disposisjonen av materiell med avvik. Brikken og rapporten kan eksempelvis vise tilstanden **Kan ikke brukes** eller **Begrenset bruk**.

Tabellen nedenfor viser seks standard avvikstyper og beskriver informasjonen som må registreres for hver type.

| Avvikstype   | Kildeinformasjon                                                                                                                                                                                                                          |
|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Kunde              | Kundens kontonummer, salgsordrenummeret eller et partinummer for en salgsordretransaksjon. Avviket kan for eksempel være knyttet til en bestemt salgsordreforsendelse eller til tilbakemeldinger fra kunder om produktkvalitet.       |
| Tjenesteforespørsel       | Kundens kontonummer, salgsordrenummeret eller et partinummer for en salgsordretransaksjon. Avviket kan for eksempel være knyttet til en bestemt salgsordreforsendelse eller til klager fra kunder om varekvalitet.     |
| Leverandør                | Leverandørens kontonummer, bestillingsnummeret eller et partinummer for en bestillingstransaksjon. Avviket kan for eksempel være relatert til et bestillingsmottak eller en leverandørs spørsmål angående en del de leverer. |
| Produksjon            | Produksjonsordrenummeret eller et partinummer til en produksjonsordretransaksjon. Avviket kan for eksempel være relatert til et konkret parti som er produsert.                                                                      |
| Intern              | Kvalitetsordrenummeret eller et partinummer til en kvalitetsordretransaksjon. Avviket kan for eksempel være relatert til testene som utføres som en del av en kvalitetsordre eller en ansatts spørsmål angående produktkvalitet.     |
| Koproduktproduksjon | Et avvik for produksjonsordre for koprodukt som er knyttet til partiproduksjonsordrer.                                                                                                                                                    |

Avvik er knyttet til en problemtype. Problemtyper som er definert på **Problemtyper**-siden, der du kan angi problemtypene som kan knyttes til hver avvikstype. Problemtypene for avvik av **Tjenesteforespørsel**-typen kan eksempelvis reflektere en klassifisering av kundeklager, mens problemtypene for avvik av **Intern**-typen kan representere en klassifisering av mangelkoder.

Når du oppretter et nytt avvik, velger du avvikstypen og problemtypen. Den innledende godkjenningsstatusen er **Ny**, som representerer en forespørsel om handling. Det neste trinnet et å endre godkjenningsstatusen til **Godkjent** eller **Avvist** for å angi at du kommer til å eller ikke kommer til å handle på avviket. Du kan også lukke et avvik (ved å merke av i en egen avmerkingsboks) for å angi at du er ferdig med det, eller du kan åpne avviket på nytt for å angi at det må ses nærmere på.

Du kan angi merknader for et avvik ved å knytte til et dokument. Det er lurt å definere en unik dokumenttype for avvik ved hjelp av **Dokumenttype**-siden. Du kan deretter bruke **Rapportoppsett**-siden til å definere om kommentarer for denne dokumenttypen skal skrives ut på avviksrapporten og avviksbrikken. Avviksrapporten og avviksbrikken kan bidra med materialfordeling. Du kan generere rapporter og brikker selektivt basert på utvalgskriterier som er knyttet til et avvik. Disse kriteriene inkluderer avviksnummer, vare, kunde, leverandør og status.

Avviksrapporten viser den avviksnummer, vare og problemtype. Avhengig av rapportoppsettpolicyen kan det hende at rapporten også viser tilknyttede merknader om avviket. Avviksbrikken viser lignende informasjon og inkluderer også karantenesonen og -typen (for eksempel **Begrenset bruk** eller **Kan ikke brukes**) som du tilordnet avviket for å lede disposisjonen av feilmaterialet.

## <a name="approved-nonconformance"></a>Godkjent avvik
Du kan velge om du vil definere en eller flere tilknyttede operasjoner for et godkjent avvik. En tilknyttet operasjon beskriver arbeidet som skal utføres, og inneholder en liste over kvalitetsoperasjonene som du har definert, og beskrivende tekst om årsaken til arbeidet. Når en operasjon er definert, kan du velge å definere ulike tillegg, varer og timelistearbeidstimer som må til for å utføre arbeidet. De beregnede kostnadene er vist for den tilknyttede operasjonen, og de totale beregnede kostnadene er vist for avviket. De beregnede kostnadene og underliggende detaljene (om varer, arbeidstimer og tillegg) representerer referanseinformasjon, og de brukes bare innenfor kvalitetsstyringsfunksjonen.

Du kan velge å opprette en kvalitetsordre fra et avvik ved å utføre en spørring for kvalitetsordrer først, og deretter opprette den nye kvalitetsordren. En kvalitetsordre kan for eksempel identifisere et behov for å teste feilmaterialet (eller teste på nytt). Den nyopprettede kvalitetsordren viser koblingen til det opprinnelige avviket.

Du kan velge å koble ett avvik til et annet og opprette et nytt avvik fra et eksisterende avvik. Koblingen kan for eksempel reflektere sammenhengen mellom kvalitetsproblemer.

## <a name="correction-handling"></a>Rettelseshåndtering
På **Rettelser**-siden kan du opprette en liste over avvik som må korrigeres. Hver rettelse er tilknyttet diagnosetypen som forårsaket problemet som ble oppdaget. **Rettelser**-siden inneholder også informasjon om hvem som må utføre en korrigerende handling, og når. Du kan beskrive detaljene for problemet og den korrigerende handlingen som kreves, ved å knytte et dokument til rettelsen. Når avviket er tatt hånd om eller løst, lukker du rettelsen ved å velge **Fullført**-alternativet. Du kan også angi at løsningen var en kortsiktig løsning.

Det er lurt å definere en unik dokumenttype for rettelser ved hjelp av **Dokumenttype**-siden. Du kan deretter bruke **Rapportoppsett**-siden til å definere om kommentarer for denne dokumenttypen skrives ut på rettelsesrapporten. En utskrevet rettelsesrapport viser informasjon om avviket og de tilknyttede avviksmerknadene. Rapporten inneholder også rettelsesinformasjonen, for eksempel diagnosetypen og de tilknyttede rettelsesmerknadene.

<a name="additional-resources"></a>Tilleggsressurser
--------

[Oversikt over kvalitetsstyring](enable-quality-management.md)

[Avviksstyring](enable-nonconformance-management.md)

[Lagerblokkering](inventory-blocking.md)

[Karanteneordrer](quarantine-orders.md)

[Definere kvalitetsordrer](tasks/set-up-quality-orders.md)

[Kontrollere varekvaliteten](tasks/inspect-quality-goods.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]