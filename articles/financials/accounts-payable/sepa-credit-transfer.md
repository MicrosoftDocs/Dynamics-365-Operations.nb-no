---
title: "Oversikt over SEPA-kredittoverføring"
description: "Denne artikkelen inneholder generell informasjon om ISO 20022-kredittoverføringer, som inkluderer kredittoverføringer for felles eurobetalingsområde (SEPA) og andre elektroniske betalinger for leverandører. En SEPA-kredittoverføring er en bestemt type betaling i euro fra ett firma eller en enkeltperson til et annet firma eller en enkeltperson. Emnet beskriver også hvordan du konfigurerer og sender en betalingsfil for kredittoverføring."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerJournalTransVendInvoice, LedgerJournalTransVendPaym, VendPaymMode
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 11124
ms.assetid: 36b0f870-16d4-4bbb-8da5-e747e69b970d
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 69eeb90387ca5765c163c7d482295ea104cc078c
ms.openlocfilehash: 49dfae79fe3914bcac9447d4fe3959128ff434ec
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---

# <a name="sepa-credit-transfer-overview"></a>Oversikt over SEPA-kredittoverføring

[!include[banner](../includes/banner.md)]


Denne artikkelen inneholder generell informasjon om ISO 20022-kredittoverføringer, som inkluderer kredittoverføringer for felles eurobetalingsområde (SEPA) og andre elektroniske betalinger for leverandører. En SEPA-kredittoverføring er en bestemt type betaling i euro fra ett firma eller en enkeltperson til et annet firma eller en enkeltperson. Emnet beskriver også hvordan du konfigurerer og sender en betalingsfil for kredittoverføring.

## <a name="what-is-a-credit-transfer-message"></a>Hva er en kredittoverføringsmelding?
Kredittoverføringsmeldingen er en forespørsel som initialiseringsparten (firmaet) sender for å flytte midler fra sin egen konto til en kreditor. Det er mange land-/områdespesifikke og bankspesifikke implementeringer av kredittoverføringsmeldinger. Noen av dem brukes innenfor ett land, og andre blir standarder. En godt etablert verdensomspennende standard er ISO 20022 og dens initieringsmeldinger, for eksempel kredittoverføring. Illustrasjonen nedenfor viser relasjoner og dekning for valgte kredittoverføringsmeldinger. 
![Kredittoverføring](./media/credit-transfer.jpg) Kredittoverføringsmeldinger 

## <a name="what-are-iso-20022-and-sepa-payments"></a>Hva er ISO 20022- og SEPA-betalinger?
Felles eurobetalingsområde (SEPA) er satt opp av EU-kommisjonen og angir at alle elektroniske betalinger betraktes som innenlandsbetalinger, uavhengig av landet/regionen der personen, virksomheten eller organisasjonen, og banken befinner seg. Det er ingen forskjell mellom nasjonale betalinger og betalinger over grenser. SEPA omfatter de 28 EU-medlemslandene pluss Island, Liechtenstein, Norge, Sveits, Monaco og San Marino. SEPA bidrar til å danne ett marked for betalingstransaksjoner i EØS. I siste instans forventes det at SEPA til slutt reduserer antall betalingsformater som banker, bedrifter og enkeltpersoner må arbeide med. EU-kommisjonen fastsatte det juridiske grunnlaget for SEPA-betalinger via PSD-direktivet (Payment Services Directive). EPC (European Payments Council) støtter SEPA gjennom følgende aktiviteter:

-   Den angir standardene for elektroniske SEPA-betalinger ved hjelp av den universelle ISO 20022-standarden for finansiell meldingsutveksling i XML-format.
-   Det oppretter regler og retningslinjer om håndtering av eurobetalinger.

EPC, som består av europeiske banker, utvikler kommersielle og tekniske rammeverk for SEPA-betalingsmidler. Tre typer SEPA-betalinger brukes:

-   Kredittoverføringer
-   Avtalegiro
-   Kort

## <a name="what-is-a-sepa-credit-transfer"></a>Hva er en SEPA-kredittoverføring?
En SEPA-kredittoverføring er en betaling fra ett firma eller en enkeltperson til et annet firma eller en enkeltperson. Betalinger må være i euro og må inneholde IBAN-nummeret (internasjonalt bankkontonummer) og BIC-koden (bankidentifikasjonskode) for begge parter. (BIC-koden er også kjent som \[SWIFT\]-kode (Society for Worldwide Interbank Financial Telecommunication). I tillegg må transaksjonskostnader deles mellom begge parter. Kreditoverføringer som forekommer mellom parter, bør bruke XML-filer som samsvarer med ISO 20022-betalingsbehandlingsstandarder og XML-formatet, som angitt av EPC.

## <a name="how-is-a-credit-transfer-implemented"></a>Hvordan implementeres SEPA-kredittoverføringer?
Betalingsformatet for kredittoverføringer for EU-land implementeres ved hjelp av Generell elektronisk rapportering- og Betalingsmåter-funksjonaliteten i Microsoft Dynamics 365 for Finance and Operations, Enterprise edition. Noen får kredittoverføringsformater som brukes i andre områder, bruker fremdeles det eldre betalingsrammeverket. Det er blant annet tolv filformater for ISO 20022-kredittoverføring som er tilgjengelig. Disse eksportformatene overholder SEPA ISO 20022 XML-standarden. De brukes til å generere ikke-euro-betalingsoverføringer for land/områder der de brukes, og euro-betalinger som er angitt i versjon 8.2 av SEPA-kredittoverføringsreglene som EPC utgir. Før du kan implementere kredittoverføringer må du kontakte banken din for å få programvaren som kreves for å laste opp filer for elektroniske banktjenester. Du vil bruke denne programvaren til å overføre XML-filene som inneholder betalingsordrer til banken.

## <a name="what-credit-transfer-formats-are-currently-supported-in-finance-and-operations"></a>Hvilke kredittoverføringsformater støttes i Finance and Operations?
Du bør alltid gå til det delte ativabiblioteket i Microsoft Dynamics Lifecycle services (LCS) og viser den mest oppdaterte listen over tilgjengelige filer som har en aktivatypen **TYSK konfigurasjon**. Den neste delen, "Hva må jeg konfigurere?", inneholder en kobling til emnet som forklarer hvordan du oppretter et LCS-repositorium for å se gjennom tilgjengelige konfigurasjoner og importere valgte konfigurasjoner.

## <a name="what-do-i-have-to-set-up"></a>Hva må jeg konfigurere?
-   Før du kan opprette kredittoverføringsfiler må minst én aktiv kredittoverføringskonfigurasjon importeres til ER-konfigurasjonene. hvis du vil ha mer informasjon, kan du se [Laste ned elektroniske rapporteringskonfigurasjoner fra Lifecycle Services](../../dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).
-   Når du konfigurerer betalingsmåter for leverandør, merker du av for **Generell elektronisk rapportering** og velger riktig kredittoverføringsformat (for eksempel **ISO 20022-kredittoverføring (AT)**) som eksportformatkonfigurasjon.
-   Du må også angi juridisk enhet og bankkontoinformasjon i Finance and Operations.
-   Bankkontonumre, IBAN-er og noen ganger SWIFT-koder (BIC-er) eller andre ID-er som er nødvendige for å opprette gyldige kredittoverføringsbetalinger. Derfor må du definere dem for leverandørens bankkonto og bankkontoen for organisasjonen som ber om overføringen.
-   Ytterligere informasjon kan være nødvendig, for eksempel merverdiavgifttall (mva) for partene som refereres i kredittoverføringsmeldingen. Denne informasjonen må defineres for leverandører og den juridiske enheten etter behov.
-   Noen betalingsmåter for leverandør, for det meste ISO 20022-baserte betalingsmåter, kan kreve ekstra oppsett for **Kodesett for betalingsformat**, som **Tjenestetype** = **SLEV**. Disse kodene brukes som ekstra koding for betalingstransaksjoner under betalingsbehandling. Standardverdier for betalingskoder, som **Kategoriformål**, **Betalingsansvarlig for gebyr**, **Lokalt instrument** og **Tjenestenivå** kan angis på to steder. Er det første stedet er **hodet for leverandørbetalingsjournal** og det andre er **betalingsmåter for leverandør**. Ved oppretting av journallinjer for betaling, blir betalingskodeverdiene som er angitt på betalingsjournalhodet, overført til en kladdelinje, og hvis ikke angitt, brukes verdiene fra betalingsmåter.

## <a name="what-parameters-are-available-for-generating-credit-transfer-payments"></a>Hvilke parametere er tilgjengelige for generering av kredittoverføringsbetalinger?
Listen over spesifikke parametere avhenger av kredittoverføringsformatet. Tabellen nedenfor viser parameterne som er tilgjengelige når du genererer en betalingsfil for ISO 20022-kredittoverføring for Tyskland i leverandørbetalingsjournalen. Ved hjelp av alternativene som er tilgjengelige på i kategorien **Kjør i bakgrunnen**, kan du kjøre betalingsgenerering i satsvis modus.

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
<li><strong>Strukturert</strong> – Velg dette alternativet for å bruke det strukturerte formatet når én betalingslinje utlignes mot én faktura. Dette alternativet er ikke tilgjengelig for de lands-/områdespesifikke eksportformatene for Frankrike, Tyskland eller Nederland.</li>
<li><strong>Ustrukturert</strong> – Velg dette alternativet for å bruke det ustrukturerte formatet når betalingen utlignes mot flere fakturaer. Fakturanumrene for de utlignede fakturaene slås sammen og brukes som remisseinformasjon. I samsvar med ISO 20022-retningslinjer er ustrukturert remisseinformasjon begrenset til 140 tegn.</li>
</ul></td>
</tr>
<tr class="even">
<td>Antall fakturaer</td>
<td>Angi antall fakturaer som <strong>Betalingsmelding</strong>-rapporten skrives ut fra.</td>
</tr>
<tr class="odd">
<td>Serienummer</td>
<td>Angi et serienummer som identifiserer filen. Serienummeret vises i <strong>Deltakernotat</strong>-rapporten.</td>
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
IBAN (International Bank Account Number) og BIC (Bank Identifier Code) brukes til å identifisere kontoer i mange land/områder over hele verden. Disse inkluderer de 34 SEPA-land/-områdene. Angi BIC i **SWIFT-kode**-feltet og IBAN i **IBAN**-feltet. For både kreditors bankkonto og kundens bankkonto er disse feltene plassert på **Tilleggsidentifikasjon**-hurtigkategorien i kategorien **Bankkonto** på siden **Bankkontoer**. Bruk av BIC for SEPA-betalinger fremtvinges ikke lenger.

## <a name="how-do-i-transmit-a-payment-file-to-the-bank"></a>Hvordan sender jeg en betalingsfil til banken?
Når du genererer betalinger, genereres betalingsfilen, og du blir bedt om å lagre den fra webleseren og til en hvilken som helst plassering. Det neste trinnet er å sende XML-filen til banken. Denne prosessen varierer fra bank til bank. Følg instruksjonene fra banken din når du skal sende filer til banken for behandling.




