---
title: Kassefunksjoner for Norge
description: Dette emnet gir en oversikt over hvilke kasse-funksjoner som er tilgjengelige for Norge. Det inneholder også retningslinjer for hvordan du konfigurerer funksjonen.
author: EvgenyPopovMBS
manager: vastrup
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailPosPermissionGroup, RetailFunctionalityProfile, RetailFormLayout, RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.region: Norway
ms.search.industry: Retail
ms.author: epopov
ms.search.validFrom: 2017-10-31
ms.dyn365.ops.version: Application update 4
ms.openlocfilehash: cd8cd0d643d9279d2deba705642a3df9dde2381b
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5225693"
---
# <a name="cash-register-functionality-for-norway"></a>Kassefunksjoner for Norge

[!include [banner](../includes/banner.md)]

Dette emnet gir en oversikt over hvilke kasse-funksjoner som er tilgjengelige for Norge i Dynamics 365 Commerce. Det inneholder også retningslinjer for hvordan du konfigurerer funksjonen. Funksjonaliteten består av følgende deler:

- Vanlige POS-funksjoner som er tilgjengelige for kunder i alle land eller områder. Eksempler inkluderer et alternativ som lar deg forhindre at en kopi av en kvittering skrives ut mer enn én gang.
- Spesifikke funksjoner for Norge, for eksempel digitale signaturer for salgstransaksjoner.

## <a name="overview-of-cash-register-functionality-for-norway"></a>Oversikt over kassefunksjoner for Norge

### <a name="common-pos-features"></a>Vanlige POS-funksjoner

Hvis du vil finne ut mer om POS-funksjoner som er tilgjengelige for kunder i alle land eller områder, kan du se [Hjelperessurser for Dynamics 365 Retail](../index.md).

Følgende POS-lokaliseringsfunksjoner som tidligere ble implementert og gjort tilgjengelige for kunder i alle land eller områder, kan nå brukes spesielt for Norge:

- **Skriv ut tekstfelt på en kvittering i en stor skriftstørrelse.** Du kan bruke **Skriftstørrelse**-parameteren i Utforming av kvitteringsformat til å angi at den store skriftstørrelsen skal brukes for et felt i kvitteringsformatet. (Den store skriftstørrelsen er omtrent dobbelt så stor som den vanlige skriftstørrelsen.) Du kan for eksempel bruke denne parameteren til å skrive ut "Kopi"-indikatoren med store bokstaver på en kopi av en kvittering.
- **Registrer utskrift av kritteringskopier i POS-overvåkingsloggen.** Du kan bruke **Overvåk** -parameteren i POS-funksjonalitetsprofilen til å aktivere kopier av kvitteringer som skal skrives ut og andre POS-overvåkingshendelser som skal registreres. Overvåkingshendelser registreres i kanaldatabasen og i Hovedkontor. Du kan vise overvåkingshendelser på siden **Overvåkingshendelser**.
- **Hindre at en kopi av en kvittering skrives ut mer enn én gang.** Når **Overvåk**-parameteren i POS-funksjonalitetsprofilen er aktivert, styrer POS-tillatelsen **Tillat utskrift av kvitteringskopi** om kopier av kvitteringer kan skrives ut. Det er også et alternativ som lar deg hindre at en kopi av en kvittering skrives ut mer enn én gang.

I tillegg ble følgende POS-funksjon implementert for Norge, men gjort tilgjengelig for kunder i alle land eller områder:

- **Registrer flere hendelser i POS-overvåkingsloggen.** Hvis **Overvåk**-parameteren i POS-funksjonalitetsprofilen er aktivert, registreres følgende hendelser i POS-overvåkingsloggen:

    - Priskontroller
    - Avgiftsoverstyringer
    - Endringer i linjeantall
    - Fjerning av transaksjoner fra kanaldatabasen

### <a name="norway-specific-pos-features"></a>Spesifikke POS-funksjoner for Norge

Følgende spesifikke POS-funksjoner for Norge aktiveres når **ISO-kode**-parameteren i POS-funksjonalitetsprofilen er satt til **NO**.

#### <a name="digital-signing-of-sales-transactions"></a>Digital signering av salgstransaksjoner

Alle salgstransaksjoner er digitalt signert. Signaturen opprettes og registreres i POS-transaksjonsjournalen samtidig som transaksjonen fullføres. Signaturen er også tilgjengelig i journalen som eksporteres for revisjonsformål.

Bare transaksjoner for kontantsalg signeres. Her er noen eksempler på transaksjoner utelates fra signeringen:

- Forskuddsbetalinger (innbetaling til kundekonto)
- Forskuddsbetalinger for salgsordrer (kundenordreinnskudd)
- Utstede et gavekort
- Ikke-salgstransaksjoner (flytoppføring, fjerning av betalingsmidler og så videre)

Dataene som signeres, er en tekststreng som består av datafeltene nedenfor. Datafeltene er atskilt med semikolon.

1. Forrige signatur for samme POS (en null \[**0**\] brukes for den første transaksjonen.)
2. Transaksjonsdato
3. Transaksjonstidspunkt
4. Sekvensielt signert transaksjonsnummer
5. Transaksjonsbeløp inkludert mva
6. Transaksjonsbeløp uten mva

Den digitale signeringen bruker en 1024-biters RSA-nøkkel med en SHA-1-hash-funksjon (RSA-SHA1-1024). Et sertifikat som er installert på Commerce Scale Unit, brukes til signering. Den unike ID-en for sertifikatet (avtrykk) registreres sammen med signaturen.

Signaturen lagres i databasen for butikken og hovedkontoret (HQ) sammen med transaksjonsdataene. Du kan vise transaksjonssignaturen sammen med transaksjonsdataene som ble brukt til å generere den, i hurtigfanen **Finansielle transaksjoner** på siden **Butikktransaksjoner**.

#### <a name="receipts"></a>Kvitteringer

Kvitteringer for Norge kan inkludere tilleggsinformasjon som ble implementert ved hjelp av egendefinerte felt:

- **Kvitteringstittel** – Du kan legge til et felt i et oppsett for kvitteringsformat for å identifisere kvitteringstypen. En salgskvittering kan for eksempel inkludere teksten "Salgskvittering".
- **Sekvensielt nummer for signert transaksjon** – Det sekvensielle nummeret for en signert transaksjon kan vises på kvitteringen for å knytte en utskrevet kvittering til en digital signatur i databasen.
- **Kvitteringstotaler** – Egendefinerte felt for kvitteringstotaler uten ikke-salgsbeløp fra totale transaksjonsbeløp. Ikke-salgsbeløp med beløp for følgende operasjoner:

    - Forskuddsbetalinger (innbetaling til kundekonto)
    - Forskuddsbetalinger for salgsordrer (kundenordreinnskudd)
    - Utstede et gavekort
    - Legge til betalingsmidler på et gavekort

#### <a name="x-and-z-reports"></a>X- og Z-rapporter

Informasjonen som er inkludert i X- og Z-rapporter er basert på norsk krav. **Totale kontantsalg**-beløp inkluderer for eksempel bare beløp for kontantsalgstransaksjoner og utelater utstedelse av gavekort og forskuddsbetalinger. Totale kontantsalg vises også per varegruppe og betalingsmåte. I tillegg vil de kumulative beløpene **Hovedsumsalg** og **Hovedsumreturer** vedlikeholdes og skrives ut.

#### <a name="saf-t-cash-register-audit-file"></a>Revisjonsfil for SAF-T-kasse

Du kan eksportere POS-transaksjonsjournalen i forhåndsdefinerte SAF-T-formatet (Standard Audit File - Tax). Revisjonsfilen inneholder informasjon om organisasjonen, relevante hoveddata (for eksempel varegrupper, varer og mva-koder), transaksjonsdata for kontantsalg sammen med signaturer for disse transaksjonene, hendelsesdata for ikke-salg og rapportdata for sluttdato.

Revisjonsfilen kan eksporteres for følgende scenarioer:

- Per butikk
- Alle butikker
- Per terminal
- Alle terminaler

Du kan også sende en rapport fra en juridisk enhet på vegne av en annen juridisk enhet. I så fall må du kjøre eksporten fra den operative juridiske enheten og angi den rapporterende juridiske enheten som avsender av rapporten.

SAF-T-kasseformatet er implementert i Hovedkontor ved hjelp av [Elektronisk rapportering](../../dev-itpro/analytics/general-electronic-reporting.md). 

## <a name="setting-up-commerce-for-norway"></a>Konfigurere Handel for Norge

Denne delen beskriver innstillingene som er spesifikke og anbefalte for Norge. Hvis du vil ha mer informasjon, kan du se [Hjelperessurser for Dynamics 365 Retail](../index.md).

Hvis du vil bruke de spesifikke funksjonene for Norge, må du fullføre disse oppgavene:

- Sett feltet **Land/område** til **NOR** (Norge) i den primære adressen for den juridiske enheten.
- Sett feltet **ISO-kode** til **NO** (Norge) i POS-funksjonalitetsprofilen for hver butikk som finnes i Norge.

Du må også angi følgende innstillinger for Norge.

### <a name="set-up-the-legal-entity"></a>Definere den juridiske enheten

Kontroller at navnet på den juridiske enheten er angitt. Dette navnet skrives ut på X- og Z-rapporter.

I tillegg angir du organisasjonsnummeret i **Registreringsnummer**-feltet i hurtigfanen **Bankkontoinformasjon**.

### <a name="set-up-value-added-tax-vat-per-norwegian-requirements"></a>Definere merverdiavgift (mva) i henhold til norske krav


Du må opprette mva-koder, mva-grupper og mva-grupper for varer. Du må også definere mva-informasjon for produkter og tjenester. Hvis du vil ha mer informasjon om hvordan du definerer og bruker mva, kan du se [Oversikt over merverdiavgift](../../financials/general-ledger/indirect-taxes-overview.md).

Du må også angi mva-grupper og aktiverer alternativet **Priser inkluderer merverdiavgift** for butikker som finnes i Norge.

### <a name="set-up-functionality-profiles"></a>Konfigurere funksjonalitetsprofiler

Du må aktivere revisjon og definere kvitteringsnummerering.

### <a name="update-pos-permissions-groups-and-individual-permission-settings-for-store-workers"></a>Oppdatere grupper for POS-tillatelser og innstillinger for individuelle tillatelser for butikkarbeidere

Sett tillatelsen **Tillat utskrift av kvitteringskopi** til en aktuell verdi:

- **Tillat alltid** – Operatoren kan skrive ut en kopi av en kvittering flere ganger.
- **Tillat bare én gang** – Operatoren kan skrive ut en kopi av en kvittering bare én gang.
- **Tillat bare én gang, og bare hvis HQ DB er tilgjengelig** – Operatoren kan skrive ut en kopi av en kvittering bare én gang, og bare hvis databasen for hovedkontoret er tilgjengelig via Commerce Data Exchange: Real-time Service, slik at systemet kan kontrollere at ingen kopier av kvitteringen er skrevet ut tidligere i andre butikker.
- **Aldri** – Operatoren kan ikke skrive ut en kopi av en kvittering.

### <a name="configure-custom-fields-so-that-they-can-be-used-in-receipt-formats-for-sales-receipts"></a>Konfigurere egendefinerte felt, slik at de kan brukes i kvitteringsformater for salgskvitteringer

På siden **Språktekst** legger du til følgende poster for etikettene for de egendefinerte feltene for kvitteringsoppsett. Vær oppmerksom på at verdiene **Språk-ID**, **Tekst-ID** og **Tekst** som vises i tabellen, bare er eksempler. Du kan endre dem slik at de oppfyller dine krav.

| Språk-ID | Tekst                   | Tekst-ID |
|-------------|------------------------|---------|
| en-US       | Mottakstittel          | 900011  |
| en-US       | Er gavekort           | 900012  |
| en-US       | Totalt (salg)          | 900013  |
| en-US       | Mva-total (salg)      | 900014  |
| en-US       | Sum med avgift (salg) | 900015  |
| en-US       | Avgiftsbeløp (salg)     | 900016  |
| en-US       | ID for kontanttransaksjon    | 900017  |

På siden **Egendefinerte felt** legger du til følgende poster for de egendefinerte feltene for oppsett av mottaket. Vær oppmerksom på at verdiene **Tekst-ID for overskrift** må samsvare med verdiene **Tekst-ID** som du har angitt på siden **Språktekst**.

| Navn                            | Type    | Tekst-ID for overskrift |
|---------------------------------|---------|-----------------|
| ReceiptTitle                    | Tilgang | 900011          |
| IsGiftCard                      | Tilgang | 900012          |
| SalesTotalExt                   | Tilgang | 900013          |
| TaxTotalExt                     | Tilgang | 900014          |
| TotalWithTaxExt                 | Tilgang | 900015          |
| AmountPerTaxExt                 | Tilgang | 900016          |
| CashTransactionSequentialNumber | Tilgang | 900017          |

### <a name="configure-receipt-formats"></a>Konfigurere mottaksformater

For alle nødvendige kvitteringsformater endrer du verdien for feltet **Utskriftsatferd** til **Skriv alltid ut** for kvitteringsformatet.

I Utforming av kvitteringsformat legger du til de egendefinerte feltene nedenfor i de aktuelle kvitteringsdelene. Vær oppmerksom på at feltnavnene samsvarer med språktekstene som du definerte i forrige del.

1. Hode:

    - **Kvitteringstittel** – Dette feltet viser kvitteringstypen.
    - **ID for kontanttransaksjon** – Dette feltet skriver ut det sekvensielle nummeret for den signerte kontanttransaksjonen.

2. Linjer:

    - **Er gavekortet** – Dette feltet merker kvitteringslinjen som knyttet til Utsted gavekort eller Legg til gavekort.

3. Bunntekst:

    - **Totalt (salg)** – Dette feltet skriver ut kvitteringens totale beløp for kontantsalg. Beløpet uten mva. Forskuddsbetalinger og gavekort utelates.
    - **Mva-totalt (salg)** – Dette feltet skriver ut kvitteringens totale mva-beløp for kontantsalg. Forskuddsbetalinger og gavekort utelates.
    - **Sum med avgift (salg)** – Dette feltet skriver ut kvitteringens totale beløp for kontantsalg. Beløpet med mva. Forskuddsbetalinger og gavekort utelates.
    - **Avgiftsbeløp (salg)** – Dette feltet skriver ut kvitteringens mva-beløp for kontantsalg per mva-kode. Forskuddsbetalinger og gavekort utelates.

Hvis du vil ha mer informasjon om hvordan du arbeider med kvitteringsformater, kan du se [Definere og utforme kvitteringsformater](../receipt-templates-printing.md).

### <a name="configure-the-saf-t-cash-register-export-format"></a>Konfigurere formatet for eksport av SAF-T-kasse

Konfigurasjon av SAF-T-kasse er tilgjengelig for nedlasting fra Microsoft Dynamics Lifecycle Services (LCS). Hvis du vil ha mer informasjon, kan du se [Importere elektroniske rapporteringskonfigurasjoner](../../dev-itpro/analytics/electronic-reporting-import-ger-configurations.md). Du må laste ned følgende konfigurasjoner:

- **Data for detaljhandelskanal.versjon.1** – Datamodellkonfigurasjonen.
- **Data for DMM Retail-kanal versjon 1.12** – Konfigurasjonen av datamodelltilordningen.
- **NO SAF T-kasse.version.1.15** – Formatkonfigurasjonen.

Når du har importert konfigurasjonene på siden **Handelsparametere**, går du til kategorien **Elektroniske dokumenter** og velger navnet på formatkonfigurasjonen som ble importert, i feltet **Format for eksport av SAF-T-kasse**.

Du må også tilordne nødvendige hoveddata til forhåndsdefinerte SAF-T-standardkoder. Hvis du vil ha mer informasjon, kan du se dokumentasjonen for SAF-T-kasse som leveres av den norske skatteetaten. Hvis du vil opprette tilordningen, må du angi feltet **SAF-T-kassekode** på følgende sider:

- Varegrupper
- Betalingsmåter
- Mva-koder

### <a name="configure-channel-components"></a>Konfigurere kanalkomponenter

Hvis du vil aktivere spesifikke funksjoner for Norge, må du konfigurere utvidelser for komponenter for kanal. Hvis du vil ha mer informasjon, kan du se [retningslinjene for distribusjon](./emea-nor-loc-deployment-guidelines.md).



[!INCLUDE[footer-include](../../includes/footer-banner.md)]