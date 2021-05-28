---
title: MVA-deklarering for Egypt
description: Dette emnet beskriver hvordan du konfigurerer og genererer mva-returskjemaet for Egypt.
author: sndray
ms.date: 03/10/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: Global
ms.author: tfehr
ms.search.validFrom: 2017-06-20
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: bd48ee96a26c59183981fae879e3659711e70ce3
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021962"
---
#  <a name="vat-declaration-for-egypt-eg-00002"></a>MVA-deklarering for Egypt (EG-00002)

[!include[banner](../includes/banner.md)]

[!include[banner](../includes/banner.md)]

Dette emnet beskriver hvordan du definerer og genererer mva-returskjemaet, og salgs- og innkjøpsbøker for juridiske enheter i Egypt.

Mva-returskjemaet for Egypt er det offisielle dokumentet som summerer totalt skyldig mva-beløp for utlevering, totalt mva-beløp som kan gjenopprettes, og det tilknyttede mva-beløpet. Skjemaet brukes for alle typer skattebetalere og bør fullføres manuelt via skattemyndighetportalen. Skjemaet for mva-retur kalles vanligvis mva-returarkivering.

Mva-returskjemaet i Dynamics 365 Finance inneholder følgende rapporter:

- Mva-returskjema nummer 10, som gir en analyse av beløp, justeringer og mva-beløp per linjevare i mva-returskjemaet som beskrevet i lovgivningen.
- Salgstransaksjonsbok
- Innkjøpstransaksjonsbok

## <a name="prerequisites"></a>Forutsetninger
Primæradressen for den juridiske enheten må være i Egypt.
I arbeidsområdet **Funksjonsstyring** aktiverer du følgende funksjon:

   - (Egypt) Kategorihierarki for mva-rapport for salg og innkjøp.

Hvis du vil ha mer informasjon om hvordan du aktiverer funksjoner, kan du se [Oversikt over funksjonsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

I arbeidsområdet **Elektronisk rapportering** importerer du følgende format for elektronisk rapportering fra repositoriet:

- Mva-deklarering Excel (EG)

> [!NOTE]
> Formatet ovenfor er basert på **mva-deklareringsmodellen** og bruker **tilordningen av mva-deklareringsmodellen**. Tilleggskonfigurasjoner vil bli importert automatisk.

Hvis du vil ha mer informasjon om hvordan du importerer konfigurasjoner for elektronisk rapportering, kan du se [Laste ned konfigurasjoner for elektronisk rapportering fra Lifecycle Services](../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).

## <a name="download-electronic-reporting-configurations"></a>Laste ned konfigurasjoner for elektronisk rapportering

Implementeringen av mva-returskjemaet for Egypt er basert på konfigurasjoner for elektronisk rapportering (ER). Hvis du vil ha mer informasjon om funksjonene og begrepene for rapportering som kan konfigureres, kan du se [Elektronisk rapportering](../../fin-ops-core/dev-itpro/analytics/general-electronic-reporting.md).

For miljøer av produksjons- og brukergodkjenningstesting (UAT) kan du se [Laste ned konfigurasjoner for elektronisk rapportering fra Lifecycle Services](../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).

Hvis du vil generere mva-returskjemaet og tilknyttede rapporter i en juridisk enhet for Egypt, laster du opp følgende konfigurasjoner:

- Tax declaration model.version.70.xml eller nyere
- Tax declaration model mapping.version.70.120.xml eller nyere
- VAT Declaration Excel (EG).version.70.32 eller nyere

Når du har lastet ned ER-konfigurasjonene fra Lifecycle Services (LCS) eller det globale repositoriet, fullfører du fremgangsmåten nedenfor.

1. Gå til arbeidsområdet **Elektronisk rapportering** og velg flisen **Rapporteringskonfigurasjoner**.
1. På siden **Konfigurasjoner** velger du **Exchange** > **Last fra XML-fil** i handlingsruten.
1. Last opp filene i samme rekkefølge som de er oppført ovenfor. Når alle konfigurasjonene er lastet opp, skal konfigurasjonstreet være til stede i Finance.

## <a name="set-up-application-specific-parameters"></a>Konfigurere programspesifikke parametere

Ved hjelp av de programspesifikke parameterne kan du fastsette kriteriene for hvordan mva-transaksjoner klassifiseres og beregnes på hver linje når rapporten genereres. Bestemmelsen er basert på konfigurasjonen til mva-gruppen for vare, mva-gruppen, mva-koden og andre kriterier som er fastsatt i oppslagsdefinisjonen.

Rapportene i salgs- og innkjøpsboken for Egypt inkluderer et sett med kolonner som samsvarer med bestemte transaksjonsklassifiseringer som typer operasjoner, produkter og dokumenter som er spesifikke for Egypt. I stedet for å inkludere disse nye klassifiseringene som nye oppføringsdata når transaksjonene posteres, bestemmes klassifiseringene basert på forskjellige oppslag som introduseres i **Konfigurasjoner** > **Konfigurere programspesifikke parametere** > **Oppsett** for å oppfylle mva-kravene for Egypt. 

![Siden Programspesifikke parametere](media/egypt-vat-declaration-setup1.png)

Disse følgende oppslagskonfigurasjonene brukes til å klassifisere transaksjonene i rapporter for mva-bøker for innkjøp og salg.

- **PurchaseItemTypeLookup** > Kolonne O: Varetype
- **VATRateTypeLookup** > Kolonne B: Avgiftstype
- **VATRateTypeLookup** > Kolonne C: Tabellvaretype
- **PurchaseOperationTypeLookup** > Kolonne A: Dokumenttype
- **SalesOperationTypeLookup** > Kolonne N: Driftstype
- **SalesItemTypeLookup** > Kolonne O: Varetype

Fullfør fremgangsmåten nedenfor for å sette opp de ulike oppslagene som brukes til å generere mva-deklarering og relaterte bøker. 

1. I arbeidsområdet **Elektroniosk rapportering** velger du **Konfigurasjoner** > **Oppsett** for å konfigurere regler for å identifisere mva-transaksjonen i den relaterte boksen for mva-returskjemaet.
2. Velg den gjeldende versjonen, og velg oppslagsnavnet i hurtigfanen **Oppslag**. For eksempel **SalesItemTypeLookup**. Dette oppslaget identifiserer listen over klassifiseringer i mva-registeret som kreves av skattemyndighetene.
3. I hurtigfanen **Betingelser** velger du **Legg til**, og i den nye linjen i kolonnen **Oppslagsresultat** velger du den relaterte linjen som representerer klassifiseringen i **Kolonne O**.
4. I kolonnen **Mva-gruppe** velger du mva-gruppen som brukes til å identifisere klassifiseringen. For eksempel **Innenlands salgsfaktura**. Du kan også bruke mva-gruppe, mva-kode eller kombinasjonen av treattributter hvis konfigurasjonen er definert på en annen måte. 
5. Velg klassifiseringen for mva-transaksjonen i kolonnen **Navn**.
6. Gjenta trinn 3-5 for alle tilgjengelige oppslag.
7. Velg **Legg til** for å ta med sluttpostlinjen, og velg **Ikke tilgjengelig** i kolonnen **Oppslagsresultat**. 
8. I resten av kolonnene velger du **Ikke tom**. 

> [!NOTE]
> Når du legger til den siste posten, **Gjelder ikke**, definerer du følgende regel: Når mva-gruppen, mva-gruppen for varesalg, mva-koden og navnet som er sendt som et argumentet, ikke oppfyller noen av de forrige reglene, blir ikke transaksjonene inkludert i mva-registeret. Selv om denne regelen ikke brukes ved generering av rapporten, bidrar regelen til å unngå feil i rapportgenerering når det er en manglende regelkonfigurasjon.

Tabellene nedenfor representerer et eksempel på foreslått konfigurasjon for de beskrevete oppslagskonfigurasjonene. 

**SalesItemTypeLookup**

| Oppslagsresultat         | Linje | Merverdiavgiftsgruppe    | Varens mva-gruppe    | Mva-kode (kode) | Navn                  |
|-----------------------|------|--------------------|-------------------------|-----------------|-----------------------|
| Innenlands              | 1    | VAT_LOCAL          | *Ikke tom*             | *Ikke tom*     | Salg                 |
| Innenlands              | 2    | VAT_LOCAL          | *Ikke tom*             | *Ikke tom*     | SalesCreditNote       |
| Innenlands              | 3    | VAT_FINALC         | *Ikke tom*             | *Ikke tom*     | Salg                 |
| Innenlands              | 4    | VAT_FINALC         | *Ikke tom*             | *Ikke tom*     | SalesCreditNote       |
| Innenlands              | 5    | VAT_PUBLIO         | *Ikke tom*             | *Ikke tom*     | Salg                 |
| Innenlands              | 6    | VAT_PUBLIO         | *Ikke tom*             | *Ikke tom*     | SalesCreditNote       |
| Eksporter                | 7    | VAT_EXPORT         | *Ikke tom*             | *Ikke tom*     | Salg                 |
| Eksporter                | 8    | VAT_EXPORT         | *Ikke tom*             | *Ikke tom*     | SalesCreditNote       |
| Maskin og utstyr | 9    | *Ikke tom*        | VAT_M&E                 | *Ikke tom*     | Salg                 |
| Maskin og utstyr | 10   | *Ikke tom*        | VAT_M&E                 | *Ikke tom*     | SalesCreditNote       |
| Delemaskiner        | 11   | *Ikke tom*        | VAT_PARTS               | *Ikke tom*     | Salg                 |
| Delemaskiner        | 12   | *Ikke tom*        | VAT_PARTS               | *Ikke tom*     | SalesCreditNote       |
| Fritak            | 13   | VAT_EXE            | *Ikke tom*           | *Ikke tom*     | SaleExempt            |
| Fritak            | 14   | VAT_EXE            | *Ikke tom*           | *Ikke tom*     | SalesExemptCreditNote |
| Gjelder ikke        | 15   | *Blank*            | *Blank*                 | VAT_ADJ         | *Ikke tom*           |
| Gjelder ikke        | 16   | *Ikke tom*        | *Ikke tom*             | *Ikke tom*     | *Ikke tom*           |

 **SalesOperationTypeLookup**

| Oppslagsresultat  | Linje | Varens mva-gruppe    | Avgiftskode    | Navn                  |
|----------------|------|-------------------------|-------------|-----------------------|
| Varer          | 1    | VAT_GOODS               | *Ikke tom* | Salg                 |
| Varer          | 2    | VAT_GOODS               | *Ikke tom* | SalesCreditNote       |
| Varer          | 3    | VAT_GOODS               | *Ikke tom* | SaleExempt            |
| Varer          | 4    | VAT_GOODS               | *Ikke tom* | SalesExemptCreditNote |
| Tjeneste       | 5    | VAT_SERV                | *Ikke tom* | Salg                 |
| Tjeneste       | 6    | VAT_SERV                | *Ikke tom* | SalesCreditNote       |
| Tjeneste       | 7    | VAT_SERV                | *Ikke tom* | SaleExempt            |
| Tjeneste       | 8    | VAT_SERV                | *Ikke tom* | SalesExemptCreditNote |
| Justeringer    | 9    | *Blank*                 | VAT_ADJ     | Salg                 |
| Justeringer    | 10   | *Blank*                 | VAT_ADJ     | Kjøp              |
| Gjelder ikke | 11   | *Ikke tom*             | *Ikke tom* | *Ikke tom*           |

**PurchaseItemTypeLookup**

| Oppslagsresultat          | Linje | Varens mva-gruppe    | Avgiftskode    | Navn                     |
|------------------------|------|-------------------------|-------------|--------------------------|
| Varer                  | 1    | VAT_GOODS               | *Ikke tom* | Kjøp                 |
| Varer                  | 2    | VAT_GOODS               | *Ikke tom* | PurchaseCreditNote       |
| Tjeneste               | 3    | VAT_SERV                | *Ikke tom* | Kjøp                 |
| Tjeneste               | 4    | VAT_SERV                | *Ikke tom*  | PurchaseCreditNote       |
| Maskin og utstyr  | 5    | VAT_M&E                 | *Ikke tom* | Kjøp                 |
| Maskin og utstyr  | 6    | VAT_M&E                 | *Ikke tom* | PurchaseCreditNote       |
| Delemaskiner         | 7    | VAT_PARTS               | *Ikke tom* | Kjøp                 |
| Delemaskiner         | 8    | VAT_PARTS               | *Ikke tom* | PurchaseCreditNote       |
| Fritak             | 9    | VAT_EXE                 | *Ikke tom*  | PurchaseExempt           |
| Fritak             | 10   | VAT_EXE                 | *Ikke tom* | PurchaseExemptCreditNote |
| Gjelder ikke         | 11   | *Blank*                 | VAT_ADJ     | *Ikke tom*              |
| Gjelder ikke         | 12   | *Ikke tom*             | *Ikke tom* | *Ikke tom*              |
| Gjelder ikke         | 13   | *Blank*                 | *Ikke tom* | *Ikke tom*              |

**PurchaseOperationTypeLookup**

| Oppslagsresultat  | Linje | Merverdiavgiftsgruppe  | Avgiftskode    | Navn                     |
|----------------|------|------------------|-------------|--------------------------|
| Innenlands       | 1    | VAT_LOCAL        | *Ikke tom* | Kjøp                 |
| Innenlands       | 2    | VAT_LOCAL        | *Ikke tom* | PurchaseCreditNote       |
| Innenlands       | 3    | VAT_LOCAL        | *Ikke tom* | PurchaseExempt           |
| Innenlands       | 4    | VAT_LOCAL        | *Ikke tom* | PurchaseExemptCreditNote |
| Importert       | 5    | VAT_IMPORT       | *Ikke tom* | Kjøp                 |
| Importert       | 6    | VAT_IMPORT       | *Ikke tom* | PurchaseCreditNote       |
| Importert       | 7    | VAT_IMPORT       | *Ikke tom* | PurchaseExempt           |
| Importert       | 8    | VAT_IMPORT       | *Ikke tom* | PurchaseExemptCreditNote |
| Justeringer    | 9    | *Blank*          | VAT_ADJ     | PurchaseCreditNote       |
| Justeringer    | 10   | *Blank*          | VAT_ADJ     | Kjøp                 |
| Gjelder ikke | 11   | *Ikke tom*      | *Ikke tom* | *Ikke tom*              |

**VATRateTypeLookup**

| Oppslagsresultat  | Linje | Mva-kode (kode) |
|----------------|------|-----------------|
| GeneralGoods   | 1    | VAT_ST          |
| GeneralGoods   | 2    | VAT_RD          |
| FirstTable     | 3    | *Ikke tom*     |
| SecondTable    | 4    | *Ikke tom*     |
| Gjelder ikke | 5    | *Ikke tom*     |


## <a name="set-up-general-ledger-parameters"></a>Konfigurere parametere for økonomimodul

Hvis du vil generere mva-returskjemarapporten formatet Microsoft Excel, definerer du et ER-format på siden **Parametere for økonomimodul**.

1. Gå til **Avgift** > **Oppsett** > **Parametere for økonomimodul**.
2. Velg **Mva-deklarering Excel (EG)** i feltet **Tilordning av format for mva-oppgave** i delen **Mva-alternativer** i fanen **Mva**. Hvis du lar feltet stå tomt, genereres standard mva-rapport i SSRS-format.
3. Velg **Kategorihierarki**. Ved hjelp av denne kategorien kan varekoden i transaksjoner for fanen Utenrikshandel tillate at brukere kan velge og klassifisere varer og tjenester. Beskrivelsen av denne klassifiseringen er beskrevet i salgs- og innkjøpstransaksjonsrapporter. Denne konfigurasjonen er valgfri.

![Deklareringsskjema](media/egypt-vat-declaration-setup2.png)


## <a name="generate-a-vat-return-report"></a>Generere en rapport for mva-retur
Prosessen som brukes til å klargjøre og sende inn en rapport for mva-retur for en periode, er basert på mva-betalingstransaksjoner som ble postert i løpet av jobben Utlign og poster merverdiavgift. Hvis du vil ha mer informasjon utligning og rapportering av mva, kan du se [Oversikt over merverdiavgift](../general-ledger/indirect-taxes-overview.md).

Fullfør fremgangsmåten nedenfor for å generere mva-deklareringsrapporten.

1. Gå til **Avgift** > **Deklarasjoner** > **Mva** > **Rapporter merverdiavgift for utligningsperiode** eller **Utlign og poster merverdiavgift**.
2. Velg **utligningsperioden**.
3. Velg fra-datoen og velg deretter mva-betalingsversjonen.
5. Velg **OK**. 
6. Angi kreditbeløpet fra forrige periode, hvis det er aktuelt, eller la beløpet være null.
7. I feltet **Rapportdetaljer** velger du ett av følgende tilgjengelige alternativer. 
   - **Mva-register for innkjøp**: Generer rapporten om mva-transaksjoner for innkjøp.
   - **Mva-register for salg**: Generer rapporten om mva-transaksjoner for salg.
   - **Mva-deklarering**: Generer bare skjemaet for mva-deklareringsretur.
8. Angi navnet på personen som er registrert for å tilordne skjemaet.
9. Velg språket. Alle rapporter er oversatt i **en-us** og **ar-eg**.
  
[!INCLUDE[footer-include](../../includes/footer-banner.md)]


