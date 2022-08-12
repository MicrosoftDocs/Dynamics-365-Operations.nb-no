---
title: Aktiver hoveddataoppslag for mva-beregningskonfigurasjon
description: Denne artikkelen beskriver hvordan du konfigurerer og aktiverer oppslagsfunksjonen for hoveddata i avgiftsberegning.
author: kai-cloud
ms.date: 07/14/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.custom: ''
ms.search.region: Global
ms.author: pashao
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 3642bb88d5b0570014513b64eef5fdab6d1ee9d3
ms.sourcegitcommit: 5b721f6fc1ba4350b5bd0eae457f71d80246db42
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/20/2022
ms.locfileid: "9181132"
---
# <a name="enable-master-data-lookup-for-tax-calculation-configuration"></a>Aktiver hoveddataoppslag for mva-beregningskonfigurasjon 

[!include [banner](../includes/banner.md)]

Denne artikkelen beskriver hvordan du konfigurerer og aktiverer oppslagsfunksjonen for hoveddata i avgiftsberegning. En rullegardinliste er tilgjengelig for å velge verdier i mva-beregningskonfigurasjonen for felter som **Juridisk enhet**, **Leverandørkonto**, **Varekode** og **Leveringsbetingelse**. Disse verdiene kommer fra det tilkoblede Microsoft Dynamics 365 Finance-miljøet ved hjelp av Microsoft Dataverse-datakilden.

> [!NOTE] 
> Funksjonen for hoveddataoppslag for avgiftsberegning er valgfri funksjonalitet. Du kan hoppe over følgende trinn hvis du deaktiverer funksjonen **Støtte for Dataverse-datakilder for avgiftstjeneste** i RCS (Regulatory Configuration Service). I så fall vil imidlertid ikke rullegardinlisten være tilgjengelig i konfigurasjonen for avgiftsberegningen.

Hvis du vil aktivere rullegardinlisten i konfigurasjonen av funksjonsversjonen for avgiftsberegning, kan du fullføre fremgangsmåten nedenfor.

1. [Aktiver Microsoft Power Platform-integrering og åpne Dataverse-miljøet.](#enable)
2. [Installer virtuelle Finance and Operations-enheter.](#install)
3. [Registrer en Azure Active Directory-app (Azure AD).](#register)
4. [Gi apptillatelser i økonomi- og driftsapper.](#grant)
5. [Konfigurer datakilden for den virtuelle enheten.](#configure)
6. [Aktiver virtuelle Dataverse-enheter.](#virtual)
7. [Konfigurer den tilkoblede appen for avgiftsberegning.](#set-up)
8. [Importer og konfigurer Dataverse-modelltilordningskonfigurasjonen.](#import)

## <a name="enable-microsoft-power-platform-integration-and-open-the-dataverse-environment"></a><a name='enable'></a>Aktiver Microsoft Power Platform-integrering og åpne Dataverse-miljøet

Integreringen av økonomi- og driftsapper med Microsoft Power Platform kan aktiveres når du oppretter et nytt miljø for økonomi- og driftsapper i Microsoft Dynamics Lifecycle Services (LCS). Hvis du vil ha mer informasjon, kan du se [Microsoft Power Platform-integrering – oversikt over tillegg](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md). Når du er ferdig, vises navnet på et Microsoft Power Platform-miljø i **Power Platform Integrering**-delen.

1. I LCS, i Finance and Operations-miljøet, i delen **Power Platform-integrering**, finner du og noterer verdien for **Miljønavn** for det koblede miljøet.

    [![Verdi for Miljønavn.](./media/tcs-dataverse-master-data-lookup-1.png)](./media/tcs-dataverse-master-data-lookup-1.png)

2. I [Power Platform-administrasjonssenteret](https://admin.powerplatform.microsoft.com/environments), på **Miljøer**-fanen, velger du miljøet som samsvarer med verdien for **Miljønavn** som du noterte ned.
3. På **Detaljer**-siden finner du verdien for **URL-adresse for miljø** til Dataverse-miljøet. Noter ned denne verdien, for du trenger den i [trinn 7: Konfigurer den tilkoblede appen for avgiftsberegning](#set-up).
4. Kontroller at du kan åpne Dataverse-miljøet i nettleseren ved å velge verdien for **URL-adresse for miljø**.

    [![Dataverse-miljøsiden.](./media/tcs-dataverse-master-data-lookup-2.png)](./media/tcs-dataverse-master-data-lookup-2.png)

    > [!NOTE]
    > La Dataverse-miljøet være åpent i nettleseren. Du trenger det i [trinn 5: Konfigurer datakilden for den virtuelle enheten](#configure).

Hvis du vil ha mer informasjon, kan du se [Aktivere Microsoft Power Platform-integrasjon](../../fin-ops-core/dev-itpro/power-platform/enable-power-platform-integration.md).

## <a name="install-finance-and-operations-virtual-entities"></a><a name='install'></a>Installer virtuelle Finance and Operations-enheter

Dataverse-løsningen for virtuelle Finance and Operations-enheter må installeres fra Microsoft AppSource-løsningen for virtuelle enheter.

1. I AppSource finner du den [virtuelle Finance and Operations-enheten](https://appsource.microsoft.com/product/dynamics-365/mscrm.finance_and_operations_virtual_entity).
2. Velg **Få den nå**.
3. I feltet **Velg et miljø** angir du verdien for **Miljønavn** som du noterte ned tidligere.
4. Merk av i boksene, og velg deretter **Installer**.

Når installasjonen er fullført, kan du finne appen for den **virtuelle Finance and Operations-enheten** i [Power Platform-administrasjonssenteret](https://admin.powerplatform.microsoft.com/) under **Ressurser** \> **Dynamics 365-apper**.

Hvis du vil ha mer informasjon, kan du se [Skaffe løsningen for den virtuelle enheten](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#get-virtual-entity-solution).

## <a name="register-an-azure-ad-application"></a><a name='register'></a>Registrer en Azure AD-app

Du må registrere en Azure AD-app i samme leier som økonomi- og driftsappene, slik at de kan kalles av Dataverse.

1. I [Azure-portalen](https://portal.azure.com) går du til **Azure Active Directory \> Appregistreringer**.
2. Velg **Ny registrering**, og angi følgende informasjon:

    - **Navn** – Angi et unikt navn.
    - **Kontotype** – Angi **Enhver Azure AD-katalog** (én leier eller flere leiere).
    - **URI for omadressering** – La dette feltet stå tomt.

3. Velg **Registrer**.
4. Noter verdien i **App-ID (klient)** ettersom du vil trenge den senere.

    [![ID-verdi for Azure AD-app (klient).](./media/tcs-dataverse-master-data-lookup-3.png)](./media/tcs-dataverse-master-data-lookup-3.png)

5. Opprett en symmetrisk nøkkel for appen.
6. I den nye appen velger du **Sertifikater og hemmeligheter**.
7. Velg **Ny klienthemmelighet**.
8. Angi en beskrivelse, velg en utløpsdato og velg deretter **Lagre**. En nøkkel opprettes og vises. Kopier verdien til senere bruk.

Hvis du vil ha mer informasjon, kan du se [Registrer Azure AD-app](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#register-the-app-in-the-azure-portal).

## <a name="grant-app-permissions-in-finance-and-operations-apps"></a><a name='grant'></a>Gi apptillatelser i økonomi- og driftsapper

Dataverse bruker Azure AD-appen du opprettet for å kalle økonomi- og driftsapper. Appen må derfor klareres av økonomi- og driftsappene og knyttes til en brukerkonto som har de riktige rettighetene. I økonomi- og driftsappene må du opprette en spesiell tjenestebruker som har rettigheter **kun** til funksjonaliteten for den virtuelle enheten. Denne tjenestebrukeren må ikke ha noen andre rettigheter. Når du har fullført dette trinnet, kan alle apper som har hemmeligheten til Azure AD-appen du opprettet, kalle miljøet for økonomi- og driftsapper og få tilgang til funksjonaliteten for den virtuelle enheten.

1. Gå til **Systemadministrasjon** \> **Brukere** \> **Brukere** i miljøet ditt.
2. Velg **Ny** for å legge til en ny bruker, og angi følgende informasjon:

    - **Bruker-ID** – Angi **dataverseintegration** eller en annen verdi.
    - **Brukernavn** – Angi **dataverse integration** eller en annen verdi.
    - **Leverandør** – Sett dette feltet til **NonAAD**.
    - **E-post** – Angi **dataverseintegration** eller en annen verdi. (Verdien behøver ikke å være en gyldig e-postkonto.)

3. Tilordne sikkerhetsrollen **Program for virtuell enhet for CDS** til brukeren.
4. Fjern alle andre roller, inkludert **Systembruker**.
5. Gå til **Systemadministrasjon** \> **Oppsett** \> **Azure Active Directory-apper** for å registrere Dataverse. 
6. Legg til en rad, gå til feltet **Klient-ID**, og angi verdien for **App-ID (klient)** du noterte ned tidligere.
7. Angi et navn i **Navn**-feltet. Skriv for eksempel inn **Dataverse-integrering**.
8. Velg bruker-IDen du opprettet tidligere, i **Bruker-ID**-feltet.

Hvis du vil ha mer informasjon, kan du se [Gi apptillatelser i økonomi- og driftsapper](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#grant-app-permissions-in-finance-and-operations-apps).

## <a name="configure-the-virtual-entity-data-source"></a><a name='configure'></a>Konfigurere datakilden for den virtuelle enheten

Du må oppgi Dataverse sammen med økonomi- og driftsappforekomsten du skal koble til.

1. Dataverse-miljøet må fortsatt være åpent i nettleseren fra [trinn 1: Aktiver Microsoft Power Platform-integrering og åpne Dataverse-miljøet](#enable). Velg Innstillinger-knappen (tannhjulsymbolet) øverst til høyre, og velg deretter **Avanserte innstillinger**.

    [![Åpne Avanserte innstillinger i Dataverse-miljøet.](./media/tcs-dataverse-master-data-lookup-4.png)](./media/tcs-dataverse-master-data-lookup-4.png)

2. På rullegardinmenyen **Innstillinger** velger du **Administrasjon**.

    [![Administrasjon.](./media/tcs-dataverse-master-data-lookup-5.png)](./media/tcs-dataverse-master-data-lookup-5.png)

3. Velg **Datakilder for virtuell enhet**.

    [![Datakilder for virtuell enhet.](./media/tcs-dataverse-master-data-lookup-6.png)](./media/tcs-dataverse-master-data-lookup-6.png)

4. Velg datakilden med navnet **Finance and Operations**.

    [![Finance and Operations-datakilden.](./media/tcs-dataverse-master-data-lookup-7.png)](./media/tcs-dataverse-master-data-lookup-7.png)

5. Angi følgende informasjon fra tidligere trinn:

    - **Mål-URL-adresse** – Angi URL-adressen der du kan få tilgang til økonomi- og driftsapper.
    - **OAuth-URL-adresse** – Angi `https://login.windows.net/`.
    - **Leier-ID** – Angi leieren din. Denne verdien kan være domenenavnet til bedriftens e-post (for eksempel contoso.com).
    - **AAD-app-ID** – Angi verdien for **App-ID (klient)** som ble opprettet tidligere.
    - **AAD-apphemmelighet** – Angi hemmeligheten som ble generert tidligere.
    - **AAD-ressurs** – Angi **00000015-0000-0000-c000-000000000000**. Denne verdien er Azure AD-appen som representerer økonomi- og driftsapper. Den skal alltid være den samme verdien.

6. Lagre endringene.
7. Lukk siden for å gå tilbake til **Administrasjon**-siden, der du starter på [trinn 6: Aktiver virtuelle Dataverse-enheter](#virtual).

    [![Lukk enheten for redigering.](./media/tcs-dataverse-master-data-lookup-8.png)](./media/tcs-dataverse-master-data-lookup-8.png)

Hvis du vil ha mer informasjon, kan du se [Konfigurer datakilden for den virtuelle enheten](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#configure-the-virtual-entity-data-source).

## <a name="enable-dataverse-virtual-entities"></a><a name='virtual'></a>Aktiver virtuelle Dataverse-enheter

Synligheten til de virtuelle enhetene fra økonomi- og driftsapper må settes til **Ja** før de kan forbrukes av konfigurasjonen for avgiftsberegning.

> [!NOTE]
> Du kan hoppe over dette trinnet ved å aktivere avgiftsberegningsrelaterte virtuelle enheter ved bare ett klikk i [trinn 8: Konfigurer den tilkoblede appen for avgiftsberegning](#import). Vi anbefaler imidlertid at du aktiverer minst én virtuell enhet manuelt, for å angi at forbindelsen mellom økonomi- og driftsapper og Dataverse er veletablert.

1. I Dataverse-miljøet, på **Administrasjon**-siden velger du filterknappen (traktsymbol) øverst til høyre.

    [![Filterknapp.](./media/tcs-dataverse-master-data-lookup-9.png)](./media/tcs-dataverse-master-data-lookup-9.png)

2. I vinduet **Avansert søk**, i feltet **Se etter**, velger du **Tilgjengelige Finance and Operations-enheter**.
3. Legg til følgende regel: **Navn** – **Inneholder** – **CompanyInfoEntity**. Velg deretter **Resultater**.

    [![Vinduet Avansert søk.](./media/tcs-dataverse-master-data-lookup-10.png)](./media/tcs-dataverse-master-data-lookup-10.png)

4. Velg **CompanyInfoEntity** i søkeresultatene, merk av for **Synlig**, og velg deretter **Lagre**.

    [![Angi enhetssynlighet.](./media/tcs-dataverse-master-data-lookup-11.png)](./media/tcs-dataverse-master-data-lookup-11.png)

5. Gjenta trinnene over for følgende enheter som det refereres til i konfigurasjonen for avgiftsberegning:

    - CompanyInfoEntity
    - CurrencyEntity
    - CustCustomerV3Entity
    - DeliveryTermsEntity
    - EcoResProductCategoryEntity
    - EcoResReleasedProductV2Entity
    - LogisticsAddressCountryRegionTranslationEntity
    - LogisticsAddressStateEntity
    - PurchProcurementChargeCDSEntity
    - SalesChargeCDSEntity
    - TaxGroupEntity
    - TaxItemGroupHeadingEntity
    - VendVendorV2Entity
    - InventOperationalSiteV2Entity
    - TaxExemptCodeEntity
    - InventWarehouseEntity

    > [!NOTE]
    > Bare de første 5000 postene for en enhet kan hentes av Dataverse og gjøres tilgjengelig i rullegardinlisten i konfigurasjonen av avgiftsberegning.

Hvis du vil ha mer informasjon, kan du se [Aktiver Microsoft Dataverse virtuelle enheter](../../fin-ops-core/dev-itpro/power-platform/enable-virtual-entities.md).

## <a name="set-up-the-connected-application-for-tax-calculation"></a><a name='set-up'></a>Konfigurer den tilkoblede appen for avgiftsberegning

1. Åpne arbeidsområdet **Funksjonsstyring** i RCS, og aktiver følgende funksjoner:

    - Støtte for Dataverse-datakilder for elektronisk rapportering
    - Støtte for Dataverse-datakilder for avgiftstjeneste
    - Globaliseringsfunksjoner

2. Gå til **Elektronisk rapportering**, og deretter, i delen **Relaterte koblinger**, velger du **Tilkoblede apper**.

    [![Tilkoblede apper.](./media/tcs-dataverse-master-data-lookup-12.png)](./media/tcs-dataverse-master-data-lookup-12.png)

3. Velg **Ny** for å legge til en oppføring, og angi følgende informasjon.

    - **Navn** – Angi et navn.
    - **Type** – Velg **Dataverse**.
    - **App** – Angi Dataverse-miljøets verdi for **URL-adresse for miljø**, som du noterte ned i [trinn 1: Aktiver Microsoft Power Platform-integrering og åpne Dataverse-miljøet](#enable).
    - **Leier** – Angi leieren din.
    - **Egendefinert URL-adresse** – Angi URL-adressen for Dataverse, og legg til **/api/data/v9.1** etter den.

4. Velg **Kontroller tilkobling**. I dialogboksen som vises, velger du **Klikk her** for å koble til den eksterne appen som er valgt.

    [![Kontroller tilkoblingen.](./media/tcs-dataverse-master-data-lookup-13.png)](./media/tcs-dataverse-master-data-lookup-13.png)
5. Pass på at du får meldingen "Vellykket!", som indikerer at tilkoblingen ble opprettet.

    [![Vellykket-melding.](./media/tcs-dataverse-master-data-lookup-14.png)](./media/tcs-dataverse-master-data-lookup-14.png)

## <a name="import-and-set-up-the-dataverse-model-mapping-configuration"></a><a name='import'></a>Importer og konfigurer Dataverse-modelltilordningskonfigurasjonen

Microsoft tilbyr standard modelltilordningskonfigurasjoner for enheter fra økonomi- og driftsapper til avgiftsberegning.

1. Gå til **Elektronisk rapportering** i RCS.
2. I delen **Konfigurasjonsleverandører**, på flisen for **Microsoft**-leverandøren, velger du **Repositorier**.

    [![Repositorier.](./media/tcs-dataverse-master-data-lookup-15.png)](./media/tcs-dataverse-master-data-lookup-15.png)

3. Velg posten **Globalt konfigurasjonsrepositorium**, og velg deretter **Åpne**.
4. Under **Avgiftsdatamodell** \> **Datamodell for avgiftsberegning** velger du konfigurasjonen **Dataverse-modelltilordning**.
5. På hurtigfanen **Versjoner** velger du en versjon som samsvarer med versjonen av økonomi- og driftsappene, og deretter velger du **Importer**.

    [![Importere konfigurasjonen for Dataverse-modelltilordning.](./media/tcs-dataverse-master-data-lookup-16.png)](./media/tcs-dataverse-master-data-lookup-16.png)

    > [!IMPORTANT]
    > Konfigurasjonen **Dataverse-modelltilordning** er bare effektiv på den høyeste importerte versjonen. Derfor bør du ikke importere en versjon av konfigurasjonen for **Dataverse-modelltilordning** som er høyere enn versjonen av konfigurasjonen for avgiftsberegning du planlegger å implementere. Hvis du for eksempel planlegger å implementere versjon 40.50.225 konfigurasjonen for avgiftsberegning, bør du bare importere versjon 40.50.13 av konfigurasjonen for **Dataverse-modelltilordning**. Du bør ikke importere versjon 40.54.14. Ellers vil det oppstå en datamodellkonflikt i konfigurasjonen.

6. Gå tilbake til **Elektronisk rapportering**, og velg flisen **Avgiftskonfigurasjoner**.
7. Velg den importerte konfigurasjonen for **Dataverse-modelltilordning**, og velg deretter **Rediger**.
8. Sett alternativet **Standard for modelltilordning** til **Ja**.
9. I feltet **Tilkoblet app** velger du den tilkoblede appen du konfigurerte i [trinn 7: Konfigurer den tilkoblede appen for avgiftsberegning](#set-up).
10. Sett alternativet **Angi synlighet for virtuell tabell** til **Ja** for å gjøre alle virtuelle enheter relatert til avgiftsberegning synlige.

Du har nå fullført oppsettet for oppslagsfunksjonaliteten for hoveddata. En rullegardinliste for felter, som for eksempel **Juridisk enhet**, **Leverandørkonto**, **Varekode** og **Leveringsbetingelse** fra Dynamics 365 Finance blir nå aktivert i oppsettet av **versjonen for avgiftsberegningsfunksjonen**.

[![Rullegardinlisten Juridisk enhet.](./media/tcs-dataverse-master-data-lookup-17.png)](./media/tcs-dataverse-master-data-lookup-17.png)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
