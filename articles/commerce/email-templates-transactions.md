---
title: Opprette e-postmaler for transaksjonshendelser
description: Dette emnet beskriver hvordan du oppretter, laster opp og konfigurerer e-postmaler for transaksjonshendelser i Microsoft Dynamics 365 Commerce.
author: bicyclingfool
manager: annbe
ms.date: 03/01/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 756e2a64ef4c33c347106968eb6bc79a413c3ff7
ms.sourcegitcommit: 88babb2fffe97e93bbde543633fc492120f2a4fc
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/06/2021
ms.locfileid: "5555251"
---
# <a name="create-email-templates-for-transactional-events"></a>Opprette e-postmaler for transaksjonshendelser

[!include [banner](includes/banner.md)]

Dette emnet beskriver hvordan du oppretter, laster opp og konfigurerer e-postmaler for transaksjonshendelser i Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Oversikt

Dynamics 365 Commerce inneholder en bruksklar prosess for sending av e-postmeldinger som varsler kunder om transaksjonshendelser (for eksempel når en ordre er plassert, en ordre er klar for henting, eller en ordre er levert). Dette emnet beskriver prosedyren for å opprette, laste opp og konfigurere e-postmalene som brukes til å sende transaksjons-e-postmeldinger.

## <a name="create-an-email-template"></a>Opprett en e-postmal

Før du kan tilordne en bestemt transaksjonshendelse til en e-postmal, må du opprette malen.

Hvis du vil opprette en e-postmal, følger du disse trinnene.

1. I Commerce Headquarters går du til **Detaljhandel og handel \> Hovedkvarteroppsett \> Maler for e-post til organisasjon** eller **Organisasjonsstyring \> Oppsett \> Maler for e-post til organisasjon**.
1. Velg **Ny**.
1. Under **Generelt** angir du følgende felt:

    - **E-post-ID** – ID-en for e-post er den unike identifikatoren for en mal, og det er verdien som vises når du velger en mal som skal tilordnes til en hendelse.
    - **E-postbeskrivelse** – Du kan bruke dette valgfrie feltet til å gi en beskrivelse av malen. Verdien du angir, vises bare i Commerce Headquarters.
    - **Avsendernavn** – Navnet du angir, vises i Fra-feltet i de fleste e-postklienter.
    - **Avsenders e-postadresse** – Angi e-postadressen som skal brukes for e-postmeldinger som sendes ved hjelp av denne malen.
    - **Standard språkkode** – Dette feltet angir den lokaliserte versjonen av e-postmeldingen som er sendt som standard, hvis det ikke er angitt noe språk av kanalen som aktiverer denne malen.

1. Velg **Nytt** under **Innhold i e-postmelding**.
1. I feltet **Språk** angir du språket for e-postmalen. Du kan legge til flere språk og lokaliserte maler senere.
1. I feltet **Emne** angir du e-postemnet som skal vises i feltet Emne i e-postmeldingen.
1. Velg **Rediger** for å laste opp e-postmalen.

## <a name="create-an-email-message-body-by-using-html"></a>Opprette en meldingstekst for e-post ved hjelp av HTML

Meldingsteksten i e-postmeldingen er opprettet i HTML. Du kan bruke alle oppsett, stiler og merking som HTML og linjebundne gjennomgripende stilark (CSS) er tillatt for. Du kan også bruke bilder hvis du drifter dem på et offentlig tilgjengelig webendepunkt. Hvis du vil legge til et bilde, angir du bildets URL-adresse i attributtet **src** for HTML-koden **&lt;img&gt;**.

> [!NOTE]
> E-postklienter bruker oppsetts- og stilbegrensninger som kan kreve endringer i HTML-koden, og CSS som du bruker til meldingsteksten. Det anbefales at du gjør deg kjent med de anbefalte fremgangsmåtene for å opprette HTML som vil bli støttet av de mest populære e-postklientene.

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

| Plassholdernavn     | Plassholderverdi                                            |
| -------------------- | ------------------------------------------------------------ |
| customername         | Navnet på kunden som la inn ordren.               |
| salesid              | Salgs-ID-en for ordren.                                   |
| deliveryaddress      | Leveringsadressen for sendte ordrer.                     |
| customeraddress      | Adressen til kunden.                                 |
| customeremailaddress | E-postadressen som kunden la inn i betalingsprosessen.     |
| deliverydate         | Leveringsdatoen.                                           |
| shipdate             | Forsendelsesdatoen.                                               |
| modeofdelivery       | Leveringsmåten for ordren.                              |
| tillegg              | De totale gebyrene for ordren.                             |
| mva                  | Den totale avgiften for ordren.                                 |
| sum                | Det totale beløpet for ordren.                              |
| ordernetamount       | Det totale beløpet for ordren, minus den totale avgiften.         |
| rabatt             | Den totale rabatten for ordren.                            |
| storename            | Navnet på butikken der ordren ble lagt inn.            |
| storeaddress         | Adressen til butikken som la inn ordren.              |
| storeopenfrom        | Åpningstidene til butikken som la inn ordren.         |
| storeopento          | Åpningstidene til butikken som la inn ordren.         |
| pickupstorename      | Navnet på butikken der ordren blir hentet.     |
| pickupstoreaddress   | Adressen til butikken der ordren blir hentet.  |
| pickupopenstorefrom  | Åpningstidene til butikken der ordren blir hentet. |
| pickupopenstoreto    | Åpningstidene til butikken der ordren blir hentet. |

### <a name="order-line-placeholders-sales-line-level"></a>Plassholdere for ordrelinje (salgslinjenivå)

Følgende plassholdere henter og viser data for individuelle produkter (linjer) i salgsordren.

| Plassholdernavn               | Plassholderverdi |
|--------------------------------|-------------------|
| productid                      | Produkt-ID-en for linjen. |
| lineproductname                | Navnet på produktet. |
| lineproductdescription         | Beskrivelsen av produktet. |
| linequantity                   | Antallet enheter som ble bestilt for linjen, pluss måleenheten (for eksempel **stk.** eller **par**). |
| lineunit                       | Måleenheten for linjen. |
| linequantity_withoutunit       | Antallet enheter som ble bestilt for linjen, uten måleenheten. |
| linequantitypicked             | Når hendelsen **PickOrder** brukes, vises antallet enheter som ble plukket. Hvis ikke brukes **0** (null). |
| linequantitypicked_withoutunit | Når hendelsen **PickOrder** brukes, vises antallet enheter som ble plukket, uten måleenhet. Hvis ikke brukes **0** (null). |
| linequantitypacked             | Når hendelsene **PackOrder** og **Ordre klar for henting** brukes, vises antallet enheter som ble pakket. Hvis ikke brukes **0** (null). |
| linequantitypacked_withoutuom  | Når hendelsene **PackOrder** og **Ordre klar for henting** brukes, vises antallet enheter som ble pakket, uten måleenheten. Hvis ikke brukes **0** (null). |
| linequantityshipped            | Alltid **0**, bortsett fra når bestemte hendelser brukes, som beskrevet i neste rad. |
| linequantityshipped_withoutuom | Når hendelsen **ShipOrder** brukes, vises antallet enheter som ble plukket, uten måleenhet. Hvis ikke brukes **0** (null). |
| lineprice                      | Prisen på en enkeltstående enhet. |
| linenetamount                  | Prisen på linjen etter antallet enheter og rabatt som brukes. |
| linediscount                   | Rabatten for en individuell enhet. |
| lineshipdate                   | Forsendelsesdatoen for linjen. |
| linedeliverydate               | Leveringsdatoen for linjen. |
| linedeliverymode               | Leveringsmåten for linjen. |
| linedeliveryaddress            | Leveringsadressen for linjen. |
| giftcardnumber                 | Gavekortnummeret for produkter av typen gavekort. |
| giftcardbalance                | Gavekortsaldoen for produkter av typen gavekort. |
| giftcardmessage                | Gavekortmeldingen for produkter av typen gavekort. |
| giftcardpin                    | Det personlige ID-nummeret (PIN-koden) for gavekortet for produkter av typen gavekort. (Denne plassholderen gjelder spesielt for eksterne gavekort.) |
| giftcardexpiration             | Utløpsdatoen for gavekortet for produkter av typen gavekort. (Denne plassholderen gjelder spesielt for eksterne gavekort.) |
| giftcardrecipientname          | Navnet på mottakeren av gavekortet for produkter av typen gavekort. |
| giftcardbuyername              | Navnet på kjøperen av gavekortet for produkter av typen gavekort. |

### <a name="format-of-order-line-placeholders-in-the-email-message-body"></a>Format for plassholdere for ordrelinje i e-postmeldingen

Når du oppretter HTML-koden for de enkeltstående ordrelinjene i teksten i e-postmeldingen, omgir du den gjentagende blokken med HTML og plassholdere for linjene med følgende plassholdere som er plassert i HTML-kommentarkoder.

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

- Kvitteringsteksten settes inn i e-postmeldingen ved hjelp av plassholderen **%message%**. For å sikre at kvitteringsteksten blir gjengitt på riktig måte, omslutter du plassholderen **%message%** med HTML-kodene **&lt;pre&gt;** og **&lt;/pre&gt;**.
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

[Definere e-postkvitteringer](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-email-receipts)

[Sende e-postkvitteringer fra Modern POS (MPOS) ](email-receipts.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
