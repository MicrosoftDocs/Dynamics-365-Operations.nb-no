---
title: Komme i gang med tjenesteadministrasjon for elektronisk fakturering
description: Dette emnet beskriver hvordan du kommer i gang med elektronisk fakturering.
author: gionoder
ms.date: 03/29/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: ec431cb4a3620459d905f64a80fd820a2113290f
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5840154"
---
# <a name="get-started-with-electronic-invoicing-service-administration"></a>Komme i gang med tjenesteadministrasjon for elektronisk fakturering

[!include [banner](../includes/banner.md)]

## <a name="prerequisites"></a>Forutsetninger

Før du kan fullføre trinnene i dette emnet må følgende forutsetninger være på plass:

- Du må ha tilgang til kontoen for Microsoft Dynamics Lifecycle Services (LCS).
- Du må ha et LCS-prosjekt som inkluderer versjon 10.0.17 eller senere av Microsoft Dynamics 365 Finance og Dynamics 365 Supply Chain Management. I tillegg må disse appene distribueres i én av følgende Azure-geografier:

    - USA øst
    - USA vest
    - EU nord
    - EU vest

- Du må ha tilgang til RCS-kontoen (Regulatory Configuration Services) for Dynamics 365.
- Du må aktivere globaliseringsfunksjonen for kontoen for RCS i Funksjonsbehandling. Hvis du vil ha mer informasjon, kan du se [Regulatory Configuration Services (RCS) – globaliseringsfunksjoner](rcs-globalization-feature.md).
- Du må opprette en Key Vault og en lagringskonto i Azure. Hvis du vil ha mer informasjon, kan du se [Opprette en Azure Storage-konto og et Key Vault](e-invoicing-create-azure-storage-account-key-vault.md).

## <a name="install-the-add-in-for-microservices-in-lifecycle-services"></a>Installere tilleggsprogrammet for mikrotjenester i Lifecycle Services

1. Logg på LCS-kontoen.
2. Velg flisen **Administrasjon av forhåndsvisningsfunksjoner**.
3. Velg delen **Funksjoner i offenlig forhåndsversjon** velger du **E-faktureringstjeneste**.
4. Kontroller at alternativet **Forhåndsversjon aktivert** er satt til **Ja**.
5. Velg LCS-distribusjonsprosjektet på LCS-instrumentbordet. LCS-prosjektet må kjøre.
7. I fanen **Miljøtillegg** velger du **Installer et nytt tillegg**.
8. Velg **E-faktureringstjenester**.
9. I feltet **App-ID for AAD** angir du **091c98b0-a1c9-4b02-b62c-7753395ccabe**. Dettee er en fast verdi.
10. I feltet **AAD-leier-ID** angir du leier-IDen for kontoen for Azure-abonnementet.
11. Gå gjennom vilkårene og betingelsene og merk deretter av i avmeringsboksen.
12. Velg **Installer**.


## <a name="set-up-the-parameters-for-rcs-integration-with-electronic-invoicing"></a>Konfigurere parametere for RCS-integrasjon med elektronisk fakturering

1. Logg på RCS-kontoen.
2. I delen **Relaterte koblinger** i arbeidsområdet **Elektronisk rapportering** velger du **Parametere for elektronisk rapportering**.
3. I kategorien **E-faktureringstjeneste**, i feltet **URI for endepunkt for tjeneste**, angir du riktig tjenesteendepunkt for Azure-geografien, som vist i følgende tabell.

    | Datasenter Azure-geografi | URI for tjenestesluttpunkt                                                       |
    |----------------------------|----------------------------------------------------------------------------|
    | USA øst                    | `https://electronicinvoicing.eus-il301.gateway.prod.island.powerapps.com/` |
    | USA vest                    | `https://electronicinvoicing.wus-il301.gateway.prod.island.powerapps.com/` |
    | EU nord                   | `https://electronicinvoicing.neu-il301.gateway.prod.island.powerapps.com/` |
    | EU vest                    | `https://electronicinvoicing.weu-il301.gateway.prod.island.powerapps.com/` |

4. Kontroller at feltet **Program-ID** er satt til **0cdb527f-a8d1-4bf8-9436-b352c68682b2**. Denne verdien er en fast verdi.
5. I feltet **ID for LCS-miljø** angir du ID-en for LCS-miljøet.
6. Velg **Lagre**, og lukk deretter siden.

## <a name="create-key-vault-references"></a>Opprette Key Vault-referanser

1. Logg på RCS-kontoen.
2. I arbeidsområdet **Globaliseringsfunksjon** velger du flisen **Elektronisk fakturering** i delen **Miljø**.
3. På siden for **Miljøkonfigurasjon**, i handlingsruten, velger du **Tjenestemiljø**, og deretter velger du **Key Vault-parametere**.
4. Velg **Ny** for å opprette en Key Vault-referanse.
5. I **Navn**-feltet angir du navnet på Key Vault-referansen. Angi en beskrivelse i **Beskrivelse**-feltet.
6. Lim inn hemmeligheten fra Azure Key Vault i feltet **URI for Key Vault**. Hvis du vil ha mer informasjon, kan du se [Opprette en Azure Storage-konto og et Key Vault](e-invoicing-create-azure-storage-account-key-vault.md).
7. Velg **Lagre**.

## <a name="create-storage-account-secret"></a>Opprette hemmelighet for lagringskonto

1. På siden **Miljøkonfigurasjon**, i handlingsruten, velger du **Tjenestemiljø** > **Key Vault-parametere**.
2. Velg en **Key Vault-referanse**, gå til **Sertifikater**-delen, og velg **Legg til**.
3. I **Navn**-feltet angir du navnet på lagringskontohemmeligheten. Hvis du vil ha mer informasjon, kan du se [Opprette en Azure Storage-konto og et Key Vault](e-invoicing-create-azure-storage-account-key-vault.md).
4. Angi en beskrivelse i **Beskrivelse**-feltet.
5. Velg **Hemmelighet** i **Type**-feltet.
6. Velg **Lagre**, og lukk deretter siden.

## <a name="create-a-digital-certificate-secret"></a>Opprette et digitalt sertifikat og opprette et digitalt sertifikat

1. På siden **Miljøkonfigurasjon**, i handlingsruten, velger du **Tjenestemiljø**, og deretter velger du **Key Vault-parametere**.
2. Velg en **Key Vault-referanse**, gå til **Sertifikater**-delen, og velg **Legg til**.
3. I **Navn**-feltet angir du navnet på hemmeligheten for det digitale sertifikatet. Hvis du vil ha mer informasjon, kan du se [Opprette en Azure Storage-konto og et Key Vault](e-invoicing-create-azure-storage-account-key-vault.md).
4. Angi en beskrivelse i **Beskrivelse**-feltet.
5. I feltet **Type** velger du **Sertifikat**.
6. Velg **Lagre**, og lukk deretter siden.

## <a name="create-a-service-environment"></a>Opprette et tjenestemiljø

1. Logg på RCS-kontoen.
2. I arbeidsområdet **Globaliseringsfunksjon** velger du flisen **Elektronisk fakturering** i delen **Miljø**.
3. Velg **Tjenestemiljø** på siden **Miljøoppsett** i handlingsruten.
4. Velg **Ny** for å opprette et nytt tjenestemiljø.
5. I **Navn**-feltet angir du navnet på e-fakturamiljøet. Angi en beskrivelse i **Beskrivelse**-feltet.
6. I feltet **Lagring av for SAS-tokenhemmelighet** velger du navnet på lagringskontohemmeligheten som må brukes til å godkjenne tilgang til lagringskontoen.
7. I **Brukere**-delen velger du **Legg til** for å legge til en bruker som har tillatelse til å sende elektroniske fakturaer gjennom miljøet og også koble seg til lagringskontoen.
8. I **Bruker-ID**-feltet angir du aliaset til brukeren. Angi brukerens e-postadresse i feltet **E-post**.
9. Velg **Lagre**.
10. Hvis den land/område-spesifikke fakturaen krever en sertifikatkjede for å bruke digitale signaturer, velger du **Kjede av sertifikater** og deretter, i handlingsruten, velger du **Key Vault-hemmeligheter**, og følg deretter denne fremgangsmåten:
    1. Velg **Ny** for å opprette en kjede av sertifikater.
    2. I **Navn**-feltet angir du navnet på kjeden av sertifikater. Angi en beskrivelse i **Beskrivelse**-feltet.
    3. I delen **Sertifikater** velger du **Legg til** for å legge til et sertifikat i kjeden.
    4. Bruk knappene **Opp** eller **Ned** for å endre posisjonen til sertifikatene i kjeden.
    5. Velg **Lagre**, og lukk deretter siden.
    6. Lukk siden.
11. På siden **Tjenestemiljø**, i handlingsruten, velger du **Publiser** for å publisere miljøet til skyen. Verdien i feltet **Status** endres til **Publisert**.

## <a name="create-a-connected-application"></a>Opprette et tilkoblet program

1. Velg **Tilkoblede programmer** på siden **Miljøoppsett** i handlingsruten.
2. Velg **Ny** for å opprette et tilkoblet program.
3. I **Navn**-feltet angir du navnet på programmet som skal kobles til.
4. I feltet **Program** angir du URL-adressen til Finance- og Supply Chain Management-miljøet du vil koble til.
4. I feltet **Leietaker** angir du leietakeren i Finance- og Supply Chain Management-miljøet.
5. Velg **Lagre**.
6. Velg **Kontroller tilkobling** i handlingsruten for å teste tilkoblingen til miljøet. Lukk deretter siden.

## <a name="link-connected-applications-to-environments"></a>Koble tilkoblede programmer til miljøer

1. På siden **Miljøoppsett** velger du **Ny** for å tilordne et tilkoblet program til et miljø.
2. I feltet **Tilkoblet program** velger du det tilkoblede programmet.
3. Velg et tjenestemiljø i feltet **Servicemiljø**.
4. Velg **Lagre**, og lukk deretter siden.

## <a name="set-up-electronic-invoicing-integration-in-finance-and-supply-chain-management"></a>Konfigurere integrasjon av elektronisk fakturering i Finance og Supply Chain Management

### <a name="turn-on-the-electronic-invoicing-integration-feature"></a>Aktivere funksjonen for integrering av Elektronisk fakturering

1. Logg på Finance- eller Supply Chain Management-forekomsten din.
2. I arbeidsområdet **Funksjonsbehandling** søker du etter funksjonen **Integrasjon av Elektronisk fakturering**. Hvis denne funksjonen ikke vises på siden, velger du **Se etter oppdateringer**.
3. Velg funksjonen, og velg deretter **Aktiver nå**.

### <a name="set-up-the-service-endpoint-url"></a>Konfigurer URL-adressen for endepunkt for tjeneste

1. Gå til **Organisasjonsstyring \> Oppsett \> parametere for elektronisk dokument**.
2. I kategorien **Innsendingstjeneste**, i feltet **URL for endepunkt for tjeneste**, angir du riktig tjenesteendepunkt for Azure-geografien, som vist i følgende tabell.

    | Datasenter Azure-geografi | URL for tjenestesluttpunkt                                                       |
    |----------------------------|----------------------------------------------------------------------------|
    | USA øst                    | `https://electronicinvoicing.eus-il301.gateway.prod.island.powerapps.com/` |
    | USA vest                    | `https://electronicinvoicing.wus-il301.gateway.prod.island.powerapps.com/` |
    | Europa, nord                   | `https://electronicinvoicing.neu-il301.gateway.prod.island.powerapps.com/` |
    | Europa, vest                    | `https://electronicinvoicing.weu-il301.gateway.prod.island.powerapps.com/` |

3. I **Miljø**-feltet angir du navnet på tjenestemiljøet som er publisert i Elektronisk fakturering.
4. Velg **Lagre**, og lukk deretter siden.

### <a name="enable-flighting-keys"></a>Aktiver testversjoneringsnøkler

Aktiver testversjoneringsnøkler for Microsoft Dynamics 365 Finance eller Microsoft Dynamics 365 Supply Chain Management, versjon 10.0.17 eller tidligere. 
1. Utfør følgende SQL-kommando:

    INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('BusinessDocumentSubmissionServiceEnabled', 1)
    
    INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('ElectronicInvoicingServiceIntegrationFeature', 1)

2. Utfør en IISreset-kommando for alle AOS'-er.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
