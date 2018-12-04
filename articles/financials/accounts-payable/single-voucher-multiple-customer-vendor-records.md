---
title: "Enkelt bilag med flere poster for kunde eller leverandør"
description: "Dette emnet gir en oversikt over hva som skjer når du posterer ett bilag med flere poster for kunde eller leverandør. Denne funksjonaliteten vil ikke være tilgjengelig i fremtidige versjoner av Microsoft Dynamics 365 for Finance and Operations. Derfor anbefales det ikke å bruke denne metoden for postering på grunn av regnskapsvirkningen på utligningsbehandling."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 222534
ms.assetid: d4df11ce-4d36-4c66-8230-f5fc58e021bc
ms.search.region: global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: 4c499e31fb42a69dff6ac41faac0c78f7f4d1876
ms.contentlocale: nb-no
ms.lasthandoff: 03/26/2018

---

# <a name="single-voucher-with-multiple-customer-or-vendor-records"></a>Enkelt bilag med flere poster for kunde eller leverandør

[!include [banner](../includes/banner.md)]

Dette emnet gir en oversikt over hva som skjer når du posterer ett bilag med flere poster for kunde eller leverandør. Denne funksjonaliteten vil ikke være tilgjengelig i fremtidige versjoner av Microsoft Dynamics 365 for Finance and Operations. Derfor anbefales det ikke å bruke denne metoden for postering på grunn av regnskapsvirkningen på utligningsbehandling. 

Noen eksempler der ett bilag brukes for flere kunder eller leverandører, inkluderer saldooverføringer mellom kunder, og motregningssaldoer mellom kunder og leverandører i den samme organisasjonen. 

Et bilag som inneholder mer enn én kunde eller leverandør, kan angis ved hjelp av én av følgende metoder:

-   Ved hjelp av en journal som har alternativet **Bare ett bilagsnummer** valgt slik at alle linjene som er lagt til i journalen, inkluderes på det samme bilaget.
-   Ved hjelp av et bilag med flere linjer, der det er ingen finansmotkontoer, med mer enn én kunde eller leverandør.
-   Angir et bilag der kontoen og motkontoen er leverandør/leverandør, kunde/kunde, leverandør/ kunde eller kunde/leverandør.

Dette emnet forklarer hvordan utligningen skal behandles når ett bilag med flere poster for kunde eller leverandør posteres. Dette emnet inneholder også løsninger som hjelper deg med å forstå hvordan du unngår å bruke ett bilag med flere kunder eller leverandører. Det er spesielt eksempler som viser to vanlige utligningsscenarier som påvirkes ved å bruke ett bilag med flere kunder eller leverandører:

-   Kontantrabattregnskap
-   Revalueringsregnskap

## <a name="how-does-settlement-impact-single-voucher-usage"></a>Hvordan påvirker utligning bruk av ett bilag
Ved postering av et bilag som inneholder flere poster for kunde eller leverandør, opprettes det ett regnskapsbilag som inneholder flere saldoer for kunde eller leverandør. Under utligningsprosessen brukes de opprinnelige regnskapsoppføringer til å opprette regnskapsoppføringer for kontantrabatt, urealisert fortjeneste og tap, realisert fortjeneste og tap og frigivelse av samlekontoen for det opprinnelige dokumentet. Hvis en kontantrabatt for eksempel blir utført når du utligner en leverandørbetaling mot en faktura, må kontantrabattregnskapet postere til leverandørfinanskontoen fra den opprinnelige fakturaen. Hvis den opprinnelige fakturaen ble bokført i et bilag som inneholder flere leverandørposter, summeres det opprinnelige regnskapet. Ettersom det er ikke mulig å få tilgang til den detaljerte regnskapsoppføringen for hver leverandørtransaksjon i det enkeltstående bilaget, er det i dette tilfellet umulig å finne ut hvordan brukeren hadde tenkt å beregne kontantrabatt.

### <a name="one-voucher-with-multiple-vendors-and-the-impact-on-cash-discount-accounting"></a>Ett bilag med flere leverandører og innvirkningen på kontantrabattregnskap

I eksemplet nedenfor blir flere leverandørfakturaer registrert i Finans på ett bilag på siden **Økonomijournal**. Disse fakturaene distribueres på tvers av flere kontodimensjoner.

|             |                  |              |                 |           |            |
|-------------|------------------|--------------|-----------------|-----------|------------|
| **Bilag** | **Kontotype** | **Konto**  | **Beskrivelse** | **Debet** | **Kreditt** |
| GNJL001     | Leverandør           | 1001         | INV1            |           | 100,00     |
| GNJL001     | Leverandør           | 1001         | INV2            |           | 200,00     |
| GNJL001     | Leverandør           | 1001         | INV3            |           | 300,00     |
| GNJL001     | Finans           | 606300-001-- | INV1            |   50,00   |            |
| GNJL001     | Finans           | 606300-002-- | INV1            |   50,00   |            |
| GNJL001     | Finans           | 606300-003-- | INV2            | 200,00    |            |
| GNJL001     | Finans           | 606300-004-- | INV3            | 300,00    |            |

Ett bilag opprettes etter bokføring.

|             |              |                  |                                    |
|-------------|--------------|------------------|------------------------------------|
| **Bilag** | **Konto**  | **Posteringstype** | **Beløp i transaksjonsvaluta** |
| GNJL001     | 606300-001-- | Finansjournal   | 50,00                              |
| GNJL001     | 606300-002-- | Finansjournal   | 50,00                              |
| GNJL001     | 606300-003-- | Finansjournal   | 200,00                             |
| GNJL001     | 606300-004-- | Finansjournal   | 300,00                             |
| GNJL001     | 200110-001-  | Leverandørsaldo   | -100,00                            |
| GNJL001     | 200110-001-  | Leverandørsaldo   | -200,00                            |
| GNJL001     | 200110-001-  | Leverandørsaldo   | -300.00                            |

Legg merke til at bilaget inneholder tre oppføringer for posteringstypen for leverandørsaldo i ett bilag. Det er ikke mulig å angi at 50.00 debet for 606300-001 og 50.00 debet for 606300-002 skal motposteres leverandørsaldoposten for 200110-001. Dette er fordi brukeren har angitt flere leverandørposter i ett bilag.

Ved hjelp av dette eksemplet kan man analysere hvordan bruk av ett bilag påvirker nedstrøms utligningsregnskap. Anta at du betaler 197,00 av fakturaens beløp på 200,00 og en kontantrabatt på 3,00. Legg merke til at verdien på kontantrabattkontoen fordeles på tvers av alle dimensjonene fra fakturabilagets utgiftskontoer. Dette skyldes at ett bilag ble brukt til å postere fakturaen ovenfor, uten informasjon om hvordan brukeren hadde tenkt at utgiftsdistribusjonene skulle samsvare med leverandørsaldoen i enkeltbilaget.

|             |              |                      |           |            |
|-------------|--------------|----------------------|-----------|------------|
| **Bilag** | **Konto**  | **Posteringstype**     | **Debet** | **Kreditt** |
| APPAYM001   | 200110-001-  | Leverandørsaldo       | 197.00    |            |
| APPAYM001   | 110110-001-  | Bank                 |           | 197.00     |
| 14000056    | 520200-001-- | Leverandørkontantrabatt |           | 0.25       |
| 14000056    | 520200-002-- | Leverandørkontantrabatt |           | 0.25       |
| 14000056    | 520200-003-- | Leverandørkontantrabatt |           | 1,00       |
| 14000056    | 520200-004-- | Leverandørkontantrabatt |           | 1.50       |
| 14000056    | 200110-001-  | Leverandørsaldo       | 3,00      |            |

Hvis brukeren er misfornøyd med kontantrabatten som tildeles på tvers av alle utgiftsdistribusjoner fra den opprinnelige fakturaen, i stedet for ett bilag, må flere bilag brukes til å registrere fakturaene. Her er et eksempel på hvordan flere bilag kan skrives inn i Økonomimodul, i stedet for å bruke ett bilag, som vist i begynnelsen av dette eksemplet.

|             |                  |              |                 |           |            |                 |                    |
|-------------|------------------|--------------|-----------------|-----------|------------|-----------------|--------------------|
| **Bilag** | **Kontotype** | **Konto**  | **Beskrivelse** | **Debet** | **Kreditt** | **Motregningstype** | **Motkonto** |
| GNJL001     | Leverandør           | 1001         | INV1            |           | 100,00     | Finans          | &lt;tomt&gt;:      |
| GNJL001     | Finans           | 606300-001-- | INV1            |   50,00   |            | Finans          | &lt;tomt&gt;:      |
| GNJL001     | Finans           | 606300-002-- | INV1            |   50,00   |            | Finans          | &lt;tomt&gt;:      |
| GNJL002     | Leverandør           | 1001         | INV2            |           | 200,00     | Finans          | 606300-003--       |
| GNJL003     | Leverandør           | 1001         | INV3            |           | 300,00     | Finans          | 606300-004--       |

Når INV2 er betalt, blir følgende oppføring utført. Legg merke til at kontantrabattens finansdimensjoner følger den tilknyttede utgiftens finansdimensjoner.

|             |              |                      |           |            |
|-------------|--------------|----------------------|-----------|------------|
| **Bilag** | **Konto**  | **Posteringstype**     | **Debet** | **Kreditt** |
| APPAYM001   | 200110-001-  | Leverandørsaldo       | 197.00    |            |
| APPAYM001   | 110110-001-  | Bank                 |           | 197.00     |
| 14000056    | 520200-003-- | Leverandørkontantrabatt |           | 3,00       |
| 14000056    | 200110-001-  | Leverandørsaldo       | 3,00      |            |

### <a name="one-voucher-with-multiple-vendors-and-the-impact-on-realized-gainloss-accounting"></a>Ett bilag med flere leverandører og innvirkningen på regnskap for realisert gevinst/tap

|             |                  |             |                 |           |            |                  |              |
|-------------|------------------|-------------|-----------------|-----------|------------|------------------|--------------|
| **Bilag** | **Kontotype** | **Konto** | **Beskrivelse** | **Debet** | **Kreditt** | **Kontotype** | **Konto**  |
| GNJL001     | Leverandør           | 1001        | INV1            |           | 100,00     | Finans           | 606300-001-- |
| GNJL001     | Leverandør           | 1001        | INV2            |           | 200,00     | Finans           | 606300-002-- |

I eksemplet nedenfor blir flere leverandørfakturaer registrert i Finans på ett bilag på siden **Økonomijournal**. Disse fakturaene distribueres på tvers av flere kontodimensjoner. Ett bilag opprettes etter bokføring.

|             |              |                  |                                          |                                         |
|-------------|--------------|------------------|------------------------------------------|-----------------------------------------|
| **Bilag** | **Konto**  | **Posteringstype** | **Beløp i transaksjonsvaluta (EUR)** | **Beløp i regnskapsvaluta (USD)** |
| GNJL001     | 606300-001-- | Finansjournal   | 100,00                                   | 114.00                                  |
| GNJL001     | 606300-002-- | Finansjournal   | 200,00                                   | 228.00                                  |
| GNJL001     | 200110-001-  | Leverandørsaldo   | -100,00                                  | -114.00                                 |
| GNJL001     | 200110-001-  | Leverandørsaldo   | -200,00                                  | -228.00                                 |

Legg merke til at bilaget inneholder to oppføringer for posteringstypen for leverandørsaldo i ett bilag. Det er ikke mulig å angi at debet for 606300-001 skal motposteres leverandørsaldoposten på 100,00 til 200110 - 001. Dette er fordi brukeren har angitt flere leverandørposter i ett bilag. 

Ved hjelp av dette eksemplet kan man analysere hvordan bruk av ett bilag påvirker nedstrøms utligningsregnskap. Anta at regnskapsvalutaen er USD og transaksjonene ovenfor ble postert i en transaksjonsvalutaen EUR. Anta at du betaler hele fakturaen på EUR 200,00, men det oppstår et realisert tap på grunn av valutakursen endret seg i tidsrommet fra du posterte fakturaen til betalingen ble gjennomført. Legg merke til at verdien på kontoen for realisert tap fordeles på tvers av alle dimensjonene fra fakturabilagets utgiftskontoer. I dette tilfellet ble både dimensjon 001 og 002 fordelt, selv om brukerens oppfatning kan være at bare 002 hører til utgiftskontoen fra fakturaen som utlignes. Dette skyldes at ett bilag ble brukt til å postere fakturaen ovenfor, og dermed er det umulig å antyde hvordan brukeren hadde tenkt at utgiftsdistribusjonene skulle samsvare med leverandørsaldoen i enkeltbilaget.

|             |             |                    |                                          |                                         |
|-------------|-------------|--------------------|------------------------------------------|-----------------------------------------|
| **Bilag** | **Konto** | **Posteringstype**   | **Beløp i transaksjonsvaluta (EUR)** | **Beløp i regnskapsvaluta (USD)** |
| APPAYM001   | 200110-001- | Leverandørsaldo     | 200,00                                   | 230.00                                  |
| APPAYM001   | 110110-001- | Bank               | -200,00                                  | -230.00                                 |
| 14000056    | 801300-001- | Kurstap | 0,00                                     | 0.67                                    |
| 14000056    | 801300-002- | Kurstap | 0,00                                     | 1.33                                    |
| 14000056    | 200110-001- | Leverandørsaldo     |                                          | -2.00                                   |

Hvis brukeren er misfornøyd med at kurstapet fordeles på tvers av alle utgiftsdistribusjoner fra den opprinnelige fakturaen, i stedet for ett bilag, må flere bilag brukes til å registrere fakturaene. Her er et eksempel på hvordan flere bilag kan skrives inn i Økonomimodul, i stedet for å bruke ett bilag, som vist i begynnelsen av dette eksemplet.

|             |                  |             |                 |           |            |                 |                    |
|-------------|------------------|-------------|-----------------|-----------|------------|-----------------|--------------------|
| **Bilag** | **Kontotype** | **Konto** | **Beskrivelse** | **Debet** | **Kreditt** | **Motregningstype** | **Motkonto** |
| GNJL002     | Leverandør           | 1001        | INV1            |           | 100,00     | Finans          | 606300-001--       |
| GNJL003     | Leverandør           | 1001        | INV2            |           | 200,00     | Finans          | 606300-002--       |

Når INV2 er betalt, blir følgende oppføring utført. Legg merke til at finansdimensjoner for kurstap følger den tilknyttede utgiftens finansdimensjoner.

|             |             |                    |                                          |                                         |
|-------------|-------------|--------------------|------------------------------------------|-----------------------------------------|
| **Bilag** | **Konto** | **Posteringstype**   | **Beløp i transaksjonsvaluta (EUR)** | **Beløp i regnskapsvaluta (USD)** |
| APPAYM001   | 200110-001- | Leverandørsaldo     | 200,00                                   | 230.00                                  |
| APPAYM001   | 110110-001- | Bank               | -200,00                                  | -230.00                                 |
| 14000056    | 801300-002- | Kurstap | 0,00                                     | 2.00                                    |
| 14000056    | 200110-001- | Leverandørsaldo     |                                          | -2.00                                   |

## <a name="one-voucher-for-balance-transfers-and-netting-scenarios"></a>Ett bilag for saldooverføringer og motregningsscenarier
To vanlige scenarier som bruker ett bilag som inneholder flere kunder eller leverandører, inkluderer saldooverføringer fra én kunde/leverandør til en annen kunde/leverandør, og motregning for en kunde og leverandør som er den samme organisasjonen. Eksemplene nedenfor illustrerer den foretrukne metoden for å angi disse scenariene i Finance and Operations som et alternativ til å skrive dem inn i ett bilag. 

En *saldooverføring* er ett bilag med flere kunder angitt med det formålet å overføre saldoen fra én kunde til en annen kunde (samme for leverandører). Dette scenariet kan oppstå når ansvaret for å betale fakturaen skifter til en annen part, for eksempel et underordnet firma som forskyver ansvaret til et overordnet firma. 

Dette eksemplet forutsetter et salg der kunden er kvalifisert for kontantrabatt hvis betaling skjer innen 10 dager. Kunden i dette eksemplet bruker et forsikringsselskap som skal være ansvarlig for å betale vekselen. Forsikringsselskapet defineres som en ny kunde i systemet. Den opprinnelige kundens saldo overføres til forsikringsselskapet, som betaler stykklisten og tar 2 % kontantrabatt for å betale i rabattperioden. 

For å illustrere dette kan du anta at følgende salg skjer til kunden ACME. Følgende regnskapsoppføringer representerer salget.

|                    |                  |           |            |
|--------------------|------------------|-----------|------------|
| **Finanskonto** | **Posteringstype** | **Debet** | **Kreditt** |
| 401100-002-023-    | Omsetning          |           | 100        |
| 130100-002-        | Kundesaldo | 100       |            |

Deretter overfører brukeren den forfalte saldoen fra ACME til forsikringsselskapet i ett bilag i betalingsjournalen for kunder. I Finance and Operations defineres forsikringsselskapet som forsikringskunde.

|             |                  |             |                 |           |            |                 |                    |
|-------------|------------------|-------------|-----------------|-----------|------------|-----------------|--------------------|
| **Bilag** | **Kontotype** | **Konto** | **Beskrivelse** | **Debet** | **Kreditt** | **Motregningstype** | **Motkonto** |
| ARPAYM001   | Kunde         | ACME        | Overføring        |           | 100,00     | Kunde        | Forsikring          |

Legg merke til at oppføringen ovenfor finnes på ett bilag. Dette bilaget inneholder to kundeposter. Følgende bilag opprettes når den ovennevnte økonomimoduloppføringen bokføres.

|             |             |                  |                                    |
|-------------|-------------|------------------|------------------------------------|
| **Bilag** | **Konto** | **Posteringstype** | **Beløp i transaksjonsvaluta** |
| ARPAYM001   | 130100-002- | Kundesaldo | 100,00                             |
| ARPAYM001   | 130100-002- | Kundesaldo | -100,00                            |

Deretter kan du anta at du mottar en betaling fra forsikringskunden for 98,00, og du vil utligne betalingen med fakturaen som er opprettet av saldooverføringen. Dette fører til at følgende bilag posteres. Det kan være en forventning om at utligningen bruker finansdimensjonene fra den opprinnelige fakturaen, men det er ikke mulig fordi det ikke er et fakturadokument for forsikringskunden. Legg merke til at distribusjonsdimensjonene i kontantrabatten som standard kommer fra kundetransaksjonen som ble opprettet fra overføringen, og ikke fra den opprinnelige fakturaens inntektskonto. Standarden er et resultat av å bruke ett bilag til å overføre saldoene.

|             |             |                  |           |            |
|-------------|-------------|------------------|-----------|------------|
| **Bilag** | **Konto** | **Posteringstype** | **Debet** | **Kreditt** |
| ARPAYM002   | 110110-002- | Bank             | 98.00     |            |
| ARPAYM002   | 130100-002- | Kundesaldo |           | 98.00      |

På det tilknyttede bilaget for kontantrabatt kommer standarden for finansdimensjonen fra kundetransaksjonen som ble opprettet fra overføringen, fordi overføringen har mer enn én kunde.

|             |             |                        |           |            |
|-------------|-------------|------------------------|-----------|------------|
| **Bilag** | **Konto** | **Posteringstype**       | **Debet** | **Kreditt** |
| ARP-00001   | 403300-002- | Kundekontantrabatt | 2.00      |            |
| ARP-00001   | 130100-002- | Kundesaldo       |           | 2.00       |

Hvis brukeren er misfornøyd med standarden for finansdimensjonene for kontantrabatten, i stedet for ett bilag, må flere bilag skal brukes til å registrere saldooverføringen. Denne situasjonen bør gjennomføres ved å opprette en kreditnota for kunden som saldoen flyttes FRA, og en debetnota eller faktura som er opprettet for kunden som saldoen flyttes TIL. Følgende eksempel viser hvordan flere bilag kan registreres i betalingsjournalen for kunder for å overføre saldoen, i stedet for å bruke ett bilag, som vist tidligere i dette eksemplet.

|             |                  |             |                 |           |            |                 |                    |
|-------------|------------------|-------------|-----------------|-----------|------------|-----------------|--------------------|
| **Bilag** | **Kontotype** | **Konto** | **Beskrivelse** | **Debet** | **Kreditt** | **Motregningstype** | **Motkonto** |
| ARPAYM001   | Kunde         | ACME        |                 |           | 100,00     | Finans          | 401100-002-023-    |
| ARPAYM002   | Kunde         | Forsikring   |                 | 100,00    |            | Finans          | 401100-002-023-    |

Dette betyr at når forsikringskunden betaler 98,00 med bilaget ARPAYM02, brukes de riktige finansdimensjonene fra finanskontooppføringen for bilaget ARPAYM002.

|             |             |                  |           |            |
|-------------|-------------|------------------|-----------|------------|
| **Bilag** | **Konto** | **Posteringstype** | **Debet** | **Kreditt** |
| ARPAYM003   | 110110-002- | Bank             | 98.00     |            |
| ARPAYM003   | 130100-002  | Kundesaldo |           | 98.00      |

På det relaterte bilaget for kontantrabatt brukes finansdimensjonene fra den motposterte inntektskontoen som vises på bilaget ARPAYM002.

|             |                 |                        |           |            |
|-------------|-----------------|------------------------|-----------|------------|
| **Bilag** | **Konto**     | **Posteringstype**       | **Debet** | **Kreditt** |
| ARP-00001   | 403300-002-023- | Kundekontantrabatt | 2.00      |            |
| ARP-00001   | 130100-002-     | Kundesaldo       |           | 2.00       |

### 

## <a name="one-voucher-with-a-netting-for-multiple-customers-and-vendors"></a>Ett bilag med en motregning for flere kunder og leverandører
Motregning kan være nyttig når en organisasjon kjøper og selger til det samme firmaet. I stedet for å betale leverandørfakturaene og vente på å motta betaling for kundefakturaer, motberegnes leverandør- og kundefakturaene. Motregningstransaksjonen utlignes mot de utestående saldoene. 

For å illustrere dette kan du anta at leverandøren 1001 og kunden US-008 er samme enhet, slik at organisasjonen din ønsker å motregne saldoene for kunder og leverandører før betaling/mottak av den gjenstående saldoen. Anta at kundeposten skylder EUR 75,00 og leverandørposten skyldes EUR 100,00. Det betyr at du heller vil motregne saldoene og bare betale leverandøren EUR 25,00. Anta i tillegg at regnskapsvalutaen er USD. I dette tilfellet registreres en motregningstransaksjon på ett bilag i betalingsjournalen for kunder.

|             |                  |             |                 |           |            |                 |                    |
|-------------|------------------|-------------|-----------------|-----------|------------|-----------------|--------------------|
| **Bilag** | **Kontotype** | **Konto** | **Beskrivelse** | **Debet** | **Kreditt** | **Motregningstype** | **Motkonto** |
| APPAYM001   | Leverandør           | 1001        | Motregning         |  75,00    |            | Kunde        | US-008             |

Flere bilag må angis i journalen for å registrere motregningstransaksjonen for å unngå uønskede problemer med senere utligninger for denne transaksjonen, i stedet for å bruke ett bilag. Legg merke til at saldoene for kunde og leverandør motregnes med én avregningskonto for å unngå bruk av ett bilag som inneholder flere saldoer for kunde og leverandør.

|             |                  |             |                 |           |            |                 |                    |
|-------------|------------------|-------------|-----------------|-----------|------------|-----------------|--------------------|
| **Bilag** | **Kontotype** | **Konto** | **Beskrivelse** | **Debet** | **Kreditt** | **Motregningstype** | **Motkonto** |
| 001         | Kunde         | US-008      |                 |           |  75,00     | Finans          | 999999---          |
| 002         | Leverandør           | 1001        |                 |  75,00    |            | Finans          | 999999---          |






