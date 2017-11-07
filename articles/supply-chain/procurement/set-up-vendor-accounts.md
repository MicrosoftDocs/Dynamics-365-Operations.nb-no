---
title: "Definere leverandørkontoer"
description: "Dette emnet beskriver hva slags type informasjon du må spesifisere når du oppretter en ny leverandørkonto."
author: mkirknel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: smmContactPerson, VendBankAccounts, VendTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 191053
ms.assetid: 06168199-7c54-40e9-a038-4eb274ca958d
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: e871acb38ccfdbe8bf298ebb05b8420c55e0093f
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---

# <a name="set-up-vendor-accounts"></a>Definere leverandørkontoer

[!include[banner](../includes/banner.md)]


Dette emnet beskriver hva slags type informasjon du må spesifisere når du oppretter en ny leverandørkonto.

Når du oppretter en leverandørkonto, angir du opplysninger om leverandøren. Denne informasjonen brukes til å sette inn data i dokumenter automatisk og til å spore aktiviteten som er knyttet til leverandøren. Du kan for eksempel konfigurere følgende informasjonen for en leverandør:

-   Tilordne en leverandørgruppe. Alle leverandører må tilordnes en leverandørgruppe. Leverandørene i en leverandørgruppe har parametere som de deler. De har for eksempel samme betalingsbetingelser.
-   Konfigurer leverandøren for katalogimport. Leverandører kan angi en fil som inneholder katalogen med sine varer og tjenester. Denne filen kan lastes opp slik at ansatte kan bestille fra leverandøren.
-   Tilordne leverandøren til innkjøpskategorier.
-   La en eksisterende leverandør drive handel en annen juridisk enhet i organisasjonen.
-   Sette en leverandør på vent for bestemte typer transaksjoner.
-   Konfigurer bankinformasjon for leverandøren, slik at du kan sende betalinger elektronisk.
-   Konfigurer informasjon om mva, faktura og betaling for leverandøren. Disse innstillingene kopieres som standard til nye dokumenter som du oppretter for leverandøren.
-   Konfigurer finansdimensjoner som brukes til automatisk postering av transaksjoner for leverandøren til finanskontoer.

Hvis du vil gjøre det raskere å opprette leverandørkontoer, kan du opprette maler. Du kan opprette en mal på **Leverandør**-siden i handlingsruten ved å klikke på **Alternativer** &gt; **Postinformasjon**. Klikk deretter **Firmakontomal**. Firmakontomaler deles med andre brukere.  

Du kan også opprette en brukermal til eget bruk. Du kan ikke slette en leverandør som er knyttet til andre oppføringer, for eksempel kontakter eller produkter.

## <a name="vendor-account-numbers"></a>Leverandørens kontonumre.
Kontonummeret er en unik identifikator for en leverandør. Du kan definere kontonumre slik at de genereres automatisk når du oppretter en leverandør. Du kan også konfigurere nummerserien slik at kontonumre angis manuelt. Du kan for eksempel bruke leverandørens telefonnummer som identifikator.

## <a name="vendor-organizations-and-individual-vendors"></a>Leverandørorganisasjoner og individuelle leverandører
Når du oppretter en ny leverandørkonto, må du velge om leverandøren er en organisasjon eller en person. Valget påvirker informasjonen som du må fylle ut for leverandøren. For en person inneholder denne informasjonen fornavn, etternavn og tittel. For en organisasjon inkluderer denne informasjonen organisasjonsnummer og antall ansatte.

## <a name="addresses"></a>Adresser
Du kan definere flere adresser som brukes til forskjellige formål, for hver leverandør. Du kan for eksempel opprette en adresse som har **faktura** som formål. Eller hvis du vil betale leverandøren med sjekk, kan du definere en adresse som har **Remitter til** som formål. Hvis du må angi en adresse som skal brukes ved pengeoverføringer til utenlandske banker, blir formålet **SWIFT**.

## <a name="vendor-contacts"></a>Leverandørkontakter
Du kan lagre kontakter for en leverandør. Disse kontaktene kan brukes på dokumenter som bestillinger eller tilbudsforespørsler.  

Hvis du vil legge til kontakter for en leverandør, går du til **Alle leverandører**-siden i kategorien **Leverandør** i **Oppsett**-gruppen, og klikker på **Kontakter** &gt; **Legg til kontakter**.  

Du kan opprette leverandørkontakter fra grunnen av. Du kan også kopiere informasjon fra en annen person som allerede er registrert i Microsoft Dynamics 365 for Finance and Operations, og redigere informasjonen etter behov.  

**Merk:** Å legge til en kontakt for en leverandør er ikke det samme som å legge til kontaktinformasjon for denne leverandøren. Selv om du kan legge til generell kontaktinformasjon for en leverandør, kan du også ha flere bestemte personer som er kontakter i bedriften, og som alle har sin egen kontaktinformasjon.  

Du kan ikke slette en kontaktpersonpost hvis det refereres til kontakten i et dokument. I stedet kan du deaktivere kontakten.  

Du kan legge til leverandørkontakter i dine personlige kontakter i Microsoft Office 365. Du må imidlertid først definere synkronisering mellom Finance and Operations og Office 365 både i Microsoft Exchange Server-synkroniseringen og installasjonsveiviseren for Microsoft Outlook.

## <a name="vendors-in-different-legal-entities"></a>Leverandører i ulike juridiske enheter
Hvis en leverandør er registrert for bare én juridisk enhet i organisasjonen og andre juridiske enheter må registrere samme leverandør, kan du bruke siden **Legg til leverandør i en annen juridisk enhet** for å konfigurere leverandøren til å gjøre forretninger med en annen juridisk enhet. Du må velge en leverandørgruppe, valuta, og ventestatus for leverandøren i den valgte juridiske enheten.  

Hvis flere juridiske enheter innenfor organisasjonen gjør forretninger med den samme leverandøren, og hver juridiske enhet har en egen leverandørkonto for den leverandøren, kan du slå sammen part-ID-ene for leverandørkontoene. På denne måten kan informasjon som adresse og antall ansatte deles, slik at du bare må oppdatere dette på ett sted.  

Hvis du vil flette part-ID-er, kan du følge disse trinnene.

1.  På siden **Global adressebok** velger du postene i adresseboken som representerer leverandøren i hver juridiske enhet som skal tas med i tilordningen.
2.  Klikk **Flett poster** i handlingsruten.

## <a name="agreements"></a>Avtaler
Når du setter opp en leverandørkonto, kan det også være at du vil registrere avtalene du har med leverandøren. Du kan definere avtalene for pris og rabatt ved hjelp av handlingene på leverandørposten. Du kan også definere en kjøpsavtale på **Kjøpsavtaler**-siden.

## <a name="putting-a-vendor-on-hold"></a>Plassere en leverandør på vent
Du kan sette en leverandør på vent for forskjellige transaksjonstyper. Følgende alternativer er tilgjengelige:

-   **Ingen** – Ingen sperrer på leverandøren.
-   **Faktura** – Ingen fakturaer kan posteres for leverandøren.
-   **Alle** – Leverandøren er satt på vent for alle transaksjonstyper. Disse transaksjonstypene inkluderer bestillinger, fakturaer og betalinger.
-   **Betaling** – Ingen betalinger kan genereres for leverandøren.
-   **Rekvisisjon** – Bare én innkjøpsrekvisisjon kan opprettes. Ingen transaksjoner kan opprettes.
-   **Aldri** – Leverandøren settes aldri på vent for inaktivitet.

Når du setter en leverandør på vent, kan du også angi en årsak og en dato for når statusen på vent avsluttes. Hvis du ikke angir en sluttdato, varer leverandørens på vent-status i det uendelige.

Du kan masseoppdatere på vent-statusen til **Alle** for leverandører som er basert på de valgte kriteriene på siden **Deaktivering av leverandør**, og tilordne en årsak til hvorfor leverandøren er på vent.

Følgende kriterier brukes til å ta med leverandører som har vært inaktive i en periode, inkludere eller ekskludere leverandører som er ansatte, og utelate leverandører som har en henstandstid før neste sperring.

- Basert på hvor mange dager du angir i feltet **Inaktivitetsperiode** på siden **Deaktivering av leverandør**, beregner programmet den seneste datoen der leverandøren kan ha en aktivitet som kan regnes som inaktiv. Det vil si at dagens dato minus antall dager du angir. Hvis det finnes én eller flere fakturaer for leverandøren der datoen er senere enn den beregnede siste datoen, vil leverandøren bli utelatt fra deaktivering. Dette blir også validert hvis leverandøren har betalinger etter denne datoen, åpne innkjøpsrekvisisjoner, åpne bestillinger, forespørsler om tilbud eller svar.
- Antall dager i feltet **Henstandstid før neste sperre** brukes til å beregne den siste datoen i henstandstiden. Det vil si at dagens dato minus antall dager du angir. Dette gjelder bare leverandører som tidligere har blitt deaktivert. Når det gjelder en tidligere deaktivering, kontrollerer programmet historikken for andre forekomster av deaktivering for leverandøren og kontrollerer hvis den siste deaktiveringen ble utført før den siste datoen i henstandstiden. Hvis dette er tilfellet, inkluderes leverandøren i deaktiveringsprosessen.
- Parameteren **Inkluder ansatte** refererer til leverandører som er koblet til en ansatt. Du kan angi om du vil ta med disse ansatte.

Denne prosessen vil alltid utelat leverandører der verdien i feltet **Leverandørsperre** er **Aldri**.

Leverandører som består valideringen, blir satt på vent, som angir verdien i feltet **Leverandørsperre** til **Alle** og **Årsak** til det som er valgt. Det opprettes en post i sperreloggen for leverandøren.

## <a name="vendor-invoice-account"></a>Leverandørfakturakonto
Hvis mer enn én leverandør har samme fakturaadresse, eller hvis en leverandør faktureres gjennom en tredjepart, kan du angi en fakturakonto i leverandørposten. Fakturakontoen er den kontoen som fakturabeløpet blir kreditert når du oppretter en leverandørfaktura fra en bestilling. Hvis du ikke angir noen fakturakonto i leverandørposten, blir leverandørkontoen brukt som fakturakonto.

## <a name="vendor-bank-accounts"></a>Leverandørbankkontoer
Hvis du må betale til en leverandørbankkonto, kan du angi informasjon om leverandørens bank og bankkontoer på **Leverandørbankkontoer**-siden. Du kan også angi validerings- og betalingsinformasjon for bankkontoen. Du kan for eksempel legge til forhåndsmerknader i leverandørbankkontoer. Disse forhåndsmerknadene kan brukes til å bekrefte nøyaktigheten til kontodata, for eksempel registreringsnumre og kontonumre. Du må angi en standardkonto for betalinger til leverandøren. Når du foretar en betaling, kan du imidlertid endre denne kontoen til en av leverandørens andre kontoer.

## <a name="ledger-accounts"></a>Finanskontoer
Du kan angi standardkontoene som vises automatisk i leverandørfakturajournaler for den angitte leverandøren. Denne funksjonaliteten kan være nyttig hvis du vanligvis betaler for samme type ting eller tjenester fra de samme leverandørene over tid. Når du angir en standardkonto, kan du raskt og effektivt angi journaloppføringer i fakturajournalen. Standardkontoene du angir, brukes ikke for bestillinger eller for leverandørfakturaer som angis på **Leverandørfaktura**-siden.  

Du velger standardkontoer på siden **Standard kontooppsett** som du kan åpne fra **Faktura**-kategorien i leverandørposten. Kontoene som du velger her, vises i den filtrerte listen over kontoer for leverandørkontoen, når du angir en journaloppføring. Du kan angi én av kontoene som standardkonto.




