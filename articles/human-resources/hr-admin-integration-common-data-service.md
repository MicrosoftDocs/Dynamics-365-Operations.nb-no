---
title: Konfigurer Dataverse-integrering
description: Du kan aktivere eller deaktivere integrering mellom Microsoft Dataverse og Dynamics 365 Human Resources. Du kan også vise synkroniseringsdetaljer, slette sporingsdata og synkronisere en tabell på nytt for å hjelpe til med å feilsøke dataproblemer mellom de to miljøene.
author: andreabichsel
manager: tfehr
ms.date: 01/25/2021
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
ms.openlocfilehash: 38c42469e62bf5457d0281540325a6c56a5f930f
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/03/2021
ms.locfileid: "5113750"
---
# <a name="configure-dataverse-integration"></a><span data-ttu-id="8cf4e-104">Konfigurer Dataverse-integrering</span><span class="sxs-lookup"><span data-stu-id="8cf4e-104">Configure Dataverse integration</span></span>

<span data-ttu-id="8cf4e-105">Du kan aktivere eller deaktivere integrering mellom Microsoft Dataverse og Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="8cf4e-105">You can turn integration between Microsoft Dataverse and Dynamics 365 Human Resources on or off.</span></span> <span data-ttu-id="8cf4e-106">Du kan også vise synkroniseringsdetaljene, slette sporingsdata og synkronisere en tabell på nytt for å hjelpe til med å feilsøke dataproblemer mellom de to miljøene.</span><span class="sxs-lookup"><span data-stu-id="8cf4e-106">You can also view the synchronization details, clear tracking data, and resync a table to help troubleshoot data issues between the two environments.</span></span>

> [!NOTE]
> <span data-ttu-id="8cf4e-107">Hvis du vil ha mer informasjon om Dataverse (tidligere Common Data Service) og terminologioppdateringer, kan du se [Hva er Microsoft Dataverse?](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro)</span><span class="sxs-lookup"><span data-stu-id="8cf4e-107">For more information about Dataverse (formerly Common Data Service) and terminology updates, see [What is Microsoft Dataverse?](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro)</span></span>

<span data-ttu-id="8cf4e-108">Når du deaktiverer integrering, kan brukere gjøre endringer i Human Resources eller Dataverse, men disse endringene synkroniseres ikke mellom de to miljøene.</span><span class="sxs-lookup"><span data-stu-id="8cf4e-108">When you turn off integration, users can make changes in Human Resources or Dataverse, but those changes aren't synced between the two environments.</span></span>

<span data-ttu-id="8cf4e-109">Som standard er dataintegrering mellom Human Resources og Dataverse slått av.</span><span class="sxs-lookup"><span data-stu-id="8cf4e-109">By default, integration between Human Resources and Dataverse is turned off.</span></span>

<span data-ttu-id="8cf4e-110">Du vil kanskje deaktivere integrering i disse situasjonene:</span><span class="sxs-lookup"><span data-stu-id="8cf4e-110">You might want to turn off integration in these situations:</span></span>

- <span data-ttu-id="8cf4e-111">Du fyller ut data gjennom databehandlingsrammeverket og må importere dataene flere ganger for å hente dem inn i riktig tilstand.</span><span class="sxs-lookup"><span data-stu-id="8cf4e-111">You're filling in data through the Data Management Framework and must import the data multiple times to get it into a correct state.</span></span>

- <span data-ttu-id="8cf4e-112">Det er problemer med data i Human Resources eller Dataverse.</span><span class="sxs-lookup"><span data-stu-id="8cf4e-112">There are issues with data in either Human Resources or Dataverse.</span></span> <span data-ttu-id="8cf4e-113">Hvis du deaktiverer integrering, kan du slette en post i ett miljø uten å slette den i det andre.</span><span class="sxs-lookup"><span data-stu-id="8cf4e-113">If you turn off integration, you can delete a record in one environment without deleting it in the other.</span></span> <span data-ttu-id="8cf4e-114">Når du slår på integreringen igjen, vil posten i miljøet der den ikke var slettet, bli synkronisert tilbake til miljøet der den ble slettet.</span><span class="sxs-lookup"><span data-stu-id="8cf4e-114">When you turn integration back on, the record in the environment where it wasn't deleted sync to the environment where it was deleted.</span></span> <span data-ttu-id="8cf4e-115">Synkroniseringen starter neste gang den satsvise jobben **Dataverse-integrering mangler forespørselssynkronisering** kjøres.</span><span class="sxs-lookup"><span data-stu-id="8cf4e-115">Synchronization begins the next time the **Dataverse integration missed request sync** batch job runs.</span></span>

> [!WARNING]
> <span data-ttu-id="8cf4e-116">Når du slår av dataintegrering, må du passe på at du ikke redigerer samme post i begge miljøene.</span><span class="sxs-lookup"><span data-stu-id="8cf4e-116">When you turn off data integration, make sure that you don't edit the same record in both environments.</span></span> <span data-ttu-id="8cf4e-117">Når du slår på integreringen igjen, blir posten du sist redigerte, synkronisert.</span><span class="sxs-lookup"><span data-stu-id="8cf4e-117">When you turn integration back on, the record that you last edited will be synced.</span></span> <span data-ttu-id="8cf4e-118">Hvis du ikke gjorde de samme endringene i posten i begge miljøer, kan det derfor oppstå datatap.</span><span class="sxs-lookup"><span data-stu-id="8cf4e-118">Therefore, if you didn't make the same changes to the record in both environments, data loss can occur.</span></span>

## <a name="access-the-dataverse-integration-page"></a><span data-ttu-id="8cf4e-119">Få tilgang til Dataverse-integreringssiden</span><span class="sxs-lookup"><span data-stu-id="8cf4e-119">Access the Dataverse integration page</span></span>

1. <span data-ttu-id="8cf4e-120">I forekomsten av Human Resources der du vil vise eller konfigurere innstillinger for integreringen med Dataverse, velger du flisen **Systemadministrasjon**.</span><span class="sxs-lookup"><span data-stu-id="8cf4e-120">In the Human Resources instance where you want to view or configure settings for the integration with Dataverse, select the **System administration** tile.</span></span>

    <span data-ttu-id="8cf4e-121">[![Flisen Systemadministrasjon](./media/hr-select-system-administration.png)](./media/hr-select-system-administration.png)</span><span class="sxs-lookup"><span data-stu-id="8cf4e-121">[![System administration tile](./media/hr-select-system-administration.png)](./media/hr-select-system-administration.png)</span></span>

2. <span data-ttu-id="8cf4e-122">Velg kategorien **Koblinger**.</span><span class="sxs-lookup"><span data-stu-id="8cf4e-122">Select the **Links** tab.</span></span>

    <span data-ttu-id="8cf4e-123">[![Koblinger-kategorien](./media/hr-system-administration-links.png)](./media/hr-system-administration-links.png)</span><span class="sxs-lookup"><span data-stu-id="8cf4e-123">[![Links tab](./media/hr-system-administration-links.png)](./media/hr-system-administration-links.png)</span></span>

3. <span data-ttu-id="8cf4e-124">Under **Integreringer** velger du **Dataverse-konfigurasjon**.</span><span class="sxs-lookup"><span data-stu-id="8cf4e-124">Under **Integrations**, select **Dataverse configuration**.</span></span>

    <span data-ttu-id="8cf4e-125">[![Dataverse-konfigurasjonskobling](./media/hr-admin-integration-dataverse-select.png)](./media/hr-admin-integration-dataverse-select.png)</span><span class="sxs-lookup"><span data-stu-id="8cf4e-125">[![Dataverse configuration link](./media/hr-admin-integration-dataverse-select.png)](./media/hr-admin-integration-dataverse-select.png)</span></span>

## <a name="turn-data-integration-between-human-resources-and-dataverse-on-or-off"></a><span data-ttu-id="8cf4e-126">Slå dataintegrering mellom Human Resources og Dataverse på eller av</span><span class="sxs-lookup"><span data-stu-id="8cf4e-126">Turn data integration between Human Resources and Dataverse on or off</span></span>

- <span data-ttu-id="8cf4e-127">Hvis du vil slå på integrering, angir du **Aktiver Dataverse-integrering** -alternativet til **Ja** på **Microsoft Dataverse-integrasjon**-siden.</span><span class="sxs-lookup"><span data-stu-id="8cf4e-127">To turn on integration, set the **Enable Dataverse integration** option to **Yes** on the **Microsoft Dataverse integration** page.</span></span>

    > [!NOTE]
    > <span data-ttu-id="8cf4e-128">Når du aktiverer integrering, blir data synkronisert neste gang den satsvise jobben **Dataverse-integrering mangler forespørselssynkronisering** kjøres.</span><span class="sxs-lookup"><span data-stu-id="8cf4e-128">When you turn on integration, data will be synced the next time that the **Dataverse integration missed request sync** batch job runs.</span></span> <span data-ttu-id="8cf4e-129">Alle data skal være tilgjengelige når den satsvise jobben er fullført.</span><span class="sxs-lookup"><span data-stu-id="8cf4e-129">All data should be available after the batch job is completed.</span></span>

- <span data-ttu-id="8cf4e-130">Hvis du vil deaktivere integrering, setter du alternativet til **Nei**.</span><span class="sxs-lookup"><span data-stu-id="8cf4e-130">To turn off integration, set the option to **No**.</span></span>

<span data-ttu-id="8cf4e-131">[![Aktivere eller deaktivere Dataverse-integrering](./media/hr-admin-integration-dataverse-enable-disable.png)](./media/hr-admin-integration-dataverse-enable-disable.png)</span><span class="sxs-lookup"><span data-stu-id="8cf4e-131">[![Turning the Dataverse integration on or off](./media/hr-admin-integration-dataverse-enable-disable.png)](./media/hr-admin-integration-dataverse-enable-disable.png)</span></span>

> [!WARNING]
> <span data-ttu-id="8cf4e-132">Vi anbefaler sterkt at du deaktiverer Dataverse-integrering mens du utfører datamigreringsoppgaver.</span><span class="sxs-lookup"><span data-stu-id="8cf4e-132">We strongly recommend turning off Dataverse integration while performing data migration tasks.</span></span> <span data-ttu-id="8cf4e-133">Store dataopplastinger kan påvirke ytelsen betydelig.</span><span class="sxs-lookup"><span data-stu-id="8cf4e-133">Large data uploads can significantly impact performance.</span></span> <span data-ttu-id="8cf4e-134">Eksempel: Opplasting av 2000 arbeidere kan ta flere timer når integrering er aktivert, og mindre enn én time når den er deaktivert.</span><span class="sxs-lookup"><span data-stu-id="8cf4e-134">For example, uploading 2000 workers can take several hours when integration is enabled, and less than one hour when it's disabled.</span></span> <span data-ttu-id="8cf4e-135">Tallene i dette eksemplet er bare for demonstrasjon.</span><span class="sxs-lookup"><span data-stu-id="8cf4e-135">The numbers provided in this example are for demonstration purposes only.</span></span> <span data-ttu-id="8cf4e-136">Den nøyaktige tiden det tar å importere poster, kan variere betraktelig, avhengig av mange faktorer.</span><span class="sxs-lookup"><span data-stu-id="8cf4e-136">The exact amount of time it takes to import records can vary greatly based on many factors.</span></span>

## <a name="view-data-integration-details"></a><span data-ttu-id="8cf4e-137">Vise detaljer om dataintegrering</span><span class="sxs-lookup"><span data-stu-id="8cf4e-137">View data integration details</span></span>

<span data-ttu-id="8cf4e-138">På hurtigfanen **Administrasjon** på siden **Microsoft Dataverse-integrering** kan du se hvordan rader kobles sammen mellom Human Resources og Dataverse.</span><span class="sxs-lookup"><span data-stu-id="8cf4e-138">On the **Administration** FastTab of the **Microsoft Dataverse integration** page, you can see how rows are linked together between Human Resources and Dataverse.</span></span>

- <span data-ttu-id="8cf4e-139">Hvis du vil vise radene for en tabell, velger du tabellen i **Dataverse-tabell**-feltet.</span><span class="sxs-lookup"><span data-stu-id="8cf4e-139">To view the rows for a table, select the table in the **Dataverse table** field.</span></span> <span data-ttu-id="8cf4e-140">I rutenettet vises alle radene som er koblet til den valgte tabellen.</span><span class="sxs-lookup"><span data-stu-id="8cf4e-140">The grid shows all the rows that are linked to the selected table.</span></span>

> [!NOTE]
> <span data-ttu-id="8cf4e-141">Ikke alle Dataverse-tabeller er oppført i listen.</span><span class="sxs-lookup"><span data-stu-id="8cf4e-141">Not all Dataverse tables are currently listed.</span></span> <span data-ttu-id="8cf4e-142">Bare tabeller som støtter bruk av egendefinerte felt, vises i rutenettet.</span><span class="sxs-lookup"><span data-stu-id="8cf4e-142">Only tables that support the use of custom fields appear in the grid.</span></span> <span data-ttu-id="8cf4e-143">Nye tabeller blir tilgjengelige via kontinuerlige utgivelser av Human Resources.</span><span class="sxs-lookup"><span data-stu-id="8cf4e-143">New tables become available through continuous releases of Human Resources.</span></span>

<span data-ttu-id="8cf4e-144">Rutenettet inneholder følgende felt:</span><span class="sxs-lookup"><span data-stu-id="8cf4e-144">The grid includes the following fields:</span></span>

- <span data-ttu-id="8cf4e-145">**Dataverse-tabell** – Navnet på tabellen i Dataverse.</span><span class="sxs-lookup"><span data-stu-id="8cf4e-145">**Dataverse table** – The name of the table in Dataverse.</span></span>
- <span data-ttu-id="8cf4e-146">**Dataverse-tabellreferanse** – Identifikatoren som Dataverse bruker til å identifisere en post.</span><span class="sxs-lookup"><span data-stu-id="8cf4e-146">**Dataverse table reference** – The identifier that Dataverse uses to identify a record.</span></span> <span data-ttu-id="8cf4e-147">Denne verdien tilsvarer en **RecId**-verdi for Human Resources.</span><span class="sxs-lookup"><span data-stu-id="8cf4e-147">This value is equivalent to a Human Resources **RecId** value.</span></span> <span data-ttu-id="8cf4e-148">Du kan finne identifikatoren når du åpner Dataverse-tabellen i Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="8cf4e-148">You can find the identifier when you open the Dataverse table in Microsoft Excel.</span></span>
- <span data-ttu-id="8cf4e-149">**Navn på Human Resource-enhet** – Human Resources-enheten som sist synkroniserte data til Dataverse.</span><span class="sxs-lookup"><span data-stu-id="8cf4e-149">**Human Resources entity name** – The Human Resources entity that last synced data to Dataverse.</span></span> <span data-ttu-id="8cf4e-150">Enheten kan ha Dataverse-prefikset eller et annet prefiks.</span><span class="sxs-lookup"><span data-stu-id="8cf4e-150">The entity can have either the Dataverse prefix or another prefix.</span></span>
- <span data-ttu-id="8cf4e-151">**Personalreferanse** – **RecId**-verdien som er knyttet til posten i Human Resources.</span><span class="sxs-lookup"><span data-stu-id="8cf4e-151">**Human Resources reference** – The **RecId** value that is associated with the record in Human Resources.</span></span>
- <span data-ttu-id="8cf4e-152">**Slettet fra Dataverse** – En verdi som indikerer om raden ble slettet fra Dataverse.</span><span class="sxs-lookup"><span data-stu-id="8cf4e-152">**Deleted from Dataverse** – A value that indicates whether the row was deleted from Dataverse.</span></span>

> [!NOTE]
> <span data-ttu-id="8cf4e-153">Poster i Human Resources tilsvarer rader i Dataverse.</span><span class="sxs-lookup"><span data-stu-id="8cf4e-153">Records in Human Resources correspond to rows in Dataverse.</span></span>

## <a name="remove-the-association-of-a-human-resources-record-from-a-dataverse-row"></a><span data-ttu-id="8cf4e-154">Fjerne tilknytningen til en Human Resources-post fra en Dataverse-rad</span><span class="sxs-lookup"><span data-stu-id="8cf4e-154">Remove the association of a Human Resources record from a Dataverse row</span></span>

<span data-ttu-id="8cf4e-155">Hvis det oppstår problemer under datasynkronisering mellom Human Resources og Dataverse, kan det hende at du kan løse dem ved å fjerne sporingen og la sporingstabellen synkroniseres på nytt.</span><span class="sxs-lookup"><span data-stu-id="8cf4e-155">If you experience issues during data synchronization between Human Resources and Dataverse, you might be able to resolve them by clearing the tracking and letting the tracking table be resynced.</span></span> <span data-ttu-id="8cf4e-156">Hvis du fjerner tilknytningen og deretter endrer eller sletter en rad i Dataverse, blir ikke endringene synkronisert med Human Resources.</span><span class="sxs-lookup"><span data-stu-id="8cf4e-156">If you remove the association, and then change or delete a row in Dataverse, the changes won't be synced to Human Resources.</span></span> <span data-ttu-id="8cf4e-157">Hvis du utfører endringer i Human Resources, opprettes det en ny sporingspost, og raden oppdateres i Dataverse.</span><span class="sxs-lookup"><span data-stu-id="8cf4e-157">If you make changes in Human Resources, a new tracking record is created, and the row is updated in Dataverse.</span></span>

- <span data-ttu-id="8cf4e-158">Hvis du vil fjerne tilknytningen mellom en Human Resources-post og en Dataverse-rad, velger du tabellen i feltet **Dataverse-tabell**, og deretter velger du **Fjern sporingsinformasjon**.</span><span class="sxs-lookup"><span data-stu-id="8cf4e-158">To remove the association of a Human Resources record and a Dataverse row, select the table in the **Dataverse table** field, and then select **Clear tracking information**.</span></span>

<span data-ttu-id="8cf4e-159">[![Fjerne sporingsinformasjon](./media/hr-admin-integration-dataverse-clear-tracking.png)](./media/hr-admin-integration-dataverse-clear-tracking.png)</span><span class="sxs-lookup"><span data-stu-id="8cf4e-159">[![Clearing tracking information](./media/hr-admin-integration-dataverse-clear-tracking.png)](./media/hr-admin-integration-dataverse-clear-tracking.png)</span></span>

<span data-ttu-id="8cf4e-160">Hvis du vil kjøre en fullstendig synkronisering med tabellen etter at du har fjernet sporingen, kan du se neste prosedyre.</span><span class="sxs-lookup"><span data-stu-id="8cf4e-160">To run a full synchronization on the table after you clear the tracking, see the next procedure.</span></span>

## <a name="sync-a-table-between-human-resources-and-dataverse"></a><span data-ttu-id="8cf4e-161">Synkronisere en tabell mellom Human Resources og Dataverse</span><span class="sxs-lookup"><span data-stu-id="8cf4e-161">Sync a table between Human Resources and Dataverse</span></span>

<span data-ttu-id="8cf4e-162">Bruk denne fremgangsmåten når:</span><span class="sxs-lookup"><span data-stu-id="8cf4e-162">Use this procedure when:</span></span>

- <span data-ttu-id="8cf4e-163">Det tar for lang tid å vise endringer fra Dataverse i Human Resources.</span><span class="sxs-lookup"><span data-stu-id="8cf4e-163">Changes from Dataverse take too long to appear in Human Resources.</span></span>

- <span data-ttu-id="8cf4e-164">Du må oppdatere sporingstabellen etter at du har fjernet sporingen.</span><span class="sxs-lookup"><span data-stu-id="8cf4e-164">You must refresh the tracking table after clearing the tracking.</span></span>

<span data-ttu-id="8cf4e-165">Slik kjører du en fullstendig synkronisering av en tabell mellom Human Resources og Dataverse:</span><span class="sxs-lookup"><span data-stu-id="8cf4e-165">To run a full synchronization on a table between Human Resources and Dataverse:</span></span>

1. <span data-ttu-id="8cf4e-166">Velg tabellen i feltet **Dataverse-tabell**.</span><span class="sxs-lookup"><span data-stu-id="8cf4e-166">Select the table in the **Dataverse table** field.</span></span>

2. <span data-ttu-id="8cf4e-167">Velg **Synkroniser nå**.</span><span class="sxs-lookup"><span data-stu-id="8cf4e-167">Select **Sync now**.</span></span>

<span data-ttu-id="8cf4e-168">[![Kjøre en full synkronisering](./media/hr-admin-integration-dataverse-sync-now.png)](./media/hr-admin-integration-dataverse-sync-now.png)</span><span class="sxs-lookup"><span data-stu-id="8cf4e-168">[![Running a full synchronization](./media/hr-admin-integration-dataverse-sync-now.png)](./media/hr-admin-integration-dataverse-sync-now.png)</span></span>

## <a name="see-also"></a><span data-ttu-id="8cf4e-169">Se også</span><span class="sxs-lookup"><span data-stu-id="8cf4e-169">See also</span></span>

[<span data-ttu-id="8cf4e-170">Dataverse-tabeller</span><span class="sxs-lookup"><span data-stu-id="8cf4e-170">Dataverse tables</span></span>](hr-developer-entities.md)<br>
[<span data-ttu-id="8cf4e-171">Konfigurere virtuelle Dataverse-tabeller</span><span class="sxs-lookup"><span data-stu-id="8cf4e-171">Configure Dataverse virtual tables</span></span>](hr-admin-integration-common-data-service-virtual-entities.md)<br>
[<span data-ttu-id="8cf4e-172">Vanlige spørsmål om virtuelle tabeller for Human Resources</span><span class="sxs-lookup"><span data-stu-id="8cf4e-172">Human Resources virtual tables FAQ</span></span>](hr-admin-virtual-entity-faq.md)<br>
[<span data-ttu-id="8cf4e-173">Hva er Microsoft Dataverse?</span><span class="sxs-lookup"><span data-stu-id="8cf4e-173">What is Microsoft Dataverse?</span></span>](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro)<br>
[<span data-ttu-id="8cf4e-174">Terminologioppdateringer</span><span class="sxs-lookup"><span data-stu-id="8cf4e-174">Terminology updates</span></span>](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro#terminology-updates)
