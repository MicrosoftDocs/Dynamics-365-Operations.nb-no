---
title: Registrerings-ID-er
description: Dette emnet gir informasjon om hvordan du setter opp og bruker registrerings-IDer.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: DirPartTaxRegistrationSearch, LogisticsPostalAddress, TaxRegistrationLegislationTypes, TaxRegistrationType
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 264824
ms.search.region: Global
ms.author: vlru
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: e85e1ef9bb27e3644264c898feb3a484c5b3ec3f
ms.contentlocale: nb-no
ms.lasthandoff: 11/03/2017

---

# <a name="registration-ids"></a>Registrerings-ID-er

[!include[banner](../includes/banner.md)]


Dette emnet gir informasjon om hvordan du setter opp og bruker registrerings-IDer.

Mange land og regioner har forskjellige bestemmelser og krav for registrering av avgiftsregisteringsnumre eller IDer. Dette emnet gir en oversikt over påkrevde innstillinger og behandling av støttede registreringstyper for parter i forskjellige europeiske land/regioner. Alle land har sine krav til å støtte ulike landsspesifikke funksjoner relatert til registreringsnumre levert av ulike statlige kontorer. Eksempler på registreringsnumre er personnummer (SSN), skatteidentifikasjonsnummer (TIN) og europeisk mva-ID (EU mva-ID). Denne funksjonen gir felles rammeverk for alle land i alle regioner ved å ta hensyn til landspesifikke kravene i noen europeiske land. Delene nedenfor beskriver den generelle informasjonsflyten som brukes til å konfigurere og behandle registrerings-IDer.

## <a name="registration-type-creation"></a>Oppretting av registreringstype
Før du kan angi registerings-ID, må du definere registeringsnummertyper for de forskjellige registreringsnumrene som hver part er underlagt. Gå til siden **Organisasjonsstyring** &gt; **Global adressebok** &gt; **Registreringstyper** &gt; **Registreringstyper** for å opprette og administrere registreringstyper for leverandører, kunder, arbeidere og juridiske enheter i ulike land/regioner.

|Felt                 |beskrivelse      |
|------------------------------|----------------------------|                                                                           
| Navn                | Navnet på registreringstypen. |                                                                           
| beskrivelse         | Beskrivelse av registreringstypen. |
| Land/område      | Den unike IDen for landet/regionen.|
| Skattemyndighet       | Skattemyndigheten som er forbundet med registreringstypen.|
| Begrenset til       | Typen begrensning som gjelder for avgiftsregistreringstypen: Ingen, Person, Organisasjon.|
| Formater              | Valideringsformatet for avgiftsregistreringstypen.|
| Kan oppdateres      | Definerer om registreringsnummeret for registreringstypen kan oppdateres etter at det er angitt.|
| Unik              | Definerer om registreringsnummeret for registreringstypen er unikt. |
| Primær for land | Hvis en part er knyttet til én eller flere adresser i bestemte land, og registrerings-IDen er gyldig for alle disse adressene, må du angi én adresse som hovedadresse for landet. Du kan bare registrere én-ID som primær. Angir om registreringsnummeret bare kan angis for primær landadresse. |

## <a name="assign-a-registration-type-to-a-registration-category"></a>Tilordne en registreringstype til en registreringskategori
Registreringskategori er registrerings-ID for land/region som er godkjent for bruk i bestemte land/områder for mva, toll og andre formål. Denne kategorien definerer valideringsregler for bestemt registrerings-ID (inkludert kontrollsifre osv.) og registrerings-ID for inkludering i ulike rapporter. Bruk siden **Organisasjonsstyring** &gt; **Global adressebok** &gt; **Registreringstyper** &gt; **Registreringskategorier** til å tilordne registreringstypen for bestemt land til støttet registreringskategori.

| Felt            | beskrivelse|
|-----------------------|----------------|
| Registreringstype     | Registreringstypen i bestemt land/region.|
| Begrenset til         | Typen begrensning gjelder for avgiftsregistreringstypen: Ingen, Person, Organisasjon.|
| Registreringskategori | Den unike registreringer-IDen som er godkjent for bruk i landet. En fullstendig liste over hva som støttes i Microsoft Dynamics 365 for Finance and Operations, Enterprise edition-kategoriene, vises nedenfor. |

## <a name="enter-registration-ids-for-global-address-book-records"></a>Angi registrerings-IDene for poster i globale adressebøker

Den globale adresseboken i Microsoft Finance and Operations inneholder konsolidert adresseinformasjon for kunder, leverandører, kontakter, forretningsforbindelser og juridiske enheter. For mer informasjon, se [Oversikt over global adressebok](../../fin-and-ops/organization-administration/overview-global-address-book.md). Partspostene som er lagret i den globale adresseboken, kan inneholde én eller flere adresseposter. Adressene brukes til forskjellige formål, for eksempel fakturering eller levering. Du kan definere registrerings-IDer for adresseinformasjon for kunder, leverandører, ansatte og juridiske enheter. Finn partsposten (juridisk enhet, leverandør, kunde, arbeider) du vil angi register-IDen for, og klikk deretter **Registrerings-IDer** i skjemaer som er knyttet til part, juridisk enhet, leverandør, kunde, arbeider for å åpne siden **Administrer adresser**. I kategorien **Avgiftsregistrering** klikker du **Legg til** og skriver inn følgende informasjon om registrering-IDen.


|Felt                |beskrivelse                                                |
|---------------------|-----------------------------------------------------------|
| Registreringstype   | Registreringstypen i det valgte landet/området.     |
| Registreringsnummer | Registrering-ID for part.                                |
| beskrivelse         | Beskrivelse av registreringsnummeret.               |
| Del             | Tilleggsinformasjonen om registreringsnummeret. |
| Utstedende byrå      | Skattemyndighetene som utstedte registreringsnummeret.        |
| Utstedt dato         | Utstedelsesdatoen for registreringsnummeret.              |
| Effektiv           | Gyldighetsdatoen for registreringsnummeret.           |
| Utløp          | Utløpsdatoen for avgiftsregistreringsnummeret.          |

> [!NOTE]
> MVA-organisasjonsnummeret for juridisk enhet, leverandør, kunde kan velges fra registrering-IDer som er knyttet til mva-IDen og angitt for parten.

## <a name="search-for-records-by-registration-id"></a>Søke etter poster ved registrerings-ID
Søk etter partsposter basert på en registrerings-ID er tilgjengelig på skjemaer som er knyttet til part, juridisk enhet, leverandør, kunde og arbeider. Klikk **Søk på registrerings-ID** for å åpne siden **Søkekriterier for registrerings-ID**. Angi søkevilkår og klikk **Søk**. Systemet viser de valgte postene fra den globale adresseboken og tilknyttede typer partspost.

## <a name="supported-registration-categories"></a>Registreringskategorier som støttes
Følgende tabell viser støttede registreringstyper i Finance and Operations. Hvis du er kjent med Microsoft Dynamics AX 2012-feltene for registrering av IDer, tilordner denne tabellen også disse feltene til registreringskategorier for Finance and Operations.

| Registreringskategorier for Finance and Operations         |Land/område  | Dynamics AX 2012-term/felt|
|---------------------------------------------------------------|---------------------|---------------------------------|
| Mva-ID                                                        | Alle landene i den europeiske Union (EU)|  Avgiftsfritaksnummer (juridiske type foretaksnummer i AX 2012 R3)|
| Foretaks-ID (COID)                                          | Belgia Tsjekkia Estland Ungarn Latvia Litauen Polen Sveits | Foretaksnummer (EnterpriseNumber) Registreringsnummer (RegNum\_W) Registreringsnummer (RegNum\_W) Registreringsnummer (RegNum\_W) Registreringsnummer (RegNum\_W) Organisasjonskode (EnterpriseCode) Registreringsnummer (RegNum\_W) UID (Juridisk type UID i AX 2012 R3) |
| Avdelings-ID                                                     | Belgia            | Avdelingsnummer (BranchNumber)|
| Spisová značka (registreringsnummer, utstedende byrå, seksjon) | Tsjekkia     | Innfelt nummer (CommercialRegisterInsetNumber) Lagret i kommersielt register (CommercialRegister) Del i kommersielt register (CommercialRegisterSection)|
| Tollkunde-ID                                           | Finland | Tollkundenummer (CustomsCustomerNumber\_FI)|
| INN                                                           | Den russiske føderasjon| INN (juridisk type INN i AX 2012 R3)|
| RRC                                                           | Den russiske føderasjon| RRC (juridisk type RRC i AX 2012 R3)|
| OKDP                                                          | Den russiske føderasjon| OKDP (juridisk type OKDP i AX 2012 R3)|
| OKPO                                                          | Den russiske føderasjon| OKPO (juridisk type OKPO i AX 2012 R3)|
| RCOAD                                                         | Den russiske føderasjon| RCOAD (juridisk type RCOAD i AX 2012 R3)|
| OGRN                                                          | Den russiske føderasjon| OGRN (juridisk type OGRN i AX 2012 R3) |
| SNILS                                                         | Den russiske føderasjon| SNILS (juridisk type SNILS i AX 2012 R3)|
| CIFTS                                                         | Den russiske føderasjon| CIFTS (juridisk type CIFTS i AX 2012 R3)|

Hvis du vil ha mer informasjon om registrering av IDer, inkludert nødvendige forutsetninger, kan du se følgende oppgaveopptak for mva-ID i Lifecycle Services (LCS):

-   Definere mva-ID
-   Registrering av mva-ID for leverandør
-   EUR 00015 Partssøk ved hjelp av mva-ID





