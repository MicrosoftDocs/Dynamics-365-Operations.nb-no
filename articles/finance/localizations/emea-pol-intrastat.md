---
title: Polsk Intrastat
description: Denne artikkelen inneholder informasjon om Intrastat-rapportering i Polen.
author: andosip
ms.date: 11/09/2021
ms.topic: article
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: ''
ms.openlocfilehash: 45bd1d3c90d0a8a8ad5db6d0b80c5eed0aa489e8
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8871108"
---
# <a name="polish-intrastat"></a>Polsk Intrastat

[!include[banner](../includes/banner.md)]

**Intrastat**-siden brukes til å generere og rapportere informasjon om handel mellom EU-land. Den polske Intrastat-deklareringen inneholder informasjon om varehandel for rapportering.

Følgende felter finnes i den polske Intrastat-deklareringen. Alle feltene er inkludert ved ankomster og fordelinger, bortsett fra **RodzajTransportu** (transportmodus) og **KrajPochodzenia** (opprinnelsesland eller -område), som ikke er inkludert ved fordelinger, og **IdKontrahenta** (kundens utenlandske mva-nummer), som ikke er inkludert ved ankomster.

| Feltnavn | Beskrivelse |
|-------------------------|-------------------------|
| Deklaracja Data | Datoen da dokumentet ble opprettet. |
| Miesiac | Referansemåneden for deklareringen. |
| Rok | Referanseåret for deklareringen. |
| Numer | Deklareringsnummeret i referanseperioden. |
| Wersja | Versjonsnummeret for deklareringen. |
| NrWlasny | ID-en for deklareringen. Verdien genereres automatisk. |
| Typ | Rapportretningen.</br><li>For ankomster vises en "P".</li><li>For fordelinger vises en "W".</li> |
| Rodzaj | Typen deklarering. Verdien angir om rapporten er den opprinnelige deklareringen eller en rettelsesdeklarering. |
| UC | Enhetskoden som Intrastat-deklareringen er adressert til. Verdien er angitt i feltet **Avgiftsfritaksnummer** i **Merverdiavgift**-delen på **Agent**-fanen på siden **Utenrikshandelsparametere**. |
| Nazwa | Navnet på firmaet. |
| Miejscowosc, UlicaNumer, KodPocztowy | Den fullstendige adressen til den juridiske enheten. |
| Nip | Det polske avgiftsidentifikasjonsnummeret (merverdiavgift-ID [mva-ID]). |
| Regon | Det polske statistiske identifikasjonsnummeret (bedriftsnummer). |
| LacznaWartoscFaktur | Summen av fakturaverdier. |
| LacznaWartoscStatystyczna | Summen av statistiske verdier. |
| LacznaLiczbaPozycji | Totalt antall vareartikler. |
| PozId | Det påfølgende nummeret til en gitt vareartikkel. |
| OpisTowaru | Handelsnavnet for artikkelen. |
| KrajPochodzeniaWysylki | ISO-koden (den internasjonale standardiseringsorganisasjonen) for betalingslandet eller -regionen til motparten. |
| WarunkiDostawy | Intrastat-koden for leveringsbetingelsene. |
| RodzajTransakcji | Koden som viser transaksjonens natur. Polske firmaer bruker tosifrede transaksjonskoder. |
| KodTowarowy | Den åttesifrede artikkelkoden i henhold til den kombinerte nomenclature-listen. |
| RodzajTransportu | Intrastat-koden for transportmodusen. |
| KrajPochodzenia | ISO-koden for landet eller regionen der artiklene ble produsert eller fremstilt. |
| MasaNetto | Nettovekten i hele kilogram. |
| IloscUzupelniajacaJm | Antallet i tilleggsmålenheten, i hele tall. |
| WartoscFaktury | Fakturaverdien til alle transaksjoner som er dekket av én vare. |
| WartoscStatystyczna | Den statistiske verdien. |
| Wypelniajacy: NazwiskoImie, Telefon, Faks, Email | For- og etternavn, telefonnummer, faksnummer og e-postadresse til personen som sender deklareringen. |
| IdKontrahenta | Kundens utenlandske mva-nummer i et EU-medlemsland. |


## <a name="set-up-intrastat"></a>Definere Intrastat

Fra det globale repositoriet importerer du den nyeste versjonen av følgende ER-konfigurasjoner (Electronic Reporting):

   - Intrastat modell
   - Intrastat-rapport
   - Intrastat (PL)

For mer informasjon, se [Last ned ER-konfigurasjoner fra det globale repositoriet for konfigurasjonstjenesten](../../fin-ops-core/dev-itpro/analytics/er-download-configurations-global-repo.md).

## <a name="set-up-a-vat-id-and-an-enterprise-number-for-your-company"></a>Definer en mva-ID og et bedriftsnummer for firmaet

### <a name="create-registration-types-for-company-codes"></a>Opprett registreringstyper for firmakoder

Du må opprette to registreringstyper for firmakoder: én for MVA-ID-en (NIP-kode) og én for bedriftsnummeret (Regon-kode).

1. Gå til **Organisasjonsstyring** > **Global adressebok** > **Registreringstyper** > **Registreringstyper**.
2. Velg **Ny** i handlingsruten for å opprette en registreringstype for MVA-ID-en.
3. I dialogboksen **Angi detaljer for registreringstypen** skriver du inn et navn på den nye registreringstypen i **Navn**-feltet. Skriv for eksempel inn **NIP**.
4. I feltet **Land/område** velger du **POL**.
5. Velg **Opprett**.
6. Velg **Ny** i handlingsruten for å opprette en registreringstype for bedriftsnummeret.
7. I dialogboksen **Angi detaljer for registreringstypen** skriver du inn et navn på den nye registreringstypen i **Navn**-feltet. Skriv for eksempel inn **Regon**.
8. I feltet **Land/område** velger du **POL**.
9. Velg **Opprett**.

### <a name="match-the-registration-types-with-registration-categories"></a>Samsvar registreringstypene med registreringskategorier

1. Gå til **Organisasjonsstyring** > **Global adressebok** > **Registreringstyper** > **Registreringskategorier**.
2. Velg **Ny** i handlingsruten for å opprette en kobling mellom hver registreringstype du opprettet, og en registreringskategori.

    - For registreringstypen for MVA-ID-en (NIP-koden) velger du registreringskategorien **MVA-ID**.
    - For registreringstypen for bedriftsnummeret (Regon-koden) velger du registreringskategorien **Foretaks-ID (COID)**.

### <a name="set-up-a-vat-id-and-an-enterprise-number-for-your-company"></a>Definer en mva-ID og et bedriftsnummer for firmaet

1. Gå til **Organisasjonsstyring** > **Organisasjoner** > **Juridiske enheter**.
2. Velg bedriften din i rutenettet.
3. I handlingsruten velger du **Registrerings-ID-er**.
4. Velg **Legg til** på hurtigfanen **Registrerings-ID**.
5. I feltet **Registreringstype** velger du en av registreringstypene du opprettet tidligere.
6. Angi bedriftens MVA-ID (NIP-kode) eller bedriftsnummer (Regon-kode), avhengig av registreringstypen du valgte i det forrige trinnet.
7. Gjenta trinn 4 til 6 for de andre registreringstypene du opprettet tidligere.

## <a name="set-up-a-company-address"></a>Definer en bedriftsadresse

1. Gå til **Organisasjonsstyring** > **Organisasjoner** > **Juridiske enheter**.
2. Velg bedriften din i rutenettet.
3. Velg **Rediger** på fanen **Adresser**.
4. I dialogboksen **Rediger adresse**, i feltet **Postnummer**, velger du bedriftens postnummer.
5. I **Gate**-feltet angir du adressen.
6. I **By**-feltet velger du byen.

## <a name="set-up-foreign-trade-parameters"></a>Angi utenrikshandelsparametere

1. Gå til **Avgift** > **Oppsett** > **Utenrikshandelsparametere**.
2. På fanen **Intrastat** i hurtigfanen **Elektronisk rapportering** i feltet **Rapportformatkartlegging** velger du Intrastat **Intrastat (PL)**.
3. I feltet **Rapportformatkartlegging** velger du **Intrastat-rapport**.
4. I hurtigfanen **Artikkelkodehierarki** i feltet **Kategorihierarki** velger du **Intrastat**.
5. I feltet **Transaksjonskode** velger du transaksjonskoden for egenskapsoverføringer. Du kan bruke denne koden for transaksjoner som forårsaker faktiske eller planlagte overføringer av eiendeler mot kompensasjon (økonomisk eller annen). Du bruker det også til korrigeringer. Firmaer i Polen bruker tosifrede transaksjonskoder.
6. I feltet **Kreditnota** velger du transaksjonskoden for retur av varer.
7. I fanen **Land-/områdeegenskaper** i feltet **Land/område** viser du alle landene eller områdene som firmaet gjør forretninger med. For hvert land som er en del av EU, velger du **EU** i feltet **Type land/område**, slik at landet vises i Intrastat-rapporten. For Polen velger du **Innenlands** i feltet **Land-/områdetype**.
8. På **Agent**-fanen, på **Agent**-hurtigfanen, i **Mva**-delen, i feltet **Avgiftsfritaksnummer**, angir du **420000** for å indikere enhetskoden som Intrastat-klareringen er adressert til.
9. På **Kontakt**-fanen angir du navn, telefonnummer, faksnummer og e-postadresse til personen som sender deklareringen.
10. På **Nummerserier**-fanen, i feltet **Nummerseriekode** for referansen **XML-filnummer**, angir du en ikke-sammenhengende nummerserie på maksimalt ni tegn. Dette feltet brukes til å generere en verdi for feltet **Deklarasjons-ID** automatisk i Intrastat-rapporten.

## <a name="set-up-product-parameters-for-the-intrastat-declaration"></a>Definer produktparametere for Intrastat-deklarering

1. Gå til **Behandling av produktinformasjon** > **Produkter** > **Frigitte produkter**.
2. Velg et produkt i rutenettet.
3. Velg artikkelkoden på hurtigfanen **Utenrikshandel** i **Intrastat**-delen i **Artikkel**-feltet. Navnet på artikkelen blir skrevet ut i feltet **Beskrivelse av artikler** i Intrastat-rapporten.
4. I **Opprinnelse**-delen, i feltet **Lang/område**, velger du produktets opprinnelsesland eller -område.
5. Angi produktets vekt i kilogram i **Nettovekt**-feltet på hurtigfanen **Behandle lager**.

## <a name="set-up-compression-of-intrastat"></a>Definer komprimering av Intrastat

-   Gå til **Avgift** > **Oppsett** > **Utenrikshandel** > **Komprimering av Intrastat**, og velg feltene som skal sammenlignes når Intrastat-informasjon summeres. For polsk Intrastat velger du følgende felter:

    - Artikkelkode
    - Transaksjonskode
    - Opprinnelsesland/-område
    - Transport
    - Leveringsbetingelser
    - Land/område for avsender
    - Land/område
    - Korrigert melding
    - Avgiftsfritaksnummer
    - Retning
    - Faktura

## <a name="set-up-the-transport-method-and-delivery-terms"></a>Definer transportmetoden og leveringsbetingelsene

1.  Definer transportkoder.

    1. Gå til **Avgift** > **Oppsett** > **Utenrikshandel** > **Transportmetode**.
    2. Velg **Ny** i handlingsruten.
    3. Angi en unik kode i **Transport**-feltet. Polske firmaer bruker ensifrede transportkoder.

2.  Definer Intrastat-koder for leveringsmåter.

    1. Gå til **Innkjøp og leverandører** > **Oppsett** > **Distribusjon** > **Leveringsbetingelser**.
    2. Velg et sett med leveringsbetingelser i rutenettet.
    3. På hurtigfanen **Generelt**, i feltet **Intrastat-kode**, angir du den unike koden.

## <a name="intrastat-transfer"></a>Intrastat-overføring

I handlingsruten på **Intrastat**-siden kan du velge **Overfør** for å overføre informasjonen om fellesskapshandel automatisk fra salgsordrene, fritekstfakturaer, bestillinger, leverandørfakturaer, leverandørproduktmottak, prosjektfakturaer og overføringsordrer. Bare dokumenter som har et EU-land som destinasjonsland eller målområde eller forsendelse, blir overført.

Du kan også angi transaksjoner manuelt ved å velge **Ny** i handlingsruten.

### <a name="generate-an-intrastat-report"></a>Generere en Intrastat-rapport

1. Gå til **Avgift** > **Deklareringer** > **Utenrikshandel** > **Intrastat**.
2. Velg **Utlevering** &gt; **Rapport** i handlingsruten.
3. I **Intrastat-rapport**-dialogboksen angir du følgende felt.

    | Felt | Beskrivelse |
    |-------------------------|-------------------------|
    | Fra dato | Velg startdatoen for rapporten. |
    | Generer fil | Sett dette alternativet til **Ja** for å generere en XML-fil for Intrastat-rapporten. |
    | Filnavn | Angi navnet på XML-filen. |
    | Generer rapport | Sett dette alternativet til **Ja** for å generere en XLSX-fil for Intrastat-rapporten. |
    | Navn på rapportfil | Angi navnet på XLSX-filen. |
    | Retning | Velg **Ankomster** for en rapport om fellesskapsankomster.</br>Velg **Fordelinger** for en rapport om fellesskapsfordelinger. |
    | ID for deklareringen | Dokument-ID-en genereres automatisk og kan oppdateres. |
    | Deklareringstype | Velg **Deklarering** for en opprinnelig deklarering.</br>Velg **Deklareringskorreksjon – erstatning** for en korreksjonsdeklarering som skal erstatte en eksisterende, tidligere sendt opprinnelig deklarering eller rettelsesdeklarering. |
    | Poststed for dokumentopprettelse | Angi verdien som skal skrives ut, i **Miejscowosc**-feltet i Intrastat-deklareringen. |
    | Dato for dokumentopprettelse | Angi verdien som skal skrives ut, i **Deklaracja Data**-feltet i Intrastat-deklareringen. |
    | Dokumentnr. | Angi verdien som skal skrives ut, i **Numer**-feltet i Intrastat-deklareringen. |
    | Dokumentversjon | Angi verdien som skal skrives ut, i **Wersja**-feltet i Intrastat-deklareringen. |

4. Velg **OK** og gå gjennom de genererte rapportene.

## <a name="example"></a>Eksempel

Dette eksemplet viser hvordan du posterer ankomster og fordelinger for Intrastat ved å bruke den juridiske enheten **DEMF**.

### <a name="preliminary-setup"></a>Foreløpig oppsett

Importer siste versjon av følgende ER-konfigurasjoner:

   - Intrastat modell
   - Intrastat-rapport
   - Intrastat (PL)

### <a name="set-up-a-company-address"></a>Definer en bedriftsadresse

1. Gå til **Organisasjonsstyring** > **Global adressebok** > **Adresser** > **Adresseoppsett**.
2. Velg **Ny** i fanen **Poststed**.
3. I feltet **Land/område** velger du **POL**.
4. I feltet **Poststed** angir du **Warszawa**.
5. Velg **Ny** i kategorien **Postnummer**.
6. I feltet **Land/område** velger du **POL**.
7. I feltet **By** velger du **Warszawa**.
8. I feltet **Postnummer** angir du **00-844**.
9. Gå til **Organisasjonsadministrasjon** > **Organisasjon** > **Juridiske enheter**, og velg den juridiske enheten **DEMF**.
10. Velg **Rediger** på hurtigfanen **Adresser**.
11. I feltet **Land/område** velger du **POL**.
12. I feltet **Postnummer** velger du **31-111**.
13. I **Gate**-feltet angir du **Statystyczna 22/1**.
14. I feltet **By** velger du **Warszawa**.
15. Velg **OK**.

## <a name="set-up-a-vat-id-and-an-enterprise-number-code-for-your-company"></a>Definer en mva-ID og en bedriftsnummerkode for firmaet

### <a name="create-registration-types-for-company-codes"></a>Opprett registreringstyper for firmakoder

1. Gå til **Organisasjonsstyring** > **Global adressebok** > **Registreringstyper** > **Registreringstyper**.
2. Velg **Ny** i handlingsruten for å opprette en registreringstype for MVA-ID-en (NIP-koden).
3. I dialogboksen **Angi detaljer for registreringstypen**, **Navn**-feltet, angir du **NIP**.
4. I feltet **Land/område** velger du **POL**.
5. Velg **Opprett**.
6. Velg **Ny** i handlingsruten for å opprette en registreringstype for bedriftsnummeret (Regon-koden).
7. I dialogboksen **Angi detaljer for registreringstypen**, **Navn**-feltet, angir du **Regon**.
8. I feltet **Land/område** velger du **POL**.
9. Velg **Opprett**.

### <a name="match-the-registration-types-with-registration-categories"></a>Samsvar registreringstypene med registreringskategorier

1. Gå til **Organisasjonsstyring** > **Global adressebok** > **Registreringstyper** > **Registreringskategorier**.
2. Velg **Ny** i handlingsruten for å opprette en kobling mellom hver registreringstype du opprettet, og en registreringskategori.

    - For registreringstypen **NIP** velger du registreringskategorien **MVA-ID**.
    - For registreringstypen **Regon** velger du registreringskategorien **Foretaks-ID (COID)**.

### <a name="set-up-a-vat-id-and-an-enterprise-number-for-your-company"></a>Definer en mva-ID og et bedriftsnummer for firmaet

1. Gå til **Organisasjonsstyring** > **Organisasjoner** > **Juridiske enheter**.
2. Velg **DEMF** i rutenettet.
3. I handlingsruten velger du **Registrerings-ID-er**.
4. Velg **Legg til** på hurtigfanen **Registrerings-ID**.
5. Velg **NIP** i **Registreringstype**-feltet.
6. Angi **1234567890** i feltet **Registreringsnummer**.
7. Velg **Legg til**.
8. Velg **Regon** i **Registreringstype**-feltet.
9. Angi **12345678901234** i feltet **Registreringsnummer**.

### <a name="set-up-a-number-sequence-code"></a>Definer en nummerseriekode

1. Gå til **Organisasjonsadministrasjon** > **Nummerserier** > **Nummerserier**.
2. Velg **Nummerserie** i gruppen **Ny** på **Nummerserie**-fanen i handlingsruten.
3. På hurtigfanen **Identifikasjon**, i feltet **Nummerseriekode**, angir du **XML\_fil**.
4. På hurtigfanen **Omfangsparametere**, i feltet **Omfang**, velger du **Selskap**.
5. Velg **DEMF** i **Selskap**-feltet.
6. På hurtigfanen **Segmenter**, i **Lengde**-feltet for **Alfanumerisk**-segmentet, angir du **4**.
7. På hurtigfanen **Generelt** i delen **Oppsett** angir du alternativet **Kontinuerlig** til **Nei**.
8. I **Nummertilordning**-delen, i **Størst**-feltet angir du **9999**.

### <a name="set-up-foreign-trade-parameters"></a>Angi utenrikshandelsparametere

1. Gå til **Avgift** > **Oppsett** > **Utenrikshandel** > **Utenrikshandelsparametere**.
2. I **Intrastat**-fanen i hurtigfanen **Generelt** i **Transaksjonskode**-feltet velger du **11**.
3. I hurtigfanen **Elektronisk rapportering** i feltet **Rapportformatkartlegging** velger du **Intrastat (PL)**.
4. I feltet **Rapportformatkartlegging** velger du **Intrastat-rapport**.
5. På hurtigfanen **Artikkelkodehierarki** må du kontrollere at feltet **Kategorihierarki** er angitt til **Intrastat**.
6. Velg **Ny** i fanen **Land-/områdeegenskaper**.
7. I feltet **Land/område for part** velger du **POL**. Velg deretter **Innenlands** i feltet **Land-/områdetype**.
8. I feltet **Land/område for part** velger du **DEU**. Velg deretter **EU** i feltet **Land-/områdetype**.
9. På **Agent**-fanen, på hurtigfanen **Agent**, i delen **Mva**, i feltet **Avgiftsfritaksnummer**, angir du **420000**.
10. På fanen **Kontakt** i feltet **Navn** angir du **Manish Chopra**.
11. I **Telefon**-feltet angir du **425-555-5068**.
12. I **Faksnummer**-feltet angir du **425-555-5049**.
13. I **E-post**-feltet angir du **manishc@contoso.com**.
14. På **Nummerserier**-fanen, i feltet **Nummerseriekode** for referansen **XML-filnummer**, velger du **XML\_fil**.

### <a name="set-up-product-information"></a>Definer produktinformasjon

1. Gå til **Behandling av produktinformasjon** > **Produkter** > **Frigitte** **produkter**.
2. Velg **D0001** i rutenettet.
3. Velg **100 200 30** i hurtigfanen **Utenrikshandel** i **Intrastat**-delen i feltet **Artikkel**.
4. Angi **2** i **Nettovekt**-feltet i hurtigfanen **Behandle lager** i delen **Vektmålinger**.
5. Velg **Lagre** i handlingsruten.
6. Velg **D0003** i rutenettet.
7. Velg **100 200 30** i hurtigfanen **Utenrikshandel** i **Intrastat**-delen i feltet **Artikkel**.
8. I delen **Opprinnelse** i feltet **Land/område**-felt velger du **DEU**.
9. Angi **5** i **Nettovekt**-feltet i hurtigfanen **Behandle lager** i delen **Vektmålinger**.
10. Velg **Lagre** i handlingsruten.

### <a name="change-the-site-address"></a>Endre områdeadressen

1. Gå til **Lagerstyring** > **Oppsett** > **Lager** > **Steder**.
2. Velg **1** i rutenettet.
3. Velg **Rediger** på hurtigfanen **Adresser**.
4. I dialogboksen **Rediger adresse**, i feltet **Land/område**, velger du **POL**.
5. Velg **OK**.

### <a name="set-up-a-transport-method"></a>Definer en transportmetode

1. Opprett en transportmetode.

    1. Gå til **Avgift** > **Oppsett** > **Utenrikshandel** > **Transportmetode**.
    2. Velg **Ny** i handlingsruten.
    3. Angi **3** i **Transport**-feltet.
    4. I **Beskrivelse**-feltet angir du **Veitransport**.

2. Tilordne den nye transportmåten til en leveringsmåte. På denne måten definerer du standardverdiene som brukes for transportmåten når den tilhørende leveringsmåten er valgt.

    1. Gå til **Innkjøp og leverandører** > **Oppsett** > **Distribusjon** > **Leveringsmåter**.
    2. Velg **10** i rutenettet.
    3. På hurtigfanen **Utenrikshandel**, i **Transport**-feltet, velger du **3**.

3. Velg standard leveringsmåte for en kunde.

    1. Gå til **Kunder** > **Kunder** > **Alle kunder**.
    2. Velg **DE-016** i rutenettet.
    3. På hurtigfanen **Faktura og levering**, feltet **Leveringsmåte** velger du **10**.

4. Velg standard leveringsmåte for en leverandør.

    1. Gå til **Leverandører** > **Leverandører** > **Alle leverandører**.
    2. Velg **DE-001** i rutenettet.
    3. På hurtigfanen **Faktura og levering**, feltet **Leveringsmåte** velger du **10**.

### <a name="set-up-codes-for-terms-of-delivery"></a>Definer koder for leveringsbetingelser

1. Definer en Intrastat-kode for leveringsbetingelsene.

    1. Gå til **Innkjøp og leverandører** > **Oppsett** > **Distribusjon** > **Leveringsbetingelser**.
    2. Velg **CIF** i rutenettet.
    3. På hurtigfanen **Generelt**, i feltet **Intrastat-kode**, angir du **CIF**.

2. Velg standard leveringsbetingelser for en kunde.

    1. Gå til **Kunder** > **Kunder** > **Alle kunder**.
    2. Velg **DE-016** i rutenettet.
    3. På hurtigfanen **Faktura og levering**, feltet **Leveringsbetingelser** velger du **CIF**.

3. Velg standard leveringsbetingelser for en leverandør.

    1. Gå til **Leverandører** > **Leverandører** > **Alle leverandører**.
    2. Velg **DE-001** i rutenettet.
    3. På hurtigfanen **Faktura og levering**, feltet **Leveringsbetingelser** velger du **CIF**.

### <a name="verify-an-eu-customers-tax-exempt-number-code"></a>Bekreft en EU-kundes avgiftsfritaksnummerkode

1. Gå til **Kunder** > **Kunder** > **Alle kunder**.
2. Velg **DE-016** i rutenettet.
3. På hurtigfanen **Faktura og levering**, i **Merverdiavgift**-delen, bekrefter du at feltet **Avgiftsfritaksnummer** er angitt til **DE9012**.

### <a name="create-a-sales-order-with-an-eu-customer"></a>Opprett en salgsordre med en EU-kunde

1. Gå til **Kunder** > **Ordrer** > **Alle salgsordrer**.
2. Velg **Ny** i handlingsruten.
3. I dialogboksen **Opprett salgsordre**, i på **Kunde**-hurtigfanen i **Kunde**-delen i feltet **Kundekonto** velger du **DE-016**.
4. Velg **1** i **Område**-feltet i delen **Lagerdimensjoner**-delen i hurtigfanen **Generelt**.
5. I **Lager**-feltet velger du **11**.
6. På **Adresse**-fanen bekrefter du at **Adresse**-feltet er angitt til **Teichgasse 12, Kiel, 24103, DEU**, siden kunden er fra Tyskland.
7. Velg **OK**.
8. På **Hode**-fanen, på **Levering**-hurtigfanen, bekrefter du at feltet **Leveringsbetingelser** er angitt til **CIF**, og at feltet **Leveringsmåte** er angitt til **10**.
9. På fanen **Linjer** på hurtigfanen **Salgsordrelinjer** i **Varenummer**-feltet velger du **D0001**. I feltet **Antall** angi **8**.
10. På hurtigfanen **Linjedetaljer**, på fanen **Utenrikshandel**, bekrefter du at feltet **Transaksjonskode** er angitt til **11**, feltet **Artikkel** er angitt til **100 200 30**, og feltet **Opprinnelsesland/-område** er angitt til **POL**.
11. Velg **Lagre** i handlingsruten.
12. I handlingsruten, på **Faktura**-fanen i **Generer**-gruppen, velger du **Faktura**.
13. I dialogboksen **Postering av faktura** i hurtigfanen **Parametere** i **Parameter**-delen i **Antall**-feltet velger du **Alle**.
14. På hurtigfanen **Oppsett**, i feltet **Salgsdato**, velger du **10/18/2021** (18. oktober 2021).
15. Klikk på **OK** for å postere fakturaen.

### <a name="transfer-the-transaction-to-the-intrastat-journal-and-review-the-result"></a>Overfør transaksjonen til Intrastat-journalen, og gå gjennom resultatet

1. Gå til **Avgift** > **Deklareringer** > **Utenrikshandel** > **Intrastat**.
2. I handlingsruten velger du **Overfør**.
3. I dialogboksen **Intrastat (overføring)** i **Parametere**-delen angir du **Kundefaktura**-alternativet til **Ja**.
4. Velg **Filter**.
5. Merk den første linjen i fanen **Område** i dialogboksen **Intrastat-filter**, og bekreft at **Felt**-feltet er satt til **Dato**.
6. Velg gjeldende dato i **Kriterier**-feltet.
7. Velg **OK** for å lukke dialogboksen **Intrastat-filter**.
8. Velg **OK** for å lukke dialogboksen **Intrastat (overfør)** og se gjennom resultatet. Linjen representerer salgsordre du opprettet tidligere.

    ![Linjen som representerer salgsordre på Intrastat-siden](media/intrastat_pl_1.png)

9. Velg transaksjonslinjen, og velg deretter fanen **Generelt** for å vise flere detaljer.

    ![Salgsordredetaljer i fanen Generelt på Intrastat-siden](media/intrastat_pl_2.png)

10. Velg **Utlevering** > **Rapport** i handlingsruten.
11. I dialogboksen **Intrastat-rapport**, på hurtigfanen **Parametere**, i **Dato**-delen, i feltet **Fra dato**, velger du den første dagen i den gjeldende måneden.
12. I delen **Eksportalternativer** angir du alternativet **Generer** **fil** til **Ja**. I **Filnavn**-feltet angir du deretter det obligatoriske navnet.
13. Sett alternativet **Generer rapport** til **Ja**. I feltet **Navn på rapportfil** angir du deretter det obligatoriske navnet.
14. I **Retning**-feltet velger du **Fordelinger**.
15. I delen **Filformattilordning** bekrefter du at **Deklareringstype**-feltet er satt til **Deklarering**.
16. I feltet **Poststed for dokumentopprettelse** angir du **Krakow**.
17. I feltet **Dato for dokumentopprettelse** velger du **10/19/2021** (19. oktober 2021).
18. I feltet **Dokumentnr.** angir du **11**.
19. I feltet **Dokumentversjon** angir du **22**.
20. Velg **OK** og gå gjennom rapporten i XML-format som genereres. Tabellen nedenfor viser verdiene i eksempelrapporten.

    <table>
    <tbody>
    <tr>
    <td>
    <p><strong>Feltnavn</strong></p>
    </td>
    <td>
    <p><strong>Feltbeskrivelse</strong></p>
    </td>
    <td>
    <p><strong>Verdi</strong></p>
    </td>
    </tr>
    <tr>
    <td colspan="3">
    <p><strong>Informasjon om dokumentet</strong></p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Deklaracja Data</p>
    </td>
    <td>
    <p>Datoen da dokumentet ble opprettet.</p>
    </td>
    <td>
    <p>2021-10-19</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Miejscowosc</p>
    </td>
    <td>
    <p>Poststedet der dokumentet ble opprettet.</p>
    </td>
    <td>
    <p>Krakow</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>LacznaLiczbaPozycji</p>
    </td>
    <td>
    <p>Totalt antall varer.</p>
    </td>
    <td>
    <p>1</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>LacznaWartoscStatystyczna</p>
    </td>
    <td>
    <p>Den totale statistiske verdien.</p>
    </td>
    <td>
    <p>2632</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>LacznaWartoscFaktur</p>
    </td>
    <td>
    <p>Den totale fakturaverdien.</p>
    </td>
    <td>
    <p>2632</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>UC</p>
    </td>
    <td>
    <p>Enhetskoden.</p>
    </td>
    <td>
    <p>420000</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Rodzaj</p>
    </td>
    <td>
    <p>Typen deklarering.</p>
    </td>
    <td>
    <p>D</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Wersja</p>
    </td>
    <td>
    <p>Dokumentversjonen.</p>
    </td>
    <td>
    <p>22</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Numer</p>
    </td>
    <td>
    <p>Dokumentnummeret</p>
    </td>
    <td>
    <p>11</p>
    </td>
    </tr>
    <tr>
    <td width="191">
    <p>Miesiac</p>
    </td>
    <td width="330">
    <p>Referansemåneden.</p>
    </td>
    <td>
    <p>10</p>
    </td>
    </tr>
    <tr>
    <td width="191">
    <p>Rok</p>
    </td>
    <td width="330">
    <p>Referanseåret.</p>
    </td>
    <td>
    <p>2021</p>
    </td>
    </tr>
    <tr>
    <td width="191">
    <p>Typ</p>
    </td>
    <td width="330">
    <p>Rapportretningen.</p>
    </td>
    <td>
    <p>O</p>
    </td>
    </tr>
    <tr>
    <td width="191">
    <p>NrWlasny</p>
    </td>
    <td width="330">
    <p>ID-en for deklareringen.</p>
    </td>
    <td>
    <p>21ISTDEMF-0001</p>
    </td>
    </tr>
    <tr>
    <td colspan="3">
    <p><strong>Informasjon om selskapet</strong></p>
    </td>
    </tr>
    <tr>
    <td width="191">
    <p>Miejscowosc</p>
    </td>
    <td width="330">
    <p>Poststedet der firmaet holder til.</p>
    </td>
    <td>
    <p>Warszawa</p>
    </td>
    </tr>
    <tr>
    <td width="191">
    <p>Regon</p>
    </td>
    <td width="330">
    <p>Selskapets Regon-kode.</p>
    </td>
    <td>
    <p>12345678901234</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Nip</p>
    </td>
    <td>
    <p>Selskapets NIP-kode.</p>
    </td>
    <td>
    <p>1234567890</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>KodPocztowy</p>
    </td>
    <td>
    <p>Selskapets postnummer.</p>
    </td>
    <td>
    <p>31-111</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>UlicaNumer</p>
    </td>
    <td>
    <p>Gaten der firmaet holder til.</p>
    </td>
    <td>
    <p>Statystyczna 22/1</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Nazwa</p>
    </td>
    <td>
    <p>Navnet på firmaet.</p>
    </td>
    <td>
    <p>Contoso Entertainment System Tyskland</p>
    </td>
    </tr>
    <tr>
    <td colspan="3">
    <p><strong>Informasjon om varen</strong></p>
    </td>
    </tr>
    <tr>
    <td>
    <p>WartoscStatystyczna</p>
    </td>
    <td>
    <p>Den statistiske verdien.</p>
    </td>
    <td>
    <p>2632</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>WartoscFaktury</p>
    </td>
    <td>
    <p>Fakturaverdien.</p>
    </td>
    <td>
    <p>2632</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>MasaNetto</p>
    </td>
    <td>
    <p>Nettovekten.</p>
    </td>
    <td>
    <p>16</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>IdKontrahenta</p>
    </td>
    <td>
    <p>Kundens mva-nummer.</p>
    </td>
    <td>
    <p>DE9012</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>KodTowarowy</p>
    </td>
    <td>
    <p>Artikkelkoden.</p>
    </td>
    <td>
    <p>10020030</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>RodzajTransakcji</p>
    </td>
    <td>
    <p>Transaksjonskoden.</p>
    </td>
    <td>
    <p>11</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>WarunkiDostawy</p>
    </td>
    <td>
    <p>Betingelsene for leveringsmåten.</p>
    </td>
    <td>
    <p>KFF</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>KrajPochodzeniaWysylki</p>
    </td>
    <td>
    <p>Koden for landet eller området for fordeling/mål.</p>
    </td>
    <td>
    <p>DE</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>OpisTowaru</p>
    </td>
    <td>
    <p>En beskrivelse av artiklene.</p>
    </td>
    <td>
    <p>Maskinvare</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>PozId</p>
    </td>
    <td>
    <p>Varenummeret.</p>
    </td>
    <td>
    <p>1</p>
    </td>
    </tr>
    <tr>
    <td colspan="3">
    <p><strong>Kontaktinformasjon</strong></p>
    </td>
    </tr>
    <tr>
    <td>
    <p>E-post</p>
    </td>
    <td>
    <p>Avsenderens e-postadresse.</p>
    </td>
    <td>
    <p>manishc@contoso.com</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Faks</p>
    </td>
    <td>
    <p>Avsenderens faksnummer.</p>
    </td>
    <td>
    <p>425-555-5049</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Telefon</p>
    </td>
    <td>
    <p>Avsenderens telefonnummer.</p>
    </td>
    <td>
    <p>425-555-5068</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>NazwiskoImie</p>
    </td>
    <td>
    <p>Avsenderens navn.</p>
    </td>
    <td>
    <p>Manish Chopra</p>
    </td>
    </tr>
    </tbody>
    </table>

21. Gå gjennom rapporten i Excel-format som genereres.

    ![Intrastat-rapport ved fordelinger](media/intrastat_pl_3.png)

### <a name="create-a-purchase-order"></a>Opprette en bestilling

1. Gå til **Leverandører** > **Bestillinger** > **Alle bestillinger**.
2. Velg **Ny** i handlingsruten.
3. I dialogboksen **Opprett bestilling**, i **Leverandørkonto**-feltet, velger du **DE-001**.
4. I **Område**-feltet velger du **1**.
5. I **Lager**-feltet velger du **11**.
6. Velg **OK**.
7. På **Hode**-fanen, på **Levering**-hurtigfanen, bekrefter du at feltet **Leveringsmåte** er angitt til **10**, og at feltet **Leveringsbetingelser** er angitt til **CIF**.
8. På fanen **Linjer** på hurtigfanen **Bestillingslinjer** i **Varenummer**-feltet velger du **D0003**. I feltet **Antall** angi **6**.
9. På hurtigfanen **Linjedetaljer**, på fanen **Utenrikshandel**, bekrefter du at feltet **Transaksjonskode** er angitt til **11**, **Transport**-feltet er angitt til **3**, **Artikkel**-feltet er angitt til **100 200 30**, og feltet **Opprinnelsesland/-område** er angitt til **DEU**.
10. I handlingsruten på fanen **Bestilling** i gruppen **Handlinger** velger du **Bekreft**.
11. I handlingsruten, på **Faktura**-fanen i **Generer**-gruppen, velger du **Faktura**.
12. I handlingsruten velger du **Standard fra**, og deretter, i feltet **Standardantall for linjer** velger du **Bestilt antall**. Velg deretter **OK**.
13. På hurtigfanen **Leverandørfakturahode**, i delen **Fakturaidentifikasjon**, i **Nummer**-feltet velger du **00010**.
14. I delen **Fakturadatoer**, i feltet **Fakturadato**, velger du dagens dato. Denne datoen brukes til Intrastat-overføring.
15. I feltet **Dato for dokumentmottak** velger du **10/18/2021** (18. oktober 2021).
16. Velg **Poster** i handlingsruten for å postere fakturaen.

### <a name="create-an-intrastat-declaration-for-arrivals"></a>Opprett en Intrastat-deklarering for ankomster

1. Gå til **Avgift** > **Deklareringer** > **Utenrikshandel** > **Intrastat**.
2. I handlingsruten velger du **Overfør**.
3. I dialogboksen **Intrastat (overfør)** setter du alternativet **Leverandørfaktura** til **Ja**.
4. Velg **OK** for å overføre transaksjonene, og gå deretter gjennom Intrastat-journalen.

    ![Linjen som representerer bestillingen på Intrastat-siden](media/intrastat_pl_4.png)

5. Gå gjennom informasjonen på **Generelt**-fanen for bestillingen.

    ![Bestillingsdetaljer på fanen Generelt på Intrastat-siden](media/intrastat_pl_5.png)

6. Velg **Utlevering** > **Rapport** i handlingsruten.
7. I dialogboksen **Intrastat-rapport**, på hurtigfanen **Parametere**, i **Dato**-delen, i feltet **Fra dato**, velger du den første dagen i den gjeldende måneden.
8. I delen **Eksportalternativer** angir du alternativet **Generer** **fil** til **Ja**. I **Filnavn**-feltet angir du deretter det obligatoriske navnet.
9. Sett alternativet **Generer rapport** til **Ja**. I feltet **Navn på rapportfil** angir du deretter det obligatoriske navnet.
10. Velg **Ankomster** i feltet **Retning**.
11. I delen **Filformattilordning** bekrefter du at **Deklareringstype**-feltet er satt til **Deklarering**.
12. I feltet **Poststed for dokumentopprettelse** angir du **Krakow**.
13. I feltet **Dato for dokumentopprettelse** velger du **10/19/2021** (19. oktober 2021).
14. I feltet **Dokumentnr.** angir du **11**.
15. I feltet **Dokumentversjon** angir du **22**.
16. Velg **OK** og gå gjennom rapporten i XML-format som genereres. Tabellen nedenfor viser verdiene i eksempelrapporten.

    <table>
    <tbody>
    <tr>
    <td>
    <p><strong>Feltnavn</strong></p>
    </td>
    <td>
    <p><strong>Feltbeskrivelse</strong></p>
    </td>
    <td>
    <p><strong>Verdi</strong></p>
    </td>
    </tr>
    <tr>
    <td colspan="3">
    <p align=center><strong>Informasjon om dokumentet</strong></p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Deklaracja Data</p>
    </td>
    <td>
    <p>Datoen da dokumentet ble opprettet.</p>
    </td>
    <td>
    <p>2021-10-19</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Miejscowosc</p>
    </td>
    <td>
    <p>Poststedet der dokumentet ble opprettet.</p>
    </td>
    <td>
    <p>Krakow</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>LacznaLiczbaPozycji</p>
    </td>
    <td>
    <p>Totalt antall varer.</p>
    </td>
    <td>
    <p>1</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>LacznaWartoscStatystyczna</p>
    </td>
    <td>
    <p>Den totale statistiske verdien.</p>
    </td>
    <td>
    <p>965</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>LacznaWartoscFaktur</p>
    </td>
    <td>
    <p>Den totale fakturaverdien.</p>
    </td>
    <td>
    <p>965</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>UC</p>
    </td>
    <td>
    <p>Enhetskoden.</p>
    </td>
    <td>
    <p>420000</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Rodzaj</p>
    </td>
    <td>
    <p>Typen deklarering.</p>
    </td>
    <td>
    <p>D</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Wersja</p>
    </td>
    <td>
    <p>Dokumentversjonen.</p>
    </td>
    <td>
    <p>22</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Numer</p>
    </td>
    <td>
    <p>Dokumentnummeret</p>
    </td>
    <td>
    <p>11</p>
    </td>
    </tr>
    <tr>
    <td width="191">
    <p>Miesiac</p>
    </td>
    <td width="332">
    <p>Referansemåneden.</p>
    </td>
    <td>
    <p>10</p>
    </td>
    </tr>
    <tr>
    <td width="191">
    <p>Rok</p>
    </td>
    <td width="332">
    <p>Referanseåret.</p>
    </td>
    <td>
    <p>2021</p>
    </td>
    </tr>
    <tr>
    <td width="191">
    <p>Typ</p>
    </td>
    <td width="332">
    <p>Rapportretningen.</p>
    </td>
    <td>
    <p>P</p>
    </td>
    </tr>
    <tr>
    <td width="191">
    <p>NrWlasny</p>
    </td>
    <td width="332">
    <p>ID-en for deklareringen.</p>
    </td>
    <td>
    <p>21ISTDEMF-0002</p>
    </td>
    </tr>
    <tr>
    <td colspan="3">
    <p align=center><strong>Informasjon om selskapet</strong></p>
    </td>
    </tr>
    <tr>
    <td width="191">
    <p>Miejscowosc</p>
    </td>
    <td width="332">
    <p>Poststedet der firmaet holder til.</p>
    </td>
    <td>
    <p>Warszawa</p>
    </td>
    </tr>
    <tr>
    <td width="191">
    <p>Regon</p>
    </td>
    <td width="332">
    <p>Selskapets Regon-kode.</p>
    </td>
    <td>
    <p>12345678901234</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Nip</p>
    </td>
    <td>
    <p>Selskapets NIP-kode.</p>
    </td>
    <td>
    <p>1234567890</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>KodPocztowy</p>
    </td>
    <td>
    <p>Selskapets postnummer.</p>
    </td>
    <td>
    <p>31-111</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>UlicaNumer</p>
    </td>
    <td>
    <p>Gaten der firmaet holder til.</p>
    </td>
    <td>
    <p>Statystyczna 22/1</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Nazwa</p>
    </td>
    <td>
    <p>Navnet på firmaet.</p>
    </td>
    <td>
    <p>Contoso Entertainment System Tyskland</p>
    </td>
    </tr>
    <tr>
    <td colspan="3">
    <p align=center><strong>Informasjon om varen</strong></p>
    </td>
    </tr>
    <tr>
    <td>
    <p>WartoscStatystyczna</p>
    </td>
    <td>
    <p>Den statistiske verdien.</p>
    </td>
    <td>
    <p>965</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>WartoscFaktury</p>
    </td>
    <td>
    <p>Fakturaverdien.</p>
    </td>
    <td>
    <p>965</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>MasaNetto</p>
    </td>
    <td>
    <p>Nettovekten.</p>
    </td>
    <td>
    <p>30</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>KrajPochodzenia</p>
    </td>
    <td>
    <p>Koden for opprinnelseslandet eller -området.</p>
    </td>
    <td>
    <p>DE</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>RodzajTransportu</p>
    </td>
    <td>
    <p>Modus for transportkoden.</p>
    </td>
    <td>
    <p>3</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>KodTowarowy</p>
    </td>
    <td>
    <p>Artikkelkoden.</p>
    </td>
    <td>
    <p>10020030</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>RodzajTransakcji</p>
    </td>
    <td>
    <p>Transaksjonskoden.</p>
    </td>
    <td>
    <p>11</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>WarunkiDostawy</p>
    </td>
    <td>
    <p>Betingelsene for leveringsmåten.</p>
    </td>
    <td>
    <p>KFF</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>KrajPochodzeniaWysylki</p>
    </td>
    <td>
    <p>Koden for landet eller området for fordeling/mål.</p>
    </td>
    <td>
    <p>DE</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>OpisTowaru</p>
    </td>
    <td>
    <p>En beskrivelse av artiklene.</p>
    </td>
    <td>
    <p>Maskinvare</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>PozId</p>
    </td>
    <td>
    <p>Varenummeret.</p>
    </td>
    <td>
    <p>1</p>
    </td>
    </tr>
    <tr>
    <td colspan="3">
    <p align=center><strong>Kontaktinformasjon</strong></p>
    </td>
    </tr>
    <tr>
    <td>
    <p>E-post</p>
    </td>
    <td>
    <p>Avsenderens e-postadresse.</p>
    </td>
    <td>
    <p>manishc@contoso.com</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Faks</p>
    </td>
    <td>
    <p>Avsenderens faksnummer.</p>
    </td>
    <td>
    <p>425-555-5049</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Telefon</p>
    </td>
    <td>
    <p>Avsenderens telefonnummer.</p>
    </td>
    <td>
    <p>425-555-5068</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>NazwiskoImie</p>
    </td>
    <td>
    <p>Avsenderens navn.</p>
    </td>
    <td>
    <p>Manish Chopra</p>
    </td>
    </tr>
    </tbody>
    </table>

17. Gå gjennom rapporten i Excel-format som genereres.

    ![Intrastat-rapport ved ankomster](media/intrastat_pl_6.png)
