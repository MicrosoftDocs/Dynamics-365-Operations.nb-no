---
title: Tjenestemiljøer
description: Denne artikkelen inneholder informasjon om tjenestemiljøer for elektronisk fakturering, og forklarer hvordan du konfigurerer dem.
author: dkalyuzh
ms.date: 02/28/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkalyuzh
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 8c743c5b2fbc7dcc3ae04fa4d7ca0e65de6c2507
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8901254"
---
# <a name="service-environments"></a>Tjenestemiljøer

[!include [banner](../includes/banner.md)]

Tjenestemiljøer er logiske partisjoner som opprettes for å støtte globaliseringsfunksjonene og de tilhørende dokumentene som behandles i tjenesten for elektronisk fakturering. Sikkerhetshemmelighetene, de digitale sertifikatene og tilgangstillatelsene (styring), må konfigureres på tjenestemiljønivå.

Du kan opprette så mange tjenestemiljøer du trenger. Alle tjenestemiljøene som du oppretter, er uavhengige av hverandre. Vi anbefaler at du oppretter minst to tjenestemiljøer (som er den anbefalte fremgangsmåten):

- Ett miljø til primær utvikling og validering. Dette miljøet er vanligvis et miljø for testing av brukeraksept.
- Ett miljø til produksjon. Dette miljøet er vanligvis et produksjonsmiljø.

Denne typen partisjonering sikrer at prosessene for e-fakturering valideres og tilpasses i sandkassen før de går til produksjon.

Tjenestemiljøer må opprettes og vedlikeholdes i Regulatory Configuration Service (RCS). Når de er klare, må de deretter publiseres i tjenesten for elektronisk fakturering. Publiseringsprosessen sender parameterne for tjenestemiljøet fra RCS-forekomsten til tjenesten for elektronisk fakturering.

Hvis du ikke fullfører publiseringsprosessen etter at du har opprettet et nytt tjenestemiljø eller justert et eksisterende tjenestemiljø (for eksempel ved å legge til eller fjerne brukere eller Microsoft Azure Key Vault-hemmeligheter), trer ikke endringene i kraft. Dynamics 365 Finance eller Dynamics 365 Supply Chain Management har bare tilgang til publiserte miljøer.

## <a name="service-environment-statuses"></a>Tjenestemiljøstatuser

Tjenestemiljøer kan administreres via statusen deres. Du kan vise statusen for et miljø på **Tjenestemiljøer**-siden. Følgende statuser er tilgjengelige:

- **Ikke publisert** – Miljøet er opprettet, men det er ennå ikke publisert.
- **Publisert** – Miljøet er publisert i tjenesten for elektronisk fakturering.
- **Endret** – Attributtene for et publisert miljø er endret, men endringene er ikke publisert ennå.

## <a name="users"></a>Brukere

Hvert tjenestemiljø må vise en liste over brukerne som kan koble seg til elektronisk fakturering fra Finance eller Supply Chain Management.

## <a name="applications"></a>Søknader

I enkelte scenarioer kan det hende at andre programmer enn Finance eller Supply Chain Management må koble seg til tjenesten for elektronisk fakturering for å sende inn elektroniske dokumenter til videre behandling, eller for å hente informasjon, for eksempel innsendingsstatusen for et dokument. I disse scenarioene bør programmet defineres i listen over programmer. Dermed får det tilgang til tjenesten for elektronisk fakturering. Programmet må også være registrert som et program i Azure Active Directory (Azure AD), og objekt-ID-en må brukes til å identifisere det. 

Siden Microsoft krever et høyt nivå av sikkerhetskontroll over programmer som kan koble seg til tjenesten for elektronisk fakturering, må du kontakte Microsoft på <DGXRegulatoryservicesengineering@service.microsoft.com> og oppgi følgende informasjon om programmet:

- Leier-ID for Azure AD
- Miljø-ID-en for Microsoft Dynamics Lifecycle Services (LCS)
- Program-ID-en (klient-ID)
- Objekt-ID
- Begrunnelse for og en høynivåbeskrivelse av programmet

Microsoft evaluerer forespørselen og registrerer programmet i sikkerhetsregisteret for å sikre at det kan fungere med elektronisk fakturering.

## <a name="number-sequences"></a>Nummerserier

Hvis scenarioene krever nummerserier (for eksempel i filnavn), kan du bruke nummerserier som er definert for et bestemt miljø, men som kan brukes enten på tvers av globaliseringsfunksjoner eller for en bestemt globaliseringsfunksjon. Etter at en nummerserie er definert, kan du bruke den i variabler og datasamlebånd for behandling. Du kan spore bruken ved å se etter en verdi for **Gjeldende** for parameteren **I bruk** på **Nummerserier**-siden.

### <a name="working-with-number-sequences"></a>Arbeide med nummerserier
På **Nummerserier**-siden: 

- Velg **Ny** for å opprette en nummerserie. Deretter angir du et navn og en beskrivelse. 
- Velg **Slett** for å slette en nummerserie hvis den ikke lenger er i bruk.
- Du trenger ikke å velge **Publiser** i handlingsruten for å publisere endringene i en nummerserie. Oppdateringen gjøres automatisk.

## <a name="create-a-key-vault-reference"></a>Opprette en Key Vault-referanse

1. Logg på RCS-kontoen.
2. I arbeidsområdet **Globaliseringsfunksjon** velger du flisen **Elektronisk fakturering** i delen **Miljø**.
3. Velg **Tjenestemiljøer** i handlingsruten på siden **Miljøoppsett**.
4. Velg **Key Vault-parametere** i handlingsruten på **Tjenestemiljøer**-siden.
5. Velg **Ny** på siden **Key Vault-parametere** for å opprette en Key Vault-parameter.
6. I **Navn**-feltet angir du navnet på Key Vault-referansen.
7. Angi en beskrivelse i **Beskrivelse**-feltet.
8. Lim inn URI-en for Key Vault fra nøkkelhvelvet (`https://<your key vault>.vault.azure.net/`) i feltet **URI for Key Vault**. Hvis du vil ha mer informasjon, kan du se [Opprette et Azure-nøkkelhvelv i Azure-portalen](e-invoicing-create-azure-key-vault-azure-portal.md).
9. Velg **Lagre**.
    
## <a name="create-a-secret-for-the-storage-account-secret-token"></a>Opprette en hemmelighet for det hemmelige tokenet for lagringskonto

1. På siden **Key Vault-parametere** velger du Key Vault-referansen du opprettet i den forrige fremgangsmåten, og deretter velger du **Legg til** i **Sertifikater**-delen.
2. I **Navn**-feltet angir du navnet på lagringskontohemmeligheten. Dette navnet må samsvare med navnet på Key Vault-hemmeligheten som inneholder tokenet for signatur for delt tilgang (SAS) for lagring. Hvis du vil ha mer informasjon, kan du se [Opprette en Azure-lagringskonto i Azure-portalen](e-invoicing-create-azure-storage-account-azure-portal.md). 
3. Angi en beskrivelse i **Beskrivelse**-feltet.
4. Velg **Hemmelighet** i **Type**-feltet.
5. Velg **Lagre**.
    
## <a name="create-a-service-environment"></a>Opprette et tjenestemiljø

1. Velg **Nytt** på siden **Tjenestemiljøer** for å opprette et tjenestemiljø.
2. I **Navn**-feltet angir du navnet på miljøet for elektronisk fakturering.
3. Angi en beskrivelse i **Beskrivelse**-feltet.
4. I feltet **Lagring av for SAS-tokenhemmelighet** velger du navnet på lagringskontohemmeligheten som må brukes til å godkjenne tilgang til lagringskontoen.
5. I **Brukere**-delen velger du **Legg til** for å legge til en bruker som har tillatelse til å sende elektroniske fakturaer gjennom miljøet og koble seg til lagringskontoen.
6. I **Bruker-ID**-feltet angir du aliaset til brukeren. 
7. Angi brukerens e-postadresse i feltet **E-post**.
8. Velg **Lagre**.
9. Velg **Publiser** i handlingsruten for å publisere miljøet i tjenesten for elektronisk fakturering. Kontroller at verdien i feltet **Status** er endret til **Publisert**.
