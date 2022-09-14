---
title: Elektroniske fakturaer for kunde i Norge
description: Denne artikkelen forklarer hvordan du konfigurerer og elektroniske fakturaer for kunder i Norge.
author: mrolecki
ms.date: 11/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Norway
ms.author: mrolecki
ms.search.validFrom: 2019-11-01
ms.dyn365.ops.version: 10.0.08
ms.search.form: ''
ms.openlocfilehash: 7aa320061c51928da973e3da1a9c1560d21cc490
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/23/2022
ms.locfileid: "9337476"
---
# <a name="customer-electronic-invoices-in-norway"></a>Elektroniske fakturaer for kunde i Norge

[!include [banner](../includes/banner.md)]

For å oppnå samsvar med EU-direktiv 2014/55/EU har formatet **EHF Billing 3.0** for elektroniske fakturaer som gjelder spesifikt for Norge, blitt implementert basert på spesifikasjonen [PEPPOL Billing 3.0](https://docs.peppol.eu/poacc/billing/3.0/).

Denne artikkelen inneholder informasjon om hvordan du konfigurerer og utsteder elektroniske fakturaer i Norge.

## <a name="prerequisites"></a>Forutsetninger

Primæradressen for den juridiske enheten må være i Norge.

## <a name="import-electronic-reporting-configurations"></a>Importere konfigurasjoner for elektronisk rapportering

I arbeidsområdet **Elektronisk rapportering** importerer du følgende ER-formater (elektronisk rapportering) fra repositoriet:

- OIOUBL Salgsfaktura
- OIOUBL Prosjektfaktura
- OIOUBL Salgskreditnota
- OIOUBL Prosjektkreditnota

> [!NOTE]
> Disse formatene er basert på konfigurasjonen **Fakturamodell** og bruker konfigurasjonen **Fakturamodelltilordning**. Alle nødvendige tilleggskonfigurasjoner importeres automatisk.

Hvis du vil ha mer informasjon om hvordan du importerer ER-konfigurasjoner, kan du se [Laste ned konfigurasjoner for elektronisk rapportering fra Lifecycle Services](../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).

### <a name="reference-the-imported-er-format-configurations"></a>Referere til de importerte ER-formatkonfigurasjonene

1. Gå til **Kunder** \> **Oppsett** \> **Kundeparametere**.
2. Velg de importerte formatene for elektroniske dokumenter i hurtigfanen **Elektronisk rapportering** i fanen **Elektroniske dokumenter**:

    - **Salgs- og fritekstfaktura:** OIOUBL Salgsfaktura
    - **Salgs- og fritekstkreditnota:** OIOUBL Salgskreditnota
    - **Prosjektfaktura:** OIOUBL Prosjektfaktura
    - **Prosjektkreditnota:** OIOUBL Prosjektkreditnota

![Formater for elektroniske dokumenter.](media/emea-nor-ger-configs.jpg)

## <a name="configure-parameters"></a>Konfigurere parametere

### <a name="configure-legal-entity-parameters"></a>Konfigurere parametere for juridisk enhet

1. Gå til **Organisasjonsstyring** \> **Organisasjoner** \> **Juridiske enheter**.
2. I feltet **Mva-nummer** i hurtigfanen **Avgiftsregistrering** angir du mva-nummeret for firmaet ditt.
3. I hurtigfanen **Registreringsnumre** setter du alternativet **Skriv ut Foretaksregisteret på salgsdokumenter** for Norge til **Ja**.
4. Angi firmaets organisasjonsnummeret i **Registreringsnummer**-feltet i hurtigfanen **Bankkontoinformasjon**.
5. I **Bankkonto**-feltet angir du firmaets bankkontonummer.

    > [!NOTE]
    > Firmaets bankkonto må allerede være opprettet i **Kontant- og bankbehandling** \> **Bankkontoer** \> **Bankkontoer**.

### <a name="configure-customer-parameters"></a>Konfigurere kundeparametere

1. Gå til **Kunder** \> **Kunder** \> **Alle kunder**, og velg en kunde.
2. I hurtigfanen **Faktura og levering** setter du alternativet **eFaktura** til **Ja** for å aktivere generering av elektroniske fakturaer.
3. Sett alternativet **Vedlegg til eFaktura** til **Ja** for å legge en PDF-kopi av den utskrivbare fakturaen ved den elektroniske fakturaen.
4. I feltet **Avgiftsfritaksnummer** skriver du inn kundens MVA-fritaksnummer.

![Kundeparametere.](media/emea-nor-ger-customer.jpg)

### <a name="units-of-measure-configuration"></a>Konfigurasjon av måleenheter

1. Gå til **Organisasjonsstyring** \> **Oppsett** \> **Enheter** \> **Enheter**.
2. Velg en enhets-ID i listen, og velg deretter **Eksterne koder**.
3. I **Kode**-feltet i **Oversikt**-delen på siden **Eksterne koder** angir du en kode som svarer til den valgte enhets-ID-en.
4. I **Verdi**-feltet i **Verdi**-delen angir du den eksterne koden som skal brukes som enhetskode for internasjonal handel. Denne koden anbefales av [FNs økonomiske kommisjon for Europa (UNECE)](https://docs.peppol.eu/poacc/billing/3.0/codelist/UNECERec20/).

![Konfigurasjon av måleenheter.](media/emea-nor-ger-units.jpg)

### <a name="sales-tax-codes-transformation"></a>Transformasjon av mva-koder

Når du genererer elektroniske fakturaer, blir satsene for mva-koder analysert og transformert til [kategorier som samsvarer med UNCL5305](https://docs.peppol.eu/pracc/catalogue/1.0/codelist/UNCL5305/). Følgende logikk brukes:

- Når det gjelder alle avgiftssatser som ikke er null, brukes **S**-kategorien som standardverdi. Du kan bruke **Eksterne koder** ved å gå til **Avgift** > **Mva-kode** for å angi en eksplisitt **verdi** som representerer den eksterne koden som skal brukes som kategorien for samsvar med avgiftsforskrifter.
- Når det gjelder alle nullavgiftssatser, brukes enten kategorien **E** eller **Z**, avhengig av hvilken rapporteringskode som er konfigurert for avgiftsfritt salg.

### <a name="customer-requisition"></a>Kunderekvisisjon

Når du registrerer fritekstfakturaer, fakturaer som er basert på salgsordrer, eller prosjektfakturaer, må du angi en kunderekvisisjon. Du kan også legge til en valgfri kundereferanse.

#### <a name="free-text-invoices"></a>Fritekstfakturaer

1. Gå til **Kunder** \> **Fakturaer** \> **Alle fritekstfakturaer**.
2. Opprett en ny faktura, eller velg en eksisterende faktura.
3. I **Referanser**-delen i hurtigfanen **Kunde** i **Hode**-visningen angir du verdier i feltene **Kunderekvisisjon** og **Kundereferanse**.

#### <a name="sales-orders"></a>Salgsordre

1. Gå til **Kunder** \> **Ordrer** \> **Alle salgsordrer**.
2. Opprett en ny salgsordre, eller velg en eksisterende salgsordre. 
3. I **Referanser**-delen i hurtigfanen **Generelt** i **Hode**-visningen angir du verdier i feltene **Kunderekvisisjon** og **Kundereferanse**.

#### <a name="project-invoices"></a>Prosjektfakturaer

1. Gå til **Prosjektstyring og regnskap** \> **Projekter** \> **Prosjektkontrakter**.
2. Opprett en prosjektkontrakt, eller velg en eksisterende prosjektkontrakt.
3. I hurtigfanen **Finansieringskilder** velger eller oppretter du en finansieringskilde av typen **Kunde**, og deretter velger du **Detaljer**.

    ![Finansieringskilder.](media/emea-nor-ger-proj-contracts.jpg)

4. I **Referanser**-delen i hurtigfanen **Andre** på siden **Finansieringskildedetaljer** angir du standardverdier for kontrakten i feltene **Kunderekvisisjon** og **Kundereferanse**. Du kan også angi prosjektspesifikke verdier i de tilsvarende feltene i hurtigfanen **E-faktura**.

    ![Prosjektreferanser.](media/emea-nor-ger-proj-refs.jpg)

5. Følg denne fremgangsmåten for å angi verdier for kunderekvisisjon og referanse direkte på prosjektfakturaforslaget:

    1. Gå til **Prosjektstyring og regnskap** \> **Prosjektfakturaer** \> **Fakturaforslag for prosjekt**.
    2. Opprett et nytt fakturaforslag, eller velg et eksisterende fakturaforslag.
    3. I **E-faktura**-delen i hurtigfanen **Hode for fakturaforslag** angir du verdier i feltene **Kunderekvisisjon** og **Kundereferanse**.

    ![Prosjektforslag.](media/emea-nor-ger-proj-prop.jpg)

### <a name="customer-accounting-code-registration"></a>Registrering av kunderegnskapskode

Du kan registrere kunderegnskapskoder når du arbeider med fritekstfakturaer, fakturaer som er basert på salgsordrer, eller prosjektfakturaer.

#### <a name="free-text-invoices"></a>Fritekstfakturaer

1. Gå til **Kunder** \> **Fakturaer** \> **Alle fritekstfakturaer**.
2. Opprett en ny faktura, eller velg en eksisterende faktura. 
3. I feltet **Dimensjonskonto** i **E-faktura**-delen i hurtigfanen **Generelt** i **Hode**-visningen angir du regnskapskoden for fakturaen. 
4. Hvis du vil ha en separat regnskapskode for hver fakturalinje, følger du denne fremgangsmåten:

    1. Sett alternativet **Linjespesifikk** til **Ja**.
    2. Gå til **Linjer**-visningen.
    3. I **Dimensjonskonto**-feltet i fanen **Generelt** i hurtigfanen **Linjedetaljer** angir du en linjebestemt regnskapskode for hver fakturalinje.

    ![Linjebestemt regnskapskode for en fritekstfaktura.](media/emea-nor-ger-fti-cost.jpg)

#### <a name="sales-orders"></a>Salgsordre

1. Gå til **Kunder** \> **Ordrer** \> **Alle salgsordrer**.
2. Opprett en ny salgsordre, eller velg en eksisterende salgsordre.
3. I feltet **Dimensjonskonto** i **E-faktura**-delen i hurtigfanen **Generelt** i **Hode**-visningen angir du regnskapskoden for ordren.
4. Hvis du vil ha en separat regnskapskode for hver ordrelinje, følger du denne fremgangsmåten:

    1. Sett alternativet **Linjespesifikk** til **Ja**.
    2. Gå til **Linjer**-visningen.
    3. I **Dimensjonskonto**-feltet i fanen **Generelt** i hurtigfanen **Linjedetaljer** angir du en linjebestemt regnskapskode for hver ordrelinje.

#### <a name="project-invoices"></a>Prosjektfakturaer

1. Gå til **Prosjektstyring og regnskap** \> **Projekter** \> **Prosjektkontrakter**.
2. Opprett en prosjektkontrakt, eller velg en eksisterende prosjektkontrakt.
3. I hurtigfanen **Finansieringskilder** oppretter eller velger du en finansieringskilde av typen **Kunde**, og deretter velger du **Detaljer**.
4. I **Dimensjonskonto**-feltet i hurtigfanen **E-faktura** på siden **Finansieringskildedetaljer** angir du den prosjektspesifikke standard regnskapskoden.

    ![Prosjektspesifikk regnskapskode.](media/emea-nor-ger-proj-cost.jpg)

5. Hvis du vil angi kunderegnskapskoder direkte i prosjektfakturaforslag, følger du denne fremgangsmåten:

    1. Gå til **Prosjektstyring og regnskap** \> **Prosjektfakturaer** \> **Fakturaforslag for prosjekt**.
    2. Opprett et nytt fakturaforslag, eller velg et eksisterende fakturaforslag.
    3. I feltet **Dimensjonskonto** i **E-faktura**-delen i hurtigfanen **Generelt** i Hode-visningen angir du regnskapskoden for fakturaen.

6. Hvis du vil ha en separat regnskapskode for hver transaksjonslinje, følger du denne fremgangsmåten:

    1. Sett alternativet **Linjespesifikk** til **Ja**.
    2. I **Dimensjonskonto**-feltet i hurtigfanen **Transaksjoner for fakturaforslag** angir du en linjebestemt regnskapskode for hver transaksjonslinje.

    ![Transaksjonslinjebestemt regnskapskode.](media/emea-nor-ger-proj-prop-cost.jpg)

## <a name="export-customer-electronic-invoices"></a>Eksportere elektroniske fakturaer for kunde

### <a name="send-e-invoices"></a>Sende e-fakturaer

Når en faktura posteres, kan du generere en elektronisk faktura ved å velge **Send** \> **Original** for den valgte fakturaen.

![Sende en e-faktura.](media/emea-nor-ger-einvoice.jpg)

### <a name="view-e-invoices"></a>Vise e-fakturaer

Hvis du vil spørre om XML-filene for elektroniske fakturaer som er generert, følger du denne fremgangsmåten.

1. Gå til **Organisasjonsstyring** \> **Elektronisk rapportering** \> **Elektroniske rapporteringsjobber**.
2. Velg en jobb, og velg deretter **Vis filer**.

    ![Vis filer-knappen.](media/emea-nor-ger-einvoice-open.jpg)

3. Velg **Åpne** for å laste ned filen som inneholder den elektroniske fakturaen.

Hvis generering av de elektroniske fakturaene mislykkes på grunn av feil, velger du **Vis logg** \> **Meldingsdetaljer** for å vise flere detaljer om feilmeldingen.

![Meldingsdetaljer.](media/emea-nor-ger-einvoice-log.jpg)

### <a name="send-e-invoices-to-er-destinations"></a>Sende e-fakturaer til ER-mål

Du kan konfigurere ER-målene for elektroniske fakturaformater. I dette tilfellet blir utdata-XML-filer som inneholder elektroniske fakturaer, automatisk sendt til de definerte målene like etter at fakturaene er postert. Når du posterer fakturaene, må du aktivere parameteren **Skriv ut faktura**.

Hvis du vil ha mer informasjon om hvordan du konfigurerer ER-mål, kan du se [Mål for elektronisk rapportering](../../fin-ops-core/dev-itpro/analytics/electronic-reporting-destinations.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
