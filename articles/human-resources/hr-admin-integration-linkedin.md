---
title: Integrere med LinkedIn Talent Hub
description: Dette emnet forklarer hvordan du kan setter opp integrasjon mellom Microsoft Dynamics 365 Human Resources LinkedIn Talent Hub.
author: jaredha
ms.date: 10/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-10-20
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 6e500125e1d96f6b595910e1168e2e1baeef0cd3
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/06/2021
ms.locfileid: "6360598"
---
# <a name="integrate-with-linkedin-talent-hub"></a>Integrere med LinkedIn Talent Hub

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [banner](includes/preview-feature.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

[LinkedIn Talent Hub](https://business.linkedin.com/talent-solutions/talent-hub) er en is ATS-plattform (programsporingssystem). Den gjør det mulig å finne, administrere og ansette alle ansatte på ett sted. Ved å integrere Microsoft Dynamics 365 Human Resources med LinkedIn Talent Hub, kan du enkelt opprette ansattposter i Human Resources for søkere som har blitt ansatt for en stilling.

## <a name="setup"></a>Installasjon

En systemadministrator må fullføre installasjonsoppgavene for å aktivere integrering med LinkedIn Talent Hub. I Power Apps-miljøet må du først konfigurere en bruker- og en sikkerhetsrolle for å gi LinkedIn Talent Hub de riktige tillatelsene til å skrive data i Human Resources.

### <a name="link-your-environment-to-linkedin-talent-hub"></a>Koble miljøet til LinkedIn Talent Hub

1. Åpne [LinkedIn Talent Hub](https://business.linkedin.com/talent-solutions/talent-hub).

2. Velg **Produktinnstillinger** på brukerrullegardinmenyen.

3. I den venstre navigasjonsruten i delen **Avansert** velger du **Integreringer**.

4. Velg **Autorisere** for Microsoft Dynamics 365 Human Resources-integreringen.

5. På **Dynamics 365 Human Resources**-siden velger du miljøet du vil koble LinkedIn Talent Hub til, og deretter velger du **Kobling**.

    ![LinkedIn Talent Hub-pålasting.](./media/hr-admin-integration-talent-hub-onboarding.jpg)

    > [!NOTE]
    > Du kan bare koble til miljøer der brukerkontoen har administratortilgang til både Human Resources-miljøet og det tilknyttede Power Apps-miljøet. Hvis det ikke vises noen miljøer Human Resources-koblingssiden, må du kontrollere at du har lisensierte Human Resources-miljøer på leieren, og at brukeren du logget deg på koblingssiden som har administratortilgang til både Human Resources-administrasjonsmiljøet og Power Apps-miljøet.

### <a name="create-a-power-apps-security-role"></a>Opprette en Power Apps-sikkerhetsrolle

1. Åpne [Administrasjonssenter for Power Platform](https://admin.powerplatform.microsoft.com).

2. I **Miljøer**-listen velger du miljøet som er knyttet til Human Resources-miljøet du vil koble forekomsten av LinkedIn Talent Hub til.

3. Velg **Innstillinger**.

4. Utvid noden **Brukere + tillatelser**, og velg **Sikkerhetsroller**.

5. På verktøylinjen på **Sikkerhetsroller**-siden velger du **Ny rolle**.

6. I kategorien **Detaljer** angir du et navn på rollen, for eksempel **LinkedIn Talent Hub HRIS-integrering**.

7. I kategorien **Tilpassing** velger du **Lese**-tilgang på organisasjonsnivå for følgende enheter:

    - Entity
    - Felt
    - Relasjon

8. Lagre og lukk sikkerhetsrollen.

### <a name="create-a-power-apps-application-user"></a>Opprette en Power Apps-programbruker

Det må opprettes en programbruker for LinkedIn Talent Hub-adapteren for å gi tillatelse til at adapteren kan skrive kandidatposter til Power Apps-miljøet.

1. Åpne [Administrasjonssenter for Power Platform](https://admin.powerplatform.microsoft.com).

2. I **Miljøer**-listen velger du miljøet som er knyttet til Human Resources-miljøet du vil koble forekomsten av LinkedIn Talent Hub til.

3. Velg **Innstillinger**.

4. Utvid noden **Brukere + tillatelser**, og velg **Brukere**.

5. Velg **Behandle brukere i Dynamics 365**.

6. Bruk rullegardinmenyen over listen til å endre visningen fra standardvisningen **Aktiverte brukere** til **Programbrukere**.

    ![Programbrukere-visningen.](./media/hr-admin-integration-power-apps-application-users.jpg)

7. Klikk **Ny** på verktøylinjen.

8. Følg denne fremgangsmåten på siden **Ny bruker**:

    1. Endre verdien for feltet **Brukertype** til **Programbruker**.
    2. Sett **Brukernavn**-feltet til **Dynamics365 HR LinkedIn HRIS-integrering**.
    3. Angi **Program-ID**-feltet til **3a225c96-d62a-44ce-b3ec-bd4e8e9befef**.
    4. Angi en verdi i feltene **Navn**, **Etternavn** og **Primær e-post**.
    5. Velg **Lagre \& lukk** på verktøylinjen.

### <a name="assign-a-security-role-to-the-new-user"></a>Tilordne en sikkerhetsrolle til den nye brukeren

Når du har lagret og lukket den nye programbrukeren i den forrige delen, kommer du tilbake til **Brukerliste**-siden.

1. På **Brukerlisten**-siden endrer du visningen til **Programbrukere**.

2. Velg programbrukeren du opprettet i den forrige delen.

3. Velg **Administrer roller** på verktøylinjen.

4. Velg sikkerhetsrollen du opprettet tidligere for integreringen.

5. Velg **OK**.

### <a name="add-an-azure-active-directory-app-in-human-resources"></a>Legge til en Azure Active Directory-app i Human Resources

1. I Dynamics 365 Human Resources åpner du siden **Azure Active Directory-programmer**.
2. Legg til en ny post i listen, og angi følgende felt:

    - **Klient-ID**: Angi **3a225c96-d62a-44ce-b3ec-bd4e8e9befef**.
    - **Navn**: Skriv inn navnet på Power Apps-sikkerhetsrollen du opprettet tidligere, for eksempel **LinkedIn Talent Hub HRIS-integrering**.
    - **Bruker-ID**: Velg en bruker som har tillatelse til å skrive data i Personaladministrasjon.

### <a name="create-the-table-in-dataverse"></a>Opprette tabellen i Dataverse

> [!IMPORTANT]
> Integreringen med LinkedIn Talent Hub er avhengig av virtuelle tabeller i Dataverse for Human Resources. Som en forutsetning for dette trinnet i oppsettet, må du konfigurere virtuelle tabeller. Hvis du vil ha informasjon om hvordan du konfigurerer virtuelle tabeller, se [Konfigurere virtuelle tabeller for Dataverse](./hr-admin-integration-common-data-service-virtual-entities.md).

1. I Human Resources åpner du siden **Dataverse-integrering**.

2. Velg kategorien **Virtuelle tabeller**.

3. Filtrer enhetslisten etter enhetsetikett for å finne **LinkedIn-eksporterte kandidater**.

4. Velg enheten, og velg deretter **Generer/oppdater**.

## <a name="exporting-candidate-records"></a>Eksportere kandidatposter

Når oppsettet er fullført, kan rekrutteringspersoner og personaleksperter bruke funksjonen **Eksporter til HRIS** i LinkedIn Talent Hub til å eksportere kandidatposter for ansatte fra LinkedIn Talent Hub til Human Resources.

### <a name="export-records-from-linkedin-talent-hub"></a>Eksportere poster fra LinkedIn Talent Hub

Når en kandidat har gått gjennom rekrutteringsprosessen og har blitt ansatt, kan du eksportere kandidatposten fra LinkedIn Talent Hub til Human Resources.

1. I LinkedIn Talent Hub åpner du prosjektet som du ansatte den nye medarbeideren for.

2. Velg en kandidatpost.

3. Velg **Endre stadium**, og velg deretter **Ansatt**.

4. På ellipsemenyen (**...**) for kandidaten velger du **Eksporter til HRIS**.

5. Skriv inn informasjonen som må eksporteres, i ruten **Eksporter til HRIS**.

    - I feltet **HRIS-leverandør** velger du **Microsoft Dynamics 365 Human Resources**.
    - Velg en verdi for den nyansatte i **Startdato**-feltet.
    - I **Stilling**-feltet angir du en stillingstittel for den nye ansattes stilling.
    - Angi lokasjonen der den ansatte skal være basert, i **Lokasjon**-feltet.
    - Angi eller kontroller den ansattes e-postadresse.

![Eksporter til HRIS-ruten i LinkedIn Talent Hub.](./media/hr-admin-integration-linkedin-talent-hub-export.jpg)

## <a name="complete-onboarding-in-human-resources"></a>Fullføre pålasting i Human Resources

Kandidatposter som eksporteres fra LinkedIn Talent Hub til Personal, vises i delen **Kandidater som skal ansette** på **Personaladministrasjon**-siden.

1. I Human Resources åpner du **Personaladministrasjon**-siden.

2. I delen **Kandidater som skal ansettes** velger du **Ansett** for den valgte kandidaten.

3. I dialogboksen **Ansett en ny arbeider** kontrollerer du posten og legger til eventuell nødvendig informasjon. Du kan også velge stillingsnummeret som kandidaten er ansatt for.

Når den nødvendige informasjonen er angitt, kan du fortsette med standardprosessene for å opprette ansattposter og sette pålaste ansatte.

Følgende detaljer blir importert og inkludert i den nye ansattposten:

- Fornavn
- Etternavn
- Startdato for ansettelse
- E-postadresse
- Telefonnummer

## <a name="see-also"></a>Se også

[Konfigurere virtuelle Dataverse-tabeller](./hr-admin-integration-common-data-service-virtual-entities.md)<br>
[Hva er Microsoft Dataverse?](/powerapps/maker/common-data-service/data-platform-intro)


[!INCLUDE[footer-include](../includes/footer-banner.md)]