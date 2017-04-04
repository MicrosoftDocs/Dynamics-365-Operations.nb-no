---
title: "Oversikt over SEPA-kredittoverføring"
description: "Denne artikkelen inneholder generell informasjon om ISO 20022 kreditt overføringer, som inkluderer én Euro betalinger området (SEPA) kreditt overføringer og andre elektroniske betalinger til leverandører. SEPA kredittoverføring er en bestemt type betaling i euro fra ett firma eller individuelle til et annet selskap eller individuelle. Dette emnet forklarer også hvordan du setter og sende en betalingsfil for kreditt overføring."
author: twheeloc
manager: AnnBe
ms.date: 2017-04-04
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: LedgerJournalTransVendInvoice, LedgerJournalTransVendPaym, VendPaymMode
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 11124
ms.assetid: 36b0f870-16d4-4bbb-8da5-e747e69b970d
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 4d6cf88788dcc5e982e509137aa444a020137a5e
ms.openlocfilehash: 848df5e3898f37284d7746c59bff8b38d35ac883
ms.lasthandoff: 03/31/2017


---

# <a name="sepa-credit-transfer-overview"></a>Oversikt over SEPA-kredittoverføring

Denne artikkelen inneholder generell informasjon om ISO 20022 kreditt overføringer, som inkluderer én Euro betalinger området (SEPA) kreditt overføringer og andre elektroniske betalinger til leverandører. SEPA kredittoverføring er en bestemt type betaling i euro fra ett firma eller individuelle til et annet selskap eller individuelle. Dette emnet forklarer også hvordan du setter og sende en betalingsfil for kreditt overføring.

## <a name="what-is-a-credit-transfer-message"></a>Hva er en kreditt overføring melding?
Kreditt overføring meldingen er en forespørsel som sender en første party (firmaet) til å flytte midler fra sin egen konto til en kreditor. Det er mange land-/ områdespesifikke og bank-spesifikke implementeringer av kredittoverføring meldinger. Noen av dem brukes innenfor ett land, og noen blir standarder. En godt etablert global standard er ISO 20022 og dens initiation-meldinger, for eksempel kredittoverføring. Følgende illustrasjon viser relasjoner og dekning for valgte kreditt overføring meldinger. 
![Kreditere overføring](./media/credit-transfer.jpg) kreditt overføring meldinger\[/bildetekst\] 

## <a name="what-are-iso-20022-and-sepa-payments"></a>Hva er ISO 20022 og SEPA-betalinger?
Felles eurobetalingsområde (SEPA) er satt opp av EU-kommisjonen og angir at alle elektroniske betalinger betraktes som innenlandsbetalinger, uavhengig av landet/regionen der personen, virksomheten eller organisasjonen, og banken befinner seg. Det er ingen forskjell mellom national betalinger og betalinger over grenser. SEPA inneholder 28 medlemsland av den europeiske Union (EU), og også Island, Liechtenstein, Norge, Sveits, Monaco og San Marino. SEPA bidrar til å danne ett marked for betalingstransaksjoner i EØS. I siste instans forventes det at SEPA til slutt reduserer antall betalingsformater som banker, bedrifter og enkeltpersoner må arbeide med. EU-kommisjonen fastsatte det juridiske grunnlaget for SEPA-betalinger via PSD-direktivet (Payment Services Directive). EPC (European Payments Council) støtter SEPA gjennom følgende aktiviteter:

-   Den angir standardene for elektroniske SEPA-betalinger ved hjelp av den universelle ISO 20022-standarden for finansiell meldingsutveksling i XML-format.
-   Det oppretter regler og retningslinjer om håndtering av eurobetalinger.

EPC, som består av europeiske banker, utvikler kommersielle og tekniske rammeverk for SEPA-betalingsmidler. Tre typer SEPA-betalinger brukes:

-   Kredittoverføringer
-   Avtalegiro
-   Kort

## <a name="what-is-a-sepa-credit-transfer"></a>Hva er en SEPA-kredittoverføring?
En SEPA-kredittoverføring er en betaling fra ett firma eller en enkeltperson til et annet firma eller en enkeltperson. Betalinger må være i euro og må inneholde IBAN-nummeret (internasjonalt bankkontonummer) og BIC-koden (bankidentifikasjonskode) for begge parter. (BIC er også kjent som Society for Worldwide Interbank Financial Telecommunication \[SWIFT\] kode.) Transaksjonskostnader må være delt mellom begge parter. Kreditoverføringer som forekommer mellom parter, bør bruke XML-filer som samsvarer med ISO 20022-betalingsbehandlingsstandarder og XML-formatet, som angitt av EPC.

## <a name="how-is-a-credit-transfer-implemented"></a>Hvordan er en kredittoverføring implementert?
Kreditt overføring betalingsformatet for europeiske land er implementert ved hjelp av elektronisk rapportering (ER) og metoder for betaling-funksjonalitet i Dynamics 365 for operasjoner. Noen kreditt overføring formatene som brukes i andre regioner fremdeles bruke eldre betaling-rammeverket. Det er tolv ISO 20022 kreditt overføring-filformater som er tilgjengelige blant mange andre formater. Disse eksportformater overholder SEPA ISO 20022 XML-standarden. De brukes til å generere-euro betalingsoverføringer for land/områder der de brukes og euro betalinger som er angitt i versjon 8.2 av den SEPA kreditt overføre fargevalget Rulebook som utgis av EPC. Før du kan implementere en kreditnota overføringer, må du kontakte banken din for å få programvaren som kreves for å laste opp filer for elektroniske banktjenester. Du vil bruke denne programvaren til å overføre XML-filene som inneholder oppdrag til banken.

## <a name="what-credit-transfer-formats-are-currently-supported-in-dynamics-365-for-operations"></a>Hvilke kreditt overføring formater støttes i Dynamics 365 for operasjoner?
Du bør alltid gå til biblioteket Delte aktiva på Microsoft Dynamics-levetidstjenester (LCS) og viser den mest oppdaterte listen over tilgjengelige filer som har en anleggsmiddeltype av **TYSK konfigurasjon**. Neste delen, "Hva jeg har til å definere?", inneholder en kobling til emnet som forklarer hvordan du oppretter en LCS repositoriet for å se gjennom konfigurasjoner og importere valgte konfigurasjoner.

## <a name="what-do-i-have-to-set-up"></a>Hva må jeg konfigurere?
-   Før du kan opprette kreditnota Overfør filer, må minst én aktiv overføring konfigurasjon importeres til ER-konfigurasjoner. For instruksjoner, se [laste ned elektronisk rapportering konfigurasjoner fra levetidstjenester](https://docs.microsoft.com/en-us/dynamics365/operations/dev-itpro/analytics/download-electronic-reporting-configuration-lcs).
-   Når du konfigurerer kontoer skyldig betalingsmåter, velg den **generisk elektronisk rapportering**, og velg riktig kreditt overføring-format (for eksempel **ISO 20022 kreditt overføring (AT)**) som en konfigurasjon for Eksporter format.
-   Du må også angi juridisk enhet og bankkonto informasjon i Dynamics 365 for operasjoner.
-   Bankkontonumre, IBANs og noen ganger SWIFT koder (BICs) eller andre IDer som er nødvendige for å opprette gyldig kredittoverføring betalinger. Derfor må du definere dem for leverandørens bankkonto og bankkonto for organisasjonen som ber om overføringen.
-   Ytterligere informasjon kan være nødvendig, for eksempel merverdiavgift (mva) tall for partene som er referert til i meldingen kreditt overføring. Denne informasjonen må defineres for leverandører og juridisk enhet når den blir forespurt.
-   Noen kontoer skyldig betalingsmåter, for det meste ISO 20022-baserte betalingsmåter, kan kreve ekstra oppsett for **betalings format kodesett**, som **Service type** = **SLEV**. Disse kodene brukes som ekstra koding for betalingstransaksjoner under betalingsbehandling. Standardverdier for betaling-koder, som **kategori formålet**, **gratis bæreren**, **lokale instrument** og **Service nivå** kan angis på to steder. Er det første stedet **kontoer leverandørbetaling journalhodet** og andre er **Accounts payable metoder for betalinger**. Ved betaling journalen linjer opprettelsen betaling kodeverdiene som er angitt på betalingsjournalhodet er overført til en kladdelinje, hvis ikke angitt, brukes verdiene fra betalingsmåter.

## <a name="what-parameters-are-available-for-generating-credit-transfer-payments"></a>Hvilke parametere er tilgjengelige for å generere betalinger for overføring av kreditt?
Liste over spesifikke parametere avhenger av kreditt overføring-format. Tabellen nedenfor viser parameterne som er tilgjengelige når du genererer en ISO 20022 kreditt overføring betalingsfil for Tyskland i en journal for leverandørbetaling. Ved hjelp av alternativene som er tilgjengelige på den **kjører i bakgrunnen** -kategorien kan du kjøre betalingsgenerering i satsvis modus.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Felt</th>
<th>beskrivelse</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Satsvis bestilling</td>
<td>Merk av i denne avmerkingsboksen for å inkludere Satsvis bestilling i XML-filen.</td>
</tr>
<tr class="even">
<td>Behandlingsdato</td>
<td>Angi datoen når banken skal behandle betalingene.</td>
</tr>
<tr class="odd">
<td>Formater</td>
<td>Velg formatet for remitteringsopplysninger, avhengig av kravene i ditt land/område eller din bank:
<ul>
<li><strong>Strd</strong> – Velg dette alternativet for å bruke strukturert format når en betalingslinje er utlignet mot en faktura. Dette alternativet er ikke tilgjengelig for land-/ områdespesifikke eksportformater for Frankrike, Tyskland eller Nederland.</li>
<li><strong>Ustrukturert</strong> – Velg dette alternativet for å bruke det ustrukturerte formatet når betalingen utlignes mot flere fakturaer. Fakturanumrene for de utlignede fakturaene slås sammen og brukes som remisseinformasjon. Samsvar ISO 20022 retningslinjer, remittering ustrukturert informasjon er begrenset til 140 tegn.</li>
</ul></td>
</tr>
<tr class="even">
<td>Antall fakturaer</td>
<td>Angi antall fakturaer som den <strong>betalingsmelding</strong> rapporten skrives ut fra.</td>
</tr>
<tr class="odd">
<td>Serienummer</td>
<td>Angi et serienummer som identifiserer filen. Sekvensnummeret vises på den <strong>deltakernotat</strong> rapport.</td>
</tr>
<tr class="even">
<td>Skriv ut deltakernotat</td>
<td>Merk av i denne avmerkingsboksen for å skrive ut <strong>Deltakernotat</strong>-rapporten.</td>
</tr>
<tr class="odd">
<td>Skriv ut kontrollrapport</td>
<td>Merk av i denne avmerkingsboksen for å skrive ut en rapport som inneholder betalingsinformasjonen.</td>
</tr>
<tr class="even">
<td>Skriv ut følgeskriv</td>
<td>Merk av for dette alternativet for å skrive ut <strong>Betalingsmelding</strong>-rapporten.</td>
</tr>
</tbody>
</table>

## <a name="what-are-ibans-and-bics"></a>Hva er IBAN-er og BIC-er?
International Bank Account nummer (IBAN) og Bank Identifier Code (BIC) brukes til å identifisere en hvilken som helst konto i mange land over hele verden. Disse inkluderer de 34 SEPA land/regionene. Angi BIC i den **SWIFT-koden** -feltet og IBAN i den **IBAN** feltet. For kreditors bankkonto og kundens bankkonto disse feltene er plassert på den **ytterligere identifikasjon** hurtigfanen på den **bankkonto** -kategorien i den **bankkonti** siden. Bruk av BIC for SEPA-betalinger fremtvinges ikke lenger.

## <a name="how-do-i-transmit-a-payment-file-to-the-bank"></a>Hvordan sender jeg en betalingsfil til banken?
Når du genererer betalinger, betalingsfilen er generert, og du blir bedt om å lagre den hvor som helst tilgjengelig fra web-leseren. Det neste trinnet er å sende XML-filen til banken. Denne prosessen varierer fra bank til bank. Følg instruksjonene fra banken din når du skal sende filer til banken for behandling.


