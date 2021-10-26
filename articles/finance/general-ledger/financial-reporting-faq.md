---
title: Vanlige spørsmål om finansrapportering
description: Dette emnet gir svar på vanlige spørsmål om finansrapportering.
author: jiwo
ms.date: 07/07/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2021-01-13
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 3690a541b503281f204221a72bfb5a371984d9e4
ms.sourcegitcommit: 25b3dd639e41d040c2714f56deadaa0906e4b493
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/06/2021
ms.locfileid: "7605285"
---
# <a name="financial-reporting-faq"></a>Vanlige spørsmål om finansrapportering

Dette emnet gir svar på vanlige spørsmål om finansrapportering.

## <a name="how-do-i-restrict-access-to-a-report-by-using-tree-security"></a>Hvordan begrenser jeg tilgang til en rapport med tresikkerhet?

Følgende eksempel viser hvordan du begrenser tilgang til en rapport med tresikkerhet.

Demofirmaet USMF har en **balanserapport** som ikke alle finansrapporteringsbrukere skal ha tilgang til. Du kan bruke tresikkerhet til å begrense tilgang til en rapport, slik at bare bestemte brukere får tilgang til den.

1. Logg på Financial Reporter Report Designer.
2. Velg **Fil \> Ny \> Tredefinisjon** til å opprette en ny tredefinisjon.
3. Dobbelttrykk (eller dobbeltklikk) på linjen **Sammendrag** i kolonnen **Enhetssikkerhet**.
4. Velg **Brukere og grupper**.
5. Velg brukerne eller gruppene som må ha tilgang til rapporten.
6. Velg **Lagre**.
7. I rapportdefinisjonen legger du til den nye tredefinisjonen.
8. Velg **Innstilling** i tredefinisjonen. Under **Valg av rapporteringsenhet** velger du **Inkluder alle enheter**.

## <a name="how-do-i-identify-which-accounts-dont-match-my-balances"></a>Hvordan identifiserer jeg hvilke kontoer som ikke samsvarer med saldoene?

Hvis du har en rapport som ikke samsvarer saldoene, bruker du følgende fremgangsmåter til å identifisere hver konto og hvert avvik.

### <a name="in-financial-reporter-report-designer"></a>I Financial Reporter Report Designer

1. Opprett en ny raddefinisjon.
2. Velg **Rediger \> Sett inn rader fra dimensjoner**.
3. Velg **MainAccount**.
4. Velg **OK**.
5. Lagre raddefinisjonen.
6. Opprett en ny kolonnedefinisjon.
7. Opprett en ny rapportdefinisjon.
8. Velg **Innstillinger** og fjern merket for dette alternativet.
9. Generer rapporten. 
10. Eksporter rapporten til Microsoft Excel.

### <a name="in-dynamics-365-finance"></a>I Dynamics 365 Finance

1. Gå til **Økonomimodul \> Forespørsler og rapporter \> Råbalanse**.
2. Angi følgende felter:

    - **Fra-dato** – Angi startdatoen på regnskapsåret.
    - **Til-dato** – Angi datoen du genererer rapporten for.
    - **Finansdimensjon** – Angi dette feltet til **Hovedkontosett**.

3. Velg **Beregn**.
4. Eksporter rapporten til Excel.

Du skal nå kunne kopiere dataene fra Excel-rapporten i Financial Reporter til rapporten **Råbalanse** slik at du kan sammenligne kolonnene **Sluttsaldo**.

## <a name="when-i-design-a-report-in-report-designer-or-when-i-generate-a-financial-report-i-received-the-following-message-the-operation-could-not-be-completed-due-to-a-problem-in-the-data-provider-framework-how-should-i-respond"></a>Når jeg utformer en rapport i Report Designer, eller når jeg genererer en finansrapport, får jeg følgende melding: Operasjonen kan ikke fullføres på grunn av et problem i dataleverandørrammeverket. Hvordan skal jeg svare?

Meldingen indikerer at det oppstod et problem da systemet forsøkte å hente økonomiske metadata fra datatorget mens du brukte finansrapportering. Det finnes to måter å svare på dette problemet på:

- Gå gjennom integreringsstatusen for dataene ved å gå til **Verktøy \> Integreringsstatus** i Report Designer. Hvis integreringen ikke er fullført, må du vente til den er fullført. Deretter prøver du det du gjorde da du mottok meldingen.
- Kontakt kundestøtte for å identifisere og arbeide deg gjennom problemet. Det kan være inkonsekvente data i systemet. Støtteteknikere kan hjelpe deg med å identifisere problemet på serveren og finne bestemte data som kan kreve en oppdatering.

## <a name="how-does-the-selection-of-historical-rate-translation-affect-report-performance"></a>Hvordan påvirker valg av historisk kursomregning rapportytelsen?

Den historiske kursen brukes vanligvis med opptjente inntekter, eiendom, anlegg og utstyr og egenkapitalkonti. Den historiske kursen kan være nødvendig, basert på retningslinjer fra styret for regnskapsstandarder (FASB) eller god regnskapsskikk (GAAP). Hvis du vil ha mer informasjon, kan du se [Valutafunksjoner i finansrapportering](financial-reporting-currency-capability.md).

## <a name="how-many-types-of-currency-rate-are-there"></a>Hvor mange typer valutakurser finnes det?

Det finnes tre typer:

- **Gjeldende kurs** – Denne typen brukes vanligvis med balansekonti. Den er vanligvis kjent som *spotvalutakursen* og kan være kursen på den siste dagen i måneden eller en annen forhåndsbestemt dato.
- **Gjennomsnittskurs** – Denne typen brukes vanligvis med resultatkonti. Du kan konfigurere gjennomsnittskursen for å utføre enten et enkelt gjennomsnitt eller et avveid gjennomsnitt.
- **Historisk kurs** – Denne typen brukes vanligvis med opptjente inntekter, eiendom, anlegg og utstyr og egenkapitalkonti. Disse kontiene kan være nødvendige, basert på FASB- eller GAAP-retningslinjer.

## <a name="how-does-historical-currency-translation-work"></a>Hvordan fungerer historisk valutaomregning?

Kursene er spesifikke for transaksjonsdatoen. Derfor omregnes hver transaksjon individuelt, basert på den nærmeste valutakursen.

For historisk valutaomregning kan de forhåndsberegnede periodesaldoene brukes i stedet for individuelle transaksjonsdetaljer. Denne virkemåten er forskjellig fra virkemåten for gjeldende kursomregning.

## <a name="how-does-historical-currency-translation-affect-performance"></a>Hvordan påvirker historisk valutaomregning ytelsen?

Når data som presenteres i rapportene, oppdateres, kan det være en forsinkelse fordi beløp må beregnes på nytt ved å kontrollere transaksjonsdetaljer. Denne forsinkelsen utløses hver gang kursene oppdateres eller flere transaksjoner posteres. Hvis for eksempel tusenvis av konti er konfigurert for historisk omregning et par ganger om dagen, kan det være en forsinkelse på opptil en time før dataene i rapporten oppdateres. På den andre siden, hvis det er et mindre antall spesifikke konti, kan behandlingstidene for oppdateringer av rapportdataene reduseres til minutter eller mindre.

På samme måte, når rapporter genereres ved hjelp av valutaomregning for historiske typekonti, vil det være ekstra beregninger per transaksjon. Avhengig av antall konti kan rapportgenereringstiden dobles eller mer.

## <a name="what-are-the-estimated-data-mart-integration-intervals"></a>Hva er de estimerte intervallene for data mart-integrering?

Financial Reporter bruker 16 oppgaver til å kopiere data fra Dynamics 365 Finance til finansrapporteringsdatabasen. Tabellen nedenfor viser disse 16 oppgavene og viser intervallet som angir hvor ofte hver oppgave skal kjøres. Intervallene kan ikke endres.

| Navn                                                       | Intervall | Intervalltid |
|------------------------------------------------------------|----------|-----------------|
| AX 2012 Kontokategorier til kontokategori            | 41       | minutter         |
| AX 2012 Kontoer til konto                                | 7        | minutter         |
| AX 2012 Firmaer til firma                               | 300      | sekunder         |
| AX 2012 Firmaer til organisasjon                          | 23       | minutter         |
| AX 2012 Dimensjonskombinasjoner til dimensjonskombinasjon    | 1        | minutt         |
| AX 2012 Dimensjonsverdier til dimensjonsverdi                | 11       | minutter         |
| AX 2012 Dimensjoner til dimensjon                            | 31       | minutter         |
| AX 2012 Valutakurser til valutakurs                    | 17       | minutter         |
| AX 2012 Regnskapsår til regnskapsår                        | 13       | minutter         |
| AX 2012 Økonomimodultransaksjoner til fakta                | 1        | minutter         |
| AX 2012 Organisasjonshierarkier til tre                   | 3 600    | sekunder         |
| AX 2012 Scenarioer til scenario                              | 29       | minutter         |
| AX 2012 Transaksjonstypekvalifikatorer til faktatypekvalifikator | 19       | minutter         |
| Vedlikeholdsoppgave                                           | 1        | minutt         |
| MR-rapportdefinisjoner til AX7-finansrapporter             | 45       | sekunder         |
| MR-rapportversjoner til AX-finansrapportversjoner         | 45       | sekunder         |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
