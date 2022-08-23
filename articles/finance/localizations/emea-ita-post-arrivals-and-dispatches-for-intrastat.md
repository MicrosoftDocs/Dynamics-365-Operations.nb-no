---
title: Poster ankomster og fordelinger for Intrastat
description: Denne artikkelen inneholder et eksempel som viser hvordan du posterer ankomster og fordelinger for Intrastat.
author: AdamTrukawka
ms.date: 08/23/2021
ms.topic: article
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: atrukawk
ms.search.validFrom: ''
ms.openlocfilehash: b6d46efd477f526c4bec3515086e10aa8172c579
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/12/2022
ms.locfileid: "9280695"
---
# <a name="post-arrivals-and-dispatches-for-intrastat"></a>Poster ankomster og fordelinger for Intrastat

[!include [banner](../includes/banner.md)]

Denne artikkelen inneholder et eksempel som viser hvordan du posterer ankomster og fordelinger for Intrastat. I eksemplet brukes den juridiske enheten **ITCO**.

## <a name="setup"></a>Installasjon

1. Importer siste versjon av følgende ER-konfigurasjoner (elektronisk rapportering):

    - Intrastat modell
    - Intrastat-rapport
    - Intrastat (IT)

    Du finner mer informasjon i [Last ned ER-konfigurasjoner fra det globale repositoriet for konfigurasjonstjenesten](../../fin-ops-core/dev-itpro/analytics/er-download-configurations-global-repo.md).

2. I Microsoft Dynamics 365 Finance definerer du følgende nummerserier som kontinuerlige: **Gene\_397**, **Acco\_16403**, **Gene\_407** og **PUR\_EU**.

    1. Gå til **Organisasjonsadministrasjon** > **Nummerserier** > **Nummerserier**.
    2. I rutenettet velger du en av nummerseriekodene.
    3. I handlingsruten velger du **Rediger**.
    4. I hurtigfanen **Generelt** i delen **Oppsett** angir du alternativet **Kontinuerlig** til **Ja**.
    5. Velg **Lagre** i handlingsruten.

3. Angi en lageradresse.

    1. Gå til **Lagerstyring** &gt; **Oppsett** &gt; **Lager** &gt; **Lagre**.
    2. Velg lager **11** i listen.
    3. Velg **Legg til** på hurtigfanen **Adresse**.
    4. I dialogboksen **Ny** **adresse** i feltet **Navne** **eller** **Beskrivelse** angir du **Hoved**.
    5. I feltet **Land/område** velger du **ITA (Italia)**.
    6. I feltet **By** velger du **Aprilia**.
    7. Velg **OK**.

4. Definer transaksjonskoder.

    1. Gå til **Avgift** > **Oppsett** > **Utenrikshandel** > **Transaksjonskoder**.
    2. Velg **Ny**, og konfigurer en transaksjonskode for overføringer av eiendom.

        - I **Transaksjonskode**-feltet skriver du inn **1**.
        - I **Navn**-feltet angir du **Overføring av eiendeler**.

    3. Velg **Ny**, og konfigurer en transaksjonskode for returer.

        - I **Transaksjonskode**-feltet skriver du inn **2**.
        - I **Navn**-feltet angir du **Retur av varer**.

5.  Angi utenrikshandelsparametere.

    1. Gå til **Avgift** > **Oppsett** > **Utenrikshandel** > **Utenrikshandelsparametere**.
    2. I **Intrastat**-fanen i hurtigfanen **Generelt** i **Transaksjonskode**-feltet velger du **1**.
    3. Velg **2** i **Kreditnota**-feltet.
    4. I feltet **Salgsrapporteringsperiode** velger du **Måned**.
    5. I feltet **Kjøpsrapporteringsperiode** velger du **Måned**.
    6. I hurtigfanen **Elektronisk rapportering** i feltet **Rapportformatkartlegging** velger du **Intrastat (IT)**.
    7. I feltet **Rapporteringsformatkartlegging** velger du **Intrastat-rapport**.
    8. På hurtigfanen **Artikkelkodehierarki** i feltet **Kategorihierarki** velger du **Intrastat**.
    9. På hurtigfanen **Statistisk verdi** angir i alternativet **Skriv ut og eksporter statistiske data** til **Ja**.
    10. På fanen **Land-/områdeegenskaper** kontrollerer du at følgende linjer finnes.

        | **Part/land/område** | **Intrastat-kode** | **Valuta.** | **Land-/områdetype** |
        |--------------------------|--------------------|--------------|-------------------------|
        | ITA                      | IT                 | EUR          | Innenlands                |
        | SMR                      | SM                 | EUR          | Spesiell innenlands        |

    11. Velg **Ny** på verktøylinjen, og opprett følgende linje.

        | **Part/land/område** | **Intrastat-kode** | **Valuta.** | **Land-/områdetype** |
        |--------------------------|--------------------|--------------|-------------------------|
        | DNK                      | DK                 | DKK          | EU                      |

6. Definer avgiftsfritaksnumre.

    1. Gå til **Avgift** > **Oppsett** > **Merverdiavgift** > **Numre for avgiftsfritak**.
    2. Velg **Ny** i handlingsruten, og opprett følgende linjer.

        | **Land/område** | **Avgiftsfritaksnummer** | **Firmanavn** |
        |--------------------|-----------------------|------------------|
        | DEU                | DE3456789012          | UE-LEVERANDØR        |
        | DNK                | DK0987654321          | Kunde ER      |

7. Angi leverandøradressen.

    1. Gå til **Leverandører** &gt; **Leverandører** &gt; **Alle leverandører**.
    2. I rutenettet velger du **UE-leverandør**.
    3. Velg **Legg til** på hurtigfanen **Adresser**.
    4. I dialogboksen **Ny adresse** i feltet **Navn eller beskrivelse** angir du **Tyskland**.
    5. I feltet **Land/område** velger du **DEU**.
    6. Velg **OK** for å opprette den nye adressen.
    7. I hurtigfanen **Faktura og levering**, i **Merverdiavgift**-delen i feltet **Avgiftsfritaksnummer**, velger du **Alle** og velger deretter **DE1234567890**.
    8. Velg **Lagre** i handlingsruten.

8. Angi kundeadresse

    1. Gå til **Kunder** > **Kunder** > **Alle kunder**.
    2. Velg **ITCO-000001** i rutenettet.
    3. Velg **Rediger** på hurtigfanen **Adresser**.
    4. I dialogboksen **Ny adresse** i feltet **Navn eller beskrivelse** angir du **San Marino**.
    5. I feltet **Land/område** velger du **SMR**.
    6. Velg **OK** for å opprette den nye adressen.
    7. På hurtigfanen **Faktura og levering**, i **Faktura**-delen, i feltet **Fakturakonto** velger du **ITCO-000001**.
    8. I feltet **Nummerseriegruppe** velger du **IT\_VENDOM**.
    9. Velg **Lagre** i handlingsruten og lukk siden.
    10. I rutenettet på **Alle kunder**-siden velger du **ITCO-000002**.
    11. Velg **Legg til** på hurtigfanen **Adresser**.
    12. I dialogboksen **Ny adresse** i feltet **Navn eller beskrivelse** angir du **Danmark**.
    13. I feltet **Land/område** velger du **DNK**.
    14. Velg **OK** for å opprette den nye adressen.
    15. På hurtigfanen **Salgsdemografi**, i **Valuta**-feltet velger du **DKK**.
    16. På hurtigfanen **Faktura og levering**, i **Merverdiavgift**-delen i feltet **Mva-gruppe**, velger du **IT\_PUREU**.
    17. I feltet **Avgiftsfritaksnummer** velger du **Alle** og velger deretter **DK0987654321**.
    18. Velg **Lagre** i handlingsruten.

9. Definer kategorihierarkiet.

    1. Gå til **Behandling av produktinformasjon** > **Oppsett** > **Kategorier og attributter** > **Kategorihierarkier**.
    2. Velg **Intrastat** i rutenettet.
    3. I handlingsruten velger du **Ny kategorinode**.
    4. Angi **Tjeneste** i feltet **Navn**.
    5. I **Kode**-feltet skriver du inn **123456**.
    6. Velg **Lagre** i handlingsruten.

10. Definer produkter.

    1. Gå til **Behandling av produktinformasjon** > **Produkter** > **Frigitte produkter**.
    2. Velg **ITEM** i rutenettet.
    3. På hurtigfanen **Innkjøp**, i **Administrasjon**-delen, i **Leverandør**-feltet velger du **ITCO-000001**.
    4. På hurtigfanen **Utenrikshandel**, i **Intrastat**-delen, i **Artikkel**-feltet velger du **\[100 200 30\] Høyttaler**.
    5. I delen **Opprinnelse** i feltet **Land/område**-felt velger du **DEU**.
    6. Velg **BE** i feltet **Delstat/område**.
    7. Angi **5** i **Nettovekt**-feltet i hurtigfanen **Behandle lager** i delen **Nettomålinger**.
    8. Velg **Lagre** i handlingsruten.
    9. I rutenettet på siden **Frigitte produkter** velger du **Servicevare**.
    10. På hurtigfanen **Utenrikshandel**, i **Intrastat**-delen, i **Artikkel**-feltet velger du **\[123456\] Service**.
    11. Velg **Lagre** i handlingsruten.

11. Definer transportmetoder.

    1. Gå til **Avgift** > **Oppsett** > **Utenrikshandel** > **Transportmetode**.
    2. Velg **Ny** i handlingsruten, og opprett følgende transportmetoder.

        | **Transport** | **Beskrivelse** |
        |---------------|-----------------|
        | 1             | Vei            |
        | 2             | Fly             |

12. Definer en leveringsmåte.

    1. Gå til **Innkjøp og leverandører** > **Oppsett** > **Distribusjon** > **Leveringsmåter**.
    2. Velg **Ny** i handlingsruten.
    3. I **Leveringsmåte**-feltet skriver du inn **1**.
    4. I **Beskrivelse**-feltet angir du **Lastebil**.
    5. På hurtigfanen **Utenrikshandel**, i **Transport**-feltet, velger du **1 Vei**.
    6. Velg **Lagre** i handlingsruten.

13. Definer leveringsbetingelser.

    1. Gå til **Leverandør** > **Oppsett** > **Leveringsbetingelser**.
    2. I listen velger du **CFR**.
    3. På hurtigfanen **Generelt**, i feltet **Intrastat-kode**, angir du **1**.

## <a name="post-arrivals-for-intrastat"></a>Postere ankomster for Intrastat

### <a name="purchase-goods-by-using-a-purchase-order"></a>Kjøpe varer ved hjelp av en bestilling

Denne delen av eksemplet viser hvordan du bruker en bestilling til å kjøpe varer (artikler) fra EU-land.

1. Gå til **Leverandører** > **Bestillinger** > **Alle bestillinger**.
2.  Velg **Ny** i handlingsruten.
3.  I dialogboksen **Opprett bestilling**, i **Leverandørkonto**-feltet, velger du **UE-leverandør**.
4.  På hurtigfanen **Administrasjon**, i **Språk**-feltet, velger du **it**.
5.  Velg **OK**.
6.  I **Overskrift**-visningen, på hurtigfanen **Utenrikshandel**, bekrefter du at feltet **Transaksjonskode** er angitt til **1**.
7.  Kontroller at feltet **Opprinnelsesregion/-mål** er satt til **RM**.
8.  På hurtigfanen **Levering**, i **Levering**-delen, i feltet **Leveringsmåte** velger du **1**.
9.  I feltet **Leveringsbetingelser** velger du **CFR**.
10. I **Linjer**-visningen, på hurtigfanen **Bestillingslinjer**, i **Varenummer**-feltet, velger du **Vare**.
11. I **Område**-feltet velger du **1**.
12. I **Lager**-feltet velger du **11**.
13. I feltet **Antall** angi **10**.
14. Angi **100** i **Enhetspris**-feltet.
15. På **Oppsett**-fanen, i **Mva**-delen, i feltet **Varens mva-gruppe**, velger du **22%EU**.
16. I handlingsruten på fanen **Bestilling** i gruppen **Handlinger** velger du **Bekreft**.
17. I handlingsruten, på **Faktura**-fanen i **Generer**-gruppen, velger du **Faktura**.
18. I handlingsruten velger du **Standard fra**.
19. I feltet **Standardantall for linjer** velger du **Bestilt antall** og deretter **OK**.
20. På hurtigfanen **Leverandørfakturahode**, i delen **Fakturaidentifikasjon**, i **Nummer**-feltet velger du **0001**.
21. I delen **Fakturadatoer**, i feltet **Fakturadato**, velger du **7/9/2021**.
22. Velg **Poster** i handlingsruten for å postere fakturaen.

### <a name="purchase-services-by-using-a-vendor-invoice"></a>Kjøpe tjenester ved hjelp av en leverandørfaktura

Denne delen av eksemplet viser hvordan du bruker en leverandørfaktura til å kjøpe tjenester fra EU-land.

1. Gå til **Leverandører** > **Fakturaer** > **Fakturajournal**.
2. Velg **Ny** i handlingsruten.
3. I **Navn**-feltet velger du **VEND\_EUINV**.
4. I handlingsruten velger du **Linjer**.
5. Angi **7/9/2021** i feltet **Dato**.
6. I **Kontotype**-feltet velger du **Leverandør**.
7. I **Konto**-feltet velger du **UE-leverandør**.
8. I feltet **Fakturadata** velger du **7/9/2021**.
9. I **Faktura**-feltet skriver du inn **ITA-0004**.
10. I **Kreditt**-feltet skriver du inn **120000**.
11. I feltet **Motkontotype** velger du **Hovedbok**.
12. I feltet **Motkonto** velger du **110130**.
13. I feltet **Merverdiavgiftsgruppe** velger du **IT\_PUREU**.
14. I feltet **Varens mva-gruppe** velger du **22%EU**.
15. Følg disse trinnene på fanen **Utenrikshandel**:

    1. I **Transaksjonskode**-feltet velger du **1**.
    2. I **Transport**-feltet velger du **2 Fly**.
    3. I **Artikkel**-feltet velger du **\[123456\] Tjeneste**.
    4. I feltet **Land/område** velger du **ITA**.
    5. Velg **LAZ** i feltet **Delstat/område**.
    6. I feltet **Opprinnelsesregion/-mål** velger du **LT**.


16. Velg **Poster** i handlingsruten.
17. Opprett en Intrastat-deklarering for ankomster.

    1. Gå til **Avgift** > **Deklareringer** > **Utenrikshandel** > **Intrastat**.
    2. I handlingsruten velger du **Overfør**.
    3. I dialogboksen **Intrastat (overfør)** setter du alternativet **Leverandørfaktura** til **Ja**.
    4. Velg **OK** for å overføre transaksjonene, og gå deretter gjennom Intrastat-journalen.

   ![Siden Intrastat-journal, fanen Oversikt.](media/ita_intrastat_journal_vendor_invoice.png)

18. Gå gjennom **Generelt**-fanen for bestillingen.

    ![Detaljer på Intrastat-journallinje for bestilling](media/ita_intrastat_journal_purchase_order_line_details.png)

19. Gå gjennom **Generelt**-fanen for leverandørfakturaen.

    ![Detaljer på Intrastat-journallinje for leverandørfaktura](media/ita_intrastat_journal_vendor_invoice_line_details.png)

20. Generer Intrastat-rapporten for ankomster

    1. Velg **Utlevering** > **Rapport** i handlingsruten.
    2. I dialogboksen **Intrastat-rapport**, i **Dato**-delen, i **Fra dato**-feltet, velger du **7/1/2021**.
    3. I **Til dato**-feltet velger du **7/31/2021**.
    4. I delen **Eksportalternativer** angir du alternativene **Generer fil** og **Generer rapport** til **Ja**.
    5. I feltet **Filnavn** angir du **Ankomstfil**.
    6. I feltet **Navn på rapportfil** angir du **Ankomstrapport**.
    7. Velg **Ankomster** i feltet **Retning**.
    8. Angi **123456** i feltet **Referansenummer**.
    9. Velg **OK** for å generere Intrastat-rapporten og Intrastat-filen, og gå gjennom dem.

    Illustrasjonen nedenfor viser et eksempel på en Intrastat-rapport.

    ![Intrastat-ankomstrapport.](media/ita_intrastat_arrivals_report.png)

    Illustrasjonen nedenfor viser et eksempel på en Intrastat-fil.

    ![Intrastat-ankomstfil.](media/ita_intrastat_arrivals_file.png)

## <a name="post-dispatches-for-intrastat"></a>Postere fordelinger for Intrastat

### <a name="sell-goods-by-using-a-sales-order"></a>Selge varer ved hjelp av en salgsordre

Denne delen av eksemplet viser hvordan du bruker en salgsordre til å selge varer (artikler) til EU-land.

1. Gå til **Kunder** > **Ordrer** > **Alle salgsordrer**.
2. Velg **Ny** i handlingsruten.
3. I **Opprett salgsordre**-dialogboksen, i **Kundekonto**-feltet, velger du **ITCO-000002**.
4. Velg **OK**.
5. I **Hode**-visningen, på hurtigfanen **Levering**, i delen **Div. leveringsinformasjon**, i feltet **Leveringsmåte**, velger du **1 Lastebil**.
6. I feltet **Leveringsbetingelser** velger du **CFR**.
7. I visningen **Linjer** på hurtigfanen **Salgsordrelinjer** i **Varenummer**-feltet velger du **ITEM**.
8. I feltet **Antall** angi **50**.
9. I **Område**-feltet velger du **1**.
10. I **Lager**-feltet velger du **11**.
11. Angi **250** i **Enhetspris**-feltet.
12. På hurtigfanen **Linjedetaljer**, på **Oppsett**-fanen, i **Mva**-delen, i feltet **Varens mva-gruppe**, velger du **22%EU**.
13. Velg **Lagre** i handlingsruten.
14. I handlingsruten på fanen **Faktura** i gruppen **Generer**, velger du **Faktura** for å opprette fakturaen for ordren.
15. I dialogboksen **Postering av faktura** på hurtigfanen **Parametere** i **Parameter**-delen i **Antall**-feltet velger du **Alle**.
16. På hurtigfanen **Oppsett**, i feltet **Fakturadato**, velger du **7/9/2021**.
17. Velg **OK**.
18. Se gjennom linjene i Intrastat-journalen.

    1. Gå til **Avgift** > **Deklareringer** > **Utenrikshandel** > **Intrastat**.
    2. I handlingsruten velger du **Overfør**.
    3. I dialogboksen **Intrastat (overfør)** setter du alternativet **Kundefaktura** til **Ja**.
    4. Velg **OK** for å overføre transaksjonene, og gå deretter gjennom Intrastat-journalen. Kreditnotatransaksjonen er merket som en rettelse og har negativt fakturabeløp.

        ![Siden Intrastat-journal](media/ita_intrastat_journal_sales_order.png)

        ![Detaljer på Intrastat-journallinje for salgsordre](media/ita_intrastat_journal_sales_order_line_details.png)

### <a name="return-goods-by-using-a-credit-note"></a>Returnere varer ved hjelp av en kreditnota

Denne delen av eksemplet viser hvordan du bruker en kreditnota til å returnere varer (artikler) fra EU-land.

1. Gå til **Kunder** > **Ordrer** > **Alle salgsordrer**.
2. Velg **Ny** i handlingsruten.
3. I **Opprett salgsordre**-dialogboksen, i **Kundekonto**-feltet, velger du **ITCO-000002**.
4. Velg **OK**.
5. I **Hode**-visningen, på hurtigfanen **Levering**, i delen **Div. leveringsinformasjon**, i feltet **Leveringsmåte**, velger du **1 Lastebil**.
6. I feltet **Leveringsbetingelser** velger du **CFR**.
7. På hurtigfanen **Utenrikshandel**, i **Transaksjonskode**-feltet, velger du **2**.
8. På fanen **Linjer** på hurtigfanen **Salgsordrelinjer** i **Varenummer**-feltet velger du **ITEM**.
9. Angi **-10** i **Antall**-feltet.
10. I **Område**-feltet velger du **1**.
11. I **Lager**-feltet velger du **11**.
12. Angi **250** i **Enhetspris**-feltet.
13. På hurtigfanen **Linjedetaljer**, på **Oppsett**-fanen, i **Mva**-delen, i feltet **Varens mva-gruppe**, velger du **22%EU**.
14. I delen **Returordre**, i feltet **Returparti-ID**, velger du partiet du opprettet tidligere.
15. Velg **Lagre** i handlingsruten.
16. I handlingsruten på fanen **Faktura** i gruppen **Generer**, velger du **Faktura** for å opprette fakturaen for ordren.
17. På hurtigfanen **Parametere**, i **Parameter**-delen, i **Antall**-feltet, velger du **Alle**.
18. I dialogboksen **Postering av faktura**, på hurtigfanen **Oppsett**, i feltet **Fakturadato**, velger du **7/9/2021**.
19. Klikk på **OK** for å postere fakturaen.
20. Se gjennom linjene i Intrastat-journalen.

    1. Gå til **Avgift** > **Deklareringer** > **Utenrikshandel** > **Intrastat**.
    2. I handlingsruten velger du **Overfør**.
    3. I dialogboksen **Intrastat (overfør)** setter du alternativet **Kundefaktura** til **Ja**.
    4. Velg **OK** for å overføre transaksjonene, og gå deretter gjennom Intrastat-journalen. Kreditnotatransaksjonen er merket som en rettelse og har negativt fakturabeløp.

    ![Kreditnota for Intrastat-journal](media/ita_intrastat_journal_credit_note.png)

    ![Detaljer på Intrastat-journallinje for kreditnota](media/ita_intrastat_journal_credit_note_line_details.png)

### <a name="sell-goods-to-san-marino-by-using-a-sales-order"></a>Selge varer til San Marino ved hjelp av en salgsordre

Denne delen av eksemplet viser hvordan du bruker en salgsordre til å kjøpe varer (artikler) til San Marino.

1. Gå til **Kunder** > **Ordrer** > **Alle salgsordrer**.
2. Velg **Ny** i handlingsruten.
3. I **Opprett salgsordre**-dialogboksen, i **Kundekonto**-feltet, velger du **ITCO-000001**.
4. Velg **OK**.
5. I **Hode**-visningen, på hurtigfanen **Levering**, i delen **Div. leveringsinformasjon**, i feltet **Leveringsmåte**, velger du **1**.
6. I feltet **Leveringsbetingelser** velger du **CFR**.
7. På fanen **Linjer** på hurtigfanen **Salgsordrelinjer** i **Varenummer**-feltet velger du **ITEM**.
8. I feltet **Antall** angi **30**.
9. I **Område**-feltet velger du **1**.
10. I **Lager**-feltet velger du **11**.
11. Angi **200** i **Enhetspris**-feltet.
12. Velg **Lagre** i handlingsruten.
13. I handlingsruten på fanen **Faktura** i gruppen **Generer**, velger du **Faktura** for å opprette fakturaen for ordren.
14. På hurtigfanen **Parametere**, i **Parameter**-delen, i **Antall**-feltet, velger du **Alle**.
15. I dialogboksen **Postering av faktura**, på hurtigfanen **Oppsett**, i feltet **Fakturadato**, velger du **7/9/2021**.
16. Klikk på **OK** for å postere fakturaen.
17. Se gjennom linjene i Intrastat-journalen.

    1. Gå til **Avgift** > **Deklareringer** > **Utenrikshandel** > **Intrastat**.
    2. I handlingsruten velger du **Overfør**.
    3. I dialogboksen **Intrastat (overfør)** setter du alternativet **Kundefaktura** til **Ja**.
    4. Velg **OK** for å overføre transaksjonene, og gå deretter gjennom Intrastat-journalen.

   ![Intrastat-journal for San Marino](media/ita_intrastat_journal_sales_order_san_marino.png)

   ![Detaljer på Intrastat-journallinje for San Marino](media/ita_intrastat_journal_sales_order_san_marino_line_details.png)

18. Opprett en Intrastat-deklarering for fordelinger.

    1. Gå til **Avgift** &gt; **Deklareringer** &gt; **Utenrikshandel** &gt; **Intrastat**.
    2. Velg **Utlevering** &gt; **Rapport** i handlingsruten.
    3. I dialogboksen **Intrastat-rapport**, i **Dato**-delen, i **Fra dato**-feltet, velger du **7/1/2021**.
    4. I **Til dato**-feltet velger du **7/31/2021**.
    5. I delen **Eksportalternativer** angir du alternativene **Generer fil** og **Generer rapport** til **Ja**.
    6. I feltet **Filnavn** angir du **Fordelingsfil**.
    7. I feltet **Navn på rapportfil** angir du **Fordelingsrapport**.
    8. I **Retning**-feltet velger du **Fordelinger**.
    9. Angi **98754** i feltet **Referansenummer**.
    10. Velg **OK** for å generere Intrastat-rapporten og Intrastat-filen.

        Illustrasjonen nedenfor viser et eksempel på en utskrevet Intrastat-rapport.

        ![Intrastat-rapport](media/ita_intrastat_report_for_dispatches.png)

        Illustrasjonen nedenfor viser et eksempel på en utskrevet Intrastat-fil.

        ![Intrastat-fil for fordelinger](media/ita_intrastat_file_for_dispatches.png)
