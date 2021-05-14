---
title: Konfigurere valgfrie funksjoner for et evalueringsmiljø for Dynamics 365 Commerce
description: Dette emnet forklarer hvordan du konfigurerer valgfrie funksjoner for et evalueringsmiljø for Microsoft Dynamics 365 Commerce.
author: psimolin
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 0a93429e836d818458f11f6f6821fda237edc291
ms.sourcegitcommit: 9eadc7ca08e2db3fd208f5fc835551abe9d06dc8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/22/2021
ms.locfileid: "5936986"
---
# <a name="configure-optional-features-for-a-dynamics-365-commerce-evaluation-environment"></a>Konfigurere valgfrie funksjoner for et evalueringsmiljø for Dynamics 365 Commerce

[!include [banner](includes/banner.md)]

Dette emnet forklarer hvordan du konfigurerer valgfrie funksjoner for et evalueringsmiljø for Microsoft Dynamics 365 Commerce.

## <a name="prerequisites"></a>Forutsetninger

Hvis du vil evaluere de transaksjonelle e-postfunksjonene, må følgende forutsetninger oppfylles:

- Du har en e-postserver tilgjengelig (\[SMTP\]-server), som kan brukes fra Microsoft Azure-abonnementet der du klargjorde evalueringsmiljøet.
- Du har serverens fullstendig kvaliserte domenenavn (FQDN)/IP-adresse, SMTP-portnummer og godkjenningsinformasjon tilgjengelig.

## <a name="configure-the-image-back-end"></a>Konfigurere bildeserveren

### <a name="find-your-media-base-url"></a>Finne primær URL-adresse for media

> [!NOTE]
> Før du kan fullføre denne prosedyren, må du fullføre trinnene i [Konfigurere området i handel](cpe-post-provisioning.md#set-up-your-site-in-commerce).

1. Logg på Commerce-områdebyggeren ved hjelp av URL-adressen du noterte da du startet e-handel under klargjøring (se [Initialisere e-handel](provisioning-guide.md#initialize-e-commerce)).
1. Åpne **Fabrikam**-området.
1. Velg **Mediebibliotek** på menyen til venstre.
1. Velg et hvilket som helst enkeltbilde.
1. I egenskapsinspektøren til høyre finner du egenskapen **Offentlig URL**. Verdien er en URL. Her er et eksempel:

    `https://images-us-sb.cms.commerce.dynamics.com/cms/api/fabrikam/imageFileData/MA1nQC`.

1. Erstatt den siste identifikatoren i URL-adressen (**MA1nQC** i forrige eksempel) med strengen **search?fileName=**. Slik ser eksempel-URL-en ut etter at denne endringen er gjort:

    `https://images-us-sb.cms.commerce.dynamics.com/cms/api/fabrikam/imageFileData/search?fileName=`

    Denne URL-adressen er primær URL-adresse for media. Noter den.

### <a name="update-the-media-base-url"></a>Oppdatere primær URL-adresse for media

1. Logg på Commerce Headquarters.
1. Bruk menyen til venstre og gå til **Moduler \> Retail og Commerce \> Kanaloppsett \> Kanalprofiler**.
1. Velg **Rediger**.
1. Fra **Profilegenskaper** erstatter du egenskapsverdien for **Primær URL-adresse for medieserver** med den primære URL-adressen for media du opprettet tidligere.
1. Velg kanalen med navnet **scXXXXXXXXX**.
1. Klikk **Legg til** under **Profilegenskaper**.
1. For egenskapen som ble lagt til, velger du **Primær URL-adresse for medieserver** som egenskapsnøkkel. Som egenskapsverdi angir du primær URL-adresse for media som du opprettet tidligere.
1. Velg **Lagre**.

## <a name="configure-and-test-the-email-server"></a>Konfigurere og teste e-postserveren

> [!NOTE]
> SMTP-serveren eller e-posttjenesten du angir her, må være tilgjengelig fra Azure-abonnementet du bruker for miljøet.

1. Logg på Commerce Headquarters.
1. Bruk menyen til venstre for å gå til **Moduler \> Detaljhandel \> Hovedkvarteroppsett \> Parametere \> E-postparametere**.
1. I kategorien **SMTP-innstillinger** i feltet **Server for utgående e-post** angir du FQDN eller IP-adressen til SMTP-serveren eller e-posttjenesten.
1. I feltet **SMTP-portnummer** angir du portnummeret. (Hvis du ikke bruker Secure Sockets Layer \[SSL\], er standard portnummer **25**.)
1. Hvis godkjenning kreves, angir du verdier i feltene **Brukernavn** og **Passord**.
1. Velg **Lagre**.
1. Velg **Oppdater**.
1. Velg **SMTP** i **E-postleverandør**-feltet i kategorien **Test e-post**.
1. I feltet **Send til** angir du e-postadressen der du vil at test-e-posten skal leveres.
1. Velg **Send e-posttest**.

## <a name="configure-email-templates"></a>Konfigurere e-postmaler

E-postmalen for hver transaksjonshendelse du vil sende e-postmeldinger for, må oppdateres med en gyldig e-postadresse for avsender.

1. Logg på Commerce Headquarters.
1. Bruk menyen til venstre for å gå til **Moduler \> Detaljhandel \> Hovedkvarteroppsett \> Parametere \> Maler for e-post til organisasjon**.
1. Velg **Vis liste**.
1. Følg disse trinnene for hver mal i listen:

    1. Angi senderens e-postadresse i feltet **Avsenders e-postadresse**.
    1. Valgfritt: I feltet **Sendernavn** angir du navnet som skal brukes som sendernavn.

1. Velg **Lagre**.

## <a name="customize-email-templates"></a>Tilpasse e-postmaler

Det kan være lurt å tilpasse e-postmalene slik at de bruker forskjellige bilder. Eller kanskje du vil oppdatere koblingene i malene slik at de går til evalueringsmiljøet. Trinnene nedenfor forklarer hvordan du laster ned standardmaler, tilpasser dem og oppdaterer malene i systemet.

1. Bruk en webleser og last ned ZIP-filen [Microsoft Dynamics 365 Commerce Evaluering av standard e-postmaler](https://download.microsoft.com/download/d/7/b/d7b6c4d4-fe09-4922-9551-46bbb29d202d/Commerce.Preview.Default.Email.Templates.zip) til den lokale datamaskinen. Denne filen inneholder følgende HTML-dokumenter:

    - Ordrebekreftelsesmal
    - Utsted gavekort-mal
    - Ny ordre-mal
    - Pakke bestilt-mal
    - Hent ordre-mal

1. Tilpass malene ved hjelp av et tekst- eller HTML-redigeringsprogram. Se listen over [støttede tokener](#supported-tokens-in-the-email-template) senere i dette emnet.
1. Logg på Commerce.
1. Bruk menyen til venstre, og gå til **Moduler \> Organisasjonsstyring \> Oppsett \> Maler for e-post til organisasjon**.
1. Utvid listen til venstre for å se alle malene.
1. Følg denne fremgangsmåten for hver mal du vil tilpasse:

    1. Velg malen fra listen.
    1. Under **Innhold i e-postmelding** velger du riktig språkversjonen fra listen. (Standardspråket er **en-us**.)
    1. Velg **Rediger** under **Innhold i e-postmelding**. Ruten **Last opp e-postmal** vises.
    1. Velg **Bla gjennom**, og finn HTML-filen med det tilpassede innholdet.
    1. Velg **Last opp**. Malen lastes opp til systemet, og en forhåndsvisning vises.
    1. Velg **OK**.
    1. Valgfritt: Tilpass egenskapen **Emne** for malen.
    1. Velg **Lagre**.

### <a name="supported-tokens-in-the-email-template"></a>Støttede tokener i e-postmalen

Når e-posten gjengis, ersattes disse tokenene med de faktiske verdiene som gjelder for kunden og kundens ordre.

#### <a name="sales-order"></a>Salgsordre

Følgende tokener gjelder for den overordnede salgsordren.

| Navnet på tokenet | Token |
|-------------------|-------|
| Ordrenummer      | %salesid% |
| Kundens navn   | %customername% |
| Leveringsadresse  | %deliveryaddress% |
| Faktureringsadresse   | %customeraddress% |
| Bestillingsdato        | %shipdate% |
| Leveringsmåte     | %modeofdelivery% |
| Rabatt          | %discount% |
| Merverdiavgift         | %tax% |
| Ordretotal       | %total% |

#### <a name="sales-line"></a>Salgslinje

Følgende tokener erstattes med verdier for hvert produkt i ordren.

> [!NOTE]
> Sett inn tokenet **Produktliste - start** i begynnelsen av HTML-blokken som gjentas for hvert produkt, og sett inn tokenet **Produktliste - slutt** på slutten av blokken.

| Navnet på tokenet      | Token |
|------------------------|-------|
| Produktliste – start   | \<!--%tablebegin.salesline% --\> |
| Produktliste – slutt     | \<!--%tableend.salesline%--\> |
| Produktnavn           | %lineproductname% |
| beskrivelse            | %lineproductdescription% |
| Antall               | %linequantity% |
| Linjeenhetspris        | %lineprice% (verifiser) |
| linjevaresum        | %linenetamount% |
| linjerabatt          | %linediscount% |
| Forsendelsesdato              | %lineshipdate% |
| Innkjøpsmetode     | %linedeliverymode% |
| leveringsadresse       | %linedeliveryaddress% |
| Salgsenhet for linjen | %lineunit% |

## <a name="additional-resources"></a>Tilleggsressurser

[Oversikt over Dynamics 365 Commerce-evalueringsmiljø](cpe-overview.md)

[Klargjøre et evalueringsmiljø for Dynamics 365 Commerce](provisioning-guide.md)

[Konfigurere et Dynamics 365 Commerce-evalueringsmiljø](cpe-post-provisioning.md)

[Konfigurere BOPIS i et evalueringsmiljø for Dynamics 365 Commerce](cpe-bopis.md)

[Vanlige spørsmål om Dynamics 365 Commerce-evalueringsmiljø](cpe-faq.md)

[Microsoft Lifecycle Services (LCS)](/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[Retail Cloud Scale Unit (RCSU)](/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[Microsoft Azure-portal](https://azure.microsoft.com/features/azure-portal)

[Dynamics 365 Commerce-webområde](https://aka.ms/Dynamics365CommerceWebsite)


[!INCLUDE[footer-include](../includes/footer-banner.md)]