---
title: Konfigurer Common Data Service-integrering
description: Du kan aktivere eller deaktivere integrering mellom Common Data Service og Dynamics 365 Human Resources. Du kan også vise synkroniseringsdetaljer, slette sporingsdata og synkronisere en enhet på nytt for å hjelpe til med å feilsøke dataproblemer mellom de to miljøene.
author: andreabichsel
manager: AnnBe
ms.date: 04/01/2020
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
ms.openlocfilehash: 7aad8217d48917d6855046a6810fe994f5564d94
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/04/2020
ms.locfileid: "3431320"
---
# <a name="configure-common-data-service-integration"></a><span data-ttu-id="9a3e6-104">Konfigurer Common Data Service-integrering</span><span class="sxs-lookup"><span data-stu-id="9a3e6-104">Configure Common Data Service integration</span></span>

<span data-ttu-id="9a3e6-105">Du kan aktivere eller deaktivere integrering mellom Common Data Service og Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="9a3e6-105">You can turn integration between Common Data Service and Dynamics 365 Human Resources on or off.</span></span> <span data-ttu-id="9a3e6-106">Du kan også vise synkroniseringsdetaljene, slette sporingsdata og synkronisere en enhet på nytt for å hjelpe til med å feilsøke dataproblemer mellom de to miljøene.</span><span class="sxs-lookup"><span data-stu-id="9a3e6-106">You can also view the synchronization details, clear tracking data, and resync an entity to help troubleshoot data issues between the two environments.</span></span>

<span data-ttu-id="9a3e6-107">Når du deaktiverer integrering, kan brukere gjøre endringer i Human Resources eller Common Data Service, men disse endringene synkroniseres ikke mellom de to miljøene.</span><span class="sxs-lookup"><span data-stu-id="9a3e6-107">When you turn off integration, users can make changes in Human Resources or Common Data Service, but those changes aren't synced between the two environments.</span></span>

<span data-ttu-id="9a3e6-108">Som standard er dataintegrering mellom Human Resources og Common Data Service slått av.</span><span class="sxs-lookup"><span data-stu-id="9a3e6-108">By default, integration between Human Resources and Common Data Service is turned off.</span></span>

<span data-ttu-id="9a3e6-109">Du vil kanskje deaktivere integrering i disse situasjonene:</span><span class="sxs-lookup"><span data-stu-id="9a3e6-109">You might want to turn off integration in these situations:</span></span>

- <span data-ttu-id="9a3e6-110">Du fyller ut data gjennom databehandlingsrammeverket og må importere dataene flere ganger for å hente dem inn i riktig tilstand.</span><span class="sxs-lookup"><span data-stu-id="9a3e6-110">You're filling in data through the Data Management Framework and must import the data multiple times to get it into a correct state.</span></span>

- <span data-ttu-id="9a3e6-111">Det er problemer med data i Human Resources eller Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="9a3e6-111">There are issues with data in either Human Resources or Common Data Service.</span></span> <span data-ttu-id="9a3e6-112">Hvis du deaktiverer integrering, kan du slette en post i ett miljø uten å slette den i det andre.</span><span class="sxs-lookup"><span data-stu-id="9a3e6-112">If you turn off integration, you can delete a record in one environment without deleting it in the other.</span></span> <span data-ttu-id="9a3e6-113">Når du slår på integreringen igjen, vil posten i miljøet der den ikke var slettet, bli synkronisert tilbake til miljøet der den ble slettet.</span><span class="sxs-lookup"><span data-stu-id="9a3e6-113">When you turn integration back on, the record in the environment where it wasn't deleted sync to the environment where it was deleted.</span></span> <span data-ttu-id="9a3e6-114">Synkroniseringen starter neste gang den satsvise jobben **Common Data Service-integrering mangler forespørselssynkronisering** kjøres.</span><span class="sxs-lookup"><span data-stu-id="9a3e6-114">Synchronization begins the next time the **Common Data Service integration missed request sync** batch job runs.</span></span>

> [!WARNING]
> <span data-ttu-id="9a3e6-115">Når du slår av dataintegrering, må du passe på at du ikke redigerer samme post i begge miljøene.</span><span class="sxs-lookup"><span data-stu-id="9a3e6-115">When you turn off data integration, make sure that you don't edit the same record in both environments.</span></span> <span data-ttu-id="9a3e6-116">Når du slår på integreringen igjen, blir posten du sist redigerte, synkronisert.</span><span class="sxs-lookup"><span data-stu-id="9a3e6-116">When you turn integration back on, the record that you last edited will be synced.</span></span> <span data-ttu-id="9a3e6-117">Hvis du ikke gjorde de samme endringene i posten i begge miljøer, kan det derfor oppstå datatap.</span><span class="sxs-lookup"><span data-stu-id="9a3e6-117">Therefore, if you didn't make the same changes to the record in both environments, data loss can occur.</span></span>

## <a name="access-the-common-data-service-integration-page"></a><span data-ttu-id="9a3e6-118">Få tilgang til Common Data Service-integreringssiden</span><span class="sxs-lookup"><span data-stu-id="9a3e6-118">Access the Common Data Service integration page</span></span>

1. <span data-ttu-id="9a3e6-119">I forekomsten av Human Resources der du vil vise eller konfigurere innstillinger for integreringen med Common Data Service, velger du flisen **Systemadministrasjon**.</span><span class="sxs-lookup"><span data-stu-id="9a3e6-119">In the Human Resources instance where you want to view or configure settings for the integration with Common Data Service, select the **System administration** tile.</span></span>

    <span data-ttu-id="9a3e6-120">[![Flisen Systemadministrasjon](./media/hr-select-system-administration.png)](./media/hr-select-system-administration.png)</span><span class="sxs-lookup"><span data-stu-id="9a3e6-120">[![System administration tile](./media/hr-select-system-administration.png)](./media/hr-select-system-administration.png)</span></span>

2. <span data-ttu-id="9a3e6-121">Velg kategorien **Koblinger**.</span><span class="sxs-lookup"><span data-stu-id="9a3e6-121">Select the **Links** tab.</span></span>

    <span data-ttu-id="9a3e6-122">[![Koblinger-kategorien](./media/hr-system-administration-links.png)](./media/hr-system-administration-links.png)</span><span class="sxs-lookup"><span data-stu-id="9a3e6-122">[![Links tab](./media/hr-system-administration-links.png)](./media/hr-system-administration-links.png)</span></span>

3. <span data-ttu-id="9a3e6-123">Under **Integreringer** velger du **Common Data Service-konfigurasjon**.</span><span class="sxs-lookup"><span data-stu-id="9a3e6-123">Under **Integrations**, select **Common Data Service configuration**.</span></span>

    <span data-ttu-id="9a3e6-124">[![Common Data Service-konfigurasjonskobling](./media/hr-select-common-data-service-configuration.png)](./media/hr-select-common-data-service-configuration.png)</span><span class="sxs-lookup"><span data-stu-id="9a3e6-124">[![Common Data Service configuration link](./media/hr-select-common-data-service-configuration.png)](./media/hr-select-common-data-service-configuration.png)</span></span>

## <a name="turn-data-integration-between-human-resources-and-common-data-service-on-or-off"></a><span data-ttu-id="9a3e6-125">Slå dataintegrering mellom Human Resources og Common Data Service på eller av</span><span class="sxs-lookup"><span data-stu-id="9a3e6-125">Turn data integration between Human Resources and Common Data Service on or off</span></span>

- <span data-ttu-id="9a3e6-126">Hvis du vil slå på integrering, angir du **Aktiver integreringen til Common Data Service**-alternativet til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="9a3e6-126">To turn on integration, set the **Enable the integration to the Common Data Service** option to **Yes**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="9a3e6-127">Når du aktiverer integrering, blir data synkronisert neste gang den satsvise jobben **Common Data Service-integrering mangler forespørselssynkronisering** kjøres.</span><span class="sxs-lookup"><span data-stu-id="9a3e6-127">When you turn on integration, data will be synced the next time that the **Common Data Service integration missed request sync** batch job runs.</span></span> <span data-ttu-id="9a3e6-128">Alle data skal være tilgjengelige når den satsvise jobben er fullført.</span><span class="sxs-lookup"><span data-stu-id="9a3e6-128">All data should be available after the batch job is completed.</span></span>

- <span data-ttu-id="9a3e6-129">Hvis du vil deaktivere integrering, setter du alternativet til **Nei**.</span><span class="sxs-lookup"><span data-stu-id="9a3e6-129">To turn off integration, set the option to **No**.</span></span>

<span data-ttu-id="9a3e6-130">[![Aktivere eller deaktivere Common Data Service-integrering](./media/hr-enable-or-disable-common-data-service-integration.png)](./media/hr-enable-or-disable-common-data-service-integration.png)</span><span class="sxs-lookup"><span data-stu-id="9a3e6-130">[![Turning the Common Data Service integration on or off](./media/hr-enable-or-disable-common-data-service-integration.png)](./media/hr-enable-or-disable-common-data-service-integration.png)</span></span>

## <a name="view-data-integration-details"></a><span data-ttu-id="9a3e6-131">Vise detaljer om dataintegrering</span><span class="sxs-lookup"><span data-stu-id="9a3e6-131">View data integration details</span></span>

<span data-ttu-id="9a3e6-132">På hurtigfanen **Administrasjon** på siden **Common Data Service-integrering** kan du se hvordan postes kobles sammen mellom Human Resources og Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="9a3e6-132">On the **Administration** FastTab of the **Common Data Service integration** page, you can see how records are linked together between Human Resources and Common Data Service.</span></span>

- <span data-ttu-id="9a3e6-133">Hvis du vil vise postene for en enhet, velger du enheten i feltet **CDS-enhetsnavn**.</span><span class="sxs-lookup"><span data-stu-id="9a3e6-133">To view the records for an entity, select the entity in the **CDS entity name** field.</span></span> <span data-ttu-id="9a3e6-134">I rutenettet vises alle postene som er koblet til den valgte enheten.</span><span class="sxs-lookup"><span data-stu-id="9a3e6-134">The grid shows all the records that are linked to the selected entity.</span></span>

<span data-ttu-id="9a3e6-135">[![Vise postene for en enhet](./media/hr-common-data-service-configuration-view-entity.png)](./media/hr-common-data-service-configuration-view-entity.png)</span><span class="sxs-lookup"><span data-stu-id="9a3e6-135">[![Viewing the records for an entity](./media/hr-common-data-service-configuration-view-entity.png)](./media/hr-common-data-service-configuration-view-entity.png)</span></span>

> [!NOTE]
> <span data-ttu-id="9a3e6-136">Ikke alle Common Data Service-enheter er oppført i listen.</span><span class="sxs-lookup"><span data-stu-id="9a3e6-136">Not all Common Data Service entities are currently listed.</span></span> <span data-ttu-id="9a3e6-137">Bare enheter som støtter bruk av egendefinerte felt, vises i rutenettet.</span><span class="sxs-lookup"><span data-stu-id="9a3e6-137">Only entities that support the use of custom fields appear in the grid.</span></span> <span data-ttu-id="9a3e6-138">Nye enheter blir tilgjengelige via kontinuerlige utgivelser av Human Resources.</span><span class="sxs-lookup"><span data-stu-id="9a3e6-138">New entities become available through continuous releases of Human Resources.</span></span>

<span data-ttu-id="9a3e6-139">Rutenettet inneholder følgende felt:</span><span class="sxs-lookup"><span data-stu-id="9a3e6-139">The grid includes the following fields:</span></span>

- <span data-ttu-id="9a3e6-140">**CDS-enhetsnavn** – Navnet på enheten i Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="9a3e6-140">**CDS entity name** – The name of the entity in Common Data Service.</span></span>
- <span data-ttu-id="9a3e6-141">**CDS-enhetsreferanse** – Identifikatoren som Common Data Service brukes til å identifisere en post.</span><span class="sxs-lookup"><span data-stu-id="9a3e6-141">**CDS entity reference** – The identifier that Common Data Service uses to identify a record.</span></span> <span data-ttu-id="9a3e6-142">Denne verdien tilsvarer en **RecId**-verdi for Human Resources.</span><span class="sxs-lookup"><span data-stu-id="9a3e6-142">This value is equivalent to a Human Resources **RecId** value.</span></span> <span data-ttu-id="9a3e6-143">Du kan finne identifikatoren når du åpner Common Data Service-enheten i Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="9a3e6-143">You can find the identifier when you open the Common Data Service entity in Microsoft Excel.</span></span>
- <span data-ttu-id="9a3e6-144">**Navn på Human Resourcesnhet** – Enheten som sist synkroniserte data til Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="9a3e6-144">**Human Resources entity name** – The entity that last synced data to Common Data Service.</span></span> <span data-ttu-id="9a3e6-145">Enheten kan ha Common Data Service-prefikset eller et annet prefiks.</span><span class="sxs-lookup"><span data-stu-id="9a3e6-145">The entity can have either the Common Data Service prefix or another prefix.</span></span>
- <span data-ttu-id="9a3e6-146">**Personalreferanse** – **RecId**-verdien som er knyttet til posten i Human Resources.</span><span class="sxs-lookup"><span data-stu-id="9a3e6-146">**Human Resources reference** – The **RecId** value that is associated with the record in Human Resources.</span></span>
- <span data-ttu-id="9a3e6-147">**Ble slettet fra CDS** – En verdi som indikerer om posten ble slettet fra Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="9a3e6-147">**Was deleted from CDS** – A value that indicates whether the record was deleted from Common Data Service.</span></span>

## <a name="remove-the-association-of-a-record-in-human-resources-from-common-data-service"></a><span data-ttu-id="9a3e6-148">Fjerne tilknytningen til en post i Human Resources fra Common Data Service</span><span class="sxs-lookup"><span data-stu-id="9a3e6-148">Remove the association of a record in Human Resources from Common Data Service</span></span>

<span data-ttu-id="9a3e6-149">Hvis det oppstår problemer under datasynkronisering mellom Human Resources og Common Data Service, kan det hende at du kan løse dem ved å fjerne sporingen og la sporingstabellen synkroniseres på nytt.</span><span class="sxs-lookup"><span data-stu-id="9a3e6-149">If you experience issues during data synchronization between Human Resources and Common Data Service, you might be able to resolve them by clearing the tracking and letting the tracking table be resynced.</span></span> <span data-ttu-id="9a3e6-150">Hvis du fjerner tilknytningen og deretter endrer eller sletter en post i Common Data Service, blir ikke endringene synkronisert med Human Resources.</span><span class="sxs-lookup"><span data-stu-id="9a3e6-150">If you remove the association, and then change or delete a record in Common Data Service, the changes won't be synced to Human Resources.</span></span> <span data-ttu-id="9a3e6-151">Hvis du utfører endringer i Human Resources, opprettes det en ny sporingspost, og posten oppdateres i Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="9a3e6-151">If you make changes in Human Resources, a new tracking record is created, and the record is updated in Common Data Service.</span></span>

- <span data-ttu-id="9a3e6-152">Hvis du vil fjerne tilknytningen av en post mellom Human Resources og Common Data Service, velger du enheten i feltet **CDS-enhetsnavn** og velger deretter **Fjern sporingsinformasjon**.</span><span class="sxs-lookup"><span data-stu-id="9a3e6-152">To remove the association of a record between Human Resources and Common Data Service, select the entity in the **CDS entity name** field, and then select **Clear tracking information**.</span></span>

<span data-ttu-id="9a3e6-153">[![Fjerne sporingsinformasjon](./media/hr-common-data-service-configuration-clear-tracking.png)](./media/hr-common-data-service-configuration-clear-tracking.png)</span><span class="sxs-lookup"><span data-stu-id="9a3e6-153">[![Clearing tracking information](./media/hr-common-data-service-configuration-clear-tracking.png)](./media/hr-common-data-service-configuration-clear-tracking.png)</span></span>

<span data-ttu-id="9a3e6-154">Hvis du vil kjøre en fullstendig synkronisering med enheten etter at du har fjernet sporingen, kan du se neste prosedyre.</span><span class="sxs-lookup"><span data-stu-id="9a3e6-154">To run a full synchronization on the entity after you clear the tracking, see the next procedure.</span></span>

## <a name="sync-an-entity-between-human-resources-and-common-data-service"></a><span data-ttu-id="9a3e6-155">Synkronisere en enhet mellom Human Resources og Common Data Service</span><span class="sxs-lookup"><span data-stu-id="9a3e6-155">Sync an entity between Human Resources and Common Data Service</span></span>

<span data-ttu-id="9a3e6-156">Bruk denne fremgangsmåten når:</span><span class="sxs-lookup"><span data-stu-id="9a3e6-156">Use this procedure when:</span></span>

- <span data-ttu-id="9a3e6-157">Det tar for lang tid å vise endringer fra Common Data Service i Human Resources.</span><span class="sxs-lookup"><span data-stu-id="9a3e6-157">Changes from Common Data Service take too long to appear in Human Resources.</span></span>

- <span data-ttu-id="9a3e6-158">Du må oppdatere sporingstabellen etter at du har fjernet sporingen.</span><span class="sxs-lookup"><span data-stu-id="9a3e6-158">You must refresh the tracking table after clearing the tracking.</span></span>

<span data-ttu-id="9a3e6-159">Slik kjører du en fullstendig synkronisering av en enhet mellom Human Resources og Common Data Service:</span><span class="sxs-lookup"><span data-stu-id="9a3e6-159">To run a full synchronization on an entity between Human Resources and Common Data Service:</span></span>

1. <span data-ttu-id="9a3e6-160">Velg enheten i feltet **CDS-enhetsnavn**.</span><span class="sxs-lookup"><span data-stu-id="9a3e6-160">Select the entity in the **CDS entity name** field.</span></span>

2. <span data-ttu-id="9a3e6-161">Velg **Synkroniser nå**.</span><span class="sxs-lookup"><span data-stu-id="9a3e6-161">Select **Sync now**.</span></span>

<span data-ttu-id="9a3e6-162">[![Kjøre en full synkronisering](./media/hr-common-data-service-configuration-sync-now.png)](./media/hr-common-data-service-configuration-sync-now.png)</span><span class="sxs-lookup"><span data-stu-id="9a3e6-162">[![Running a full synchronization](./media/hr-common-data-service-configuration-sync-now.png)](./media/hr-common-data-service-configuration-sync-now.png)</span></span>


