---
title: Elektroniske fakturaer for kunde i Danmark
description: Dette emnet forklarer hvordan du konfigurerer og elektroniske fakturaer i Danmark.
author: ilkond
ms.date: 12/20/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Norway
ms.author: ilyako
ms.search.validFrom: 2021-01-01
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 5bde6b55810d48fa8f852e4f1215879c371736b9
ms.sourcegitcommit: d13ea8b6baf73601a8b57548232aac84ffaba717
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/21/2021
ms.locfileid: "7941390"
---
# <a name="customer-electronic-invoices-in-denmark"></a>Elektroniske fakturaer for kunde i Danmark

[!include [banner](../includes/banner.md)]

Dette emnet beskriver hvordan du konfigurerer og utsteder elektroniske kundefakturaer i Danmark ved hjelp av [OIOUBL](http://www.oioubl.info/Classes/da/Invoice.html)-formatet for elektroniske fakturaer.

## <a name="prerequisites"></a>Forutsetninger

Primæradressen for den juridiske enheten må være i Danmark.

## <a name="import-electronic-reporting-configurations"></a>Importere konfigurasjoner for elektronisk rapportering

I arbeidsområdet **Elektronisk rapportering** importerer du følgende ER-formater (elektronisk rapportering) fra repositoriet:

- OIOUBL Salgsfaktura (DK)
- OIOUBL Prosjektfaktura (DK)
- OIOUBL Salgskreditnota (DK)
- OIOUBL Prosjektkreditnota (DK)

> [!NOTE]
> Alle andre nødvendige konfigurasjoner importeres automatisk.

Hvis du vil ha mer informasjon om hvordan du importerer ER-konfigurasjoner, kan du se [Laste ned konfigurasjoner for elektronisk rapportering fra Lifecycle Services](../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).

### <a name="reference-the-imported-er-format-configurations"></a>Referere til de importerte ER-formatkonfigurasjonene

1. Gå til **Kunder** \> **Oppsett** \> **Kundeparametere**.
2. Velg de importerte formatene for elektroniske dokumenter i hurtigfanen **Elektronisk rapportering** i fanen **Elektroniske dokumenter**:

    - **Salgs- og fritekstfaktura:** OIOUBL Salgsfaktura (DK)
    - **Salgs- og fritekstkreditnota:** OIOUBL Salgskreditnota (DK)
    - **Prosjektfaktura:** OIOUBL Prosjektfaktura (DK)
    - **Prosjektkreditnota:** OIOUBL Prosjektkreditnota (DK)

## <a name="configure-parameters"></a>Konfigurere parametere

### <a name="configure-legal-entity-parameters"></a>Konfigurere parametere for juridisk enhet

1. Gå til **Organisasjonsstyring** \> **Organisasjoner** \> **Juridiske enheter**.
2. I feltet **Mva-nummer** i hurtigfanen **Avgiftsregistrering** angir du mva-nummeret for firmaet ditt.
3. Angi firmaets registreringsnummer i **Registreringsnummer**-feltet i hurtigfanen **Bankkontoinformasjon**.
4. I feltet **FI-Kreditor-ID** angir du kreditorens identifikasjonsnummer hvis du planlegger å bruke FIK-betalinger.

### <a name="configure-methods-of-payment"></a>Konfigurer betalingsmetoder

I henhold til OIOUBL-standardene må betalingsmetodekodene i XML-filen for elektroniske fakturaer samsvare med den [offisielle listen over standardiserte koder](http://www.oioubl.info/codelists/en/urn_oioubl_codelist_paymentmeanscode-1.1.html).

Systemet støtter følgende forhåndsdefinerte koder for betalingsmetoder og gir automatisk konvertering til de offisielle kodene.

| Intern betalingsmetodekode | Offisiell betalingsmetodekode |
|------------------------------|------------------------------|
| DK:BANK                      | 42                           |
| DK:FIK                       | 93                           |
| DK:GIRO                      | 50                           |
| Alle andre koder              | 97                           |

Følg denne fremgangsmåten for å konfigurere betalingsmetoder.

1. Gå til **Kunder** \> **Oppsett** \> **Betalingsoppsett** \> **Betalingsmetoder**.
2. Opprett en ny betalingsmetode, eller velg en eksisterende metode som skal konfigureres.
3. Velg **Bank** i **Kontotype**-feltet i delen **Postering**-delen i hurtigfanen **Generelt**.
4. I **Betalingskonto**-feltet angir du firmaets bankkonto som er knyttet til betalingsmetoden.

    > [!NOTE]
    > Firmaets bankkonto må allerede være opprettet i **Kontant- og bankbehandling** \> **Bankkontoer** \> **Bankkontoer**.

### <a name="configure-units-of-measure"></a>Konfigurer måleenheter

1. Gå til **Organisasjonsstyring** \> **Oppsett** \> **Enheter** \> **Enheter**.
2. Velg en enhets-ID i listen, og velg deretter **Eksterne koder**.
3. I **Kode**-feltet i **Oversikt**-delen på siden **Eksterne koder** angir du en kode som svarer til den valgte enhets-ID-en.
4. I **Verdi**-feltet i **Verdi**-delen angir du den eksterne koden som skal brukes som anbefalt måleenhetskode i henhold til [koder for måleenheter for internasjonal handel](https://docs.oasis-open.org/ubl/prd1-UBL-2.1/cva/UBL-DefaultDTQ-2.1.html#d27e1).

### <a name="configure-sales-tax-codes"></a>Konfigurer mva-koder

Når du genererer elektroniske fakturaer i OIOUBL-format, må avgiftsinformasjonen i XML-filen som sendes ut, struktureres hierarkisk på en bestemt måte.

Det øverste nivået i hierarkiet er **Mva-plan**. Du finner en offisiell liste over avgiftsplaner som gjelder for OIOUBL-formatet under [OIOUBL-avgiftsplaner](http://oioubl.info/documents/da/da/Kodelister/OIOUBL_CODE_TaxSchemeID-1.5.pdf). 

Det neste nivået av avgiftsdatagruppering innenfor avgiftsplanen, er **Mva-kategori**. Du finner en offisiell liste over avgiftskategorier som gjelder for OIOUBL-formatet under [OIOUBL-avgiftskategorier](http://oioubl.info/documents/da/da/Kodelister/OIOUBL_CODE_TAXCATEGORYID.pdf). 

For enkelte avgifter må det også defineres et tilleggsattributt, **mva-typekode**.

Du kan knytte avgiftsplaner, avgiftskategorier og avgiftstypekoder til mva-koder ved hjelp av programspesifikke parametere. Hvis du vil ha informasjon om hvordan du konfigurerer programspesifikke parametere, kan du se neste del.

### <a name="configure-application-specific-parameters"></a>Konfigurer programspesifikke parametere 

Programspesifikke parametere må konfigureres for følgende konfigurasjoner:

- OIOUBL Salgsfaktura (DK)
- OIOUBL Prosjektfaktura (DK)
- OIOUBL Salgskreditnota (DK)
- OIOUBL Prosjektkreditnota (DK)

For hver konfigurasjon følger du disse trinnene.

1. I arbeidsområdet **Elektronisk rapportering** på flisen **Rapporteringskonfigurasjoner** i listen over konfigurasjoner velger du en nødvendig konfigurasjon. Velg for eksempel **OIOUBL salgsfaktura (DK)**.
2. I menyen **Konfigurasjoner**, i delen **Programspesifikke parametere**, velg **Oppsett**.
3. På siden **Programspesifikke parametere** i hurtigfanen **Oppslag** velger du **TaxSchemeSelector** i rutenettet.

    I hurtigfanen **Betingelser** konfigurerer du deretter korrespondansen mellom interne mva-koder og offisielle avgiftsplankoder. 

4. I hurtigfanen **Betingelser** velger du **Legg til** for å legge til en betingelse i rutenettet.
5. I **Kode**-feltet for den nye betingelsen velger du mva-koden som er definert i systemet. 

    > [!NOTE]
    > I **Kode**-feltet kan du velge plassholderverdien **\*Tom\*** eller **\*Ikke tom\*** i stedet for en bestemt mva-kode.

6. I **Oppslagsresultat**-feltet velger du en tilsvarende offisiell avgiftsplankode.

    ![Definere betingelser for TaxSchemeSelector-oppslag på siden Programspesifikke parametere.](media/emea-dnk-ASP-parameters.jpg)

7. I hurtigfanen **Oppslag** velger **TaxCategorySelector** i rutenettet.
8. I hurtigfanen **Betingelser** gjentar du trinn 4 til 6 for å konfigurere korrespondansen mellom interne mva-koder og offisielle avgiftskategorikoder.
9. I hurtigfanen **Oppslag** velger **TaxCodeTypeSelector** i rutenettet.
10. I hurtigfanen **Betingelser** gjentar du trinn 4 til 6 for å konfigurere korrespondansen mellom interne mva-koder og avgiftstypekoder. Hvis det ikke kreves noen avgiftstypekode, velger du **Ikke tilgjengelig**.
11. Velg **Fullført**, og lagre endringene i **Tilstand**-feltet øverst på siden.

### <a name="configure-customer-parameters"></a>Konfigurere kundeparametere

1. Gå til **Kunder** \> **Kunder** \> **Alle kunder**, og velg en kunde.
2. I hurtigfanen **Faktura og levering** setter du alternativet **eFaktura** til **Ja** for å aktivere generering av elektroniske fakturaer.
3. Sett alternativet **Vedlegg til eFaktura** til **Ja** for å legge en PDF-kopi av den utskrivbare fakturaen ved den elektroniske fakturaen.
4. I feltet **Avgiftsfritaksnummer** skriver du inn kundens MVA-fritaksnummer.
5. I **EAN**-feltet angir du kundens identifikasjonsnummer. Dette nummeret blir brukt som verdien **Sluttpunkt-ID** i XML-filen for den elektroniske fakturaen.
6. Velg en person som regnes som kjøpers kontakt, i hurtigfanen **Salgsdemografi** i feltet **Primærkontakt**.

    > [!NOTE]
    > Alle tilgjengelige kontaktpersoner må allerede være definert for denne kunden.

## <a name="export-customer-electronic-invoices"></a>Eksportere elektroniske fakturaer for kunde

### <a name="send-e-invoices"></a>Sende e-fakturaer

Når en faktura er postert, kan du generere en elektronisk faktura ved å velge fakturaen og deretter velge **Send** \> **Original** i **Dokument**-gruppen i fanen **Faktura** i handlingsruten.

![Sende en e-faktura.](media/emea-nor-ger-einvoice.jpg)

### <a name="view-e-invoices"></a>Vise e-fakturaer

Følg denne fremgangsmåten hvis du vil spørre om XML-filene for elektroniske fakturaer som er generert.

1. Gå til **Organisasjonsstyring** \> **Elektronisk rapportering** \> **Elektroniske rapporteringsjobber**.
2. Velg en jobb, og velg deretter **Vis filer**.
3. Velg **Åpne** for å laste ned filen som inneholder den elektroniske fakturaen.

    Hvis genereringen av de elektroniske fakturaene mislyktes på grunn av feil, velger du **Vis logg**. Deretter velger du **Meldingsdetaljer** på meldingslinjen for å vise flere detaljer om feilen.

    ![Viser meldingsdetaljene for en feil.](media/emea-nor-ger-einvoice-log.jpg)

### <a name="send-e-invoices-to-er-destinations"></a>Sende e-fakturaer til ER-mål

Du kan konfigurere ER-målene for elektroniske fakturaformater. I dette tilfellet blir utdata-XML-filer som inneholder elektroniske fakturaer, automatisk sendt til de definerte målene like etter at fakturaene er postert. Når du posterer fakturaene, må du aktivere parameteren **Skriv ut faktura**.

Hvis du vil ha mer informasjon om hvordan du konfigurerer ER-mål, kan du se [Mål for elektronisk rapportering](../../fin-ops-core/dev-itpro/analytics/electronic-reporting-destinations.md).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
