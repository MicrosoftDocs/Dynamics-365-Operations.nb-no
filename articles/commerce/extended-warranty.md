---
title: Opprette og konfigurere utvidede garantier
description: Denne artikkelen dekker utvidede garantier og beskriver hvordan du oppretter og konfigurerer dem i Microsoft Dynamics 365 Commerce.
author: josaw1
ms.date: 06/08/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.search.industry: ''
ms.openlocfilehash: 3754de54763be52c9090596fac0e170b0c5fc520
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/12/2022
ms.locfileid: "9268375"
---
# <a name="create-and-configure-extended-warranties"></a>Opprette og konfigurere utvidede garantier

[!include [banner](includes/banner.md)]

Denne artikkelen dekker utvidede garantier og beskriver hvordan du oppretter og konfigurerer dem i Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Oversikt

Kunder velger i økende grad utvidet kundestøtte og tjenester når de kjøper produkter, spesielt forbruksprodukter som selges til premium price point, for eksempel telefoner og datamaskiner. Ved å gi utvidede garantier for innkjøp kan forhandlere hjelpe til med å bygge kundelojalitet. Utvidede garantier gir kundene beskjed hvor de kan gå for å få service og kundestøtte. De kan derfor være sikre på problemene vil bli behandlet på en effektiv måte.

Utvidede garantier kan selges til kunder i en detaljhandelskanal i løpet av det opprinnelige produktinnkjøpet. De kan også selges i en begrenset periode etter det opprinnelige kjøpet.

### <a name="warranty-item-setup"></a>Oppsett av garantivare

Dynamics 365 Commerce inneholder funksjoner som gjør det mulig å opprette en garantivare og angi attributter for den. Disse attributtene omfatter tilknytningen mellom et produkt og en garantivare, prisen på garantien og varigheten til garantien. Når en garantivare konfigureres og frigis til organisasjonsenheten, kan en forhandler selge garantier gjennom Modern Point of Sale (MPOS), nettbutikker og andre detaljhandelskanaler.

### <a name="warranty-item-sales"></a>Salg av garantivare

Utvidede garantier selges i en detaljhandelskanal i løpet av det opprinnelige produktinnkjøpet. De kan også selges i en begrenset periode etter det opprinnelige kjøpet.

På salgsstedet (POS) blir selgeren bedt om å legge til en utvidet garanti når et tilknyttet produkt legges til i en kundeshandlevogn. Derfor presenteres en kryssalgsmulighet til salgsmedarbeidere som en del av salgsflyten.

Kunder kan også returnere senere og kjøpe en utvidet garanti for et produkt som de tidligere har kjøpt. I disse tilfellene kan en salgsmedarbeider slå opp den opprinnelige transaksjonen og selge tilknyttede utvidede garantivarer til kunden.

### <a name="warranty-terminology"></a>Garantiterminologi

Følgende tabell definerer noen garantirelaterte betingelser.

| Semester | beskrivelse |
|------------------------------|--------------|
| Utvidet garanti / garanti | En *utvidet garanti* viser til en serviceavtale eller kontrakt som gir kunder en langsiktig garanti. Den utvidede garantien omfatter tilleggstjenesten med å erstatte eller reparere varer i dekningsperioden på den utvidede garantien. |
| Produsentens garanti | En *produsentgaranti* (også kalt *begrenset garanti*) er garantien kunder mottar når de kjøper et produkt. Her er noen kjennetegn ved en produsentgaranti:<ul><li>Garantikostnadene er inkludert i kostnaden til produktet. Kunder trenger ikke betale et tilleggsbeløp for en produsentgaranti.</li><li>Avhengig av produktkategorien varer en produsentgaranti vanligvis 30 dager, seks måneder eller ett år. (For de fleste typer forbrukerelektronikk varer garantien ett år).</li><li>Garantien dekker eventuelle defekter som forårsakes av mekaniske eller elektriske feil. Dekning er begrenset, og den inkluderer ikke ulykkesskade på det innkjøpte produktet. Kunder som vil beskytte produktene de kjøper, mot dagligdagse skader, bør investere i en utvidet garanti. Utvidede garantier varer to til ti år, avhengig av produktkategorien. De har også bredere dekning og dekker daglige uhell, for eksempel fall, søl og flekker.</li></ul> |
| Garantivare | En *garantivare* er en utvidet garantivare som selges for en garantiberettiget vare. Et eksempel er en 2-åring ulykkesbeskyttelsesplan for bærbare datamaskiner. |
| Garantiberettiget vare | En *garantiberettiget vare* er et serialisert produkt som en garanti er solgt for. En bærbar datamaskin er for eksempel en garantiberettigede vare som det selges toårige og treårige utvidede garantier for. |
| Garantigruppe | En *garantigruppe* er en relasjon mellom garantivarer og garantiberettigede varer. Salgsstedet bruker garantigrupper til å bestemme hvilke garantivarer salgsmedarbeidere bør spørres om å legge til når en garantiberettiget vare legges til i en kundes handlevogn. |
| Garantipolicy | En *garantipolicy* er en enhet som opprettes i Commerce når en garantipolicy selges. En garantipolicy omfatter informasjon som start- og sluttdatoer for den innkjøpte garantivaren, vilkårene og betingelsene og serienummeret til garantiproduktet. Garantipolicy numre kan deles med kunder, slik at de har en referanse for den utvidede garantien de kjøpte. |

## <a name="create-a-warranty-item"></a>Opprette en garantivare

Følg denne fremgangsmåten for å opprette en garantivare i Commerce.

1. Gå til **Detaljhandel og handel \> Produkter og kategorier \> Produkter**.
1. Velg **Ny** for å opprette en garantivare.
1. I dialogboksen **Nytt produkt**, i feltet **Produkttype**, velger du **Service**.
1. Velg **Produkt** i feltet **Produktets undertype**.
1. Velg **Service** i feltet **Produktservicetype**.
1. I **Produktnavn**-feltet angir du produktnavnet.
1. I **Detaljhandelkategori** velger du en verdi i rullegardindialogboksen, og deretter velger du **OK**.
1. I **Produktnummer** angir du produktnavnet.
1. Velg **OK**.
1. På siden **Produktdetaljer** på hurtigfanen **Garanti** angir du feltene **Tidslengde** og **Tidsenhet**.

    | Feltnavn | Verdi | beskrivelse |
    |------------|-------|-------------|
    | Tidsenhet | **Dag(er)**, **Uke(r)**, **Måned(er)** eller **År** | Dette feltet angir tidsenheten som brukes for garantien. |
    | Tidsrom | En positiv heltallsverdi | Dette feltet angir varigheten av garantien i den valgte tidsenheten. |

    For en garanti på to år kan du for eksempel sette **Tidsenhet**-feltet til **År** og feltet **Tidslengde** til **2**. Du kan også sette feltet **Tidsenhet** til **Måned(er)** og feltet **Tidslengde** til **24**, som vist i følgende illustrasjon.

    ![Siden produktdetaljer for en garantivare.](./media/ew-time-properties.png)

1. Velg **Lagre** for å lagre garantivaren.
1. Frigi garantiproduktet til firmaet slik at det kan selges. Hvis du vil ha mer informasjon, kan du se [Definere detaljhandelsprodukter](set-up-retail-products.md).
1. På siden **Detaljer om frigitt produkt**, på hurtigfanen **Garanti**, angir du feltene **Prisområdebase**, **Nedre grense** og **Øvre grense**.

    | Feltnavn | Verdi | beskrivelse |
    |------------|-------|-------------|
    | Grunnlag for prisområde | **Ingen**, **Basispris** eller **Salgspris** | <ul><li>**Ingen** – Verdiene for **Nedre grense** og **Øvre grense** for prisområder er ikke gjeldende.</li><li>**Basispris** – En gitt garanti vil være gjeldende hvis basisprisen (det vil si prisen uten rabatter) for den garantiberettigede varen er mellom verdiene for **Nedre grense** og **Øvre grense** som er angitt her, basert på prisen på den garantiberettigede varen.</li><li>**Salgspris** – Denne verdien er reservert for fremtidig bruk.</li></ul> |
    | Nedre grense, Øvre grense | En positiv heltallsverdi | Disse feltene definerer den øvre og nedre prisgrensen for den garantiberettigede varen, og hvordan den gjeldende garantivaren gjelder for den garantiberettigede varen. Disse grensene kan være basert på basisprisen for den garantiberettigede varen (også kalt produsentens foreslåtte utsalgspris \[MSRP\]). Hvis feltet **Prisområdebase** er satt til **Basispris**, vil bare en garantiberettiget vare (produkt) som har en basispris mellom verdiene for **Nedre grense** og **Øvre grense**, utløse en ledetekst for å legge til en garantivare på salgsstedet. |

    Følgende illustrasjon viser for eksempel at feltet **Prisområdebase** er satt til **Basispris**, feltet **Nedre grense** er satt til USD 500, og **Øvre grense**-feltet er satt til USD 1000.
    
    ![Siden Detaljer om frigitt produkt for en garantivare.](./media/ew-release-product-details.png)

1. Plasser garantivaren i kanalen der den skal selges. Hvis du vil ha mer informasjon, kan du se [Definere sortimenter](set-up-assortments.md).

### <a name="example"></a>Eksempel

Et garantiberettiget vare (produkt) for bærbar datamaskin har basisprisen $999, og det finnes to garantivarer for bærbar datamaskin:

- Garanti\_1 har en nedre grense på USD 500 og en øvre grense på USD 1000, og feltet **Prisområdebase** settes til **Basispris**.
- Garanti\_2 har en nedre grense på USD 1001 og øvre grense på USD 2000, og feltet **Prisområdebase** settes til **Basispris**.

I dette tilfellet vises en ledetekst for å legge til garanti\_1 på salgsstedet når en garantiberettiget vare for en bærbar datamaskin legges til i kundens handlevogn, fordi prisen på den bærbare datamaskinen er mellom den nedre og øvre grensen for garanti\_1.

> [!NOTE]
> Hvis du for eksempel vil at det skal vises en ledetekst for både Garanti\_1 og Garanti\_2, uavhengig av prisen på den garantiberettigede varen, setter du feltet **Prisområdebase** til **Ingen**.

## <a name="configure-channel-specific-settings"></a>Konfigurere kanalspesifikke innstillinger

Med kanalspesifikke innstillinger kan du angi om en ledetekst om å legge til en garantivare skal vises på salgsstedet når en garantiberettiget vare legges til i en kundeshandlevogn.

Følg denne fremgangsmåten for å konfigurere kanalspesifikk innstilling i Commerce.

1. Gå til **Detaljhandel og handel \> Produkter og kategoriers \> Garanti \> Garantiinnstillinger**.
1. Følg et av disse trinnene i fanen **Kanalspesifikke** i kolonnen **Be om garanti** for kanalen:

    - Merk av i avmerkingsboksen hvis det skal vises en ledetekst for garantivare på salgsstedet når den tilhørende garantiberettigede varen blir lagt til i handlekurven.
    - Fjern merket i avmerkingsboksen hvis det ikke skal vises en ledetekst for garantivare på salgsstedet når den tilhørende garantiberettigede varen blir lagt til i handlekurven.

1. Kjør **1070**-jobben for å synkronisere dataene til kanalen.

## <a name="configure-a-number-sequence-for-warranty-policies"></a>Konfigurere en nummerserie for garantipolicyer

Hver garantipolicy identifiseres unikt ved hjelp av et garantipolicynummer som genereres av en nummerserie. Hvis du vil ha mer informasjon om nummerserier, kan du se [Oversikt over nummerserier](../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md).

Følg denne fremgangsmåten for å konfigurere en nummerserie for garantipolicyer i Commerce.

1. Gå til **Detaljhandel og handel \> Produkter og kategoriers \> Garanti \> Garantiinnstillinger**.
1. I fanen **Nummerserie** i raden for **Garantipolicy**-referanse angir eller velger du en verdi i feltet **Nummerseriekode**.

## <a name="set-up-a-warranty-group"></a>Konfigurere en garantigruppe

En garantigruppe er en relasjon mellom garantivarer og garantiberettigede varer. Salgsstedet bruker garantigrupper til å bestemme hvilke garantivarer salgsmedarbeidere bør spørres om å legge til når en garantiberettiget vare legges til i en kundes handlevogn.

Hvis du vil konfigurere en garantigruppe i Commerce, følger du disse trinnene.

1. Gå til **Detaljhandel og handel \> Produkter og kategoriers \> Garanti \> Garantigrupper**.
1. Velg **Ny** for å opprette en garantigruppe.
1. I **Navn**-feltet angir du et unikt navn på den nye gruppen.
1. Skriv inn en beskrivelse av gruppen i hurtigfanen **Generelt** i feltet **Beskrivelse**.
1. I hurtigfanen **Garantiprodukter** velger du **Legg til linje** for å legge til en garantivare.
1. I feltet **Visningsrekkefølge** angir du et tall for å rangere garantigruppen på salgsstedet. Salgsstedet vil vise garantivarer i rekkefølge etter stigende rangering i garantiforespørselen.
1. I hurtigfanen for **Garantiberettigede produkter** velger du **Legg til linje** for å legge til garantiberettigede produkter.
1. Hvis garantivaren gjelder for en hel kategori med garantiberettigede varer (produkter), velger du kategorien i **Kategori**-feltet. Hvis garantivaren gjelder for en bestemt garantiberettiget vare (produkt), velger du produktet i **Produkt**-feltet.
1. På hurtigfanen **Gjeldende kanaler** velger du **Legg til linje** for å legge til kanalen der du vil selge garantivaren.
1. Velg **Lagre** for å lagre konfigurasjonen.
1. Velg **Publiser** for å publisere garantigruppen.
1. Kjør **1040**-jobben for å synkronisere dataene til kanalen.

## <a name="sell-warranty-items-at-the-pos"></a>Selge garantivarer på salgsstedet

To salgsstedsoperasjoner lar salgsmedarbeideren selge garantivarer under arbeidsflyten for kundekjøp:

- **Legg til garanti** – Denne operasjonen utløser en ledetekst som viser gjeldende garantier for en garantiberettiget vare som velges i handlekurven.
- **Legg til garanti i eksisterende transaksjon** – Ved hjelp av denne operasjonen kan salgsmedarbeidere selge garantier for garantiberettigede varer som ble solgt tidligere. Salgsmedarbeidere finner den opprinnelige transaksjonen for en garantiberettiget vare ved å angi kvitteringsnummeret for transaksjonen.

Følgende illustrasjon viser et eksempel på en salgsstedsterminalside med en ledetekst for å legge til en garantivare for det gjeldende kjøpet av en garantiberettiget vare.

![Eksempel på en ledetekst for å legge til en garantivare for det gjeldende kjøpet.](./media/ew-sell-warranty.png)

Følgende illustrasjon viser et eksempel på funksjonen for å legge til en garantivare for en garantiberettiget vare som er solgt tidligere.

![Eksempel på funksjonen for å legge til en garantivare for en tidligere solgt garantiberettiget vare.](./media/ew-add-warranty-existing.png)

## <a name="process-warranty-transactions"></a>Behandle garantitransaksjoner

Når det selges garantier i hentesalgstransaksjoner, kan Commerce-brukere, etter at transaksjonene er postert i Commerce Headquarters, kjøre jobben **Behandle garantitransaksjoner** for å behandle garantitransaksjonene og opprette garantipolicyer.

Følg denne fremgangsmåten for å behandle garantitransaksjoner i Commerce Headquarters.

1. Gå til **Detaljhandel og handel \> Produkter og kategoriers \> Garanti \> Behandle garantitransaksjoner**.
1. I dialogboksen **Velg organisasjonsnoder** i feltet **Organisasjonshierarki** velger du en verdi.
1. I listen **Tilgjengelige organisasjonsnoder** velger du enten en enkeltbutikk eller, hvis du vil opprette den satsvise jobben for en gruppe butikker, en node.
1. Velg høyre pilknapp for å legge til valget ditt i listen **Valgte organisasjonsnoder**.
1. Velg fanen **Kjør i bakgrunnen**.
1. Sett alternativet **Satsvis behandling** til **Ja**, og velg deretter **Regelmessighet**.
1. I dialogboksen **Definer regelmessighet** i feltet **Startdato** velger eller angir du en startdato for regelmessighet.
1. I **Starttidspunkt**-feltet velger eller angir du et starttidspunkt for regelmessighet.
1. Følg ett av disse trinnene:

    - Velg alternativet **Ingen sluttdato** hvis regelmessigheten aldri skal slutte.
    - Velg **Avslutt etter**-alternativet hvis regelmessigheten skal slutte etter et bestemt antall kjøringer. Hvis du velger dette alternativet, angir du antall kjøringer.
    - Velg alternativet **Avslutt innen** hvis regelmessigheten skal slutte innen en bestemt dato. Hvis du velger dette alternativet, velger eller angir du datoen.

1. Velg **OK**.
1. Velg **OK**.

## <a name="warranty-policies"></a>Garantipolicyer

Når en utvidet garanti selges, opprettes det automatisk en garantipolicyenhet. Garantipolicynumre kan deles med kunder, slik at de har en referanse for garantivaren de kjøpte. Egenskaper for garantipolicyer omfatter gyldig startdato og utløpsdato for garantien, vilkår og betingelser og serienummeret for den garantiberettigede varen som garantien ble solgt for.

> [!NOTE]
> Egenskaper for garantipolicy genereres automatisk når garantipolicyenheter opprettes. De kan for øyeblikket ikke konfigureres manuelt eller redigeres.

Følgende tabell beskriver egenskapene for garantipolicyen og deres verdier. I Commerce Headquarters kalles databasetabellen WARRANTYPOLICY.

| Egenskapsnavn | Verdi | beskrivelse |
|---------------|-------|-------------|
| PolicyNumber | En tegnstreng (maksimalt 20 tegn) | Garantipolicynummeret |
| WarrantiedItemId | En tegnstreng (maksimalt 20 tegn) | ID-en til den garantiberettigede varen |
| WarrantiedInventoryLotId | En tegnstreng (maksimalt 20 tegn) | Beholdningsparti-IDen til den garantiberettigede varen |
| WarrantiedSerialNumber | En tegnstreng (maksimalt 20 tegn) | Serienummeret til den garantiberettigede varen |
| WarrantiedFulfilledDate | En dato | Fullføringsdatoen for den garantiberettigede varen |
| WarrantyItemId | En tegnstreng (maksimalt 20 tegn) | ID-en til garantivaren |
| WarrantyInventoryLotId | En tegnstreng (maksimalt 20 tegn) | Beholdningsparti-IDen til garantivaren |
| WarrantySalesDate | En dato | Salgsdatoen til garantivaren |
| WarrantyEffectiveDate | En dato | Gyldighetsdato for garantipolicyen |
| WarrantyExpirationDate | En dato | Utløpsdatoen for garantipolicyen |
| CustAccount | En tegnstreng (maksimalt 20 tegn) | Kundekontonummeret |
| Status | **Opprettet**, **Annullert**, **Gyldig** eller **Utløpt** | Statusen for garantipolicyen |
| Notater | En tegnstreng (maksimalt 255 tegn) | Merknader om garantipolicyen, for eksempel vilkår og betingelser |

## <a name="frequently-asked-questions-faq"></a>Vanlige spørsmål

**Hvorfor kan jeg ikke se en garantiforespørselen på salgsstedet?**

Kontroller at garantivaren er assortert til kanalen. Kontroller også at garantigruppen er konfigurert, slik at den omfatter den gjeldende kanalen.

**Når jeg prøver å legge til en garanti i en eksisterende transaksjon og angi kvitteringsnummeret for kundens bestilling, hvorfor kan jeg ikke se noen transaksjonslinjevarer?**

Du kan bare finne kvitteringer hvis en hentejobb (P-jobb) kjøres for å laste opp kvitteringene til Commerce Headquarters. For å kjøre P-jobben går du til **Detaljhandel og handel \> IT for Detaljhandel og handel \> Distribusjonsplan**, velger **P-0001**-jobben og deretter **Kjør nå**.

**Hvorfor gjelder garantifunksjonen bare for serialiserte produkter?**

En garanti er en tjeneste som er tilgjengelig for et bestemt, unikt produkt. I Dynamics 365 kan et produkt bare identifiseres av et serienummer.

## <a name="additional-resources"></a>Tilleggsressurser

[Definere detaljhandelsprodukter](set-up-retail-products.md)

[Definere sortimenter](set-up-assortments.md)

[Oversikt over nummerserier](../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
