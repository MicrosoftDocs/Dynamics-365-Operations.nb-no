---
title: Opprette e-postmaler for transaksjonshendelser
description: Dette emnet beskriver hvordan du oppretter, laster opp og konfigurerer e-postmaler for transaksjonshendelser i Microsoft Dynamics 365 Commerce.
author: bicyclingfool
ms.date: 12/10/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 25d7fcb803645f50ee4f5c608f5b6e789dfe3c31
ms.sourcegitcommit: eef5d9935ccd1e20e69a1d5b773956aeba4a46bc
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/11/2021
ms.locfileid: "7913758"
---
# <a name="create-email-templates-for-transactional-events"></a>Opprette e-postmaler for transaksjonshendelser

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Dette emnet beskriver hvordan du oppretter, laster opp og konfigurerer e-postmaler for transaksjonshendelser i Microsoft Dynamics 365 Commerce.

Dynamics 365 Commerce inneholder en standardløsning for å sende e-postmeldinger som varsler kunder om transaksjonshendelser. E-postmeldinger kan for eksempel sendes når en ordre blir plassert, er klar til plukking eller er sendt. Dette emnet beskriver prosedyren for å opprette, laste opp og konfigurere e-postmalene som brukes til å sende transaksjons-e-postmeldinger.

## <a name="notification-types"></a>Varslingstyper

Varslinger kan konfigureres for å informere kunder via e-post når bestemte hendelser forekommer som en del av ordren og kundens livssyklus. Hvis du vil konfigurere varslinger, må du tilordne en e-postmal til en varslingstype ved å opprette en e-postvarslingsprofil for Commerce. Hvis du vil ha mer informasjon om hvordan du definerer e-postvarslingsprofiler, kan du se [Definere en e-postvarslingsprofil](email-notification-profiles.md).

Dynamics 365 Commerce støtter følgende varslingstyper.

### <a name="order-created"></a>Ordre opprettet

Varslingstypen *ordre opprettet* utløses når en ny salgsordre opprettes i Commerce Headquarters.

> [!NOTE]
> Ordre opprettet-varslingstypen utløses ikke for hentesalgstransaksjoner som skjer ved en salgsstedsterminal. I dette tilfellet genereres det i stedet en e-postkvittering og/eller utskrevet kvittering. Hvis du vil ha mer informasjon, kan du se [Sende e-postkvitteringer fra Modern POS (MPOS)](email-receipts.md).

### <a name="order-confirmed"></a>Ordre bekreftet

*Ordre bekreftet*-meldingstypen utløses når et ordrebekreftelsesdokument genereres for en salgsordre fra Commerce Headquarters.

### <a name="picking-completed"></a>Plukking fullført

Varslingstypen *plukking fullført* utløses når en plukkliste for en ordre merkes som fullført i Commerce Headquarters.

> [!NOTE]
> Varslingstypen for plukking som er fullført, utløses ikke når en vare merkes som plukket ved en salgsstedsterminal.

### <a name="packing-completed"></a>Pakking fullført

Varslingstypen *pakking fullført* utløses når et følgeseddeldokument genereres for en ordre i Commerce Headquarters.

Varslingstypen pakking fullført støtter følgende ekstra e-postplassholdere for å legge til rette for "ordre klar for henting" og bestillingsoppslagsfunksjonalitet fra transaksjons-e-postmeldinger.

| Plassholdernavn    | Formål |
| ------------------- | ------- |
| `pickupstorename`     | Navnet på butikken der ordren er tilgjengelig for plukking. |
| `pickupstoreaddress`  | Adressen til butikken der ordren er tilgjengelig for plukking. |
| `pickupstorehourfrom` | Åpningstiden for plukkbutikken. |
| `pickupstorehourto`   | Stengetiden for plukkbutikken. |
| `pickupchannelid`     | Butikkkanal-IDen for plukkbutikken. |
| `packingslipid`      | IDen for følgeseddelen for ordren som blir hentet. |
| `confirmationid`      | Ordrebekreftelses-IDen for ordren som blir hentet. (Denne IDen kalles noen ganger kanalreferanse-IDen.) |

Hvis du vil ha mer informasjon om funksjonene for innsjekk og ordreoppslag for kunde, kan du se [Konfigurere registrering og omdirigering av georeplikering](geo-detection-redirection.md) og [Aktivere ordreoppslag for gjestebetalinger](order-lookup-guest.md).

### <a name="order-ready-for-pickup"></a>Ordre klar til henting

Varslingstypen *ordre klar for henting* utløses når en ordre merkes som pakket, og leveringsmåten er satt til **Kundeplukking** på én eller flere ordrelinjer.

> [!NOTE]
> Varslingstypen Ordre klar for plukking er avskrevet til fordel for varslingstypen pakking fullført. Denne varslingstypen tilpasses etter leveringsmåte.

### <a name="order-shipped"></a>Ordre sendt

Varslingstypen *ordre sendt* utløses når en ordre som har leveringsmåte som ikke er i butikk, faktureres.

> [!NOTE]
> Varslingstypen Ordre sendt er avskrevet til fordel for varslingstypen ordre fakturert. Denne varslingstypen tilpasses etter leveringsmåte.

### <a name="order-invoiced"></a>Ordre fakturert

Varslingstypen *ordre fakturert* utløses når en ordre faktureres på salgsstedet eller i Commerce Headquarters.

### <a name="issue-gift-card"></a>Utsted gavekort

Varslingstypen *Utsted gavekort* utløses når en salgsordre som inneholder et produkt av gavekorttypen, faktureres.

> [!NOTE]
> Epostvarslingen Utsted gavekort sendes til gavekortmottakeren. Gavekortmottakeren er angitt i Commerce Headquarters på en enkelt salgsordrelinje i kategorien **Emballasje** under **Linjedetaljer**. Den kan angis enten manuelt eller programmert.

Varslingstypen for Utsted gavekort støtter følgende ekstra plassholdere.

| Plassholdernavn      | Formål |
| --------------------- | ------- |
| `giftcardnumber`        | Gavekortnummeret for produkter av typen gavekort. |
| `giftcardbalance`       | Gavekortsaldoen for produkter av typen gavekort. |
| `giftcardmessage`       | Gavekortmeldingen for produkter av typen gavekort. |
| `giftcardpin`         | Det personlige ID-nummeret (PIN-koden) for gavekortet for produkter av typen gavekort. (Denne plassholderen gjelder spesielt for eksterne gavekort.) |
| `giftcardexpiration`    | Utløpsdatoen for gavekortet for produkter av typen gavekort. (Denne plassholderen gjelder spesielt for eksterne gavekort.) |
| `giftcardrecipientname` | Navnet på mottakeren av gavekortet for produkter av typen gavekort. |
| `giftcardbuyername`     | Navnet på kjøperen av gavekortet for produkter av typen gavekort. |

Hvis du vil ha mer informasjon om gavekort, kan du se [Digitale gavekort for e-handel](digital-gift-cards.md) og [Støtte for eksterne gavekort](dev-itpro/gift-card.md).

### <a name="order-cancellation"></a>Ordreannullering

Varslingstypen *ordre fakturert* utløses når en ordre annulleres i Commerce Headquarters.

### <a name="customer-created"></a>Kunden er opprettet

Varslingstypen *kunde opprettet* utløses når en ny kundeenhet opprettes i Commerce Headquarters.

### <a name="b2b-prospect-approved"></a>B2B-kundeemne godkjent

Varslingstypen for *B2B-kundeemne godkjent* utløses når et kundeemnes pålastingsforespørsel godkjennes i Commerce Headquarters. Hvis du vil ha mer informasjon om hvordan du godkjenner eller avviser B2B-kundeemner, kan du se [Konfigurere administratorbrukeren for en ny forretningspartner](b2b/manage-b2b-users.md#set-up-the-administrator-user-for-a-new-business-partner). 

Varslingstypen B2B-kundeemne godkjent støtter følgende ekstra plassholdere.

| Plassholdernavn | Formål                                                      |
| ---------------- | ------------------------------------------------------------ |
| `firstname`       | Fornavnet til B2B-kundeemnet slik det er angitt i programmet. |
| `lastname`         | Etternavnet til B2B-kundeemnet slik det er angitt i programmet. |
| `company`          | Navnet til søkerens firma slik det er angitt i programmet. |
| `email`            | Epostadressen til kundeemnet slik det er angitt i programmet.   |
| `zipcode`          | Postnummeret til kundeemnets primæradresse. |
| `comments`         | Kommentaren som kundeemnet la inn i programmet. |
| `storename`        | Navnet på kanalen der kundeemnet ble opprettet. |
| `storeurl`         | Tom som standard. En egendefinert utvidelse må opprettes for å bruke denne plassholderen. |

### <a name="b2b-prospect-rejected"></a>B2B-kundeemne avvist

Varslingstypen for *B2B-kundeemne avvist* utløses når et kundeemnes pålastingsforespørsel avvises i Commerce Headquarters. Hvis du vil ha mer informasjon om hvordan du godkjenner eller avviser B2B-kundeemner, kan du se [Konfigurere administratorbrukeren for en ny forretningspartner](b2b/manage-b2b-users.md#set-up-the-administrator-user-for-a-new-business-partner). 

Varslingstypen B2B-kundeemne avvist støtter følgende ekstra plassholdere.

| Plassholdernavn | Formål                                                      |
| ---------------- | ------------------------------------------------------------ |
| `firstname`        | Fornavnet til B2B-kundeemnet slik det er angitt i programmet. |
| `lastname`         | Etternavnet til B2B-kundeemnet slik det er angitt i programmet. |
| `company`          | Navnet til søkerens firma slik det er angitt i programmet. |

## <a name="create-an-email-template"></a>Opprett en e-postmal

Før du kan tilordne en bestemt transaksjonshendelse til en e-postmal, må du opprette malen.

Hvis du vil opprette en e-postmal, følger du disse trinnene.

1. I Commerce Headquarters går du til **Detaljhandel og handel \> Hovedkvarteroppsett \> Maler for e-post til organisasjon** eller **Organisasjonsstyring \> Oppsett \> Maler for e-post til organisasjon**.
1. Velg **Ny**.
1. Under **Generelt** angir du følgende felt:

    - **E-post-ID** – E-post-IDen er den unike identifikatoren for en mal. Det er verdien som vises når du velger en mal som skal tilordnes til en hendelse.
    - **E-postbeskrivelse** – Du kan bruke dette valgfrie feltet til å gi en beskrivelse av malen. Verdien du angir, vises bare i Commerce Headquarters.
    - **Avsendernavn** – Navnet du angir, vises i Fra-feltet i de fleste e-postklienter.
    - **Avsenders e-postadresse** – Angi e-postadressen som skal brukes for e-postmeldinger som sendes ved hjelp av denne malen.
    - **Standard språkkode** – Dette feltet angir den lokaliserte versjonen av e-postmeldingen som er sendt som standard, hvis kanalen som aktiverer denne malen, ikke angir et språk.

1. Velg **Nytt** under **Innhold i e-postmelding**.
1. I feltet **Språk** angir du språket for e-postmalen. Du kan legge til flere språk og lokaliserte maler senere.
1. I feltet **Emne** angir du e-postemnet som skal vises i feltet Emne i e-postmeldingen.
1. Velg **Rediger** for å laste opp e-postmalen.

## <a name="create-an-email-message-body-by-using-html"></a>Opprette en meldingstekst for e-post ved hjelp av HTML

Meldingsteksten i e-postmeldingen er opprettet i HTML. Du kan bruke alle oppsett, stiler og merking som HTML og linjebundne gjennomgripende stilark (CSS) er tillatt for. Du kan også bruke bilder hvis du drifter dem på et offentlig tilgjengelig webendepunkt. Hvis du vil legge til et bilde, angir du bildets URL-adresse i attributtet **src** for HTML-koden **&lt;img&gt;**.

> [!NOTE]
> E-postklienter bruker oppsetts- og stilbegrensninger som kan kreve endringer i HTML-koden, og CSS som du bruker til meldingsteksten. Det anbefales at du gjør deg kjent med de anbefalte fremgangsmåtene for å opprette HTML som de mest populære e-postklientene støtter.

## <a name="add-placeholders-to-the-email-message-body"></a>Legge til plassholdere i meldingsteksten i e-postmeldingen

E-posten kan inneholde plassholdere som erstattes med kundespesifikke og transaksjonsspesifikke verdier når e-postmeldingen genereres. Plassholdere er alltid omgitt av prosenttegn (%) og settes direkte inn i HTML-dokumentet.

Her er et eksempel:

```html
<p>
    Hello %customername%,<br />
    Order number %salesid%, can be picked up from the <b>%pickupstorename%</b> store.
</p>
```

### <a name="order-placeholders-sales-order-level"></a>Plassholdere for ordre (salgsordrenivå)

Følgende plassholdere henter og viser data som er definert på salgsordrenivå (i motsetning til på salgslinjenivå).

| Plassholdernavn     | Formål                                                      |
| -------------------- | ------------------------------------------------------------ |
| `customername`         | Navnet på kunden som la inn ordren.               |
| `customeraddress`      | Adressen til kunden.                                 |
| `customeremailaddress` | E-postadressen som kunden la inn i betalingsprosessen.     |
| `salesid`              | Salgs-ID-en for ordren.                                   |
| `orderconfirmationid`  | Tverrkanals-ID-en som ble generert ved ordreoppretting.   |
| `channelid`            | ID-en til detaljhandelen eller nettkanalen som bestillingen ble gjort gjennom. |
| `deliveryname`         | Navnet som er angitt for leveringsadressen.         |
| `deliveryaddress`      | Leveringsadressen for sendte ordrer.                     |
| `deliverydate`         | Leveringsdatoen.                                           |
| `shipdate`             | Forsendelsesdatoen.                                               |
| `modeofdelivery`       | Leveringsmåten for ordren.                              |
| `ordernetamount`       | Det totale beløpet for ordren, minus den totale avgiften.         |
| `discount`            | Den totale rabatten for ordren.                            |
| `charges`              | De totale gebyrene for ordren.                             |
| `tax`                  | Den totale avgiften for ordren.                                 |
| `total`                | Det totale beløpet for ordren.                              |
| `storename`            | Navnet på butikken der ordren ble lagt inn.            |
| `storeaddress`         | Adressen til butikken som la inn ordren.              |
| `storeopenfrom`        | Åpningstidene til butikken som la inn ordren.         |
| `storeopento`          | Åpningstidene til butikken som la inn ordren.         |
| `pickupstorename`      | Navnet på butikken der ordren blir hentet.\*   |
| `pickupstoreaddress`   | Adressen til butikken der ordren blir hentet.\* |
| `pickupopenstorefrom`  | Åpningstidene til butikken der ordren blir hentet.\* |
| `pickupopenstoreto`    | Åpningstidene til butikken der ordren blir hentet.\* |
| `pickupchannelid`     | Kanal-ID-en for butikken som er angitt for en hentemåte for levering.\* |
| `packingslipid`        | ID-en til følgeseddelen som ble generert da linjer i en ordre ble pakket.\* |

\* Disse plassholderne returnerer bare data når de brukes for varslingstypen **Ordre klar for henting**. 

### <a name="order-line-placeholders-sales-line-level"></a>Plassholdere for ordrelinje (salgslinjenivå)

Følgende plassholdere henter og viser data for individuelle produkter (linjer) i salgsordren.

| Plassholdernavn               | Formål |
|--------------------------------|-------------------|
| `productid`                      | <p>ID-en for produktet. Denne ID-en står for varianter.</p><p><strong>Obs!</strong> Denne plassholderen er avskrevet til fordel for `lineproductrecid`.</p> |
| `lineproductrecid`               | ID-en for produktet. Denne ID-en står for varianter. Den identifiserer en vare unikt på variantnivå. |
| `lineitemid`                     | Produktnivå-ID-en for produktet. (Denne ID-en står ikke for varianter.) |
| `lineproductvariantid`           | ID-en for produktvarianten. |
| `lineproductname`                | Navnet på produktet. |
| `lineproductdescription`         | Beskrivelsen av produktet. |
| `linequantity`                   | Antallet enheter som ble bestilt for linjen, pluss måleenheten (for eksempel **stk.** eller **par**). |
| `lineunit`                       | Måleenheten for linjen. |
| `linequantity_withoutunit`       | Antallet enheter som ble bestilt for linjen, uten måleenheten. |
| `linequantitypicked`             | Når hendelsen **PickOrder** brukes, vises antallet enheter som ble plukket. Hvis ikke brukes **0** (null). |
| `linequantitypicked_withoutunit` | Når hendelsen **PickOrder** brukes, vises antallet enheter som ble plukket, uten måleenhet. Hvis ikke brukes **0** (null). |
| `linequantitypacked`             | Når hendelsene **PackOrder** og **Ordre klar for henting** brukes, vises antallet enheter som ble pakket. Hvis ikke brukes **0** (null). |
| `linequantitypacked_withoutuom`  | Når hendelsene **PackOrder** og **Ordre klar for henting** brukes, vises antallet enheter som ble pakket, uten måleenheten. Hvis ikke brukes **0** (null). |
| `linequantityshipped`            | Alltid **0**, bortsett fra når bestemte hendelser brukes, som beskrevet i neste rad. |
| `linequantityshipped_withoutuom` | Når hendelsen **ShipOrder** brukes, vises antallet enheter som ble plukket, uten måleenhet. Hvis ikke brukes **0** (null). |
| `lineprice`                      | Prisen på en enkeltstående enhet. |
| `linenetamount`                  | Prisen på linjen etter antallet enheter og rabatt som brukes. |
| `linediscount`                   | Rabatten for en individuell enhet. |
| `lineshipdate`                   | Forsendelsesdatoen for linjen. |
| `linedeliverydate`               | Leveringsdatoen for linjen. |
| `linedeliverymode`               | Leveringsmåten for linjen. |
| `linedeliveryaddress`            | Leveringsadressen for linjen. |
| `linepickupdate`                 | Hentedatoen som kunden har angitt, for ordrer som bruker en henteleveringsmåte. |
| `linepickuptimeslot`             | Tidsområdet for henting som kunden har angitt, for ordrer som bruker en henteleveringsmåte. |
| `giftcardnumber`                 | Gavekortnummeret for produkter av typen gavekort. |
| `giftcardbalance`                | Gavekortsaldoen for produkter av typen gavekort. |
| `giftcardmessage`                | Gavekortmeldingen for produkter av typen gavekort. |
| `giftcardpin`                    | PIN-koden for gavekortet, for produkter av typen gavekort. (Denne plassholderen gjelder spesielt for eksterne gavekort.) |
| `giftcardexpiration`             | Utløpsdatoen for gavekortet for produkter av typen gavekort. (Denne plassholderen gjelder spesielt for eksterne gavekort.) |
| `giftcardrecipientname`          | Navnet på mottakeren av gavekortet for produkter av typen gavekort. |
| `giftcardbuyername`              | Navnet på kjøperen av gavekortet for produkter av typen gavekort. |

### <a name="format-of-order-line-placeholders-in-the-email-message-body"></a>Format for plassholdere for ordrelinje i e-postmeldingen

Når du oppretter HTML-koden for de enkeltstående ordrelinjene i teksten i e-postmeldingen, omgir du den gjentagende blokken med HTML og plassholdere for linjene med følgende plassholdere. Legg merke til at plassholderne er i HTML-kommentarkoder.

```html
<!--%tablebegin.salesline%-->

(Insert the repeating block of HTML and placeholders for individual lines here.)

<!--%tableend.salesline%-->
```

Her er et eksempel:

```HTML
<table>
    <tr>
        <td>Product name</td>
        <td>Quantity</td>
        <td>Price</td>
    </tr>
    <!--%tablebegin.salesline%-->
    <tr>
        <td>%lineproductname%</td>
        <td>%linequantity_withoutunit%</td>
        <td>%lineprice%</td>
    </tr>
    <!--%tableend.salesline%-->
</table>
```

## <a name="create-a-template-for-emailed-receipts"></a>Opprette en mal for e-postkvitteringer

Kvitteringer kan sendes som e-post til kunder som kjøper på et salgssted (POS). Fremgangsmåten for oppretting av malen for e-postkvitteringer er vanligvis de samme som fremgangsmåten for å opprette maler for andre transaksjonshendelser. Følgende endringer er imidlertid nødvendige:

- Plassholderen **%message%** brukes til å sette inn tekst for kvitteringen i e-posten. For å sikre at kvitteringsteksten blir gjengitt på riktig måte, omslutter du plassholderen **%message%** med HTML-kodene **&lt;pre&gt;** og **&lt;/pre&gt;**.
- Plassholderen **%receiptid%** kan brukes til å vise en QR-kode eller strekkode som representerer kvitterings-IDen. (QR-koder og strekkoder genereres dynamisk og betjenes av en tredjepartstjeneste.) Hvis du vil ha mer informasjon om hvordan du viser en QR-kode eller strekkode i en e-postkvittering, kan du se [Legge til en QR-kode eller strekkode i e-postmeldinger for transaksjon og kvittering](add-qr-code-barcode-email.md).

## <a name="upload-the-email-html"></a>Laste opp HTML for e-post

Når du har opprettet og testet HTML-koden for meldingsteksten, må den lastes opp til Commerce Headquarters. For øyeblikket kan ikke HTML for e-post eksporteres. Du må derfor beholde hovedkopien av HTML-koden utenfor Commerce Headquarters.

Hvis du vil laste opp en ny eller redigert HTML for e-postmal, gjør du følgende.

1. I Commerce Headquarters går du til **Detaljhandel og handel \> Hovedkvarteroppsett \> Maler for e-post til organisasjon**.
1. Velg raden for språket du vil legge til eller erstatte HTML for. Du kan også velge **Ny** for å opprette en rad for et nytt språk.
1. Velg **Rediger**.
1. I dialogboksen som vises, velger du **Bla gjennom**. Bla til HTML-dokumentet du vil laste opp, merk det, og velg deretter **Åpne**.
1. Velg **Last opp**.
1. Når e-posthtmlen vises i forhåndsvisningsvinduet, velger du **OK**.
1. Sørg for at det er merket av for **Har brødtekst** for raden.

Hvis du allerede har konfigurert Commerce Headquarters til å sende e-post, vil den nye eller oppdaterte e-postmeldingen bli sendt til alle kunder som utfører en transaksjon som aktiverer hendelsen som er tilordnet til malen.

Hvis du vil ha mer informasjon om hvordan du konfigurerer e-post i Dynamics 365 Commerce, kan du se [Konfigurere og sende e-post](../fin-ops-core/fin-ops/organization-administration/configure-email.md).

## <a name="additional-resources"></a>Tilleggsressurser 

[Definere en profil for e-postvarsling](email-notification-profiles.md)

[Konfigurere og sende e-post](../fin-ops-core/fin-ops/organization-administration/configure-email.md)

[Definere e-postkvitteringer](/dynamicsax-2012/appuser-itpro/set-up-email-receipts)

[Sende e-postkvitteringer fra Modern POS (MPOS) ](email-receipts.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
