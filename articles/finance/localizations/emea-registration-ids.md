---
title: Registrerings-ID-er
description: Denne artikkelen gir informasjon om hvordan du setter opp og bruker registrerings-IDer.
author: kfend
ms.date: 11/08/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.custom: 264824
ms.search.form: DirPartTaxRegistrationSearch, LogisticsPostalAddress, TaxRegistrationLegislationTypes, TaxRegistrationType
ms.openlocfilehash: 380cb1d2b52d5d0debffdbe73183be2f5e783f21
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/12/2022
ms.locfileid: "9274559"
---
# <a name="registration-ids"></a>Registrerings-ID-er

[!include [banner](../includes/banner.md)]

Denne artikkelen gir informasjon om hvordan du setter opp og bruker registrerings-IDer.

Mange land og regioner har forskjellige bestemmelser og krav for registrering av avgiftsregisteringsnumre eller IDer. Denne artikkelen gir en oversikt over påkrevde innstillinger og behandling av støttede registreringstyper for parter i forskjellige europeiske land/regioner. Alle land har sine krav til å støtte ulike landsspesifikke funksjoner relatert til registreringsnumre levert av ulike statlige kontorer. Eksempler på registreringsnumre er personnummer (SSN), skatteidentifikasjonsnummer (TIN) og europeisk mva-ID (EU mva-ID). Denne funksjonen gir felles rammeverk for alle land i alle regioner ved å ta hensyn til landspesifikke kravene i noen europeiske land. Delene nedenfor beskriver den generelle informasjonsflyten som brukes til å konfigurere og behandle registrerings-IDer.

## <a name="registration-type-creation"></a>Oppretting av registreringstype
Før du kan angi registerings-ID, må du definere registeringsnummertyper for de forskjellige registreringsnumrene som hver part er underlagt. Gå til siden **Organisasjonsstyring** &gt; **Global adressebok** &gt; **Registreringstyper** &gt; **Registreringstyper** for å opprette og administrere registreringstyper for leverandører, kunder, arbeidere og juridiske enheter i ulike land/regioner.

|Felt                 |Beskrivelse      |
|------------------------------|----------------------------|                                                                           
| Navn                | Navnet på registreringstypen. |                                                                           
| Beskrivelse         | Beskrivelse av registreringstypen. |
| Land/område      | Den unike IDen for landet/regionen.|
| Skattemyndighet       | Skattemyndigheten som er forbundet med registreringstypen.|
| Begrenset til       | Typen begrensning som gjelder for avgiftsregistreringstypen: Ingen, Person, Organisasjon.|
| Formater              | Valideringsformatet for avgiftsregistreringstypen.|
| Kan oppdateres      | Definerer om registreringsnummeret for registreringstypen kan oppdateres etter at det er angitt.|
| Unik              | Definerer om registreringsnummeret for registreringstypen er unikt. |
| Primær for land | Hvis en part er knyttet til én eller flere adresser i bestemte land, og registrerings-IDen er gyldig for alle disse adressene, må du angi én adresse som hovedadresse for landet. Du kan bare registrere én-ID som primær. Angir om registreringsnummeret bare kan angis for primær landadresse. |

## <a name="assign-a-registration-type-to-a-registration-category"></a>Tilordne en registreringstype til en registreringskategori
Registreringskategori er registrerings-ID for land/region som er godkjent for bruk i bestemte land/områder for mva, toll og andre formål. Denne kategorien definerer valideringsregler for bestemt registrerings-ID (inkludert kontrollsifre osv.) og registrerings-ID for inkludering i ulike rapporter. Bruk siden **Organisasjonsstyring** &gt; **Global adressebok** &gt; **Registreringstyper** &gt; **Registreringskategorier** til å tilordne registreringstypen for bestemt land til støttet registreringskategori.

| Felt            | Beskrivelse|
|-----------------------|----------------|
| Registreringstype     | Registreringstypen i bestemt land/region.|
| Begrenset til         | Typen begrensning gjelder for avgiftsregistreringstypen: Ingen, Person, Organisasjon.|
| Registreringskategori | Den unike registreringer-IDen som er godkjent for bruk i landet. Den fullstendige listen over kategorier som støttes, vises senere i denne artikkelen. |

## <a name="enter-registration-ids-for-global-address-book-records"></a>Angi registrerings-IDene for poster i globale adressebøker

Den globale adresseboken inneholder konsolidert adresseinformasjon for kunder, leverandører, kontakter, forretningsforbindelser og juridiske enheter. For mer informasjon, se [Oversikt over global adressebok](../../fin-ops-core/fin-ops/organization-administration/overview-global-address-book.md). Partspostene som er lagret i den globale adresseboken, kan inneholde én eller flere adresseposter. Adressene brukes til forskjellige formål, for eksempel fakturering eller levering. Du kan definere registrerings-IDer for adresseinformasjon for kunder, leverandører, ansatte og juridiske enheter. Finn partsposten (juridisk enhet, leverandør, kunde, arbeider) du vil angi register-IDen for, og klikk deretter **Registrerings-IDer** i skjemaer som er knyttet til part, juridisk enhet, leverandør, kunde, arbeider for å åpne siden **Administrer adresser**. I kategorien **Avgiftsregistrering** klikker du **Legg til** og skriver inn følgende informasjon om registrering-IDen.


|Felt                |Beskrivelse                                                |
|---------------------|-----------------------------------------------------------|
| Registreringstype   | Registreringstypen i det valgte landet/området.     |
| Registreringsnummer | Registrering-ID for part.                                |
| Beskrivelse         | Beskrivelse av registreringsnummeret.               |
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
Tabellen nedenfor viser registreringstypene som støttes. Hvis du er kjent med Microsoft Dynamics AX 2012-feltene for registrering av IDer, tilordner denne tabellen også disse feltene til registreringskategorier for Dynamics 365 Finance.

| Registreringskategori for Finance         |Land/område  | Dynamics AX 2012-term/felt|
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
| Pass                                                      | Spania             | Pass|
| Offisielt ID-dokument                              | Spania             | Offisielt ID-dokument|
| Bostedssertifikat                                         | Spania             | Bostedssertifikat|
| Annet ID-dokument                                 | Spania             | Annet ID-dokument|
| Ingen opptelling                                                  | Spania             | Ikke tilgjengelig i AX 2012 R3|


Hvis du vil ha mer informasjon om registrering av IDer, inkludert nødvendige forutsetninger, kan du se følgende oppgaveopptak for mva-ID i Lifecycle Services (LCS):

-   Definere mva-ID
-   Registrering av mva-ID for leverandør
-   EUR 00015 Partssøk ved hjelp av mva-ID






[!INCLUDE[footer-include](../../includes/footer-banner.md)]
