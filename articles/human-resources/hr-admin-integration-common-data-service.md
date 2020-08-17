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
# <a name="configure-common-data-service-integration"></a><span data-ttu-id="28460-104">Konfigurer Common Data Service-integrering</span><span class="sxs-lookup"><span data-stu-id="28460-104">Configure Common Data Service integration</span></span>

<span data-ttu-id="28460-105">Du kan aktivere eller deaktivere integrering mellom Common Data Service og Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="28460-105">You can turn integration between Common Data Service and Dynamics 365 Human Resources on or off.</span></span> <span data-ttu-id="28460-106">Du kan også vise synkroniseringsdetaljene, slette sporingsdata og synkronisere en enhet på nytt for å hjelpe til med å feilsøke dataproblemer mellom de to miljøene.</span><span class="sxs-lookup"><span data-stu-id="28460-106">You can also view the synchronization details, clear tracking data, and resync an entity to help troubleshoot data issues between the two environments.</span></span>

<span data-ttu-id="28460-107">Når du deaktiverer integrering, kan brukere gjøre endringer i Human Resources eller Common Data Service, men disse endringene synkroniseres ikke mellom de to miljøene.</span><span class="sxs-lookup"><span data-stu-id="28460-107">When you turn off integration, users can make changes in Human Resources or Common Data Service, but those changes aren't synced between the two environments.</span></span>

<span data-ttu-id="28460-108">Som standard er dataintegrering mellom Human Resources og Common Data Service slått av.</span><span class="sxs-lookup"><span data-stu-id="28460-108">By default, integration between Human Resources and Common Data Service is turned off.</span></span>

<span data-ttu-id="28460-109">Du vil kanskje deaktivere integrering i disse situasjonene:</span><span class="sxs-lookup"><span data-stu-id="28460-109">You might want to turn off integration in these situations:</span></span>

- <span data-ttu-id="28460-110">Du fyller ut data gjennom databehandlingsrammeverket og må importere dataene flere ganger for å hente dem inn i riktig tilstand.</span><span class="sxs-lookup"><span data-stu-id="28460-110">You're filling in data through the Data Management Framework and must import the data multiple times to get it into a correct state.</span></span>

- <span data-ttu-id="28460-111">Det er problemer med data i Human Resources eller Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="28460-111">There are issues with data in either Human Resources or Common Data Service.</span></span> <span data-ttu-id="28460-112">Hvis du deaktiverer integrering, kan du slette en post i ett miljø uten å slette den i det andre.</span><span class="sxs-lookup"><span data-stu-id="28460-112">If you turn off integration, you can delete a record in one environment without deleting it in the other.</span></span> <span data-ttu-id="28460-113">Når du slår på integreringen igjen, vil posten i miljøet der den ikke var slettet, bli synkronisert tilbake til miljøet der den ble slettet.</span><span class="sxs-lookup"><span data-stu-id="28460-113">When you turn integration back on, the record in the environment where it wasn't deleted sync to the environment where it was deleted.</span></span> <span data-ttu-id="28460-114">Synkroniseringen starter neste gang den satsvise jobben **Common Data Service-integrering mangler forespørselssynkronisering** kjøres.</span><span class="sxs-lookup"><span data-stu-id="28460-114">Synchronization begins the next time the **Common Data Service integration missed request sync** batch job runs.</span></span>

> [!WARNING]
> <span data-ttu-id="28460-115">Når du slår av dataintegrering, må du passe på at du ikke redigerer samme post i begge miljøene.</span><span class="sxs-lookup"><span data-stu-id="28460-115">When you turn off data integration, make sure that you don't edit the same record in both environments.</span></span> <span data-ttu-id="28460-116">Når du slår på integreringen igjen, blir posten du sist redigerte, synkronisert.</span><span class="sxs-lookup"><span data-stu-id="28460-116">When you turn integration back on, the record that you last edited will be synced.</span></span> <span data-ttu-id="28460-117">Hvis du ikke gjorde de samme endringene i posten i begge miljøer, kan det derfor oppstå datatap.</span><span class="sxs-lookup"><span data-stu-id="28460-117">Therefore, if you didn't make the same changes to the record in both environments, data loss can occur.</span></span>

## <a name="access-the-common-data-service-integration-page"></a><span data-ttu-id="28460-118">Få tilgang til Common Data Service-integreringssiden</span><span class="sxs-lookup"><span data-stu-id="28460-118">Access the Common Data Service integration page</span></span>

1. <span data-ttu-id="28460-119">I forekomsten av Human Resources der du vil vise eller konfigurere innstillinger for integreringen med Common Data Service, velger du flisen **Systemadministrasjon**.</span><span class="sxs-lookup"><span data-stu-id="28460-119">In the Human Resources instance where you want to view or configure settings for the integration with Common Data Service, select the **System administration** tile.</span></span>

    <span data-ttu-id="28460-120">[![Flisen Systemadministrasjon](./media/hr-select-system-administration.png)](./media/hr-select-system-administration.png)</span><span class="sxs-lookup"><span data-stu-id="28460-120">[![System administration tile](./media/hr-select-system-administration.png)](./media/hr-select-system-administration.png)</span></span>

2. <span data-ttu-id="28460-121">Velg kategorien **Koblinger**.</span><span class="sxs-lookup"><span data-stu-id="28460-121">Select the **Links** tab.</span></span>

    <span data-ttu-id="28460-122">[![Koblinger-kategorien](./media/hr-system-administration-links.png)](./media/hr-system-administration-links.png)</span><span class="sxs-lookup"><span data-stu-id="28460-122">[![Links tab](./media/hr-system-administration-links.png)](./media/hr-system-administration-links.png)</span></span>

3. <span data-ttu-id="28460-123">Under **Integreringer** velger du **Common Data Service-konfigurasjon**.</span><span class="sxs-lookup"><span data-stu-id="28460-123">Under **Integrations**, select **Common Data Service configuration**.</span></span>

    <span data-ttu-id="28460-124">[![Common Data Service-konfigurasjonskobling](./media/hr-select-common-data-service-configuration.png)](./media/hr-select-common-data-service-configuration.png)</span><span class="sxs-lookup"><span data-stu-id="28460-124">[![Common Data Service configuration link](./media/hr-select-common-data-service-configuration.png)](./media/hr-select-common-data-service-configuration.png)</span></span>

## <a name="turn-data-integration-between-human-resources-and-common-data-service-on-or-off"></a><span data-ttu-id="28460-125">Slå dataintegrering mellom Human Resources og Common Data Service på eller av</span><span class="sxs-lookup"><span data-stu-id="28460-125">Turn data integration between Human Resources and Common Data Service on or off</span></span>

- <span data-ttu-id="28460-126">Hvis du vil slå på integrering, angir du **Aktiver integreringen til Common Data Service**-alternativet til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="28460-126">To turn on integration, set the **Enable the integration to the Common Data Service** option to **Yes**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="28460-127">Når du aktiverer integrering, blir data synkronisert neste gang den satsvise jobben **Common Data Service-integrering mangler forespørselssynkronisering** kjøres.</span><span class="sxs-lookup"><span data-stu-id="28460-127">When you turn on integration, data will be synced the next time that the **Common Data Service integration missed request sync** batch job runs.</span></span> <span data-ttu-id="28460-128">Alle data skal være tilgjengelige når den satsvise jobben er fullført.</span><span class="sxs-lookup"><span data-stu-id="28460-128">All data should be available after the batch job is completed.</span></span>

- <span data-ttu-id="28460-129">Hvis du vil deaktivere integrering, setter du alternativet til **Nei**.</span><span class="sxs-lookup"><span data-stu-id="28460-129">To turn off integration, set the option to **No**.</span></span>

<span data-ttu-id="28460-130">[![Aktivere eller deaktivere Common Data Service-integrering](./media/hr-enable-or-disable-common-data-service-integration.png)](./media/hr-enable-or-disable-common-data-service-integration.png)</span><span class="sxs-lookup"><span data-stu-id="28460-130">[![Turning the Common Data Service integration on or off](./media/hr-enable-or-disable-common-data-service-integration.png)](./media/hr-enable-or-disable-common-data-service-integration.png)</span></span>

> [!WARNING]
> <span data-ttu-id="28460-131">Vi anbefaler sterkt at du deaktiverer Common Data Service-integrering mens du utfører datamigreringsoppgaver.</span><span class="sxs-lookup"><span data-stu-id="28460-131">We strongly recommend turning off Common Data Service integration while performing data migration tasks.</span></span> <span data-ttu-id="28460-132">Store dataopplastinger kan påvirke ytelsen betydelig.</span><span class="sxs-lookup"><span data-stu-id="28460-132">Large data uploads can significantly impact performance.</span></span> <span data-ttu-id="28460-133">Eksempel: Opplasting av 2000 arbeidere kan ta flere timer når integrering er aktivert, og mindre enn én time når den er deaktivert.</span><span class="sxs-lookup"><span data-stu-id="28460-133">For example, uploading 2000 workers can take several hours when integration is enabled, and less than one hour when it's disabled.</span></span> <span data-ttu-id="28460-134">Tallene i dette eksemplet er bare for demonstrasjon.</span><span class="sxs-lookup"><span data-stu-id="28460-134">The numbers provided in this example are for demonstration purposes only.</span></span> <span data-ttu-id="28460-135">Den nøyaktige tiden det tar å importere poster, kan variere betraktelig, avhengig av mange faktorer.</span><span class="sxs-lookup"><span data-stu-id="28460-135">The exact amount of time it takes to import records can vary greatly based on many factors.</span></span>

## <a name="view-data-integration-details"></a><span data-ttu-id="28460-136">Vise detaljer om dataintegrering</span><span class="sxs-lookup"><span data-stu-id="28460-136">View data integration details</span></span>

<span data-ttu-id="28460-137">På hurtigfanen **Administrasjon** på siden **Common Data Service-integrering** kan du se hvordan postes kobles sammen mellom Human Resources og Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="28460-137">On the **Administration** FastTab of the **Common Data Service integration** page, you can see how records are linked together between Human Resources and Common Data Service.</span></span>

- <span data-ttu-id="28460-138">Hvis du vil vise postene for en enhet, velger du enheten i feltet **CDS-enhetsnavn**.</span><span class="sxs-lookup"><span data-stu-id="28460-138">To view the records for an entity, select the entity in the **CDS entity name** field.</span></span> <span data-ttu-id="28460-139">I rutenettet vises alle postene som er koblet til den valgte enheten.</span><span class="sxs-lookup"><span data-stu-id="28460-139">The grid shows all the records that are linked to the selected entity.</span></span>

<span data-ttu-id="28460-140">[![Vise postene for en enhet](./media/hr-common-data-service-configuration-view-entity.png)](./media/hr-common-data-service-configuration-view-entity.png)</span><span class="sxs-lookup"><span data-stu-id="28460-140">[![Viewing the records for an entity](./media/hr-common-data-service-configuration-view-entity.png)](./media/hr-common-data-service-configuration-view-entity.png)</span></span>

> [!NOTE]
> <span data-ttu-id="28460-141">Ikke alle Common Data Service-enheter er oppført i listen.</span><span class="sxs-lookup"><span data-stu-id="28460-141">Not all Common Data Service entities are currently listed.</span></span> <span data-ttu-id="28460-142">Bare enheter som støtter bruk av egendefinerte felt, vises i rutenettet.</span><span class="sxs-lookup"><span data-stu-id="28460-142">Only entities that support the use of custom fields appear in the grid.</span></span> <span data-ttu-id="28460-143">Nye enheter blir tilgjengelige via kontinuerlige utgivelser av Human Resources.</span><span class="sxs-lookup"><span data-stu-id="28460-143">New entities become available through continuous releases of Human Resources.</span></span>

<span data-ttu-id="28460-144">Rutenettet inneholder følgende felt:</span><span class="sxs-lookup"><span data-stu-id="28460-144">The grid includes the following fields:</span></span>

- <span data-ttu-id="28460-145">**CDS-enhetsnavn** – Navnet på enheten i Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="28460-145">**CDS entity name** – The name of the entity in Common Data Service.</span></span>
- <span data-ttu-id="28460-146">**CDS-enhetsreferanse** – Identifikatoren som Common Data Service brukes til å identifisere en post.</span><span class="sxs-lookup"><span data-stu-id="28460-146">**CDS entity reference** – The identifier that Common Data Service uses to identify a record.</span></span> <span data-ttu-id="28460-147">Denne verdien tilsvarer en **RecId**-verdi for Human Resources.</span><span class="sxs-lookup"><span data-stu-id="28460-147">This value is equivalent to a Human Resources **RecId** value.</span></span> <span data-ttu-id="28460-148">Du kan finne identifikatoren når du åpner Common Data Service-enheten i Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="28460-148">You can find the identifier when you open the Common Data Service entity in Microsoft Excel.</span></span>
- <span data-ttu-id="28460-149">**Navn på Human Resourcesnhet** – Enheten som sist synkroniserte data til Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="28460-149">**Human Resources entity name** – The entity that last synced data to Common Data Service.</span></span> <span data-ttu-id="28460-150">Enheten kan ha Common Data Service-prefikset eller et annet prefiks.</span><span class="sxs-lookup"><span data-stu-id="28460-150">The entity can have either the Common Data Service prefix or another prefix.</span></span>
- <span data-ttu-id="28460-151">**Personalreferanse** – **RecId**-verdien som er knyttet til posten i Human Resources.</span><span class="sxs-lookup"><span data-stu-id="28460-151">**Human Resources reference** – The **RecId** value that is associated with the record in Human Resources.</span></span>
- <span data-ttu-id="28460-152">**Ble slettet fra CDS** – En verdi som indikerer om posten ble slettet fra Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="28460-152">**Was deleted from CDS** – A value that indicates whether the record was deleted from Common Data Service.</span></span>

## <a name="remove-the-association-of-a-record-in-human-resources-from-common-data-service"></a><span data-ttu-id="28460-153">Fjerne tilknytningen til en post i Human Resources fra Common Data Service</span><span class="sxs-lookup"><span data-stu-id="28460-153">Remove the association of a record in Human Resources from Common Data Service</span></span>

<span data-ttu-id="28460-154">Hvis det oppstår problemer under datasynkronisering mellom Human Resources og Common Data Service, kan det hende at du kan løse dem ved å fjerne sporingen og la sporingstabellen synkroniseres på nytt.</span><span class="sxs-lookup"><span data-stu-id="28460-154">If you experience issues during data synchronization between Human Resources and Common Data Service, you might be able to resolve them by clearing the tracking and letting the tracking table be resynced.</span></span> <span data-ttu-id="28460-155">Hvis du fjerner tilknytningen og deretter endrer eller sletter en post i Common Data Service, blir ikke endringene synkronisert med Human Resources.</span><span class="sxs-lookup"><span data-stu-id="28460-155">If you remove the association, and then change or delete a record in Common Data Service, the changes won't be synced to Human Resources.</span></span> <span data-ttu-id="28460-156">Hvis du utfører endringer i Human Resources, opprettes det en ny sporingspost, og posten oppdateres i Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="28460-156">If you make changes in Human Resources, a new tracking record is created, and the record is updated in Common Data Service.</span></span>

- <span data-ttu-id="28460-157">Hvis du vil fjerne tilknytningen av en post mellom Human Resources og Common Data Service, velger du enheten i feltet **CDS-enhetsnavn** og velger deretter **Fjern sporingsinformasjon**.</span><span class="sxs-lookup"><span data-stu-id="28460-157">To remove the association of a record between Human Resources and Common Data Service, select the entity in the **CDS entity name** field, and then select **Clear tracking information**.</span></span>

<span data-ttu-id="28460-158">[![Fjerne sporingsinformasjon](./media/hr-common-data-service-configuration-clear-tracking.png)](./media/hr-common-data-service-configuration-clear-tracking.png)</span><span class="sxs-lookup"><span data-stu-id="28460-158">[![Clearing tracking information](./media/hr-common-data-service-configuration-clear-tracking.png)](./media/hr-common-data-service-configuration-clear-tracking.png)</span></span>

<span data-ttu-id="28460-159">Hvis du vil kjøre en fullstendig synkronisering med enheten etter at du har fjernet sporingen, kan du se neste prosedyre.</span><span class="sxs-lookup"><span data-stu-id="28460-159">To run a full synchronization on the entity after you clear the tracking, see the next procedure.</span></span>

## <a name="sync-an-entity-between-human-resources-and-common-data-service"></a><span data-ttu-id="28460-160">Synkronisere en enhet mellom Human Resources og Common Data Service</span><span class="sxs-lookup"><span data-stu-id="28460-160">Sync an entity between Human Resources and Common Data Service</span></span>

<span data-ttu-id="28460-161">Bruk denne fremgangsmåten når:</span><span class="sxs-lookup"><span data-stu-id="28460-161">Use this procedure when:</span></span>

- <span data-ttu-id="28460-162">Det tar for lang tid å vise endringer fra Common Data Service i Human Resources.</span><span class="sxs-lookup"><span data-stu-id="28460-162">Changes from Common Data Service take too long to appear in Human Resources.</span></span>

- <span data-ttu-id="28460-163">Du må oppdatere sporingstabellen etter at du har fjernet sporingen.</span><span class="sxs-lookup"><span data-stu-id="28460-163">You must refresh the tracking table after clearing the tracking.</span></span>

<span data-ttu-id="28460-164">Slik kjører du en fullstendig synkronisering av en enhet mellom Human Resources og Common Data Service:</span><span class="sxs-lookup"><span data-stu-id="28460-164">To run a full synchronization on an entity between Human Resources and Common Data Service:</span></span>

1. <span data-ttu-id="28460-165">Velg enheten i feltet **CDS-enhetsnavn**.</span><span class="sxs-lookup"><span data-stu-id="28460-165">Select the entity in the **CDS entity name** field.</span></span>

2. <span data-ttu-id="28460-166">Velg **Synkroniser nå**.</span><span class="sxs-lookup"><span data-stu-id="28460-166">Select **Sync now**.</span></span>

<span data-ttu-id="28460-167">[![Kjøre en full synkronisering](./media/hr-common-data-service-configuration-sync-now.png)](./media/hr-common-data-service-configuration-sync-now.png)</span><span class="sxs-lookup"><span data-stu-id="28460-167">[![Running a full synchronization](./media/hr-common-data-service-configuration-sync-now.png)](./media/hr-common-data-service-configuration-sync-now.png)</span></span>


