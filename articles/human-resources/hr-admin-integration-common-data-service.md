---
title: Konfigurer Dataverse-integrering
description: Du kan aktivere eller deaktivere integrering mellom Microsoft Dataverse og Dynamics 365 Human Resources. Du kan også vise synkroniseringsdetaljer, slette sporingsdata og synkronisere en tabell på nytt for å hjelpe til med å feilsøke dataproblemer mellom de to miljøene.
author: andreabichsel
ms.date: 01/25/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: bf406a954f5bb8b49627b58a901d0721cdad407b
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/13/2021
ms.locfileid: "5890034"
---
# <a name="configure-dataverse-integration"></a>Konfigurer Dataverse-integrering

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Du kan aktivere eller deaktivere integrering mellom Microsoft Dataverse og Dynamics 365 Human Resources. Du kan også vise synkroniseringsdetaljene, slette sporingsdata og synkronisere en tabell på nytt for å hjelpe til med å feilsøke dataproblemer mellom de to miljøene.

> [!NOTE]
> Hvis du vil ha mer informasjon om Dataverse (tidligere Common Data Service) og terminologioppdateringer, kan du se [Hva er Microsoft Dataverse?](/powerapps/maker/data-platform/data-platform-intro)

Når du deaktiverer integrering, kan brukere gjøre endringer i Human Resources eller Dataverse, men disse endringene synkroniseres ikke mellom de to miljøene.

Som standard er dataintegrering mellom Human Resources og Dataverse slått av.

Du vil kanskje deaktivere integrering i disse situasjonene:

- Du fyller ut data gjennom databehandlingsrammeverket og må importere dataene flere ganger for å hente dem inn i riktig tilstand.

- Det er problemer med data i Human Resources eller Dataverse. Hvis du deaktiverer integrering, kan du slette en post i ett miljø uten å slette den i det andre. Når du slår på integreringen igjen, vil posten i miljøet der den ikke var slettet, bli synkronisert tilbake til miljøet der den ble slettet. Synkroniseringen starter neste gang den satsvise jobben **Dataverse-integrering mangler forespørselssynkronisering** kjøres.

> [!WARNING]
> Når du slår av dataintegrering, må du passe på at du ikke redigerer samme post i begge miljøene. Når du slår på integreringen igjen, blir posten du sist redigerte, synkronisert. Hvis du ikke gjorde de samme endringene i posten i begge miljøer, kan det derfor oppstå datatap.

## <a name="access-the-dataverse-integration-page"></a>Få tilgang til Dataverse-integreringssiden

1. I forekomsten av Human Resources der du vil vise eller konfigurere innstillinger for integreringen med Dataverse, velger du flisen **Systemadministrasjon**.

    [![Flisen Systemadministrasjon](./media/hr-select-system-administration.png)](./media/hr-select-system-administration.png)

2. Velg kategorien **Koblinger**.

    [![Koblinger-kategorien](./media/hr-system-administration-links.png)](./media/hr-system-administration-links.png)

3. Under **Integreringer** velger du **Dataverse-konfigurasjon**.

    [![Dataverse-konfigurasjonskobling](./media/hr-admin-integration-dataverse-select.png)](./media/hr-admin-integration-dataverse-select.png)

## <a name="turn-data-integration-between-human-resources-and-dataverse-on-or-off"></a>Slå dataintegrering mellom Human Resources og Dataverse på eller av

- Hvis du vil slå på integrering, angir du **Aktiver Dataverse-integrering** -alternativet til **Ja** på **Microsoft Dataverse-integrasjon**-siden.

    > [!NOTE]
    > Når du aktiverer integrering, blir data synkronisert neste gang den satsvise jobben **Dataverse-integrering mangler forespørselssynkronisering** kjøres. Alle data skal være tilgjengelige når den satsvise jobben er fullført.

- Hvis du vil deaktivere integrering, setter du alternativet til **Nei**.

[![Aktivere eller deaktivere Dataverse-integrering](./media/hr-admin-integration-dataverse-enable-disable.png)](./media/hr-admin-integration-dataverse-enable-disable.png)

> [!WARNING]
> Det anbefales sterkt at du deaktiverer Dataverse-integrering mens du utfører datamigreringsoppgaver. Store dataopplastinger kan påvirke ytelsen betydelig. Eksempel: Opplasting av 2000 arbeidere kan ta flere timer når integrering er aktivert, og mindre enn én time når den er deaktivert. Tallene i dette eksemplet er bare for demonstrasjon. Den nøyaktige tiden det tar å importere poster, kan variere betraktelig, avhengig av mange faktorer.

## <a name="view-data-integration-details"></a>Vise detaljer om dataintegrering

På hurtigfanen **Administrasjon** på siden **Microsoft Dataverse-integrering** kan du se hvordan rader kobles sammen mellom Human Resources og Dataverse.

- Hvis du vil vise radene for en tabell, velger du tabellen i **Dataverse-tabell**-feltet. I rutenettet vises alle radene som er koblet til den valgte tabellen.

> [!NOTE]
> Ikke alle Dataverse-tabeller er oppført i listen. Bare tabeller som støtter bruk av egendefinerte felt, vises i rutenettet. Nye tabeller blir tilgjengelige via kontinuerlige utgivelser av Human Resources.

Rutenettet inneholder følgende felt:

- **Dataverse-tabell** – Navnet på tabellen i Dataverse.
- **Dataverse-tabellreferanse** – Identifikatoren som Dataverse bruker til å identifisere en post. Denne verdien tilsvarer en **RecId**-verdi for Human Resources. Du kan finne identifikatoren når du åpner Dataverse-tabellen i Microsoft Excel.
- **Navn på Human Resource-enhet** – Human Resources-enheten som sist synkroniserte data til Dataverse. Enheten kan ha Dataverse-prefikset eller et annet prefiks.
- **Personalreferanse** – **RecId**-verdien som er knyttet til posten i Human Resources.
- **Slettet fra Dataverse** – En verdi som indikerer om raden ble slettet fra Dataverse.

> [!NOTE]
> Poster i Human Resources tilsvarer rader i Dataverse.

## <a name="remove-the-association-of-a-human-resources-record-from-a-dataverse-row"></a>Fjerne tilknytningen til en Human Resources-post fra en Dataverse-rad

Hvis det oppstår problemer under datasynkronisering mellom Human Resources og Dataverse, kan det hende at du kan løse dem ved å fjerne sporingen og la sporingstabellen synkroniseres på nytt. Hvis du fjerner tilknytningen og deretter endrer eller sletter en rad i Dataverse, blir ikke endringene synkronisert med Human Resources. Hvis du utfører endringer i Human Resources, opprettes det en ny sporingspost, og raden oppdateres i Dataverse.

- Hvis du vil fjerne tilknytningen mellom en Human Resources-post og en Dataverse-rad, velger du tabellen i feltet **Dataverse-tabell**, og deretter velger du **Fjern sporingsinformasjon**.

[![Fjerne sporingsinformasjon](./media/hr-admin-integration-dataverse-clear-tracking.png)](./media/hr-admin-integration-dataverse-clear-tracking.png)

Hvis du vil kjøre en fullstendig synkronisering med tabellen etter at du har fjernet sporingen, kan du se neste prosedyre.

## <a name="sync-a-table-between-human-resources-and-dataverse"></a>Synkronisere en tabell mellom Human Resources og Dataverse

Bruk denne fremgangsmåten når:

- Det tar for lang tid å vise endringer fra Dataverse i Human Resources.

- Du må oppdatere sporingstabellen etter at du har fjernet sporingen.

Slik kjører du en fullstendig synkronisering av en tabell mellom Human Resources og Dataverse:

1. Velg tabellen i feltet **Dataverse-tabell**.

2. Velg **Synkroniser nå**.

[![Kjøre en full synkronisering](./media/hr-admin-integration-dataverse-sync-now.png)](./media/hr-admin-integration-dataverse-sync-now.png)

## <a name="see-also"></a>Se også

[Dataverse-tabeller](hr-developer-entities.md)<br>
[Konfigurere virtuelle Dataverse-tabeller](hr-admin-integration-common-data-service-virtual-entities.md)<br>
[Vanlige spørsmål om virtuelle tabeller for Human Resources](hr-admin-virtual-entity-faq.md)<br>
[Hva er Microsoft Dataverse?](/powerapps/maker/data-platform/data-platform-intro)<br>
[Terminologioppdateringer](/powerapps/maker/data-platform/data-platform-intro#terminology-updates)


[!INCLUDE[footer-include](../includes/footer-banner.md)]