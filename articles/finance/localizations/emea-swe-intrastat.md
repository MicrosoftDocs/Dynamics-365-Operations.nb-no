---
title: Svensk Intrastat
description: Dette emnet inneholder informasjon om Intrastat-rapportering i Sverige.
author: andosip
ms.date: 8/24/2021
ms.topic: article
audience: Application User
ms.reviewer: kfender
ms.search.region: Global
ms.author: v-aosipov
ms.search.validFrom: ''
ms.openlocfilehash: 404fb8dff1519aefb2f4af25eb95dfa6fce75b7c
ms.sourcegitcommit: 259ba130450d8a6d93a65685c22c7eb411982c92
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/24/2021
ms.locfileid: "7417088"
---
# <a name="swedish-intrastat"></a>Svensk Intrastat

[!include[banner](../includes/banner.md)]

**Intrastat**-siden brukes til å generere og rapportere informasjon om handel mellom EU-land. Den svenske Intrastat-deklareringen inneholder informasjon om varehandel for rapportering.

Følgende felter finnes i den svenske Intrastat-deklareringen:

   - ISO-kode for partnerland
   - Transaksjonskode
   - Artikkelkode
   - Tilleggsenhet
   - Tykkelse
   - Fakturabeløp

## <a name="set-up-intrastat"></a>Definere Intrastat

Importer siste versjon av følgende ER-konfigurasjoner (elektronisk rapportering):

   - Intrastat modell
   - Intrastat-rapport
   - Intrastat (SE)

For mer informasjon, se [Last ned ER-konfigurasjoner fra det globale repositoriet for konfigurasjonstjenesten](../../fin-ops-core/dev-itpro/analytics/er-download-configurations-global-repo.md).

## <a name="set-up-foreign-trade-parameters"></a>Angi utenrikshandelsparametere

1. I Microsoft Dynamics 365 Finance går du til **Avgift** > **Oppsett** > **Utenrikshandelsparametere**.
2. På fanen **Intrastat** i hurtigfanen **Elektronisk rapportering** i feltet **Rapportformatkartlegging** velger du Intrastat **Intrastat (SE)**.
3. I feltet **Rapportformatkartlegging** velger du **Intrastat-rapport**.
4. I hurtigfanen **Artikkelkodehierarki** i feltet **Kategorihierarki** velger du **Intrastat**.
5. I feltet **Transaksjonskode** velger du transaksjonskoden for egenskapsoverføringer. Du kan bruke denne koden for transaksjoner som forårsaker faktiske eller planlagte overføringer av eiendeler mot kompensasjon (økonomisk eller annen). Du bruker det også til korrigeringer. Firmaer i Sverige bruker ensifrede transaksjonskoder.
6. I feltet **Kreditnota** velger du transaksjonskoden for retur av varer. Du bruker denne koden til retur av varer etter at transaksjonen som opprinnelig ble registrert under transaksjonskoden. Firmaer i Sverige bruker ensifrede transaksjonskoder.
7. I fanen **Land-/områdeegenskaper** i feltet **Land/område** viser du alle landene eller områdene som firmaet gjør forretninger med. For hvert land som er en del av EU, velger du **EU** i feltet **Type land/område**, slik at landet vises i Intrastat-rapporten.

## <a name="set-up-the-product-parameters-for-the-intrastat-declaration"></a>Definere produktparameterne for Intrastat-deklarering

1. Gå til **Behandling av produktinformasjon** > **Produkter** > **Frigitte produkter**.
2. Velg et produkt i rutenettet.
3. Velg artikkelkoden på hurtigfanen **Utenrikshandel** i **Intrastat**-delen i **Artikkel**-feltet.
4. Angi produktets vekt i kilogram i **Nettovekt**-feltet på hurtigfanen **Behandle lager**.
5. Gå til **Avgift** > **Oppsett** > **Utenrikshandel** > **Komprimering av Intrastat**, og velg feltene som skal sammenlignes når Intrastat-informasjon summeres. For svensk Intrastat velger du følgende felter:

    - Artikkelkode
    - Transaksjonskode
    - Retning
    - Land/område
    - Korrigert melding
    - Faktura

## <a name="intrastat-transfer"></a>Intrastat-overføring

I handlingsruten på **Intrastat**-siden kan du velge **Overfør** for å overføre informasjonen om fellesskapshandel automatisk fra salgsordrene, fritekstfakturaer, bestillinger, leverandørfakturaer, leverandørproduktmottak, prosjektfakturaer og overføringsordrer. Bare dokumenter som har et EU-land som destinasjonsland eller målområde (for fordelinger) eller forsendelse (for ankomster) blir overført.

Du kan også angi transaksjoner manuelt ved å velge **Ny** i handlingsruten.

### <a name="generate-an-intrastat-report"></a>Generere en Intrastat-rapport

1. Gå til **Avgift** > **Deklareringer** > **Utenrikshandel** > **Intrastat**.
2. Velg **Utlevering** > **Rapport** i handlingsruten.
3. I **Intrastat-rapport**-dialogboksen angir du følgende felt.

    | Felt            | beskrivelse                                                                                                                         |
    |------------------|-------------------------------------------------------------------------------------------------------------------------------------|
    | Fra dato        | Velg startdatoen for rapporten.                                                                                               |
    | Til dags dato          | Velg sluttdatoen for rapporten.                                                                                                 |
    | Generer fil    | Sett dette alternativet til **Ja** for å generere en TXT-fil for Intrastat-rapporten.                                                       |
    | Filnavn        | Angi navnet på TXT-filen.                                                                                                    |
    | Generer rapport  | Sett dette alternativet til **Ja** for å generere en XLSX-fil for Intrastat-rapporten.                                                     |
    | Navn på rapportfil | Angi navnet på XLSX-filen.                                                                                                   |
    | Retning        | Velg **Ankomster** for en rapport om fellesskapsankomster. Velg **Fordelinger** for en rapport om fellesskapsfordelinger. |

4. Velg **OK** og gå gjennom de genererte rapportene.

## <a name="example"></a>Eksempel

Dette eksemplet viser hvordan du posterer ankomster og fordelinger for Intrastat. Den bruker den juridiske enheten **DEMF**.

### <a name="preliminary-setup"></a>Foreløpig oppsett

1. Gå til **Organisasjonsadministrasjon** > **Organisasjon** > **Juridiske enheter**, og velg den juridiske enheten **DEMF**.
2. På hurtigfanen **Adresser** velger du **Rediger**, og i feltet **Land område** velger du deretter **SWE (Sverige)**.
3. Importer siste versjon av følgende ER-konfigurasjoner:

    - Intrastat modell
    - Intrastat-rapport
    - Intrastat (SE)

### <a name="create-transaction-codes"></a>Opprett transaksjonskoder

1. Gå til **Avgift** > **Oppsett** > **Utenrikshandel** > **Transaksjonskoder**.
2. Velg **Ny** i handlingsruten.
3. I **Transaksjonskode**-feltet skriver du inn **1**.
4. I **Navn**-feltet angir du **Vanlige transaksjoner**.
5. Velg **Lagre** i handlingsruten.

### <a name="set-up-foreign-trade-parameters"></a>Angi utenrikshandelsparametere

1. Gå til **Avgift** > **Oppsett** > **Utenrikshandel** > **Utenrikshandelsparametere**.
2. I **Intrastat**-fanen i hurtigfanen **Generelt** i **Transaksjonskode**-feltet velger du **1**.
3. I hurtigfanen **Elektronisk rapportering** i feltet **Rapportformatkartlegging** velger du **Intrastat (SE)**.
4. I feltet **Rapportformatkartlegging** velger du **Intrastat-rapport**.
5. I hurtigfanen **Artikkelkodehierarki** i feltet **Kategorihierarki** må du kontrollere at **Intrastat** er valgt.
6. Velg **Ny** i fanen **Land-/områdeegenskaper**.
7. I feltet **Land/område for part** velger du **SWE**.
8. Velg **Innenlands** i feltet **Land-/områdetype**.
9. I feltet **Land/område for part** velger du **DEU** og velger deretter **EU** i feltet **Type land/område**.

### <a name="set-up-product-information"></a>Definer produktinformasjon

1. Gå til **Behandling av produktinformasjon** > **Produkter** > **Frigitte produkter**.
2. Velg **D0001** i rutenettet.
3. Velg **100 200 30** i hurtigfanen **Utenrikshandel** i **Intrastat**-delen i feltet **Artikkel**.
4. Angi **5** i **Nettovekt**-feltet i hurtigfanen **Behandle lager** i delen **Vektmålinger**.
5. Velg **Lagre** i handlingsruten.

### <a name="change-the-site-address"></a>Endre områdeadressen

1. Gå til **Lagerstyring** > **Oppsett** > **Lager** > **Steder**.
2. Velg **1** i rutenettet.
3. Velg **Rediger** på hurtigfanen **Adresser**.
4. I dialogboksen **Rediger adresse**, i feltet **Land/område**, velger du **SWE**.
5. Velg **OK**.

### <a name="create-a-sales-order-with-an-eu-customer"></a>Opprett en salgsordre med en EU-kunde

1. Gå til **Kunder** > **Ordrer** > **Alle salgsordrer**.
2. Velg **Ny** i handlingsruten.
3. I dialogboksen **Opprett salgsordre**, i på **Kunde**-hurtigfanen i **Kunde**-delen i feltet **Kundekonto** velger du **DE-015**.
4. Velg **1** i **Område**-feltet i delen **Lagerdimensjoner**-delen i hurtigfanen **Generelt**.
5. I **Lager**-feltet velger du **11**.
6. Velg **OK**.
7. På fanen **Linjer** på hurtigfanen **Salgsordrelinjer** i **Varenummer**-feltet velger du **D0001**. I feltet **Antall** angi **10**.
8. På hurtigfanen **Linjedetaljer**, på fanen **Utenrikshandel**, kontrollerer du at feltene **Transaksjonskode** og **Artikkel** er angitt automatisk.
9. Velg **Lagre** i handlingsruten.
10. I handlingsruten, på **Faktura**-fanen i **Generer**-delen, velger du **Faktura**.
11. I dialogboksen **Postering av faktura** i hurtigfanen **Parametere** i **Parameter**-delen i **Antall**-feltet velger du **Alle**.
12. Klikk på **OK** for å postere fakturaen.

### <a name="transfer-the-transaction-to-the-intrastat-journal-and-review-the-result"></a>Overfør transaksjonen til Intrastat-journalen, og gå gjennom resultatet

1. Gå til **Avgift** > **Deklareringer** > **Utenrikshandel** > **Intrastat**.
2. I handlingsruten velger du **Overfør**.
3. I dialogboksen **Intrastat (overføring)** i **Parametere**-delen angir du **Kundefaktura**-alternativet til **Ja**.
4. Velg **Filter**.
5. Merk den første linjen i fanen **Område** i dialogboksen **Intrastat-filter**, og kontroller at **Felt**-feltet er satt til **Dato**.
6. Velg gjeldende dato i **Kriterier**-feltet.
7. Velg **OK** for å lukke dialogboksen **Intrastat-filter**.
8. Velg **OK** for å lukke dialogboksen **Intrastat (overfør)** og se gjennom resultatet. Linjen representerer salgsordre du opprettet tidligere.

    ![Intrastat-journallinjer for salgsordre](media/swe_intrastat_journal_sales_order.png)

9. Velg transaksjonslinjen, og velg deretter fanen **Generelt** for å vise flere detaljer.

    ![Detaljer på Intrastat-journallinje for salgsordre](media/swe_intrastat_journal_sales_order_line_details.png)

10. Velg **Utlevering** > **Rapport** i handlingsruten.
11. I dialogboksen **Intrastat-rapport** velger du måneden for salgsordren du opprettet, i hurtigfanen **Parametere** i **Dato**-delen.
12. I delen **Eksportalternativer** angir du alternativet **Generer** **fil** til **Ja**. I **Filnavn**-feltet angir du deretter det obligatoriske navnet.
13. Sett alternativet **Generer rapport** til **Ja**. I feltet **Navn på rapportfil** angir du deretter det obligatoriske navnet.
14. I **Retning**-feltet velger du **Fordelinger**.
15. Velg **OK** og gå gjennom rapporten i TXT-format som genereres. Tabellen nedenfor viser verdiene i eksempelrapporten.

    | ISO-kode for partnerland | Transaksjonskode | Artikkelkode | Tilleggsenhet | Tykkelse | Fakturabeløp |
    |--------------------------|------------------|----------------|-----------------|--------|----------------|
    | IT                       | 1                | 10020030       | 0               | 50     | 3290           |

16. Gå gjennom rapporten i Excel-format som genereres.

    ![Intrastat-rapport](media/swe_intrastat_report_for_dispatches.png)

### <a name="create-a-purchase-order"></a>Opprette en bestilling

1. Gå til **Leverandører** > **Bestillinger** > **Alle bestillinger**.
2. Velg **Ny** i handlingsruten.
3. I dialogboksen **Opprett bestilling**, i **Leverandørkonto**-feltet, velger du **DE-001**.
4. Velg **OK**.
5. På **Hode**-fanen, på hurtigfanen **Utenrikshandel**, bekrefter du at feltet **Transaksjonskode** er angitt til **1**.
6. På fanen **Linjer** på hurtigfanen **Bestillingslinjer** i **Varenummer**-feltet velger du **D0001**. I feltet **Antall** angi **6**.
7. I handlingsruten på fanen **Bestilling** i gruppen **Handlinger** velger du **Bekreft**.
8. I handlingsruten, på **Faktura**-fanen i **Generer**-gruppen, velger du **Faktura**.
9. I handlingsruten velger du **Standard fra**. Velg **Bestilt antall** i feltet **Standardantall for linjer**. Velg deretter **OK**.
10. På hurtigfanen **Leverandørfakturahode**, i delen **Fakturaidentifikasjon**, i **Nummer**-feltet velger du **0001**.
11. Velg **Poster** i handlingsruten for å postere fakturaen.

### <a name="create-an-intrastat-declaration-for-arrivals"></a>Opprett en Intrastat-deklarering for ankomster

1. Gå til **Avgift** > **Deklareringer** > **Utenrikshandel** > **Intrastat**.
2. I handlingsruten velger du **Overfør**.
3. I dialogboksen **Intrastat (overfør)** setter du alternativet **Leverandørfaktura** til **Ja**.
4. Velg **OK** for å overføre transaksjonene, og gå deretter gjennom Intrastat-journalen.

    ![Intrastat-journal for bestilling](media/swe_intrastat_journal_purchase_order.png)

5. Gå gjennom **Generelt**-fanen for bestillingen.

    ![Detaljer på Intrastat-journallinje for bestilling](media/swe_intrastat_journal_purchase_order_line_details.png)

6. Velg **Utlevering** > **Rapport** i handlingsruten.
7. I dialogboksen **Intrastat-rapport** velger du måneden for salgsordren du opprettet, i hurtigfanen **Parametere** i **Dato**-delen.
8. I delen **Eksportalternativer** angir du alternativet **Generer** **fil** til **Ja**. I **Filnavn**-feltet angir du deretter det obligatoriske navnet.
9. Sett alternativet **Generer rapport** til **Ja**. I feltet **Navn på rapportfil** angir du deretter det obligatoriske navnet.
10. Velg **Ankomster** i feltet **Retning**.
11. Velg **OK**, og gå gjennom rapporten i TXT-format som genereres. Tabellen nedenfor viser verdiene i eksempelrapporten.

    | ISO-kode for partnerland | Transaksjonskode | Artikkelkode | Tilleggsenhet | Tykkelse | Fakturabeløp |
    |--------------------------|------------------|----------------|-----------------|--------|----------------|
    | IT                       | 1                | 10020030       | 0               | 30     | 1714           |

12. Gå gjennom rapporten i Excel-format som genereres.

    ![Intrastat-ankomstrapport](media/swe_intrastat_arrivals_report.png)
