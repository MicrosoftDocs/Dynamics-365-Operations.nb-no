---
title: Konfigurer Common Data Service-integrering
description: Du kan aktivere eller deaktivere integrering mellom Common Data Service og Dynamics 365 Human Resources. Du kan også vise synkroniseringsdetaljer, slette sporingsdata og synkronisere en enhet på nytt for å hjelpe til med å feilsøke dataproblemer mellom de to miljøene.
author: andreabichsel
manager: AnnBe
ms.date: 07/27/2020
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
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 8cbead2961c4576a5394080aae2fec109bce3f10
ms.sourcegitcommit: 4a981ee4be6d7e6c0e55541535d386bce2565cba
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/27/2020
ms.locfileid: "3621310"
---
# <a name="configure-common-data-service-integration"></a>Konfigurer Common Data Service-integrering

Du kan aktivere eller deaktivere integrering mellom Common Data Service og Dynamics 365 Human Resources. Du kan også vise synkroniseringsdetaljene, slette sporingsdata og synkronisere en enhet på nytt for å hjelpe til med å feilsøke dataproblemer mellom de to miljøene.

Når du deaktiverer integrering, kan brukere gjøre endringer i Human Resources eller Common Data Service, men disse endringene synkroniseres ikke mellom de to miljøene.

Som standard er dataintegrering mellom Human Resources og Common Data Service slått av.

Du vil kanskje deaktivere integrering i disse situasjonene:

- Du fyller ut data gjennom databehandlingsrammeverket og må importere dataene flere ganger for å hente dem inn i riktig tilstand.

- Det er problemer med data i Human Resources eller Common Data Service. Hvis du deaktiverer integrering, kan du slette en post i ett miljø uten å slette den i det andre. Når du slår på integreringen igjen, vil posten i miljøet der den ikke var slettet, bli synkronisert tilbake til miljøet der den ble slettet. Synkroniseringen starter neste gang den satsvise jobben **Common Data Service-integrering mangler forespørselssynkronisering** kjøres.

> [!WARNING]
> Når du slår av dataintegrering, må du passe på at du ikke redigerer samme post i begge miljøene. Når du slår på integreringen igjen, blir posten du sist redigerte, synkronisert. Hvis du ikke gjorde de samme endringene i posten i begge miljøer, kan det derfor oppstå datatap.

## <a name="access-the-common-data-service-integration-page"></a>Få tilgang til Common Data Service-integreringssiden

1. I forekomsten av Human Resources der du vil vise eller konfigurere innstillinger for integreringen med Common Data Service, velger du flisen **Systemadministrasjon**.

    [![Flisen Systemadministrasjon](./media/hr-select-system-administration.png)](./media/hr-select-system-administration.png)

2. Velg kategorien **Koblinger**.

    [![Koblinger-kategorien](./media/hr-system-administration-links.png)](./media/hr-system-administration-links.png)

3. Under **Integreringer** velger du **Common Data Service-konfigurasjon**.

    [![Common Data Service-konfigurasjonskobling](./media/hr-select-common-data-service-configuration.png)](./media/hr-select-common-data-service-configuration.png)

## <a name="turn-data-integration-between-human-resources-and-common-data-service-on-or-off"></a>Slå dataintegrering mellom Human Resources og Common Data Service på eller av

- Hvis du vil slå på integrering, angir du **Aktiver integreringen til Common Data Service**-alternativet til **Ja**.

    > [!NOTE]
    > Når du aktiverer integrering, blir data synkronisert neste gang den satsvise jobben **Common Data Service-integrering mangler forespørselssynkronisering** kjøres. Alle data skal være tilgjengelige når den satsvise jobben er fullført.

- Hvis du vil deaktivere integrering, setter du alternativet til **Nei**.

[![Aktivere eller deaktivere Common Data Service-integrering](./media/hr-enable-or-disable-common-data-service-integration.png)](./media/hr-enable-or-disable-common-data-service-integration.png)

> [!WARNING]
> Vi anbefaler sterkt at du deaktiverer Common Data Service-integrering mens du utfører datamigreringsoppgaver. Store dataopplastinger kan påvirke ytelsen betydelig. Eksempel: Opplasting av 2000 arbeidere kan ta flere timer når integrering er aktivert, og mindre enn én time når den er deaktivert. Tallene i dette eksemplet er bare for demonstrasjon. Den nøyaktige tiden det tar å importere poster, kan variere betraktelig, avhengig av mange faktorer.

## <a name="view-data-integration-details"></a>Vise detaljer om dataintegrering

På hurtigfanen **Administrasjon** på siden **Common Data Service-integrering** kan du se hvordan postes kobles sammen mellom Human Resources og Common Data Service.

- Hvis du vil vise postene for en enhet, velger du enheten i feltet **CDS-enhetsnavn**. I rutenettet vises alle postene som er koblet til den valgte enheten.

[![Vise postene for en enhet](./media/hr-common-data-service-configuration-view-entity.png)](./media/hr-common-data-service-configuration-view-entity.png)

> [!NOTE]
> Ikke alle Common Data Service-enheter er oppført i listen. Bare enheter som støtter bruk av egendefinerte felt, vises i rutenettet. Nye enheter blir tilgjengelige via kontinuerlige utgivelser av Human Resources.

Rutenettet inneholder følgende felt:

- **CDS-enhetsnavn** – Navnet på enheten i Common Data Service.
- **CDS-enhetsreferanse** – Identifikatoren som Common Data Service brukes til å identifisere en post. Denne verdien tilsvarer en **RecId**-verdi for Human Resources. Du kan finne identifikatoren når du åpner Common Data Service-enheten i Microsoft Excel.
- **Navn på Human Resourcesnhet** – Enheten som sist synkroniserte data til Common Data Service. Enheten kan ha Common Data Service-prefikset eller et annet prefiks.
- **Personalreferanse** – **RecId**-verdien som er knyttet til posten i Human Resources.
- **Ble slettet fra CDS** – En verdi som indikerer om posten ble slettet fra Common Data Service.

## <a name="remove-the-association-of-a-record-in-human-resources-from-common-data-service"></a>Fjerne tilknytningen til en post i Human Resources fra Common Data Service

Hvis det oppstår problemer under datasynkronisering mellom Human Resources og Common Data Service, kan det hende at du kan løse dem ved å fjerne sporingen og la sporingstabellen synkroniseres på nytt. Hvis du fjerner tilknytningen og deretter endrer eller sletter en post i Common Data Service, blir ikke endringene synkronisert med Human Resources. Hvis du utfører endringer i Human Resources, opprettes det en ny sporingspost, og posten oppdateres i Common Data Service.

- Hvis du vil fjerne tilknytningen av en post mellom Human Resources og Common Data Service, velger du enheten i feltet **CDS-enhetsnavn** og velger deretter **Fjern sporingsinformasjon**.

[![Fjerne sporingsinformasjon](./media/hr-common-data-service-configuration-clear-tracking.png)](./media/hr-common-data-service-configuration-clear-tracking.png)

Hvis du vil kjøre en fullstendig synkronisering med enheten etter at du har fjernet sporingen, kan du se neste prosedyre.

## <a name="sync-an-entity-between-human-resources-and-common-data-service"></a>Synkronisere en enhet mellom Human Resources og Common Data Service

Bruk denne fremgangsmåten når:

- Det tar for lang tid å vise endringer fra Common Data Service i Human Resources.

- Du må oppdatere sporingstabellen etter at du har fjernet sporingen.

Slik kjører du en fullstendig synkronisering av en enhet mellom Human Resources og Common Data Service:

1. Velg enheten i feltet **CDS-enhetsnavn**.

2. Velg **Synkroniser nå**.

[![Kjøre en full synkronisering](./media/hr-common-data-service-configuration-sync-now.png)](./media/hr-common-data-service-configuration-sync-now.png)


