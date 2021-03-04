---
title: Konfigurere virtuelle enheter for Common Data Service
description: Dette emnet beskriver hvordan du konfigurerer virtuelle enheter for Dynamics 365 Human Resources. Generer og oppdater eksisterende virtuelle enheter og analyser genererte og tilgjengelige enheter.
author: andreabichsel
manager: tfehr
ms.date: 11/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: CDSIntegrationAdministration
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-10-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 2b590faeab600d04c9d5303693ec1e9ac682250d
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/25/2020
ms.locfileid: "4645607"
---
# <a name="configure-common-data-service-virtual-entities"></a>Konfigurere virtuelle enheter for Common Data Service

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Dynamics 365 Human Resources er en virtuell datakilde i Common Data Service. Den gir fullstendige opprettings-, lese-, oppdaterings- og sletteoperasjoner (CRUD) fra Common Data Service og Microsoft Power Platform. Dataene for virtuelle enheter er ikke lagret i Common Data Service, men i programdatabasen. 

Hvis du vil aktivere CRUD-operasjoner på Human Resources-enheter fra Common Data Service, må du gjøre enhetene tilgjengelige som virtuelle enheter i Common Data Service. Dette lar deg utføre CRUD-operasjoner fra Common Data Service og Microsoft Power Platform i Human Resources. Operasjonene støtter også den fullstendige forretningslogikken for Human Resources for å sikre dataintegritet ved skriving av data til enhetene.

## <a name="available-virtual-entities-for-human-resources"></a>Tilgjengelige virtuelle enheter for Human Resources

Alle OData-enheter (Open Data Protocol) i Human Resources er tilgjengelige som virtuelle enheter i Common Data Service. De er også tilgjengelige i Power Platform. Du kan nå bygge apper og opplevelser med data direkte fra Human Resources med fullstendig CRUD-funksjonalitet, uten å kopiere eller synkronisere data til Common Data Service. Du kan bruke Power Apps-portaler til å bygge eksterne nettsteder som muliggjør samarbeidsscenarier for forretningsprosesser i Human Resources.

Du kan vise listen over virtuelle enheter som er aktivert i miljøet, og begynne å arbeide med enhetene i [Power Apps](https://make.powerapps.com), i løsningen **Dynamics 365 HR Virtual Entities**.

![Dynamics 365 HR Virtual Entities i Power Apps](./media/hr-admin-integration-virtual-entities-power-apps.jpg)

## <a name="virtual-entities-versus-natural-entities"></a>Virtuelle enheter kontra naturlige enheter

Virtuelle enheter for Human Resources er ikke det samme som de naturlige Common Data Service-enhetene som opprettes for Human Resources. De naturlige enhetene for Human Resources genereres separat og vedlikeholdes i den HCM Common-løsningen i Common Data Service. For naturlige enheter lagres dataene i Common Data Service og krever synkronisering med appdatabasen for Human Resources.

> [!NOTE]
> Hvis du vil ha en liste over de naturlige Common Data Service-enhetene for Human Resources, kan du se [Common Data Service-enheter](https://docs.microsoft.com/dynamics365/human-resources/hr-developer-entities).

## <a name="setup"></a>Installasjon

Følg disse oppsettstrinnene for å aktivere virtuelle enheter i miljøet.

### <a name="enable-virtual-entities-in-human-resources"></a>Aktiver virtuelle enheter i Human Resources

Først må du aktivere virtuelle enheter i arbeidsområdet **Funksjonsbehandling**.

1. Velg **Systemadministrasjon** i Human Resources.

2. Velg flisen **Funksjonsbehandling**.

3. Velg **Støtte for virtuell enhet i HR/CDS** og velg deretter **Aktiver**.

Hvis du vil ha mer informasjon om aktivering og deaktivering av funksjoner, kan du se [Behandle funksjoner](hr-admin-manage-features.md).

### <a name="register-the-app-in-microsoft-azure"></a>Registrere appen i Microsoft Azure

Du må registrere Human Resources-forekomsten i Azure Portal slik at Microsoft-identitetsplattform kan tilby godkjennings- og autorisasjonstjenester for appen og brukerne. Hvis du vil ha mer informasjon om registrering av apper i Azure, kan du se [Hurtigstart: Registrer en app i Microsoft-identitetsplattformen](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app).

1. Åpne [Microsoft Azure-portalen](https://portal.azure.com).

2. I listen over Azure-tjenester velger du **Appregistreringer**.

3. Velg **Ny registrering**.

4. I **Navn**-feltet angir du et beskrivende navn for appen. For eksempel **Virtuelle enheter for Dynamics 365 Human Resources**.

5. I feltet **URI for omadressering** angir du URL-adressen til navneområdet til forekomsten av Human Resources.

6. Velg **Registrer**.

7. Når registreringen er fullført, viser Azure-portalen appregistreringens **Oversikt**-rute, som inkluderer **App-ID (klient)**. Noter **App-ID (klient)**. Du angir denne informasjonen når du [konfigurerer datakilden for den virtuelle enheten](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-entity-data-source).

8. I den venstre navigasjonsruten velger du **Sertifikater og hemmeligheter**.

9. I delen **Klienthemmeligheter** på siden, velger du **Ny klienthemmelighet**.

10. Angi en beskrivelse, velg en varighet og velg **Legg til**.

11. Noter verdien for hemmeligheten. Du angir denne informasjonen når du [konfigurerer datakilden for den virtuelle enheten](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-entity-data-source).

    > [!IMPORTANT]
    > Husk å notere hemmelighetens verdi. Hemmeligheten vises aldri på nytt når du forlater denne siden.

### <a name="install-the-dynamics-365-hr-virtual-entity-app"></a>Installer Dynamics 365 HR Virtual Entity-appen

Installer Dynamics 365 HR Virtual Entity-appen i Power Apps-miljøet for å distribuere løsningspakken for den virtuelle enheten til Common Data Service.

1. Åpne [Administrasjonssenter for Power Platform](https://admin.powerplatform.microsoft.com).

2. I **Miljøer**-listen velger du Power Apps-miljøet som er tilknyttet Human Resources-forekomsten.

3. I **Ressurser**-delen på siden velger du **Dynamics 365-apper**.

4. Velg handlingen **Installer app**.

5. Velg **Dynamics 365 HR Virtual Entity**, og velg deretter **Neste**.

6. Se gjennom og merk for å godta vilkårene for bruk.

7. Velg **Installer**.

Installasjonen tar noen minutter. Når den er fullført, fortsetter du til de neste trinnene.

![Installere Dynamics 365 HR Virtual Entity-appen fra Administrasjonssenter for Power Platform](./media/hr-admin-integration-virtual-entities-power-platform-install.jpg)

### <a name="configure-the-virtual-entity-data-source"></a>Konfigurere datakilden for den virtuelle enheten 

Det neste trinnet er å konfigurere datakilden for den virtuelle enheten i Power Apps-miljøet. 

1. Åpne [Administrasjonssenter for Power Platform](https://admin.powerplatform.microsoft.com).

2. I **Miljøer**-listen velger du Power Apps-miljøet som er tilknyttet Human Resources-forekomsten.

3. Velg **URL-adresse for miljø** i **Detaljer**-delen på siden.

4. I **huben for løsningstilstand** velger du **Avansert søk**-ikonet øverst til høyre på appsiden.

5. På siden **Avansert søk** i rullegardinlisten **Søk etter**, velger du **Konfigurere virtuell datakilde for Finance and Operations**.

6. Velg **Resultater**.

7. Velg posten **Microsoft HR-datakilde**.

8. Angi den nødvendige informasjonen for konfigurasjon av datakilden:

   - **Mål-URL-adresse**: URL-adressen til Human Resources-navneområdet. Formatet på mål-URL-adressen er:
     
     https://\<hostname\>.hr.talent.dynamics.com/namespaces/\<namespaceID\>/

     For eksempel:
     
     `https://aos.rts-sf-5ea54e35c68-westus2.hr.talent.dynamics.com/namespaces/49d24c565-8f4d-4891-b174-bf83d948ed0c/`

     >[!NOTE]
     >Pass på at du inkluderer tegnet **/** på slutten av URL-adressen for å unngå å motta en feil.

   - **Leier-ID**: Leier-ID for Azure Active Directory ( Azure AD).

   - **AAD-app-ID**: App-ID (klient) som ble opprettet for appen som er registrert i Microsoft Azure-portalen. Du har mottatt denne informasjonen tidligere i trinnet [Registrere appen i Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).

   - **AAD-apphemmelighet**: Klienthemmeligheten som ble opprettet for appen som er registrert i Microsoft Azure-portalen. Du har mottatt denne informasjonen tidligere i trinnet [Registrere appen i Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).

   ![Microsoft HR-datakilde](./media/hr-admin-integration-virtual-entities-hr-data-source.jpg)

9. Velg **Lagre og lukk**.

### <a name="grant-app-permissions-in-human-resources"></a>Gi apptillatelser i Human Resources

Gi tillatelser for de to Azure AD-appene i Human Resources:

- Appen som ble opprettet for leieren din i Microsoft Azure-portalen
- Dynamics 365 HR Virtual Entity-appen som er installert i Power Apps-miljøet 

1. I Human Resources åpner du siden **Azure Active Directory-apper**.

2. Velg **Ny** for å opprette en ny appost:

    - I **Klient-ID**-feltet angir du klient-ID-en til appen du registrerte i Microsoft Azure-portalen.
    - I **Navn**-feltet angir du navnet til appen du registrerte i Microsoft Azure-portalen.
    - I **Bruker-ID**-feltet velger du bruker-ID-en til en bruker med administratortillatelser i Human Resources og Power Apps-miljøet.

3. Velg **Ny** for å opprette enda en appost:

    - **Klient-ID**: f9be0c49-aa22-4ec6-911a-c5da515226ff
    - **Navn**: Dynamics 365 HR Virtual Entity
    - I **Bruker-ID**-feltet velger du bruker-ID-en til en bruker med administratortillatelser i Human Resources og Power Apps-miljøet.

## <a name="generate-virtual-entities"></a>Generere virtuelle enheter

Når installasjonen er fullført, kan du velge de virtuelle enhetene du vil generere og aktivere i Common Data Service-forekomsten.

1. I Human Resources åpner du siden **Common Data Service (CDS)-integrering**.

2. Velg kategorien **Virtuelle enheter**.

> [!NOTE]
> Veksleknappen for **aktivering av virtuell enhet** vil bli satt til **Ja** automatisk når alle nødvendige oppsett er fullført. Hvis veksleknappen er satt til **Nei**, går du gjennom trinnene i tidligere deler av dette dokumentet for å være sikker på at alle nødvendige oppsett er fullført.

3. Velg enheten eller enhetene du vil generere i Common Data Service.

4. Velg **Generer/oppdater**.

![Common Data Service-integrering](./media/hr-admin-integration-common-data-service-integration.jpg)

## <a name="check-entity-generation-status"></a>Kontrollere status for enhetsgenerering

Virtuelle enheter blir generert i Common Data Service gjennom en asynkron bakgrunnsprosess. Oppdateringer av prosessvisningen i handlingssenteret. Detaljer om prosessen, inkludert feillogger, vises på siden for **prosessautomatiseringer**.

1. I Human Resources åpner du **Prosessautomatiseringer**-siden.

2. Velg kategorien **Bakgrunnsprosesser**.

3. Velg **Bakgrunnsprosess for asynkron operasjon for virtuell enhet**.

4. Velg **Vis de siste resultatene**.

Hurtigmenyen viser de siste utførelsesresultatene for prosessen. Du kan vise loggen for prosessen, inkludert eventuelle feil som returneres fra Common Data Service.

## <a name="see-also"></a>Se også

[Hva er Common Data Service?](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro)<br>
[Enhetsoversikt](https://docs.microsoft.com/powerapps/maker/common-data-service/entity-overview)<br>
[Oversikt over enhetsrelasjoner](https://docs.microsoft.com/powerapps/maker/common-data-service/relationships-overview)<br>
[Opprette og redigere virtuelle enheter som inneholder data fra en ekstern datakilde](https://docs.microsoft.com/powerapps/maker/common-data-service/create-edit-virtual-entities)<br>
[Hva er Power Apps-portaler?](https://docs.microsoft.com/powerapps/maker/portals/overview)<br>
[Oversikt over oppretting av apper i Power Apps](https://docs.microsoft.com/powerapps/maker/)


[!INCLUDE[footer-include](../includes/footer-banner.md)]