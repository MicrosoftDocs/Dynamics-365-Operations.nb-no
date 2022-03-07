---
title: Komme i gang med tjenesteadministrasjon for tillegget for Elektronisk fakturering
description: Dette emnet beskriver hvordan du kommer i gang med tillegget Elektronisk fakturering.
author: gionoder
manager: AnnBe
ms.date: 03/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
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
ms.openlocfilehash: 05b00380cec7511adad2467d3f252799a4aaee5c
ms.sourcegitcommit: 543772ee97efe215cf6f2ec6e092cc1568919f20
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/13/2021
ms.locfileid: "5592532"
---
# <a name="get-started-with-electronic-invoicing-add-on-service-administration"></a>Komme i gang med tjenesteadministrasjon for tillegget for Elektronisk fakturering

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

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

## <a name="install-the-add-on-for-microservices-in-lifecycle-services"></a>Installere tillegget for mikrotjenester i Lifecycle Services

1. Logg på LCS-kontoen.
2. Velg flisen **Administrasjon av forhåndsvisningsfunksjoner**.
3. Velg delen **Funksjoner i offenlig forhåndsversjon** velger du **E-faktureringstjeneste**.
4. Kontroller at alternativet **Forhåndsversjon aktivert** er satt til **Ja**.
5. Velg LCS-distribusjonsprosjektet på LCS-instrumentbordet. LCS-prosjektet må kjøre.
7. I fanen **Miljøtillegg** velger du **Installer et nytt tillegg**.
8. Velg **e-faktureringstjenester**, og i feltet **ID for AAD-program** angir du **091c98b0-a1c9-4b02-b62c-7753395ccabe**. Dettee er en fast verdi.
10. I feltet **AAD-leier-ID** angir du leier-IDen for kontoen for Azure-abonnementet.
11. Gå gjennom vilkårene og betingelsene og merk deretter av i avmeringsboksen.
12. Velg **Installer**.


## <a name="set-up-the-parameters-for-rcs-integration-with-the-electronic-invoicing-add-on"></a>Konfigurere parametere for RCS-integrasjon med Elektronisk fakturering-tillegget

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
5. I feltet **ID for LCS-miljø** angir du IDen for LCS-abonnementskontoen.
6. Velg **Lagre**, og lukk deretter siden.

## <a name="create-key-vault-secret"></a>Opprette Key Vault-hemmelighet

1. Logg på RCS-kontoen.
2. I arbeidsområdet **Globaliseringsfunksjon** velger du tittelen **Tillegg for elektronisk fakturering** i delen **Miljø**.
3. På siden for **Miljøkonfigurasjon**, i handlingsruten, velger du **Tjenestemiljø**, og deretter velger du **Key Vault-parametere**.
4. Velg **Ny** for å opprette en Key Vault-nøkkel.
5. I **Navn**-feltet angir du navnet på Key Vault-hemmeligheten. Angi en beskrivelse i **Beskrivelse**-feltet.
6. Lim inn hemmeligheten fra Azure Key Vault i feltet **URI for Key Vault**.
7. Velg **Lagre**.

## <a name="create-storage-account-secret"></a>Opprette hemmelighet for lagringskonto

1. Gå til **Systemadministrasjon** > **Oppsett** > **Key Vault-parametere**, og velg en Key Vault-hemmelighet.
2. Velg **Legg til** i delen **Sertifikater**.
3. I feltet **Navn** angir du navnet på lagringskontonavnet og en beskrivelse i feltet **Beskrivelse**.
4. I feltet **Type** velger du **Sertifikat**.
5. Velg **Lagre**, og lukk deretter siden.

## <a name="create-a-digital-certificate-secret"></a>Opprette et digitalt sertifikat og opprette et digitalt sertifikat

1. Gå til **Systemadministrasjon** > **Oppsett** > **Key Vault-parametere**, og velg en Key Vault-hemmelighet.
2. Velg **Legg til** i delen **Sertifikater**.
3. I feltet **Navn** angir du navnet på den digitale sertifikathemmeligheten, og i feltet **Beskrivelse** angir du en beskrivelse.
4. I feltet **Type** velger du **Sertifikat**.
5. Velg **Lagre**, og lukk deretter siden.

## <a name="create-an-electronic-invoicing-add-on-environment"></a>Opprette et miljø for tillegget Elektronisk fakturering

1. Logg på RCS-kontoen.
2. I arbeidsområdet **Globaliseringsfunksjon** velger du tittelen **Tillegg for elektronisk fakturering** i delen **Miljø**.

## <a name="create-a-service-environment"></a>Opprette et tjenestemiljø

1. Velg **Tjenestemiljø** på siden **Miljøoppsett** i handlingsruten.
2. Velg **Ny** for å opprette et nytt tjenestemiljø.
3. I **Navn**-feltet angir du navnet på e-fakturamiljøet. Angi en beskrivelse i **Beskrivelse**-feltet.
4. I feltet **Lagring av for SAS-tokenhemmelighet** velger du navnet på lagringskontohemmeligheten som må brukes til å godkjenne tilgang til lagringskontoen.
5. I **Brukere**-delen velger du **Legg til** for å legge til en bruker som har tillatelse til å sende elektroniske fakturaer gjennom miljøet og også koble seg til lagringskontoen.
6. I **Bruker-ID**-feltet angir du aliaset til brukeren. Angi brukerens e-postadresse i feltet **E-post**.
7. Velg **Lagre**.
8. Hvis den land/område-spesifikke fakturaen krever en sertifikatkjede for å bruke digitale signaturer, velger du **Kjede av sertifikater** og deretter, i handlingsruten, velger du **Key Vault-hemmeligheter**, og følg deretter denne fremgangsmåten:

    1. Velg **Ny** for å opprette en kjede av sertifikater.
    2. I **Navn**-feltet angir du navnet på kjeden av sertifikater. Angi en beskrivelse i **Beskrivelse**-feltet.
    3. I delen **Sertifikater** velger du **Legg til** for å legge til et sertifikat i kjeden.
    4. Bruk knappene **Opp** eller **Ned** for å endre posisjonen til sertifikatene i kjeden.
    5. Velg **Lagre**, og lukk deretter siden.
    6. Lukk siden.
9. På siden **Tjenestemiljø**, i handlingsruten, velger du **Publiser** for å publisere miljøet til skyen. Verdien i feltet **Status** endres til **Publisert**.

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

## <a name="set-up-the-electronic-invoicing-add-on-integration-in-finance-and-supply-chain-management"></a>Konfigurere integrasjonen av tillegget Elektronisk fakturering i Finance og Supply Chain Management

### <a name="turn-on-the-electronic-invoicing-add-on-integration-feature"></a>Aktivere funksjonen for integrering av tillegget Elektronisk fakturering

1. Logg på Finance- eller Supply Chain Management-forekomsten din.
2. I arbeidsområdet **Funksjonsbehandling** søker du etter funksjonen **Integrasjon av tillegget Elektronisk fakturering**. Hvis denne funksjonen ikke vises på siden, velger du **Se etter oppdateringer**.
3. Velg funksjonen, og velg deretter **Aktiver nå**.

### <a name="set-up-the-service-endpoint-url"></a>Konfigurer URL-adressen for endepunkt for tjeneste

1. Gå til **Organisasjonsstyring \> Oppsett \> parametere for elektronisk dokument**.
2. I kategorien **Innsendingstjeneste**, i feltet **URL for endepunkt for tjeneste**, angir du riktig tjenesteendepunkt for Azure-geografien, som vist i følgende tabell.

    | Datasenter Azure-geografi | URL for tjenestesluttpunkt                                                       |
    |----------------------------|----------------------------------------------------------------------------|
    | USA øst                    | `https://electronicinvoicing.eus-il301.gateway.prod.island.powerapps.com/` |
    | USA vest                    | `https://electronicinvoicing.wus-il301.gateway.prod.island.powerapps.com/` |
    | EU nord                   | `https://electronicinvoicing.neu-il301.gateway.prod.island.powerapps.com/` |
    | EU vest                    | `https://electronicinvoicing.weu-il301.gateway.prod.island.powerapps.com/` |

3. I **Miljø**-feltet angir du navnet på miljøet for tillegget Elektronisk fakturering.
4. Velg **Lagre**, og lukk deretter siden.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
