---
title: Konfigurer virtuelle Dataverse-tabeller
description: Dette emnet viser hvordan du konfigurerer, genererer, oppdaterer eksisterende virtuelle tabeller og analyserer genererte og tilgjengelige tabeller for Dynamics 365 Human Resources.
author: twheeloc
ms.date: 08/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CDSIntegrationAdministration
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-10-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: f7ffe522f0f17a21280e53728c6efc2823743733
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/31/2022
ms.locfileid: "8069152"
---
# <a name="configure-dataverse-virtual-tables"></a>Konfigurer virtuelle Dataverse-tabeller


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



Dynamics 365 Human Resources er en virtuell datakilde i Microsoft Dataverse. Den gir fullstendige opprettings-, lese-, oppdaterings- og sletteoperasjoner (CRUD) fra Dataverse og Microsoft Power Platform. Dataene for virtuelle tabeller er ikke lagret i Dataverse, men i programdatabasen.

Hvis du vil aktivere CRUD-operasjoner på Human Resources-enheter fra Dataverse, må du gjøre enhetene tilgjengelige som virtuelle tabeller i Dataverse. Dette lar deg utføre CRUD-operasjoner fra Dataverse og Microsoft Power Platform i Human Resources. Operasjonene støtter også den fullstendige forretningslogikken for Human Resources for å sikre dataintegritet ved skriving av data til enhetene.

> [!NOTE]
> Human Resources-enheter tilsvarer Dataverse-tabeller. Hvis du vil ha mer informasjon om Dataverse (tidligere Common Data Service) og terminologioppdateringer, kan du se [Hva er Microsoft Dataverse?](/powerapps/maker/data-platform/data-platform-intro)

## <a name="available-virtual-tables-for-human-resources"></a>Tilgjengelige virtuelle tabeller for Human Resources

Alle OData-enheter (Open Data Protocol) i Human Resources er tilgjengelige som virtuelle tabeller i Dataverse. De er også tilgjengelige i Power Platform. Du kan nå bygge apper og opplevelser med data direkte fra Human Resources med fullstendig CRUD-funksjonalitet, uten å kopiere eller synkronisere data til Dataverse. Du kan bruke Power Apps-portaler til å bygge eksterne nettsteder som muliggjør samarbeidsscenarier for forretningsprosesser i Human Resources.

Du kan vise listen over virtuelle tabeller som er aktivert i miljøet, og begynne å arbeide med enhetene i [Power Apps](https://make.powerapps.com), i løsningen **Dynamics 365 HR Virtual Tables**.

![Dynamics 365 HR Virtual Tables i Power Apps.](./media/hr-admin-integration-virtual-entities-power-apps.jpg)

## <a name="virtual-tables-versus-native-tables"></a>Virtuelle tabeller kontra interne tabeller

Virtuelle tabeller for Human Resources er ikke det samme som de interne Dataverse-tabeller som opprettes for Human Resources. 

De interne tabellene for Human Resources genereres separat og vedlikeholdes i HCM Common-løsningen i Dataverse. For interne tabeller lagres dataene i Dataverse og krever synkronisering med appdatabasen for Human Resources.

> [!NOTE]
> Hvis du vil ha en liste over de interne Dataverse-tabellene for Human Resources, kan du se [Dataverse-tabeller](./hr-developer-entities.md).

## <a name="setup"></a>Installasjon

Følg disse oppsettstrinnene for å aktivere virtuelle tabeller i miljøet.

### <a name="enable-virtual-tables-in-human-resources"></a>Aktiver virtuelle tabeller i Human Resources

Først må du aktivere virtuelle tabeller i arbeidsområdet **Funksjonsbehandling**.

1. Velg **Systemadministrasjon** i Human Resources.

2. Velg flisen **Funksjonsbehandling**.

3. Velg **Støtte for virtuell tabell for i HR i Dataverse**, og velg deretter **Aktiver**.

Hvis du vil ha mer informasjon om aktivering og deaktivering av funksjoner, kan du se [Behandle funksjoner](hr-admin-manage-features.md).

### <a name="register-the-app-in-microsoft-azure"></a>Registrere appen i Microsoft Azure

Du må registrere Human Resources-forekomsten i Azure Portal slik at Microsoft-identitetsplattform kan tilby godkjennings- og autorisasjonstjenester for appen og brukerne. Hvis du vil ha mer informasjon om registrering av apper i Azure, kan du se [Hurtigstart: Registrer en app i Microsoft-identitetsplattformen](/azure/active-directory/develop/quickstart-register-app).

1. Åpne [Microsoft Azure-portalen](https://portal.azure.com).

2. I listen over Azure-tjenester velger du **Appregistreringer**.

3. Velg **Ny registrering**.

4. I **Navn**-feltet angir du et beskrivende navn for appen. For eksempel **Virtuelle tabeller for Dynamics 365 Human Resources**.

5. I feltet **URI for omadressering** angir du URL-adressen til navneområdet til forekomsten av Human Resources.

6. Velg **Registrer**.

7. Når registreringen er fullført, viser Azure-portalen appregistreringens **Oversikt**-rute, som inkluderer **App-ID (klient)**. Noter **App-ID (klient)**. Du angir denne informasjonen når du [konfigurerer datakilden for den virtuelle tabellen](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-table-data-source).

8. I den venstre navigasjonsruten velger du **Sertifikater og hemmeligheter**.

9. I delen **Klienthemmeligheter** på siden, velger du **Ny klienthemmelighet**.

10. Angi en beskrivelse, velg en varighet og velg **Legg til**.

11. Registrer verdien for hemmeligheten fra **Verdi**-egenskapen til tabellen. Du angir denne informasjonen når du [konfigurerer datakilden for den virtuelle tabellen](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-table-data-source).

    > [!IMPORTANT]
    > Husk å notere hemmelighetens verdi. Hemmeligheten vises aldri på nytt når du forlater denne siden.

### <a name="install-the-dynamics-365-hr-virtual-table-app"></a>Installer Dynamics 365 HR Virtual Table-appen

Installer Dynamics 365 HR Virtual Table-appen i Power Apps-miljøet for å distribuere løsningspakken for den virtuelle tabellen til Dataverse.

1. I Human Resources åpner du siden **Microsoft Dataverse-integrering**.

2. Velg kategorien **Virtuelle tabeller**.

3. Velg **Installer virtuell tabellapp**.

### <a name="configure-the-virtual-table-data-source"></a>Konfigurere datakilden for den virtuelle tabellen

Det neste trinnet er å konfigurere datakilden for den virtuelle tabellen i Power Apps-miljøet.

1. Åpne [Administrasjonssenter for Power Platform](https://admin.powerplatform.microsoft.com).

2. I **Miljøer**-listen velger du Power Apps-miljøet som er tilknyttet Human Resources-forekomsten.

3. Velg **URL-adresse for miljø** i **Detaljer**-delen på siden.

4. I **huben for løsningstilstand** velger du **Avansert søk**-ikonet øverst til høyre på appsiden.

5. På siden **Avansert søk**, i rullegardinlisten **Søk etter**, velger du **Konfigurere virtuell datakilde for økonomi og drift**.

   > [!NOTE]
   > Installasjonen av den virtuelle tabellappen fra forrige konfigurasjonstrinn kan ta noen minutter. Hvis **Konfigurere virtuell datakilde for økonomi og drift** ikke er tilgjengelig i listen, venter du et minutt og oppdaterer listen.

6. Velg **Resultater**.

7. Velg posten **Microsoft HR-datakilde**.

8. Angi den nødvendige informasjonen for konfigurasjon av datakilden:

   - **Mål-URL-adresse**: URL-adressen til Human Resources-navneområdet. Formatet på mål-URL-adressen er:
     
     https://\<hostname\>.hr.talent.dynamics.com/namespaces/\<namespaceID\>/

     For eksempel:
     
     `https://aos.rts-sf-5ea54e35c68-westus2.hr.talent.dynamics.com/namespaces/49d24c565-8f4d-4891-b174-bf83d948ed0c/`

     >[!NOTE]
     >Pass på at du inkluderer tegnet **/** på slutten av URL-adressen for å unngå å motta en feil.

     >[!NOTE]
     >Mål-URL-adressen bestemmer Human Resources-miljøet som virtuelle tabeller vil peke til for data. Hvis du oppretter et sandkassemiljø ved å opprette en kopi av produksjonsmiljøet, oppdaterer du denne verdien til navneområde-URL-en for det nye sandkassemiljøet. Dette sikrer at de virtuelle tabellene er koblet til dataene fra sandkassemiljøet i stedet for fortsatt å peke på produksjonsmiljøet.

   - **Leier-ID**: Leier-ID for Azure Active Directory ( Azure AD).

   - **AAD-app-ID**: App-ID (klient) som ble opprettet for appen som er registrert i Microsoft Azure-portalen. Du har mottatt denne informasjonen tidligere i trinnet [Registrere appen i Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).

   - **AAD-apphemmelighet**: Klienthemmeligheten som ble opprettet for appen som er registrert i Microsoft Azure-portalen. Du har mottatt denne informasjonen tidligere i trinnet [Registrere appen i Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).

   ![Microsoft HR-datakilde.](./media/hr-admin-integration-virtual-entities-hr-data-source.jpg)

9. Velg **Lagre og lukk**.

### <a name="grant-app-permissions-in-human-resources"></a>Gi apptillatelser i Human Resources

Gi tillatelser for de to Azure AD-appene i Human Resources:

- Appen som ble opprettet for leieren din i Microsoft Azure-portalen
- Dynamics 365 HR Virtual Table-appen som er installert i Power Apps-miljøet 

1. I Human Resources åpner du siden **Azure Active Directory-apper**.

2. Velg **Ny** for å opprette en ny appost:

    - I **Klient-ID**-feltet angir du klient-ID-en til appen du registrerte i Microsoft Azure-portalen.
    - I **Navn**-feltet angir du navnet til appen du registrerte i Microsoft Azure-portalen.
    - I **Bruker-ID**-feltet velger du bruker-ID-en til en bruker med administratortillatelser i Human Resources og Power Apps-miljøet.

3. Velg **Ny** for å opprette enda en appost:

    - **Klient-ID**: f9be0c49-aa22-4ec6-911a-c5da515226ff
    - **Navn**: Dynamics 365 HR Virtual Table
    - I **Bruker-ID**-feltet velger du bruker-ID-en til en bruker med administratortillatelser i Human Resources og Power Apps-miljøet.

## <a name="generate-virtual-tables"></a>Generere virtuelle tabeller

Når installasjonen er fullført, kan du velge de virtuelle tabeller du vil generere og aktivere i Dataverse-forekomsten.

1. I Human Resources åpner du siden **Microsoft Dataverse-integrering**.

2. Velg kategorien **Virtuelle tabeller**.

> [!NOTE]
> Veksleknappen for **aktivering av virtuell tabell** vil bli satt til **Ja** automatisk når alle nødvendige oppsett er fullført. Hvis veksleknappen er satt til **Nei**, går du gjennom trinnene i tidligere deler av dette dokumentet for å være sikker på at alle nødvendige oppsett er fullført.

3. Velg tabellen eller tabellene du vil generere i Dataverse.

4. Velg **Generer/oppdater**.

![Dataverse-integrering.](./media/hr-admin-integration-dataverse-integration.png)

## <a name="check-table-generation-status"></a>Kontrollere status for tabellgenerering

Virtuelle tabeller blir generert i Dataverse gjennom en asynkron bakgrunnsprosess. Oppdateringer av prosessvisningen i handlingssenteret. Detaljer om prosessen, inkludert feillogger, vises på siden for **prosessautomatiseringer**.

1. I Human Resources åpner du **Prosessautomatiseringer**-siden.

2. Velg kategorien **Bakgrunnsprosesser**.

3. Velg **Bakgrunnsprosess for asynkron operasjon for virtuell tabell**.

4. Velg **Vis de siste resultatene**.

Hurtigmenyen viser de siste utførelsesresultatene for prosessen. Du kan vise loggen for prosessen, inkludert eventuelle feil som returneres fra Dataverse.

## <a name="see-also"></a>Se også

[Hva er Dataverse?](/powerapps/maker/common-data-service/data-platform-intro)<br>
[Tabeller i Dataverse](/powerapps/maker/common-data-service/entity-overview)<br>
[Oversikt over tabellrelasjoner](/powerapps/maker/common-data-service/relationships-overview)<br>
[Opprette og redigere virtuelle tabeller som inneholder data fra en ekstern datakilde](/powerapps/maker/common-data-service/create-edit-virtual-entities)<br>
[Hva er Power Apps-portaler?](/powerapps/maker/portals/overview)<br>
[Oversikt over oppretting av apper i Power Apps](/powerapps/maker/)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
