---
title: Registrerings-ID-er
description: Dette emnet inneholder informasjon om hvordan du konfigurerer og bruker registrering IDer.
author: ShylaThompson
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: DirPartTaxRegistrationSearch, LogisticsPostalAddress, TaxRegistrationLegislationTypes, TaxRegistrationType
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 264824
ms.assetid: e86f0a35-be58-4ef5-b5ab-bcfc495eaa13
ms.search.region: Global
ms.author: vlru
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: f707d45290682e79ee439ba0d504852429defa90
ms.openlocfilehash: 32cd09975861083b8940368ed53ae16e89bcd748
ms.lasthandoff: 03/31/2017


---

# <a name="registration-ids"></a>Registrerings-ID-er

Dette emnet inneholder informasjon om hvordan du konfigurerer og bruker registrering IDer.

Mange land og regioner har forskjellige reguleringer og krav for registrering av registreringsnumre eller IDer. Dette emnet gir en oversikt over påkrevde innstillingene og behandling av støttede Registreringstyper for parter i forskjellige europeiske land/regioner. Alle land har sine krav til å støtte ulike Landsspesifikke funksjoner relatert til registreringsnumre levert av ulike tilstand kontorer. Eksempler på registreringsnumre er personnummer (SSN), mva-ID-nummer (TIN) og europeiske mva-ID (EU mva-ID). Denne funksjonen gir felles rammeverk for alle land i alle regioner ved å ta i kontoen landspesifikke kravene i noen europeiske land. Følgende avsnitt beskriver generelle informasjonsflyten som brukes for å definere og behandle registrering IDer.

## <a name="registration-type-creation"></a>Oppretting av typen registrering
Før du kan angi registrerings-IDen, må du definere Registreringstyper for forskjellige typer registrering tall som hver part er underlagt. Gå til **organisasjonsadministrasjon**&gt;**globale adresseboken**&gt;**Registreringstyper**&gt;**Registreringstyper** siden til å opprette og behandle Registreringstyper for leverandører, kunder, ansatte og juridiske enheter i forskjellige land/regioner.

|Felt                 |beskrivelse      |
|------------------------------|----------------------------|                                                                           
| Navn                | Navnet av registreringstypen. |                                                                           
| beskrivelse         | Beskrivelse av registreringstypen. |
| Land/område      | Den unike IDen av landet/regionen.|
| Skattemyndighet       | Skattemyndighetene som er tilknyttet registreringstypen.|
| Begrenset til       | Typen begrensning som gjelder for avgiftsregistreringstypen: Ingen, Person, organisasjon.|
| Formater              | Valideringsformatet for registreringstypen.|
| Kan oppdateres      | Angir om registreringsnummeret for registreringstypen kan oppdateres etter at den er angitt.|
| Unik              | Angir om registreringsnummeret for registreringstypen er unik. |
| Primær for land | Hvis en part er knyttet til én eller flere adresser i bestemte land og registrerings-IDen er gyldig for alle disse adressene, må du angi én adresse som primært for landet. Du kan bare registrere én-ID som primær. Angir om registreringsnummeret kan angis bare for primære for land adresse. |

## <a name="assign-a-registration-type-to-a-registration-category"></a>Tilordne en registreringstype til en kategori for registrering
Registrering er land registrering identifikator som er godkjent for bruk i bestemte land/område for mva, toll og andre formål. Denne kategorien definerer valideringsregler av bestemt registrerings-ID (inkludert kontrollsifrene osv.) og registrerings-IDen for inkludering i ulike rapporter. Bruk siden **organisasjonsadministrasjon**&gt;**globale adresseboken**&gt;**Registreringstyper**&gt;**Registreringskategorier** å tilordne registreringstypen for bestemt land til støttede registrering kategori.

| Felt            | beskrivelse|
|-----------------------|----------------|
| Registreringstype     | Registreringen inn i bestemte land.|
| Begrenset til         | Typen begrensning gjelder for avgiftsregistreringstypen: Ingen, Person, organisasjon.|
| Registreringskategori | Unike registreringer-IDen som er godkjent for bruk i landet. Den fullstendige listen over AX7.1 som støttes i kategorier som er under. |

## <a name="enter-registration-ids-for-global-address-book-records"></a>Angi registrering IDene for postene i globale adresseboken
Den globale adresseboken (globale adresseboken) i Microsoft Dynamics 365 for operasjoner inneholder konsoliderte adresseinformasjon for kunder, leverandører, kontakter, forretningsforbindelser og juridiske enheter. For mer informasjon, se [globale adressebok oversikt](/dynamics365/operations/organization-administration/overview-global-address-book). Partiposter som er lagret i den globale adresseboken kan inneholde én eller flere adresseposter. Adressene brukes til forskjellige formål, for eksempel fakturering eller levering. Du kan definere registrering IDer for adresseinformasjon for kunder, leverandører, ansatte og juridiske enheter. Finn parten (juridisk enhet, leverandør, kunde, arbeider), registrerer du vil angi register-IDen, og klikk deretter **registrering IDer** i skjemaer som er knyttet til party, juridisk enhet, leverandør, kunde, arbeider for å åpne den **behandle adresser** siden. På den **mva-registrering**, klikk **Legg til**, og Skriv inn følgende informasjon om registrering-ID.

|Felt                |beskrivelse                                                |
|---------------------|-----------------------------------------------------------|
| Registreringstype   | Registreringstype for valgt land/område.     |
| Registreringsnummer | Party registrering-ID.                                |
| beskrivelse         | Beskrivelse av registreringsnummeret.               |
| Del             | Tilleggsinformasjon om registreringsnummeret. |
| Utstedende byrå      | Sertifiseringsinstansen som utstedte registreringsnummeret.        |
| Utstedt dato         | Utstedte datoen for registreringsnummeret.              |
| Effektiv           | Den effektive datoen for registreringsnummeret.           |
| Utløp          | Utløpsdato for registreringsnummeret.          |

> [!NOTE]
> Tax exempt-nummer for juridisk enhet, leverandør, kunde kan velges fra registrering-IDer som er knyttet til mva-IDen og angitt for parten.

## <a name="search-for-records-by-registration-id"></a>Søke etter poster ved registrerings-ID
Søk etter party poster basert på en registrerings-ID er tilgjengelig på skjemaene som er knyttet til party, juridisk enhet, leverandør, kunde og arbeider. Klikk **Søk registrerings-ID** å åpne den **søkevilkår registrerings-ID** siden. Angi søkevilkår og klikk **finne**. Systemet viser de valgte postene fra den globale adresseboken og tilknyttede typer partspost.

## <a name="supported-registration-categories"></a>Støttede Registreringskategorier
Følgende tabell viser typene støttede registrering i Dynamics 365 for operasjoner. Hvis du er kjent med Microsoft Dynamics AX 2012-feltene for registrering IDer, tilordner denne tabellen også disse feltene til Dynamics-365 for operasjoner Registreringskategorier.

| Dynamics 365 for registrering av operasjoner-kategorien         |Land/område  | Dynamics AX 2012 term/felt|
|---------------------------------------------------------------|---------------------|---------------------------------|
| Mva-ID                                                        | Alle landene i den europeiske Union (EU)|  Mva-nummer (juridisk type TAX-ID i AX 2012 R3)|
| Foretaks-ID (COID)                                          | Belgia den tsjekkiske republikken Estland Ungarn Latvia Litauen Polen Sveits | Registreringsnummer for Enterprise-nummer (EnterpriseNumber) (Regnum.dat\_W) registreringsnummer (Regnum.dat\_W) registreringsnummer (Regnum.dat\_W) registreringsnummer (Regnum.dat\_W) registreringsnummer for Enterprise-kode (EnterpriseCode) (Regnum.dat\_W) UID (juridisk type UID i AX 2012 R3) |
| Avdelings-ID                                                     | Belgia            | Avdelingsnummer (BranchNumber)|
| Spisová značka (nummer, utstedelse byrå, inndeling) | Tsjekkia     | Cellerammemargen tall (CommercialRegisterInsetNumber)-Kept på kommersielle registrere (CommercialRegister)-delen av kommersiell register (CommercialRegisterSection)|
| Tollkunde-ID                                           | Finland | Tollkundenummer (CustomsCustomerNumber\_FI)|
| INN                                                           | Den russiske føderasjon| INN (juridisk type INN i AX 2012 R3)|
| RRC                                                           | Den russiske føderasjon| RRC (juridisk type RRC i AX 2012 R3)|
| OKDP                                                          | Den russiske føderasjon| OKDP (juridisk type OKDP i AX 2012 R3)|
| OKPO                                                          | Den russiske føderasjon| OKPO (juridisk type OKPO i AX 2012 R3)|
| RCOAD                                                         | Den russiske føderasjon| RCOAD (juridisk type RCOAD i AX 2012 R3)|
| OGRN                                                          | Den russiske føderasjon| OGRN (juridisk type OGRN i AX 2012 R3) |
| SNILS                                                         | Den russiske føderasjon| SNILS (juridisk type SNILS i AX 2012 R3)|
| CIFTS                                                         | Den russiske føderasjon| CIFTS (juridisk type CIFTS i AX 2012 R3)|

Hvis du vil ha mer informasjon om IDer for registrering behandling, inkludert nødvendige forutsetninger, kan du se følgende aktivitet innspillingene for mva-ID i livssyklusen tjenester (LCS):

-   Definere mva-ID
-   IDen for mva-registrering av leverandør
-   EUR 00015 Partssøk ved hjelp av mva-ID



