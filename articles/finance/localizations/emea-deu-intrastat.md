---
title: Tysk Intrastat
description: Dette emnet inneholder informasjon om Intrastat-deklarering i Tyskland.
author: andosip
ms.date: 08/2/2021
ms.topic: article
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: v-aosipov
ms.search.validFrom: ''
ms.openlocfilehash: e1dbf0997417f9f1ad313e6a7b3c2c9cfae41efc6b1cfda60a5500ae0af94709
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6759849"
---
# <a name="german-intrastat"></a>Tysk Intrastat

**Intrastat**-siden brukes til å generere og rapportere informasjon om handel mellom EU-land. Den tyske Intrastat-deklareringen inneholder informasjon om varehandel for rapportering.

Følgende tabell viser feltene som er inkludert i den tyske Intrastat-deklareringen.

| Felt | Fordelinger | Tilganger |
|-------------------------|-------------------------|-------------------------|
| Referanseperiode | X | X |
| Retningskode | X | X |
| Valuta for Intrastat-deklareringen</br>**Obs!** Denne valutaen er <em>regnskapsvalutaen</em>. | X | X |
| Artikkelkode | X | X |
| Artikkelnavn | X | X |
| Tilleggsenhetskode | X | X |
| Medlemsland for forsendelse/mål | X | X |
| Nettomasse | X | X |
| Antall i tilleggsenheter | X | X |
| Opprinnelsesland |  | X |
| Fakturabeløp | X |  |
| Statistisk verdi | X | X |
| Transaksjonstyper | X | X |
| Transportmodus | X | X |
| Områdekode</br>**Obs:**</br><ul></br><li>Hvis landet eller området for opprinnelsen er Tyskland og fakturaen er for fordelinger, vises en Intrastat-kode for opprinnelseslandet.</li></br><li>Hvis landet eller området for opprinnelsen gjelder Tyskland og fakturaen gjelder for fordelinger, vises koden **99**.</li></br><li>Hvis fakturaen gjelder for ankomster, vises det en Intrastat-kode for landet.</li></br></ul> | X | X |
| Kode for port/flyplass/innlandsport | X | X |
| Leveringsbetingelse | X | X |


## <a name="set-up-intrastat"></a>Definere Intrastat

1. Angi firmaets koder.

    1. Gå til **Organisasjonsstyring** > **Organisasjoner** > **Juridiske enheter**.
    2. I hurtigganen **Utenrikshandel og logistikk** angir du ID-en for utvekslingsavtale i **DVR**-feltet i delen **Identifikasjon**. Denne ID-en inkluderes i rapporten.
    3. I feltet **Mva-fritaksnummer for eksport** angir du firmaets merverdiavgiftnummer (mva.) for eksport.
    4. I feltet **Mva-fritaksnummer for import** angir du firmaets mva-nummer for import.
    5. I feltet **Intrastat-kode** angir du Intrastat-koden som er tilordnet den juridiske enheten.
    6. I feltet **Mva-nummer** i hurtigfanen **Avgiftsregistrering** angir du mva-nummeret for firmaet ditt.

    > [!NOTE]
    > Hvis du genererer en Intrastat-rapport for samarbeidspartnere, angir du mva-registreringsnummeret for hovedfirmaet i feltet **Avgiftsregistreringsnummer**.

2. I [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index), i biblioteket over delt aktiva, laster du ned de nyeste versjonene av følgende ER-konfigurasjoner for Intrastat-erklæringen.

    - Intrastat modell
    - Intrastat-rapport
    - INSTAT XML
    - INSTAT XML (DE)

3. Angi utenrikshandelsparametere:

    1. I Dynamics 365 Finance går du til **Avgift** > **Oppsett** > **Utenrikshandelsparametere**.
    2. På fanen **Intrastat** i hurtigfanen **Elektronisk rapportering** i feltet **Rapportformatkartlegging** velger du Intrastat **Intrastat XML (DE)**.
    3. I feltet **Rapportformatkartlegging** velger du **Intrastat-rapport**.
    4. I hurtigfanen **Artikkelkodehierarki** i feltet **Kategorihierarki** velger du **Intrastat**.
    5. I feltet **Transaksjonskode** velger du transaksjonskoden for egenskapsoverføringer. Du kan bruke denne koden for transaksjoner som forårsaker faktiske eller planlagte overføringer av eiendeler mot kompensasjon (økonomisk eller annen). Du bruker det også til korrigeringer.
    6. I feltet **Kreditnota** velger du transaksjonskoden for retur av varer. Du bruker denne koden til retur av varer etter at transaksjonen som opprinnelig ble registrert under transaksjonskoden.
    7. I **Myndighet**-feltet velger du Intrastat-myndigheten.
    8. Gå til **Avgift** > **Indirekte avgifter** > **Merverdiavgift** > **Skattemyndigheter**, og angi følgende informasjon for Intrastat-myndighetene du valgte i det forrige trinnet:

       - Identifikasjon av skattemyndighet
       - Adresse
       - Kontaktinformasjon

    9. I fanen **Land-/områdeegenskaper** i feltet **Land/område** viser du alle landene eller områdene som firmaet gjør forretninger med. For hvert land eller område velger du **EU** i feltet **Type land/område**, slik at landet eller området vises i Intrastat-rapporten.

4. Definer områdekoder.

    1. Gå til **Organisasjonsstyring** > **Global adressebok** > **Adresser** > **Adresseoppsett**.
    2. Velg **DEU** i feltet **Land/område** i fanen **Delstat/område**, og velg deretter **Bruk filter**.
    3. Velg delstaten i rutenettet. Deretter angir du den unike Intrastat-koden i feltet **Intrastat-kode**.

5. Definer opprinnelsesadressen for et produkt.

    1. Gå til **Behandling av produktinformasjon** > **Produkter** > **Frigitte produkter**.
    2. Velg produktet i rutenettet.
    3. Velg **DEU** i hurtigfanen **Utenrikshandel** i **Intrastat**-delen i feltet **Opprinnelsesland**.

6. Gå til **Avgift** > **Oppsett** > **Utenrikshandel** > **Komprimering av Intrastat**, og velg feltene som skal sammenlignes når Intrastat-informasjon summeres. For tysk Intrastat velger du følgende felter:

    - Artikkelkode
    - Land/område
    - Korrigert melding
    - Retning
    - Leveringsbetingelse
    - Faktura
    - Opprinnelsesland/-område
    - Havn
    - Land/område for avsender
    - Delstat for avsender
    - Statistisk prosedyre
    - Transaksjonskode
    - Transport
    - Avgiftsfritaksnummer

### <a name="intrastat-transfer"></a>Intrastat-overføring

I handlingsruten på **Intrastat**-siden kan du velge **Overfør** for å overføre informasjonen om fellesskapshandel automatisk fra salgsordrene, fritekstfakturaer, bestillinger, leverandørfakturaer, leverandørproduktmottak **,** prosjektfakturaer og overføringsordrer. Bare dokumenter som har et EU-land som destinasjonsland eller målområde (for fordelinger) eller forsendelse (for ankomster) blir overført.

Du kan også angi transaksjoner manuelt ved å velge **Ny** i handlingsruten.

### <a name="generate-an-intrastat-report"></a>Generere en Intrastat-rapport

1. Gå til **Avgift** > **Deklareringer** > **Utenrikshandel** > **Intrastat**.
2. Velg **Utlevering** > **Rapport** i handlingsruten.
3. I **Intrastat-rapport**-dialogboksen angir du følgende felt.

    | Felt | beskrivelse |
    |-------------------------|-------------------------|
    | Fra dato | Velg startdatoen for rapporten. |
    | Til dags dato | Velg sluttdatoen for rapporten. |
    | Generer fil | Sett dette alternativet til **Ja** for å generere en XML-fil. |
    | Filnavn | La dette feltet stå tomt. Filnavnet genereres automatisk og består av verdien til **&lt;envelopeID&gt;** XML-koden pluss XML-filen for filtypen **XML**.</br>Verdien **&lt;envelopeId&gt;** er en sammenslåing av følgende elementer i denne rekkefølgen:</br><ol type="1"></br><li>Verdien til **&lt;interchangeAgreementId&gt;**-koden</li></br><li>En bindestrek (-)</li></br><li>Verdien til **&lt;referencePeriod i YYYYMM&gt;**-koden</li></br><li>En bindestrek (-)</li></br><li>Verdien for **&lt;Envelope/DateTime/date i YYYYMMDD&gt;**-koden</li></br><li>En bindestrek (-)</li></br><li>Verdien for **&lt;Envelope/DateTime/time in hhmm&gt;**-koden</li></br></ol> |
    | Retning | <ul></br><li>Velg **Ankomster** for rapport om fellesskapsankomster.</li></br><li>Velg **Fordelinger** for rapport om fellesskapsfordelinger.</li></br><li>Velg **Begge** for rapport om både ankomster og fordelinger.</li></br></ul> |
    | Avgiftsregistreringsnummer | Angi registreringsnummeret som skal brukes til å generere identifikasjonskoden til avsenderen, hvis nummeret er forskjellig fra avgiftsregistreringsnummeret for den juridiske enheten. |


## <a name="example"></a>Eksempel

Dette eksemplet viser hvordan du posterer ankomster og fordelinger for Intrastat. Den bruker den juridiske enheten **DEMF**.

1. I [LCS](https://lcs.dynamics.com/Logon/Index) i biblioteket over delt aktiva, laster du ned de nyeste versjonene av følgende ER-konfigurasjoner for formatet i Intrastat-erklæringen:

    - Intrastat modell
    - Intrastat-rapport
    - Intrastat XML
    - Intrastat XML (DE)

2. Opprett transaksjonskoder.

    1. Gå til **Avgift** > **Oppsett** > **Utenrikshandel** > **Transaksjonskoder**.
    2. Velg **Ny** i handlingsruten.
    3. I **Transaksjonskode**-feltet skriver du inn **21**.
    4. I **Navn**-feltet angir du **Retur av varer**.
    5. Velg **Lagre** i handlingsruten.

3. Definer myndighetens ID-nummer.

    1. Gå til **Avgift** > **Indirekte avgifter** > **Merverdiavgift** > **Skattemyndigheter**.
    2. I -listen velger du **TA**.
    3. I **Myndighetsidentifikasjon**-feltet skriver du inn **123**.

4. Definer områdekoder.

    1. Gå til **Organisasjonsstyring** > **Global adressebok** > **Adresser** > **Adresseoppsett**.
    2. Velg **DEU** i feltet **Land/område** i fanen **Delstat/område**, og velg deretter **Bruk filter**.
    3. I rutenettet velger du **BE**, og deretter skriver du inn **11** i feltet **Intrastat-kode**.
    4. Velg **Lagre** i handlingsruten.

5. Angi utenrikshandelsparametere.

    1. Gå til **Avgift** > **Oppsett** > **Utenrikshandel** > **Utenrikshandelsparametere**.
    2. I **Intrastat**-fanen i hurtigfanen **Generelt** i **Transaksjonskode**-feltet velger du **11**.
    3. Velg **21** i **Kreditnota**-feltet.
    4. Velg **TA** i **Myndighet**-feltet.
    5. I hurtigfanen **Elektronisk rapportering** i feltet **Rapportformatkartlegging** velger du **INSTAT XML (DE)**.
    6. I feltet **Rapportformatkartlegging** velger du **Intrastat-rapport**.
    7. I hurtigfanen **Artikkelkodehierarki** i feltet **Kategorihierarki** må du kontrollere at **Intrastat** er valgt.
    8. Velg **Ny** i fanen **Land-/områdeegenskaper**.
    9. I feltet **Land/område for part** velger du **FRA**.
    10. Velg **EU** i feltet **Land-/områdetype**.

6. Tilordne en varekode til et produkt, og angi produktets opprinnelse. Feltene **Varekode**, **Opprinnelsesland/-område** og **Opprinnelsesstat** angis deretter automatisk for salgsordrer og bestillinger når du velger produktet.

    1. Gå til **Behandling av produktinformasjon** > **Produkter** > **Frigitte produkter**.
    2. Velg **D0001** i rutenettet.
    3. Velg **920 20 34** i hurtigfanen **Utenrikshandel** i **Intrastat**-delen i feltet **Artikkel**.
    4. I delen **Opprinnelse** i feltet **Land/område**-felt velger du **DEU**.
    5. Angi **12** i **Nettovekt**-feltet i hurtigfanen **Behandle lager** i delen **Vektmålinger**.
    6. Velg **Lagre** i handlingsruten.

7. Tilordne transport til en leveringsmåte. Transportkoden vil automatisk bli angitt for ordrer når du velger leveringsmåte.

    1. Gå til **Innkjøp og leverandører** > **Oppsett** > **Distribusjon** > **Leveringsmåter**.
    2. I listen velger du **10**.
    3. På hurtigfanen **Utenrikshandel**, i **Transport**-feltet, velger du **01**.

8. Opprett en salgsordre med en EU-kunde.

    1. Gå til **Kunder** > **Ordrer** > **Alle salgsordrer**.
    2. Velg **Ny** i handlingsruten.
    3. I dialogboksen **Opprett salgsordre**, i på **Kunde**-hurtigfanen i **Kunde**-delen i feltet **Kundekonto** velger du **DE-012**.
    4. Velg **1** i **Område**-feltet i delen **Lagerdimensjoner**-delen i hurtigfanen **Generelt**.
    5. I **Lager**-feltet velger du **11**.
    6. Velg **OK**.
    7. På fanen **Hode** på hurtigfanen **Utenrikshandel**, i **Port**-feltet, velger du **53**.
    8. Velg **31710** i **Statistikkprosedyre**-feltet.
    9.  I fanen **Linjer** på **Salgsordrelinjer**-hurtigfanen i **Varenummer**-feltet velger du **D0001**. I feltet **Antall** angi **10**.
    10. I hurtigfanen **Linjedetaljer** kontrollerer du at feltene **Transaksjonskode**, **Utenrikshandel**, **Transport**, **Artikkel** og **Land/område for opprinnelse** angis automatisk.
    11. Velg **Lagre** i handlingsruten.
    12. I handlingsruten, på **Faktura**-fanen i **Generer**-delen, velger du **Faktura**.
    13. I dialogboksen **Postering av faktura** i hurtigfanen **Parametere** i **Parameter**-delen i **Antall**-feltet velger du **Alle**.
    14. Klikk på **OK** for å postere fakturaen.

9.  Overfør transaksjonen til Intrastat-journalen, og gå gjennom resultatet.

    1. Gå til **Avgift** > **Deklareringer** > **Utenrikshandel** > **Intrastat**.
    2. I handlingsruten velger du **Overfør**.
    3. I dialogboksen **Intrastat (overføring)** i **Parametere**-delen angir du **Kundefaktura**-alternativet til **Ja**.
    4. Velg **Filter**.
    5. Merk den første linjen i fanen **Område** i dialogboksen **Intrastat-filter**, og kontroller at **Felt**-feltet er satt til **Dato**.
    6. Velg gjeldende dato i **Kriterier**-feltet.
    7. Velg **OK** for å lukke dialogboksen **Intrastat-filter**.
    8. Velg **OK** for å lukke dialogboksen **Intrastat (overfør)** og se gjennom resultatet. Linjen representerer salgsordre du opprettet tidligere.

        ![Linjen som representerer salgsordre på Intrastat-siden](media/intrastat_deu_1.png)

10. Velg transaksjonslinjen, og velg deretter fanen **Generelt** for å vise flere detaljer.

    ![Salgsordredetaljer i fanen Generelt på Intrastat-siden](media/intrastat_deu_2.png)

11. Opprette en kreditnota ved å bruke en salgsordre.

    1. Gå til **Kunder** > **Ordrer** > **Alle salgsordrer**.
    2. Velg **Ny** i handlingsruten.
    3. I dialogboksen **Opprett salgsordre**, i på **Kunde**-hurtigfanen i **Kunde**-delen i feltet **Kundekonto** velger du **DE-012**.
    4. Velg **1** i **Område**-feltet i delen **Lagerdimensjoner**-delen i hurtigfanen **Generelt**.
    5. I **Lager**-feltet velger du **11**.
    6. På fanen **Hode** på hurtigfanen **Utenrikshandel**, i **Port**-feltet, velger du **53**.
    7. Velg **31710** i **Statistikkprosedyre**-feltet.
    8. I fanen **Linjer** på **Salgsordrelinjer**-hurtigfanen i **Varenummer**-feltet velger du **D0001**. I feltet **Antall** angi **-2**.
    9. I **Utenlandshandel**-fanen i hurtigfanen **Linjedetaljer** i **Transaksjonskode**-feltet velger du **21**.
    10. Kontroller at feltene **Transport**, **Artikkel** og **Land/område for opprinnelse** angis automatisk.
    11. Velg **Lagre** i handlingsruten.
    12. I handlingsruten, på **Faktura**-fanen i **Generer**-delen, velger du **Faktura**.
    13. I dialogboksen **Postering av faktura** i hurtigfanen **Parametere** i **Parameter**-delen i **Antall**-feltet velger du **Alle**.
    14. Klikk på **OK** for å postere fakturaen.

12. Overfør transaksjonen til Intrastat-journalen, og gå gjennom resultatet.

    1. Gå til **Avgift** > **Deklareringer** > **Utenrikshandel** > **Intrastat**.
    2. I handlingsruten velger du **Overfør**.
    3. I dialogboksen **Intrastat (overføring)** i **Parametere**-delen angir du **Kundefaktura**-alternativet til **Ja**.
    4. Velg **OK** for å lukke dialogboksen **Intrastat (overfør)** og se gjennom resultatet. En ny linje der **Retning**-feltet er satt til **Ankomster**, er lagt til.            
        Denne linjen representerer fysisk retur av varer.

        ![Linje for fysisk retur av varer på Intrastat-siden](media/intrastat_deu_3.png)

13. Velg transaksjonslinjen, og velg deretter fanen **Generelt** for å vise flere detaljer.

    ![Detaljer om fysisk retur av varer i fanen Generelt på Intrastat-siden](media/intrastat_deu_4.png)

14. Opprett en korrigering ved å bruke en salgsordre:

    1. Gå til **Kunder** > **Ordrer** > **Alle salgsordrer**.
    2. Velg **Ny** i handlingsruten.
    3. I dialogboksen **Opprett salgsordre**, i på **Kunde**-hurtigfanen i **Kunde**-delen i feltet **Kundekonto** velger du **DE-012**.
    4. Velg **1** i **Område**-feltet i delen **Lagerdimensjoner**-delen i hurtigfanen **Generelt**.
    5. I **Lager**-feltet velger du **11**.
    6. På fanen **Hode** på hurtigfanen **Utenrikshandel**, i **Port**-feltet, velger du **53**.
    7. Velg **31710** i **Statistikkprosedyre**-feltet.
    8. I fanen **Linjer** på **Salgsordrelinjer**-hurtigfanen i **Varenummer**-feltet velger du **D0001**. I feltet **Antall** angi **-3**.
    9. I **Utenlandshandel**-fanen i hurtigfanen **Linjedetaljer** i **Transaksjonskode**-feltet velger du **11**.
    10. Kontroller at feltene **Transport**, **Artikkel** og **Land/område for opprinnelse** angis automatisk.
    11. Velg **Lagre** i handlingsruten.
    12. Sørg for at feltet **Transaksjonskode** er satt til 11.
    13. I handlingsruten, på **Faktura**-fanen i **Generer**-delen, velger du **Faktura**.
    14. I dialogboksen **Postering av faktura** i hurtigfanen **Parametere** i **Parameter**-delen i **Antall**-feltet velger du **Alle**.
    15. Klikk på **OK** for å postere fakturaen.

15. Overfør transaksjonen til Intrastat-journalen, og gå gjennom resultatet:

    1. Gå til **Avgift** > **Deklareringer** > **Utenrikshandel** > **Intrastat**.
    2. I handlingsruten velger du **Overfør**.
    3. I dialogboksen **Intrastat (overføring)** i **Parametere**-delen angir du **Kundefaktura**-alternativet til **Ja**.
    4. Velg **OK** for å lukke dialogboksen **Intrastat (overfør)** og se gjennom resultatet. Det er lagt til en ny linje der det vises en hake i **Korrigering**-kolonnen.

        ![Linje for korrigeringen på Intrastat-siden](media/intrastat_deu_5.png)

16. Velg transaksjonslinjen, og velg deretter fanen **Generelt** for å vise flere detaljer.

    ![Detaljer om korrigeringen i fanen Generelt på Intrastat-siden](media/intrastat_deu_6.png)

17. Velg **Utlevering** > **Rapport** i handlingsruten.
18. I dialogboksen **Intrastat-rapport** velger du måneden for salgsordren du opprettet, i hurtigfanen **Parametere** i **Dato**-delen.
19. I delen **Eksportalternativer** angir du alternativet **Generer** **fil** til **Ja**.
20. I **Filnavn**-feltet angir du det obligatoriske navnet.
21. Velg **OK** og gå gjennom rapporten som genereres. Tabellen nedenfor viser verdiene i eksempelrapporten.

    | **Navn**                  | **Salgsfaktura**  |   **Korrigert melding**   | **Kreditnota** |
    |---------------------------|--------------------|--------------------|-----------------|
    | declarationId             | 2021-07-D          | 2021-07-A          |                 |
    | referencePeriod           | 2021-07            | 2021-07            |                 |
    | PSIId                     | 11203/118/12345000 | 11203/118/12345000 |                 |
    | functionCode              | O                  | O                  |                 |
    | flowCode                  | D                  | A                  |                 |
    | CurrencyCode              | EUR                | EUR                |                 |
    | itemNumber                | 0000362            | 0000362            | 0000361         |
    | CN8Code                   | 9202034            | 9202034            | 9202034         |
    | goodsDescription          | Speaker            | Speaker            | Speaker         |
    | MSConsDestCode            | FR                 | FR                 | FR              |
    | countryOfOriginCode       | \-                 | \-                 | DE              |
    | netMass                   | 120                | -36                | 24              |
    | invoicedAmount            | 3290               | -987               | \-              |
    | StatisticalValue          | 3290               | -987               | 658             |
    | natureOfTransactionACode  | 1                  | 1                  | 2               |
    | natureOfTransactionBCode  | 1                  | 1                  | 1               |
    | modeOfTransportCode       | 01                 | 01                 | 01              |
    | regionCode                | 11                 | 11                 | 11              |
    | portAirportInlandportCode | 53                 | 53                 | 53              |

