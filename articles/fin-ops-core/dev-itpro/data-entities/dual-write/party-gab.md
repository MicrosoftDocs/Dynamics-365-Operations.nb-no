---
title: Part og global adressebok
description: Dette emnet beskriver funksjonaliteten for part og global adressebok for dobbel skriving.
author: RamaKrishnamoorthy
ms.date: 02/22/2021
ms.topic: article
ms.service: dynamics-ax-applications
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2021-02-22
ms.openlocfilehash: e7bec58f8094a1448017822e7d8840368cc482b8
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5750794"
---
# <a name="party-and-global-address-book"></a>Part og global adressebok

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Part og global adressebok er konsepter i Finance and Operations-programmer. En part kan være en organisasjon eller en person. Det er praktisk å lagre og administrere egenskapene til en **part** globalt, for eksempel navn, språk, kontakter og adresser. Når en egenskapsverdi endres ett sted, gjenspeiles den alle steder der **parten** er involvert.

## <a name="party"></a>Part

En *part* er en person eller en organisasjon som er involvert i bedriften. Ved hjelp av partskonseptet kan en person eller en organisasjon ha flere roller (arbeider, kunde, leverandør eller kontakt) i en virksomhet. Rollen er basert på konteksten og formålet. Her er noen eksempler fra to fiktive virksomheter, Contoso og Fabrikam.

+ **Arbeider**: En ansatt. For eksempel en ansatt hos Contoso.
+ **Leverandør**: En leverandørorganisasjon, eller en enkelt innehaver som leverer varer eller tjenester til en virksomhet. Hvis for eksempel Fabrikam selger forsyninger til Contoso, får Fabrikam rollen som leverandør.
+ **Kontakt**: En person som kan kontaktes. Hvis Contoso for eksempel kjøper forsyninger fra Fabrikam, vil en ansatt hos Contoso kontakte kontakten hos Fabrikam.
+ **Kunde**: En kunde er en person eller et firma som kjøper ting fra et firma. Hvis Contoso for eksempel kjøper forsyninger fra Fabrikam, er Contoso en kunde hos Fabrikam.

Partsmodellen brukes ofte til å representere middels til komplekse relasjoner mellom organisasjoner og personer, spesielt når en part spiller mer enn én rolle. Her er noen vanlige eksempler:

+ En part kan være både en kunde og en leverandør. I Nord-Amerika selger for eksempel Fabrikam elektriske kabler til Contoso og kjøper ferdig monterte høyttalere fra Contoso. I Europa selger Fabrikam deler til Contoso, men kjøper ikke noe fra Contoso.
+ En part kan være både en ansatt og en kunde. En ansatt hos Contoso kjøper for eksempel elektronikk fra Contoso til personlig bruk.
+ Det kan være en mange-til-mange-relasjon mellom en person og en organisasjon. Fabrikam leverer for eksempel servicespesialister og ansetter en plasseringskoordinator. Koordinatoren matcher servicespesialistene med arbeidsforespørsler fra flere av Fabrikams kunder. Contoso er en av kundekontoene. Når Contoso trenger en spesialist, kontakter Contoso koordinatoren, som deretter legger til rette for forespørselen. Koordinatoren håndterer forespørsler for alle kunder og oppretter en mange-til-mange-relasjon.

Følgende bilde viser datamodellen for part:

![Datamodell for part](media/party-gab-image1.png)

> [!Tip]
> Når du prøver å opprette en ny kontopost, bruker du "Part"-feltet til å søke etter posten per navn. Hvis du finner posten, trenger du bare å velge posten. Systemet fyller automatisk ut alle dataene fra parten. Du trenger ikke angi alle de nødvendige feltene manuelt. Du finner denne virkemåten på Konto-, Kontakt- og Leverandør-skjemaene som følger med.

Ikke alle partsroller i Finance and Operations-apper støttes av dobbel skriving. Hvis du vil ha en fullstendig liste over partsroller, kan du se [Oversikt over global adressebok](../../../fin-ops/organization-administration/overview-global-address-book.md).

### <a name="global-address-book"></a>Global adressebok

Den globale adresseboken er en katalog med postadresser og elektroniske adresser til organisasjonene og personene som deltar i en virksomhet.

Den globale adresseboken lagrer og håndterer så mange postadresser og elektroniske adresser som nødvendig. La oss for eksempel anta at Fabrikam har bensinstasjoner på 50 lokasjoner. Hver lokasjon har separat postadresse, e-postadresse og telefonnummer. Alle forretningskjøp faktureres til hovedbensinstasjonen, men innkjøp sendes direkte til den bestemte bensinstasjonen som anmodet om innkjøpet. Den globale adresseboken lagrer hovedbensinstasjonen som fakturaadresse, og hver bensinstasjon som leveringsadresse for Fabrikam. Adressene kan lagres én gang og hentes etter behov for tilbud og ordrer.

En person eller en organisasjon kan ha mer enn én rolle, basert på forretningskonteksten. Når de gjør dette, kan det hende at postadressene og de elektroniske adressene er like. I så fall skal en adresseendring i én rolle vises for den andre rollen, og omvendt. Den globale adresseboken lagrer og håndterer adresser globalt.

![Datamodell for global adressebok](media/party-gab-image2.png)

## <a name="contacts"></a>Kontakter

I Customer Engagement-apper er en *kontakt* en person. **Kontakt**-tabellen har imidlertid blitt overbelastet for å representere en person, en portalbruker, en B2C-kunde eller en leverandør. Representasjonen er implisitt, og du kan ikke se forskjellen uten å se nærmere på tilknyttede transaksjoner. **Kontakt**-tabellen er begrenset til å ha et 1:1-forhold med **Konto**-tabellen. Som en del av en modell med part og global adressebok innfører dobbel skriving eksplisitte egenskaper for klaassifisering, og dobbel skriving tillater N:N-relasjoner mellom en **kontakt** og en organisasjon (Konto-enhet eller Leverandør-enhet).

Det finnes to typer **Kontakt**-rader:

+ Stripet kontakt – Kontakt-rad med en obligatorisk verdi i **Firma**-feltet.
+ Ustripet kontakt – Kontakt-rad med tomt **Firma**-felt.

**Kontakt**-tabellen kan lagre disse radtypene:

Radtype | beskrivelse
---|---
En person som er kunde, for eksempel en salgbar kontakt eller B2C-kunde. | En stripet kontaktoppføring der **Firma**-feltet ikke er tomt, og der **Er kunde**-feltet er angitt til **Ja**.
En person som er leverandør, for eksempel en enkelt innehaver som leverandør. | En stripet kontaktoppføring der **Firma**-feltet ikke er tomt, og der **Er leverandør**-feltet er angitt til **Ja**.
En person som er både en kunde og en leverandør. | En stripet kontaktoppføring der **Firma**-feltet ikke er tomt, **Er kunde**-feltet er angit til **Ja** og **Er leverandør**-feltet er angitt til **Ja**. En person kan være både en produsent for ett produkt og en forbruker for et annet produkt. Både Finance and Operations-apper dobbel skriving støtter denne relasjonen.
En person som er kontaktperson for en organisasjon, men ikke kunde eller leverandør. | En ustripet kontaktoppføring der **Firma**-feltet er tomt, **Er kunde**-feltet er angitt til **Nei** og **Er leverandør**-feltet er angitt til **Nei**.

## <a name="contact-for-party"></a>Kontakt for part

**Kontakt for part** lagrer og håndterer N:N-relasjoner mellom **Konto**-rader og **Kontakt**-rader. Den kan filtrere ut de stripede **Kontakt**-radene fra ustripede rader og tilknytte bare de ustripede **Kontakt**-radene til **Konto**- eller **Leverandør**-rader.

Natasha Jones og Miguel Reyes er for eksempel veterinærer som betjener gårder i nærområdet. Natasha betjener Seattle-området, og Miguel opererer i Kent. I Customer Engagement-appen er gårdene representert som kunder, og veterinærene er kontaktpersoner. En enkelt **Kontakt**-post for Natasha er tilknyttet alle gårdene som Natasha arbeider med. På samme måte er en enkelt **Kontakt**-post for Miguel tilknyttet alle gårdene som Miguel arbeider med.

Disse relasjonene er lagret i tabellen **Kontakt for part**. Du kan finne informasjonen i de medfølgende skjemaene:

+ Når du er i **Konto**-skjemaet, finnes det en fane med navnet **Tilknyttede kontakter**. Bruk denne fanen til å knytte én eller flere kontakter til **Konto**-raden. I dette skjemaet tilordner du en kontaktperson for en organisasjon. Når du har tilordnet kontakter, kan du velge en som primærkontakt for denne kontoen. Ved hjelp **Hurtigopprett**-skjemaet kan du bare velge en kontaktperson. Virkemåten er den samme som når du bruker **Leverandør**-skjemaet, og posttypen er **Organisasjon**.
+ Når du er i **Kontakt**-skjemaet og raden er en kunde eller leverandør eller begge deler (en stripet kontakt), finnes det en fane med navnet **Tilknyttede kontakter**. Bruk denne fanen til å tilknytte én eller flere kontakter. I dette skjemaet tilordner du en kontaktperson for B2C-kunden eller -leverandøren. Når du har tilordnet kontakter, kan du velge en som primærkontakt. Ved hjelp **Hurtigopprett**-skjemaet kan du bare velge en kontaktperson.
+ Når du er i **Kontakt**-skjemaet og raden er en kontaktperson (en ustripet kontakt), finnes det en fane med navnet **Tilknyttede organisasjoner**. Bruk denne fanen til å tilknytte én eller flere kunder eller leverandører. I dette skjemaet tilordner du en kunde eller leverandør til den underliggende kontaktpersonen. Kunden eller leverandøren kan være en organisasjon, en person eller begge deler. Du kan bare velge én verdi fra de fire feltene på et gitt tidspunkt.

    ![Fanen Tilknyttede organisasjoner](media/party-gab-image3.png)

    + Hvis du velger **Part-ID**, tilordnes den underliggende kontakten til alle rollene til den valgte parten.
    + Hvis du velger **Tilknyttet kontakt**, velger du den stripede kontakten som er av typen person.
    + Hvis du velger **Tilknyttet konto** eller **Leverandør**, velger du en organisasjon.

    Uansett hva du velger, opprettes tilknytningen på partsnivå og gjelder alle rollene til parten og lagres i "Kontakt for part"-enheten.

> [!Note]
> Visningsnavnet for tabellen **Kontakt for part** i Customer Engagement-appen er **Kontakt for kunde/leverandør**.

Når du åpner en **Kontakt**-rad der **Er kunde** er **Nei** og **Er leverandør** er **Nei**, vises fanen **Tilknyttede organisasjoner**. Bruk denne fanen til å tilknytte én eller flere kunde- eller leverandørorganisasjoner til kontakten.

Når du åpner en **Kontakt**-rad der **Er kunde** er **Ja** eller **Er leverandør** er **Ja**, vises fanen **Tilknyttede kontakter**. Bruk denne fanen til å tilknytte én eller flere kontakter.

## <a name="postal-address"></a>Postadresse

En ny fane med navnet **Adresser** er innført i skjemaene **Konto**, **Kontakt** og **Leverandør**. **Adresser**-skjemaet støtter N-adresser ved å bruke et rutenett, som vist i dette bildet:

![Rutenett for postadresse](media/party-gab-image4.png)

+ Kolonnen **Postadresseroller** viser formålet med adressen.
+ **Er primær**-kolonnen viser primæradressen.
+ **Adressenummer**-kolonnen viser adresserekkefølgen.
+ Med knappen **+ Ny adresse** kan du opprette en ny adresse. Du kan opprette så mange adresser som du vil.

Feltene **Adresse 1** og **Adresse 2** på **Sammendrag**-fanen på **Konto**-skjemaet samsvarer med henholdsvis **Levering**- og **Faktura**-adressene.

![Sammendrag-fanen for postadresse](media/party-gab-image5.png)

Feltene **Adresse 1**, **Adresse 2** og **Adresse 3** på **Sammendrag**-fanen i **Kontakt**-skjemaet samsvarer med henholdsvis **Forretning**-, **Levering**- og **Faktura**-adressene.

## <a name="electronic-address"></a>Elektronisk adresse

En ny fane med navnet **Elektroniske adresser** er innført i skjemaene **Konto**, **Kontakt** og **Leverandør**. **Adresser**-skjemaet støtter N-adresser ved å bruke et rutenett, som vist i dette bildet:

![Rutenett for elektronisk adresse](media/party-gab-image6.png)

+ **Type**-kolonnen viser adressetypen.
+ **Er primær**-kolonnen viser primæradressen.
+ Kolonnen **Formål** viser formålet med den elektroniske adressen.
+ Med knappen **+ Ny elektronisk adresse** kan du opprette en ny adresse. Du kan opprette så mange adresser som du vil.

Elektroniske adresser er bare tilgjengelige i dette rutenettet. I fremtidige versjoner blir alle felter for elektroniske adresser og postadresser fjernet fra andre faner, for eksempel fanene **Sammendrag** og **Detaljer**.

## <a name="setup-instructions"></a>Installasjonsinstruksjoner

Hvis du er en eksisterende kunde med dobbel skriving, kreves følgende instruksjoner for oppsett. Ellers kan du hoppe over denne delen.

1. Stopp følgende tilordninger fordi de ikke er obligatoriske lenger. I stsedet kan du kjøre Contacts V2-tilordningen (msdyn_contactforparties).

    + CDS-kontakter v2 og Kontakter (refererer til kundekontakter)
    + CDS-kontakter v2 og Kontakter (refererer til leverandørkontakter)

2. Følgende enhetstilordninger oppdateres for partsfunksjonalitet, så den nyeste versjonen må brukes på disse tilordningene.

Tilordning | Oppdater til denne versjonen | Endringer
---|---|---
Kunder V3 (kontoer) | 1.0.0.5 |Fjernet PartyNumber og andre partsrelaterte felt som navn, personlige opplysninger, postadressefelt, elektronisk kontaktadressefelt osv.
Kunde V3 (kontakter) | 1.0.0.5 | Fjernet PartyNumber og andre partsrelaterte felt som navn, personlige opplysninger, postadressefelt, elektronisk kontaktadressefelt osv.
Leverandører V2 (msdyn_vendors) | 1.0.0.6 | Fjernet PartyNumber og andre partsrelaterte felt som navn, personlige opplysninger, postadressefelt, elektronisk kontaktadressefelt osv.
CDS-salgstilbudshoder (tilbud) | 1.0.0.6 | Erstattet kontaktpersonen med ContactforParty-referanse.
Salgsfakturahoder V2 (fakturaer) | 1.0.0.4 | Erstattet kontaktpersonen med ContactforParty-referanse.
CDS-salgsordrehoder (salesorders) | 1.0.0.5 | Erstattet kontaktpersonen med ContactforParty-referanse.
Kontakter V2 (msdyn_contactforparties) | 1.0.0.2 | Dette er en ny tilordning. Hvis du har en tidligere versjon av partsløsningen, må du oppdatere denne tilordningen kartet til den nyeste versjonen som nevnt.
Postadressesteder for CDS-part (msdyn_partypostaladdresses) | 1.0.0.1  | Dette er en ny tilordning som er lagt til som en del av forhåndsversjonen for en tidligere part.
Historikk for CDS-postadresse V2 (msdyn_postaladdresses) | | Dette er en ny tilordning som er lagt til som en del av forhåndsversjonen for en tidligere part.
CDS-postadressesteder (msdyn_postaladdresscollections) | | Dette er en ny tilordning som er lagt til som en del av forhåndsversjonen for en tidligere part.
Partskontakter V3 (msdyn_partyelectronicaddresses) | | Dette er en ny tilordning som er lagt til som en del av denne versjonen.

## <a name="templates"></a>Maler

En samling tabelltilordninger fungerer sammen for samhandling mellom parter og den globale adresseboken, som vist i følgende tabell.

Finance and Operations-app | Kundeengasjementsapp     | beskrivelse
----------------------------|-----------------------------|------------
[Kontaktpersontitler](mapping-reference.md#223) | msdyn_salescontactpersontitles |
[Kunder V3](mapping-reference.md#101) | kontoer |
[Kunder V3](mapping-reference.md#116) | kontakter |
[CDS-parter](mapping-reference.md#220) | msdyn_parties |
[Postadressesteder for CDS-part](mapping-reference.md#233) | msdyn_partypostaladdresses |
[Historikk for CDS-postadresse V2](mapping-reference.md#235) | msdyn_postaladdresses |
[Postadressesteder for CDS](mapping-reference.md#234) | msdyn_postaladdresscollections |
[CDS-salgstilbudshode](mapping-reference.md#215) | tilbud |
[CDS-salgsordrehoder](mapping-reference.md#217) | salesorders |
[Avsluttende hilsener](mapping-reference.md#222) | msdyn_complimentaryclosings |
[Kontakter V2](mapping-reference.md#221) | msdyn_contactforparties |
[Roller for beslutningstaking](mapping-reference.md#224) | msdyn_decisionmakingroles |
[Jobbfunksjoner for ansettelse](mapping-reference.md#225) | msdyn_employmentjobfunctions |
[Fordelsnivåer](mapping-reference.md#226) | msdyn_loyaltylevels |
[Partskontakter V3](mapping-reference.md#236) | msdyn_partyelectronicaddresses |
[Typer personlige tegn](mapping-reference.md#227) | msdyn_personalcharactertypes |
[Salgsfakturahoder V2](mapping-reference.md#118) | fakturaer |
[Hilsener](mapping-reference.md#228) | msdyn_salutations |
[Leverandører V2](mapping-reference.md#202) | msdyn_vendors |

Hvis du vil ha mer informasjon, kan du se [Referanse for lesetilgang til skrivetilgang](mapping-reference.md).
