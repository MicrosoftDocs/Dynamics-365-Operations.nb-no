---
title: Installer tillegget for lagersynlighet
description: Denne artikkelen beskriver hvordan du installerer tillegget for lagersynlighet for Microsoft Dynamics 365 Supply Chain Management.
author: yufeihuang
ms.date: 05/27/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 42c2c287e2a813f8bb07ce0c7f21f4224a217946
ms.sourcegitcommit: f2175fe5e900d39f34167d671aab5074b09cc1b8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/17/2022
ms.locfileid: "9306062"
---
# <a name="install-and-set-up-inventory-visibility"></a>Installer og definer Inventory Visibility

[!include [banner](../includes/banner.md)]

Denne artikkelen beskriver hvordan du installerer tillegget for lagersynlighet for Microsoft Dynamics 365 Supply Chain Management.

Du må bruke Microsoft Dynamics Lifecycle Services (LCS) til å installere tillegget for lagersynlighet. LCS er en samarbeidsportal som gir et miljø og et sett med jevnlig oppdaterte tjenester som hjelper deg med å administrere applivssyklusen til Finance and Operations-appene dine. Hvis du vil ha mer informasjon, se [Lifecycle Services-ressurser](../../fin-ops-core/dev-itpro/lifecycle-services/lcs.md).

> [!TIP]
> Vi anbefaler at du blir med i brukergruppen Tillegg for lagersynlighet, der du kan finne nyttige guider, få de siste oppdateringene og postere eventuelle spørsmål du måtte ha om bruk av lagersynlighet. Hvis du vil delta, kan du sende en e-postmelding til produktgruppen Lagersynlighet på [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) og inkludere miljø-IDen for Supply Chain Management.

## <a name="inventory-visibility-prerequisites"></a>Forutsetninger for lagersynlighet

Før du kan installere lagersynlighet, må du gjøre følgende:

- Hent et LCS-implementeringsprosjekt der minst ett miljø er distribuert.
- Sørg for at forutsetningene for å definere tillegg er fullført. Hvis du vil ha mer informasjon om disse forutsetningene, kan du se [Oversikt over tillegg](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md). Lagersynlighet krever ikke kobling til dobbel skriving.

> [!NOTE]
> Landene og regionene som for øyeblikket støttes, omfatter Canada (CCA, ECA), USA (WUS, EUS), EU (NEU, WEU), Storbritannia (SUK, WUK), Australia (EAU, SEAU), Japan (EJP, WJP) og Brasil (SBR, SCUS).

Hvis du har spørsmål om disse forutsetningene, kan du ta kontakt med produktteamet for lagersynlighet på [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com).

## <a name="install-the-inventory-visibility-add-in"></a><a name="install-add-in"></a>Installer tillegget for lagersynlighet

Før du installerer tillegget, må du registrere en app og legge til en klienthemmelighet i Azure Active Directory (Azure AD) under Azure-abonnementet ditt. Hvis du vil ha instruksjoner, kan du se [Registrer en app](/azure/active-directory/develop/quickstart-register-app) og [Legg til en klienthemmelighet](/azure/active-directory/develop/quickstart-register-app#add-a-certificate). Skriv ned verdiene for **App-ID (klient)**, **Klienthemmelighet** og **Leier-ID**, siden du trenger dem senere.

> [!IMPORTANT]
> Hvis du har mer enn ett LCS-miljø, oppretter du et annet Azure AD program for hvert miljø. Hvis du bruker samme program-ID og leie-ID til å installere tillegget for lagersynlighet for forskjellige miljøer, vil det oppstå et tokenproblem for eldre miljøer. Som et resultat vil bare den siste installasjonen være gyldig.

Når du har registrert en app og lagt til en klienthemmelighet i Azure AD, følger du denne fremgangsmåten for å installere tillegget for lagersynlighet.

1. Logg på [LCS](https://lcs.dynamics.com/Logon/Index).
1. På hjemmesiden velger du prosjektet der miljøet er distribuert.
1. På prosjektsiden velger du miljøet du vil installere tillegget i.
1. På miljøsiden ruller du ned til du ser delen delen **Miljøtillegg** i delen **Power Platform-integrering**. Der kan du finne Dataverse-miljønavnet. Bekreft at Dataverse-miljønavnet er det du vil bruke for lagersynlighet.

    > [!NOTE]
    > For øyeblikket støttes kun Dataverse-miljøer som ble opprettet ved hjelp av LCS. Hvis Dataverse-miljøet ble opprettet på en annen måte (for eksempel ved å bruke Power Apps-administrasjonssenteret), og hvis det er koblet til Supply Chain Management-miljøet ditt, må du først kontakte produktgruppen i Lagersynlighet på [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) for å løse tilordningsproblemet. Du kan deretter installere Lagersynlighet.

1. I delen **Miljøtillegg** velger du **Installer et nytt tillegg**.

    ![Miljøsiden i LCS](media/inventory-visibility-environment.png "Miljøsiden i LCS")

1. Velg koblingen **Installer et nytt tillegg**. En liste over tilgjengelige tillegg vises.
1. Velg **Lagersynlighet** i listen.
1. Angi følgende felter for miljøet:

    - **ID for AAD-app (klient)** – Angi ID-en for Azure AD-appen du opprettet og noterte ned tidligere.
    - **ID for AAD-leier** – Angi leier-ID-en du noterte tidligere.

    ![Siden Konfigurer tillegg](media/inventory-visibility-setup.png "Siden Konfigurer tillegg")

1. Godta vilkåret og betingelsen ved å merke av for **Vilkår og betingelser**.
1. Velg **Installer**. Statusen for tillegget vises som **Installerer**. Når installasjonen er fullført, oppdaterer du siden. Statusen skal endres til **Installert**.
1. I Dataverse merker du **Apper**-delen i venstre navigasjon, og kontrollerer at **lagersynligheten** Power Apps er installert. Hvis **Apper**-deler ikke finnes, kontakter du produktteamet til Lagersynlighet på [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com).

> [!NOTE]
> Hvis det tar mer enn en time å installere fra LCS-siden, mangler brukerkontoen din sannsynligvis tillatelse til å installere løsninger i Dataverse-miljøet. Følg fremgangsmåten nedenfor for å løse problemet:
>
> 1. Avbryt installasjonen av tilleggsprogrammet Lagersynlighet fra LCS-siden.
> 1. Logg deg på [Microsoft 365-administrasjonssenteret](https://admin.microsoft.com), og kontroller at brukerkontoen du vil bruke til å installere tilleggsprogrammet, har "Dynamics 365 Unified Operations-plan" tilordnet. Tilordne lisensen hvis det er nødvendig.
> 1. Logg deg på [Power Platform-administrasjonssenteret](https://admin.powerplatform.microsoft.com) med den aktuelle brukerkontoen. Installer deretter tilleggsprogrammet Lagersynlighet ved å gjøre følgende:
>     1. Velg miljøet der du vil installere tilleggsprogrammet.
>     1. Velg **Dynamics 365-apper**.
>     1. Velg **Installer app**.
>     1. Velg **Lagersynlighet**
>
> 1. Når installasjonen er fullført, kan du gå tilbake til LCS-siden og prøve å installere tilleggsprogrammet **Lagersynlighet** på nytt.

## <a name="set-up-inventory-visibility-in-supply-chain-management"></a><a name="setup-dynamics-scm"></a>Definere lagersynlighet i Supply Chain Management

### <a name="deploy-the-inventory-visibility-integration-package"></a><a name="deploy-inventory-visibility-package"></a>Distribuere integreringspakken for lagersynlighet

Hvis du kjører Supply Chain Management versjon 10.0.17 eller tidligere, kan du kontakte kundestøttegruppen for lagersynlighet på [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) for å hente pakkefilen. Deretter distribuerer du pakken i LCS.

> [!NOTE]
> Hvis det oppstår en versjonsfeil under distribusjon, må du importere X++-prosjektet til utviklingsmiljøet manuelt. Opprett deretter den distribuerbare pakken i utviklingsmiljøet, og distribuer den i produksjonsmiljøet.
>
> Koden er inkludert i Supply Chain Management versjon 10.0.18. Hvis du kjører den versjonen eller senere, er det ikke nødvendig å distribuere påkrevd distribusjon.

Sørg for at følgende funksjoner er aktivert i miljøet i Supply Chain Management. (De er som standard aktiverte.)

| Funksjonsbeskrivelse | Kodeversjon | Veksle klasse |
|---|---|---|
| Aktivere eller deaktivere bruk av lagerdimensjoner i InventSum-tabell      | 10.0.11 | InventUseDimOfInventSumToggle      |
| Aktivere eller deaktivere bruk av lagerdimensjoner i InventSumDelta-tabell | 10.0.12 | InventUseDimOfInventSumDeltaToggle |

### <a name="set-up-inventory-visibility-integration"></a><a name="setup-inventory-visibility-integration"></a>Definer integrering av lagersynlighet

Når du har installert tillegget, forbereder du Supply Chain Management-systemet slik at du kan arbeide med det ved å gjøre følgende:

1. I Supply Chain Management åpner du arbeidsområdet **[Funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)** og aktiverer følgende funksjoner:
    - *Integrering av lagersynlighet* – Obligatorisk.
    - *Integrering av lagersynlighet med motpostering av reservasjon* – Anbefales, men valgfritt. Krever versjon 10.0.22 eller nyere. Hvis du vil ha mer informasjon, kan du se [Lagersynlighetsreservasjoner](inventory-visibility-reservations.md).

1. Gå til **Lagerstyring \> Oppsett \> Parametere for integrering av lagersynlighet**.
1. Åpne kategorien **Generelt**, og gjør følgende innstillinger:
    - **Endepunkt for lagersynlighet** – Angi URL-adressen til miljøet der du kjører Lagersynlighet. Hvis du ønsker mer informasjon, se [Finn endepunkt for tjeneste](inventory-visibility-configuration.md#get-service-endpoint).
    - **Maksimalt antall poster i en enkelt forespørsel** – Angi til det maksimale antallet poster som skal inkluderes i en enkelt forespørsel. Du må angi et positivt heltall som er mindre enn eller lik 1 000. Standardverdien er 512. Vi anbefaler på det sterkeste at du ikke beholder standardverdien med mindre du har mottatt råd fra Microsoft Kundestøtte eller på annen måte er sikker på at du må endre den.

1. Hvis du aktiverte den valgfrie funksjonen *Integrering av lagersynlighet med motpostering av reservasjon*, åpner du fanen **Motpostering av reservasjon** og gjør følgende innstillinger:
    - **Aktiver motpostering av reservasjon** – Sett til *Ja* for å aktivere denne funksjonaliteten.
    - **Motposteringsmodifikator for reservasjon** – Velg lagertransaksjonsstatusen som motposterer reserveringer som gjøres i lagersynligheten. Denne innstillingen bestemmer ordrebehandlingsstadiet som utløser motregninger. Fasen spores etter ordrens lagertransaksjonsstatus. Velg ett av følgende alternativer:
        - *I ordre/bestilling* – Når det gjelder statusen *I transaksjon*, sender en ordre en motposteringsforespørsel når den opprettes. Motposteringsantallet vil være antallet i den opprettede ordren.
        - *Reserver* – For statusen *Reserver bestilt transaksjon* sender en ordre en motforespørsel når den er reservert, plukket, følgeseddelpostert eller fakturert. Forespørselen utløses bare én gang, for første trinn når den nevnte prosessen inntreffer. Motposteringsantallet vil være antallet der lagertransaksjonsstatusen endres fra *I ordre/bestilling* til *Reservert av bestilt* (eller senere status) på den tilsvarende ordrelinjen.

1. Gå til **Lagerstyring \> Periodisk \> Integrering av lagersynlighet** og aktiver jobben. Alle lagerendringshendelser fra Supply Chain Management posteres nå til Lagersynlighet.

## <a name="uninstall-the-inventory-visibility-add-in"></a><a name="uninstall-add-in"></a>Avinstaller tillegget for lagersynlighet

Hvis du vil avinstallere tillegget for lagersynlighet, følger du denne fremgangsmåten:

1. Logg på Supply Chain Management.
1. Gå til **Lagerstyring \> Periodisk \> Integrering av lagersynlighet** og deaktiver jobben.
1. Gå til LCS og åpne siden for miljøet der du vil avinstallere tillegget (se også [Installer tillegget for lagersynlighet](#install-add-in)).
1. Velg **Avinstaller**.
1. Avinstalleringsprosessen avslutter nå tillegget for lagersynlighet, fjerner registreringen av tillegget fra LCS og sletter alle midlertidige data som er lagret i hurtigbufferen i tillegget for lagersynlighet. De primære lagerdataene som var synkronisert til Dataverse-abonnementet, lagres fremdeles der. For å slette disse dataene må du utføre denne fremgangsmåten.
1. Åpne [Power Apps](https://make.powerapps.com).
1. Velg **Miljø** på navigasjonslinjen
1. Velg Dataverse-miljøet som er knyttet til LCS-miljøet.
1. Gå til **Løsninger** og sletter følgende fem løsninger i følgende rekkefølge:
    1. Forankringsløsning for Inventory Visibility-program i Dynamics 365-løsninger
    1. Løsning for lagersynlighetsapper i Dynamics 365 FNO SCM
    1. Konfigurasjon av lagertjeneste
    1. Frittstående versjon av Lagersynlighet
    1. Basisløsning for lagersynlighet i Dynamics 365 FNO SCM

    Når du har slettet disse løsningene, blir dataene som er lagret i tabeller, også slettet.

> [!NOTE]
> Hvis du gjenoppretter en Supply Chain Management-database etter at du har avinstallert tillegget for lagersynlighet, og deretter vil installere tillegget på nytt, må du sørge for at du har slettet de gamle lagersynlighetsdataene som er lagret i Dataverse-abonnementet (som beskrevet i forrige fremgangsmåte) før du installerer tillegget på nytt. Dette vil forhindre problemer med datainkonsekvens som ellers kan forekomme.

## <a name="clean-inventory-visibility-data-from-dataverse-before-restoring-the-supply-chain-management-database"></a><a name="restore-environment-database"></a>Rens lagersynlighetsdata fra Dataverse før gjenoppretting av Supply Chain Management-databasen

Hvis du bruker Lagersynlig og gjenoppretter en Supply Chain Management-database, kan den gjenopprettede databasen inneholde data som ikke lenger er konsekvent med data som tidligere er synkronisert med Lagersynlighet til Dataverse. Denne datainkonsekvensen kan forårsake systemfeil og andre problemer. Det er derfor viktig at du alltid renser alle lagersynlighetsdata fra Dataverse før du gjenoppretter en Supply Chain Management-database.

Hvis du har behov for å gjenopprette en Supply Chain Management-database, bruker du følgende fremgangsmåte:

1. Avinstaller tillegget Lagersynlighet og fjern alle relaterte data i Dataverse, som beskrevet i [Avinstaller tillegget Lagersynlighet](#uninstall-add-in)
1. Gjenopprett Supply Chain Management-databasen, for eksempel som beskrevet i [Tilbakestilling av databasepunkt (PITR)](../../fin-ops-core/dev-itpro/database/database-point-in-time-restore.md) eller [Tidspunkt for gjenoppretting av produksjonsdatabasen til et sandkassemiljø](../../fin-ops-core/dev-itpro/database/database-pitr-prod-sandbox.md).
1. Hvis du likevel vil bruke det, installerer du og konfigurerer tillegget Lagersynlighet på nytt som beskrevet i [Installer tillegget Lagersynlighet](#install-add-in) og [Konfigurerer integrering av lagersynlighet](#setup-inventory-visibility-integration)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
