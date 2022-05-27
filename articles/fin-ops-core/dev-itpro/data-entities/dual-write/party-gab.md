---
title: Part og global adressebok
description: Dette emnet beskriver funksjonaliteten for part og global adressebok for dobbel skriving.
author: RamaKrishnamoorthy
ms.date: 04/25/2022
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2021-02-22
ms.openlocfilehash: 1e2dcfa69308f6691e787a1ff1893f9080dcaef1
ms.sourcegitcommit: 1d2eeacad11c28889681504cdc509c90e3e8ea86
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/05/2022
ms.locfileid: "8717453"
---
# <a name="party-and-global-address-book"></a>Part og global adressebok

[!include [banner](../../includes/banner.md)]



*Part* og *global adressebok* er konsepter i økonomi- og driftsapper. En part kan være en organisasjon eller en person. Det er praktisk å lagre og administrere egenskapene til en part globalt, for eksempel navn, språk, kontakter og adresser. Når en egenskapsverdi endres ett sted, gjenspeiles den alle steder der parten er involvert.

## <a name="party"></a>Part

En part er en person eller en organisasjon som er involvert i en bedrift. Når et partskonsept brukes, kan en person eller en organisasjon ha flere roller i en virksomhet (for eksempel arbeider, kunde, leverandør eller kontakt). Rollen er basert på konteksten og formålet. Her er noen eksempler på roller fra to fiktive virksomheter, Contoso og Fabrikam:

+ **Arbeider** – En ansatt. Et eksempel er en ansatt hos Contoso.
+ **Leverandør** – En leverandørorganisasjon, eller en enkelt innehaver som leverer varer eller tjenester til en virksomhet. Hvis for eksempel Fabrikam selger forsyninger til Contoso, er Fabrikam en leverandør for Contoso.
+ **Kontakt** – En person som kan kontaktes. Hvis Contoso for eksempel kjøper forsyninger fra Fabrikam, vil ansatte hos Contoso kontakte kontakten hos Fabrikam.
+ **Kunde** – En kunde er en person eller et firma som kjøper ting fra et firma. Hvis Contoso for eksempel kjøper forsyninger fra Fabrikam, er Contoso en kunde hos Fabrikam.

Partsmodellen brukes ofte til å representere middels til komplekse relasjoner mellom organisasjoner og personer, spesielt når en part spiller mer enn én rolle. Her er noen vanlige eksempler:

+ En part kan være både en kunde og en leverandør. I Nord-Amerika selger for eksempel Fabrikam elektriske kabler til Contoso og kjøper ferdig monterte høyttalere fra Contoso. I Europa selger Fabrikam deler til Contoso, men kjøper ikke noe fra Contoso.
+ En part kan være både en ansatt og en kunde. En ansatt hos Contoso kjøper for eksempel elektronikk fra Contoso til personlig bruk.
+ Det kan være en mange-til-mange-relasjon mellom en person og en organisasjon. Fabrikam leverer for eksempel servicespesialister og ansetter en plasseringskoordinator. Plasseringskoordinatoren matcher servicespesialistene med arbeidsforespørsler fra flere av Fabrikams kunder. Contoso er en av Fabrikams kunder. Når Contoso trenger en servicespesialist, kontakter firmaet plasseringskoordinatoren, som deretter legger til rette for forespørselen. Fordi plasseringskoordinatoren håndterer forespørsler for alle kunder, er en N:N-relasjon involvert.

Følgende bilde viser datamodellen for part.

![Datamodell for part.](media/party-gab-image1.png)

> [!TIP]
> Når du prøver å opprette en ny kontopost, bruker du **Part** -feltet til å søke etter posten per navn. Hvis du finner posten, trenger du da bare å velge posten. Systemet fyller automatisk ut alle dataene fra parten. Du trenger ikke angi alle de nødvendige feltene manuelt. Du finner denne virkemåten på **Konto-**, **Kontakt-** og **Leverandør**-sidene som følger med.

Ikke alle partsroller i økonomi- og driftsapper støttes av dobbel skriving. Hvis du vil ha en fullstendig liste over partsroller, kan du se [Oversikt over global adressebok](../../../fin-ops/organization-administration/overview-global-address-book.md).

### <a name="global-address-book"></a>Global adressebok

Den globale adresseboken er en katalog med postadresser og elektroniske adresser til organisasjonene og personene som deltar i en virksomhet.

Den globale adresseboken lagrer og håndterer så mange postadresser og elektroniske adresser som nødvendig. La oss for eksempel anta at Fabrikam har bensinstasjoner på 50 lokasjoner. Hver lokasjon har separat postadresse, e-postadresse og telefonnummer. Alle forretningskjøp faktureres til hovedbensinstasjonen, men sendes direkte til den bestemte bensinstasjonen som anmodet om innkjøpet. Den globale adresseboken lagrer hovedbensinstasjonen som fakturaadresse for Fabrikam, og lagrer hver bensinstasjon som leveringsadresse. Adressene kan lagres én gang og hentes etter behov for tilbud og ordrer.

Det kan hende at en person eller en organisasjon spiller mer enn én rolle, og den samme postadressen og den elektroniske adressen kan brukes for alle rollene, avhengig av forretningskonteksten. I så fall skal en adresseendring i én rolle vises i alle de andre rollene. Den globale adresseboken lagrer og håndterer adresser globalt.

Illustrasjonen nedenfor viser datamodellen for den globale adresseboken.

![Datamodell for den globale adresseboken.](media/party-gab-image2.png)

## <a name="contact"></a>Kontakt

I Customer Engagement-apper er en kontakt en person. **Kontakt**-tabellen har imidlertid blitt overbelastet for å representere en person, en portalbruker, en forretning-til-forbruker (B2C)-kunde eller en leverandør. Representasjonen er implisitt, og du kan ikke se forskjellen uten å se nærmere på tilknyttede transaksjoner. **Kontakt**-tabellen er begrenset til å ha et 1:1-forhold med **Konto**-tabellen. Som en del av en modell med part og global adressebok innfører dobbel skriving eksplisitte egenskaper for klassifisering og tillater N:N-relasjoner mellom en kontakt som er er person, og en organisasjon (**Konto**-enhet eller **Leverandør**-enhet).

Det finnes to typer **Kontakt**-rader:

+ **Stripet kontakt** – En **Kontakt**-rad der **Firma**-feltet har en obligatorisk verdi.
+ **Ustripet kontakt** – En **Kontakt**-rad med tomt **Firma**-felt.

**Kontakt**-tabellen kan lagre disse radtypene.

| Radtype | beskrivelse |
|----------|-------------|
| En person som er kunde (for eksempel en salgbar kontakt eller B2C-kunde) | En stripet kontaktoppføring der **Firma**-feltet ikke er tomt, og der **Er kunde**-feltet er angitt til **Ja**. |
| En person som er leverandør (for eksempel en enkelt innehaver som leverandør) | En stripet kontaktoppføring der **Firma**-feltet ikke er tomt, og der **Er leverandør**-feltet er angitt til **Ja**. |
| En person som er både en kunde og en leverandør | En stripet kontaktoppføring der **Firma**-feltet ikke er tomt, **Er kunde**-feltet er angit til **Ja** og **Er leverandør**-feltet er angitt til **Ja**. En person kan være både en produsent for ett produkt og en forbruker for et annet produkt. Både økonomi- og driftsapper og dobbel skriving støtter denne relasjonen. |
| En person som er kontaktperson for en organisasjon, men ikke kunde eller leverandør | En ustripet kontaktoppføring der **Firma**-feltet er tomt, **Er kunde**-feltet er angitt til **Nei** og **Er leverandør**-feltet er angitt til **Nei**. |

## <a name="contact-for-party-table"></a>Kontakt for part-tabell

Tabellen **Kontakt for part** lagrer og håndterer N:N-relasjoner mellom **Konto**-rader og **Kontakt**-rader. Den kan filtrere ut de stripede **Kontakt**-radene fra ustripede rader og tilknytte bare de ustripede **Kontakt**-radene til **Konto**- eller **Leverandør**-rader.

Natasha Jones og Miguel Reyes er for eksempel veterinærer som betjener gårder i nærområdet. Natasha betjener Seattle-området, og Miguel opererer i Kent. I Customer Engagement-appen er gårdene representert som kunder, og veterinærene som kontaktpersoner. En enkelt **Kontakt**-post for Natasha er tilknyttet alle gårdene som Natasha arbeider med. På samme måte er en enkelt **Kontakt**-post for Miguel tilknyttet alle gårdene som Miguel arbeider med.

Disse relasjonene er lagret i tabellen **Kontakt for part**. Du finner denne informasjonen på **Konto-**, **Kontakt-** og **Leverandør**-sidene som følger med:

+ På **Konto**-siden kan du bruke kategorien **Tilknyttede kontakter** til å knytte én eller flere kontakter til **Konto**-raden. På denne måten tilordner du en kontaktperson for en organisasjon. Du kan deretter velge én kontakt som primærkontakt for kontoen. Hvis du bruker **hurtigoppretting**-siden, kan du bare velge en kontaktperson. Virkemåten er den samme som når du bruker **Leverandør**-siden, og posttypen er **Organisasjon**.
+ Når raden er en kunde, leverandør eller begge deler på **Kontakt**-siden, kan du bruke kategorien **Tilknyttede kontakter** til å knytte én eller flere kontakter. På denne måten tilordner du kontaktpersoner for B2C-kunden eller -leverandøren. Du kan deretter velge én kontakt som primærkontakt. Hvis du bruker **hurtigoppretting**-siden, kan du bare velge en kontaktperson.
+ Når raden er en kontaktperson på **Kontakt**-siden (en ustripet kontakt), kan du bruke kategorien **Tilknyttede kontakter** til å knytte én eller flere kontakter eller leverandører. På denne måten tilordner du kunder eller leverandører til den underliggende kontaktpersonen. Kunden eller leverandøren kan være en organisasjon, en person eller begge deler. Du kan bare velge én verdi fra ett de fire feltene om gangen:

    + Hvis du velger en verdi i **Part-ID**-feltet, tilordnes den underliggende kontakten til alle rollene til den valgte parten.
    + Hvis du velger verdi i feltet **Tilknyttet kontakt**, velger du den stripede kontakten som er av typen **Person**.
    + Hvis du velger en verdi i feltet **Tilknyttet konto** eller **Tilknyttet leverandør**, velger du en organisasjon.

    ![Kategorien Tilknyttede organisasjoner på kontaktsiden.](media/party-gab-image3.png)

    Uansett hva du velger, opprettes tilknytningen på partsnivå og gjelder alle rollene til parten og lagres i **Kontakt for part**-enheten.

> [!NOTE]
> Visningsnavnet for tabellen **Kontakt for part** i Customer Engagement-apper er **Kontakt for kunde/leverandør**.

Når du åpner en **Kontakt**-rad der både **Er kunde**-feltet og **Er leverandør** er satt til **Nei**, vises kategorien **Tilknyttede organisasjoner**. Bruk denne kategorien til å knytte én eller flere kunde- eller leverandørorganisasjoner til kontakten.

Når du åpner en **Kontakt**-rad der enten **Er kunde**-feltet eller **Er leverandør** er satt til **Ja**, vises kategorien **Tilknyttede kontakter**. Bruk denne fanen til å tilknytte én eller flere kontakter.

## <a name="postal-addresses"></a>Postadresser

En ny fane med navnet **Adresser** er innført på sidene **Konto**, **Kontakt** og **Leverandør**. Denne kategorien støtter flere postadresser ved hjelp av et rutenett, som vist i illustrasjonen nedenfor.

![Rutenett for postadresser.](media/party-gab-image4.png)

Rutenettet inneholder følgende kolonner:

+ **Postadresseroller** – formålet med postadressen.
+ **Er primær** – En verdi som angir om adressen er primæradressen.
+ **Adressenummer** – Adresseordren.

Du kan bruke **Ny adresse**-knappen over rutenettet til å opprette så mange postadresser du vil.

Feltene **Adresse 1** og **Adresse 2** på **Sammendrag**-fanen på **Konto**-siden samsvarer med henholdsvis **Levering**- og **Faktura**-adressene.

![Sammendrag-fanen for postadresser.](media/party-gab-image5.png)

Feltene **Adresse 1**, **Adresse 2** og **Adresse 3** på **Sammendrag**-fanen i **Kontakt**-siden samsvarer med henholdsvis **Forretning**-, **Levering**- og **Faktura**-adressene.

## <a name="electronic-addresses"></a>Elektroniske adresser

En ny fane med navnet **Elektroniske adresser** er innført på sidene **Konto**, **Kontakt** og **Leverandør**. Denne kategorien støtter flere elektroniske adresser ved hjelp av et rutenett, som vist i illustrasjonen nedenfor.

![Rutenett for elektroniske adresser.](media/party-gab-image6.png)

Rutenettet inneholder følgende kolonner:

+ **Type** – Typen elektronisk adresse.
+ **Er primær** En verdi som angir om adressen er primæradressen.
+ **Formål** – Formålet med den elektroniske adressen.

Du kan bruke **Ny elektronisk adresse**-knappen over rutenettet til å opprette så mange adresser du vil.

I løpet av kvalifiseringsprosessen kan du oppgi både et bedriftstelefonnummer og et mobiltelefonnummer. Forretningstelefonnummeret regnes som det primære telefonnummeret hvis **IsMobile=Nei**, og mobiltelefonnummeret regnes som det sekundære telefonnummeret hvis **IsMobile=Ja**.

> [!TIP]
> Bruk kategoriene **Adresser** og **Elektroniske adresser** på skjemaene **Konto** og **Kontakt** til å administrere post- og elektroniske adresser. Dette sikrer at adressedata synkroniseres med økonomi- og driftsapper.

## <a name="setup"></a>Installasjon

1. Åpne appmiljøet for kundeengasjement.

2. Installer alle løsningene som kreves, som beskrevet i [Separert programiverksettingspakke med dobbel skriving](separated-solutions.md).

3. Installer [Løsninger for part med dobbel skriving og global adressebok](https://aka.ms/dual-write-gab).

4. Åpne Finance and Operations-appen. Gå til Databehandling-modulen, og velg fanen Dobbel skriving. Siden for administrasjon av dobbel skriving åpnes.

5. Bruk begge løsningene som ble installert i trinn 2 og 3, ved hjelp av funksjonen [Bruk løsning](link-your-environment.md).

6. Stopp følgende tilordninger fordi de ikke er obligatoriske lenger. I stedet kjører du `Contacts V2 (msdyn_contactforparties)`-tilordningen.

    + CDS-kontakter v2 og Kontakter (refererer til kundekontakter)
    + CDS-kontakter v2 og Kontakter (refererer til leverandørkontakter)

7. Følgende enhetstilordninger oppdateres for partsfunksjonalitet, så den nyeste versjonen må brukes på disse tilordningene.

    Tilordning | Oppdater til denne versjonen | Endringer
    ---|---|---
    `CDS Parties (msdyn_parties)`| 1.0.0.2 | Dette er en ny tilordning som er lagt til som en del av denne versjonen.
    `Contacts V2 (msdyn_contactforparties)`| 1.0.0.6 | Dette er en ny tilordning som er lagt til som en del av denne versjonen.
    `Customers V3 (accounts)` | 1.0.0.5 |Fjernet `PartyNumber` og andre partsrelaterte felt som navn, personlige opplysninger, postadressefelt og elektronisk kontaktadressefelt.
    `Customer V3 (contacts)` | 1.0.0.5 | Fjernet `PartyNumber` og andre partsrelaterte felt som navn, personlige opplysninger, postadressefelt og elektronisk kontaktadressefelt.
    `Vendors V2 (msdyn_vendors)` | 1.0.0.6 | Fjernet `PartyNumber` og andre partsrelaterte felt som navn, personlige opplysninger, postadressefelt og elektronisk kontaktadressefelt.
    `CDS Sales quotation headers (quotes)` | 1.0.0.7 | Erstattet kontaktpersonen med `ContactforParty`-referanse.
    `Sales invoice headers V2 (invoices)` | 1.0.0.4 | Erstattet kontaktpersonen med `ContactforParty`-referanse.
    `CDS Sales order headers (salesorders)` | 1.0.0.5 | Erstattet kontaktpersonen med `ContactforParty`-referanse.
    `CDS Party postal address locations (msdyn_partypostaladdresses)` | 1.0.0.1  | Dette er en ny tilordning som er lagt til som en del av denne versjonen.
    `CDS postal address history V2 (msdyn_postaladdresses)` | 1.0.0.2 | Dette er en ny tilordning som er lagt til som en del av denne versjonen.
    `CDS postal address locations (msdyn_postaladdresscollections)` | 1.0.0.0 | Dette er en ny tilordning som er lagt til som en del av denne versjonen.
    `Party Contacts V3 (msdyn_partyelectronicaddresses)` | 1.0.0.0 | Dette er en ny tilordning som er lagt til som en del av denne versjonen.
    `Complimentary Closings (msdyn_compliemntaryclosings)` | 1.0.0.0 | Dette er en ny tilordning som er lagt til som en del av denne versjonen.
    `Decision making roles (msdyn_decisionmakingroles)` | 1.0.0.0 | Dette er en ny tilordning som er lagt til som en del av denne versjonen.
    `Loyalty levels (msdyn_loyaltylevels)` | 1.0.0.0 | Dette er en ny tilordning som er lagt til som en del av denne versjonen.
    `Contact person titles (msdyn_salescontactpersontitles)` | 1.0.0.0 | Dette er en ny tilordning som er lagt til som en del av denne versjonen.
    `Personal character types (msdyn_personalcharactertypes)` | 1.0.0.0 | Dette er en ny tilordning som er lagt til som en del av denne versjonen.
    `Salutations (msdyn_salutations)` | 1.0.0.0 | Dette er en ny tilordning som er lagt til som en del av denne versjonen.
    `Employment job functions (msdyn_employmentjobfunctions)` | 1.0.0.0 | Dette er en ny tilordning som er lagt til som en del av denne versjonen.
    `CDS Address roles (msdyn_addressroles)` | 1.0.0.0 | Dette er en ny tilordning som er lagt til som en del av denne versjonen.

8. Før du kjører tilordningene ovenfor, må du oppdatere integreringsnøklene manuelt som beskrevet i fremgangsmåten nedenfor. Velg deretter **Lagre**.

    | Tilordning | Nøkler |
    |-----|------|
    | Konto |  accountnumber [Kontonummer]<br>msdyn_company.cdm_companycode [Selskap (Selskapskode)] |
    | Kontakt | msdyn_contactpersonid [Kontonummer/Kontaktperson-ID]<br>msdyn_company.cdm_companycode [Selskap (Selskapskode)] |
    | Kontakt for kunde/leverandør | msdyn_contactforpartynumber [Kontakt for partsnummer]<br>msdyn_associatedcompanyid.cdm_companycode [Tilknyttet selskap (Firmakode)] |
    | Leverandør | msdyn_vendoraccountnumber [Leverandørens kontonummer]<br>msdyn_company.cdm_companycode [Selskap (Selskapskode)]|

9. I Dataverse har tegngrensene for duplikatregistreringsregler økt fra 450 til 700 tegn. Ved hjelp av denne grensen kan du legge til en eller flere nøkler i duplikatregistreringsreglene. Utvid duplikatregistreringsregelen for **Kontoer**-tabellen ved å angi følgende felt.

    | Felt | Verdi |
    |-------|-------|
    | Navn | Kontoer med samme kontonavn. |
    | beskrivelse | Oppdager kontoposter som har samme verdi i kontonavnattributtet. |
    | Basisposttype | Konto |
    | Samsvarende posttype | Konto |
    | Kontonavn (felt) | Nøyaktig samsvar |
    | Firma (felt) | Nøyaktig samsvar |
    | Relasjonstype (felt) | Nøyaktig samsvar |
    | Parts-ID (felt) | Nøyaktig samsvar |
    | Velg (felt) | (tomt) |

    ![Duplikatregel for kontoer.](media/duplicate-rule-1.PNG)

10. Utvid duplikatregistreringsregelen for **Kontakter**-tabellen ved å angi følgende felt.

    | Felt | Verdi |
    |-------|-------|
    | Navn | Kontakter med samme fornavn og etternavn. |
    | beskrivelse | Oppdager kontaktposter som har de samme verdiene i fornavn- og etternavn-feltene. |
    | Basisposttype | Kontakt |
    | Samsvarende posttype | Kontakt |
    | Fornavn (felt) | Nøyaktig samsvar |
    | Etternavn (felt) | Nøyaktig samsvar |
    | Firma (felt) | Nøyaktig samsvar |
    | Parts-ID (felt) | Nøyaktig samsvar |
    | Velg (felt) | (tomt) |

    ![Duplikatregel for kontakter.](media/duplicate-rule-2.PNG)

11. Hvis du er en eksisterende kunde med dobbel skriving, følger du instruksjonene i [Oppgrader til parten og den globale adressebokmodellen](upgrade-party-gab.md) og oppgraderer dataene. **Ikke gå videre til trinn 12 uten å fullføre dette trinnet.** Hvis du er en ny bruker av dobbel skriving, kan du gå videre til trinn 12.

12. Hvis du er en eksisterende bruker av dobbel skriving, fullfører du trinn 11, og deretter kan du kjøre tilordningene i denne rekkefølgen: Hvis du er en ny kunde av dobbel skriving, kan du fortsette direkte. Hvis du får en feilmelding som angir at "prosjektvalidering mislyktes. Manglende målfelt...", åpner du kartet og velger **Oppdater tabeller** og kjører deretter kartet.

    Økonomi- og driftsapper | Kundeengasjementsapp  
    ----------------------------|------------------------
    [CDS-parter](mapping-reference.md#220) | msdyn_parties
    [Postadressesteder for CDS](mapping-reference.md#234) | msdyn_postaladdresscollections
    [Historikk for CDS-postadresse V2](mapping-reference.md#235) | msdyn_postaladdresses
    [Postadressesteder for CDS-part](mapping-reference.md#233) | msdyn_partypostaladdresses
    [Partskontakter V3](mapping-reference.md#236) | msdyn_partyelectronicaddresses
    [Kunder V3](mapping-reference.md#101) | kontoer
    [Kunder V3](mapping-reference.md#116) | kontakter
    [Leverandører V2](mapping-reference.md#202) | msdyn_vendors
    [Kontaktpersontitler](mapping-reference.md#223) | msdyn_salescontactpersontitles
    [Avsluttende hilsener](mapping-reference.md#222) | msdyn_complimentaryclosings
    [Hilsener](mapping-reference.md#228) | msdyn_salutations
    [Roller for beslutningstaking](mapping-reference.md#224) | msdyn_decisionmakingroles
    [Jobbfunksjoner for ansettelse](mapping-reference.md#225) | msdyn_employmentjobfunctions
    [Fordelsnivåer](mapping-reference.md#226) | msdyn_loyaltylevels
    [Typer personlige tegn](mapping-reference.md#227) | msdyn_personalcharactertypes
    [Kontakter V2](mapping-reference.md#221) | msdyn_contactforparties
    [CDS-salgstilbudshode](mapping-reference.md#215) | tilbud
    [CDS-salgsordrehoder](mapping-reference.md#217) | salesorders
    [Salgsfakturahoder V2](mapping-reference.md#118) | fakturaer
    [CDS-adresseroller](mapping-reference.md#301) | msdyn_addressroles

> [!NOTE]
> Kartet `CDS Contacts V2 (contacts)` er kartet som du stoppet i trinn 1. Når du prøver å kjøre andre kart, kan disse 2 kartene vises i listen over avhengige kart. Ikke kjør disse kartene.
>
> Hvis parten og den globale adressebokløsningen er installert, må du deaktivere plugin-modulen kalt `Microsoft.Dynamics.SCMExtended.Plugins.Plugins.LeadPrimaryContactPostCreate: QualifyLead of lead`. Hvis du avinstallerer parten og den globale adressebokløsningen, må du aktivere plugin-modulen på nytt.
>
> Feltet `msdyn_*partynumber` (ett enkelt linjetekstfelt) som er inkludert i tabellene for **konto**, **kontakt** og **leverandør**, skal ikke brukes fremover. Etikettnavnet har prefikset **(Avskrevet)** for klarhet. I stedet bruker du **msdyn_partyid**-feltet. Feltet er et oppslag i **msdyn_party**-tabellen.
>
> Tabellnavn | Gammelt felt | Nytt felt
> --------|-------|--------
> Konto | `msdyn_partynumber` | `msdyn_partyid`
> Kontakt | `msdyn_partynumber` | `msdyn_partyid`
> msdyn_vendor | `msdyn_vendorpartynumber` | `msdyn_partyid`

## <a name="templates"></a>Maler

En samling tabelltilordninger fungerer sammen for samhandling mellom parter og den globale adresseboken, som vist i følgende tabell.

| Økonomi- og driftsapper | Kundeengasjementsapp | Beskrivelse |
|----------------------------|-------------------------|-------------|
| [Kontaktpersontitler](mapping-reference.md#223) | msdyn\_salescontactpersontitles |
| [Kunder V3](mapping-reference.md#101) | kontoer |
| [Kunder V3](mapping-reference.md#116) | kontakter |
| [CDS-parter](mapping-reference.md#220) | msdyn\_parties |
| [Postadressesteder for CDS-part](mapping-reference.md#233) | msdyn\_partypostaladdresses |
| [Historikk for CDS-postadresse V2](mapping-reference.md#235) | msdyn\_postaladdresses |
| [Postadressesteder for CDS](mapping-reference.md#234) | msdyn\_postaladdresscollections |
| [CDS-salgstilbudshode](mapping-reference.md#215) | tilbud |
| [CDS-salgsordrehoder](mapping-reference.md#217) | salesorders |
| [Avsluttende hilsener](mapping-reference.md#222) | msdyn\_complimentaryclosings |
| [Kontakter V2](mapping-reference.md#221) | msdyn\_contactforparties |
| [Roller for beslutningstaking](mapping-reference.md#224) | msdyn\_decisionmakingroles |
| [Jobbfunksjoner for ansettelse](mapping-reference.md#225) | msdyn\_employmentjobfunctions |
| [Fordelsnivåer](mapping-reference.md#226) | msdyn\_loyaltylevels |
| [Partskontakter V3](mapping-reference.md#236) | msdyn\_partyelectronicaddresses |
| [Typer personlige tegn](mapping-reference.md#227) | msdyn\_personalcharactertypes |
| [Salgsfakturahoder V2](mapping-reference.md#118) | fakturaer |
| [Hilsener](mapping-reference.md#228) | msdyn\_salutations |
| [Leverandører V2](mapping-reference.md#202) | msdyn\_vendors |
| [CDS-adresseroller](mapping-reference.md#301) |msdyn\_addressroles|

Hvis du vil ha mer informasjon, kan du se [Referanse for lesetilgang til skrivetilgang](mapping-reference.md).

## <a name="address-roles-as-a-multi-select-drop-down-list"></a>Adresseroller som en rullegardinliste med flere valg
En postadresse eller en elektronisk adresse kan fungere som flere ting. En postadresse kan for eksempel fungere som både en fakturaadresse og en leveringsadresse. I slike tilfeller kan en bruker velge både **Faktura** og **Levering** i rullegardinlisten, som vist i illustrasjonen nedenfor. 

![Rullegardinlisten Formål/rolle.](media/purpose.png)

## <a name="known-issues-and-limitations"></a>Kjente problemer og begrensninger

+ Når du oppretter en kunde sammen med adresse og lagrer den i økonomi- og driftsapper, kan det hende at adressen ikke synkroniseres med **Adresse**-tabellen. Dette skyldes et sekvenseringsproblem med plattform for dobbel skriving. Det er mulig å omgå dette ved å opprette kunden først og lagre den. Deretter legger du til adressen.
+ Når en kundepost har en primæradresse i økonomi- og driftsapper, og du oppretter en ny kontakt for denne kunden, arver kontaktposten en primæradresse fra den tilknyttede kundeposten. Dette skjer også for leverandørkontakten. Dataverse støtter for øyeblikket ikke denne funksjonaliteten. Hvis dobbel skriving er aktivert, vil en kundekontakt som arves med en primæradresse fra økonomi- og driftsappen, synkroniseres med Dataverse sammen med adressen.
+ I økonomi- og driftsapper kan du opprette en kontaktpost fra **Legg til kontakt**-skjemaet. Når du prøver å opprette en ny kontakt fra **Vis kontakt**-skjemaet, mislykkes handlingen. Dette er et kjent problem.

    ![Kjent problem med Legg til kontakt.](media/party-gab-contact-issue.png)

+ **Innledende synkronisering** støtter ikke feltene **Tilgjengelig fra** og **Tilgjengelig til** på **ContactForParty**, fordi DIXF konverterer verdien til en streng i stedet for et heltall. Konverteringen utløser feilen `Cannot convert the literal '<say 08:00:00>' to the expected type edm.int32`.
+ Du kan ikke angi en fremtidig datert postadresse ved hjelp av en økonomi- og driftsapp med dobbel skriving, fordi Dataverse ikke støtter datogyldighet. Hvis du angir en fremtidig datert postadresse ved hjelp av en økonomi- og driftsapp, synkroniseres den fullstendig til Dataverse, og du ser adressen i brukergrensesnittet umiddelbart. Alle oppdateringer til denne posten vil føre til en feil når den er fremtidig datert og ikke gjeldende i økonomi- og driftsappen.
