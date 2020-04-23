---
title: Vedlikeholdsrunder
description: Dette emnet beskriver vedlikeholdsrunder i Aktivastyring.
author: josaw1
manager: tfehr
ms.date: 08/27/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 97f1984b71ab60519f81bb1f6ab38278a0e5aa43
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/02/2020
ms.locfileid: "3206110"
---
# <a name="maintenance-rounds"></a><span data-ttu-id="54300-103">Vedlikeholdsrunder</span><span class="sxs-lookup"><span data-stu-id="54300-103">Maintenance rounds</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="54300-104">I **Aktivastyring** kan du opprette vedlikeholdsrunder for ulike aktiva, der du må utføre en lignende oppgave med jevne mellomrom.</span><span class="sxs-lookup"><span data-stu-id="54300-104">In **Asset Management**, you can create maintenance rounds for various assets, on which you need to carry out a similar task at regular intervals.</span></span> <span data-ttu-id="54300-105">For eksempel smørejobber eller sikkerhetsinspeksjonsjobber som må utføres på flere maskiner i samme intervall.</span><span class="sxs-lookup"><span data-stu-id="54300-105">For example, lubrication jobs or safety inspection jobs that need to be carried out on a number of machines within the same intervals.</span></span> <span data-ttu-id="54300-106">Første trinn er å opprette en vedlikeholdsrunde, inkludert aktiva som krever samme form for vedlikeholdsjobb.</span><span class="sxs-lookup"><span data-stu-id="54300-106">First step is to create a maintenance round, including assets that require the same form of maintenance job.</span></span> <span data-ttu-id="54300-107">Deretter planlegger du vedlikeholdsrundene.</span><span class="sxs-lookup"><span data-stu-id="54300-107">Next, you schedule the maintenance rounds.</span></span> <span data-ttu-id="54300-108">Når du har fullført vedlikeholdsrundeplanen, kan du se alle jobbpostene knyttet til runden i **Alle vedlikeholdsplaner** og **Åpne vedlikeholdsplanlinjer**.</span><span class="sxs-lookup"><span data-stu-id="54300-108">When you have completed the maintenance rounds schedule, you can see all the job records relating to the round in the **All maintenance schedule** and **Open maintenance schedule lines**.</span></span>

>[!NOTE]
><span data-ttu-id="54300-109">Vedlikeholdsrunder kan også defineres på arbeidssteder, som skal fullføres for aktivaene på arbeidsstedet når den rundebaserte arbeidsordren opprettes.</span><span class="sxs-lookup"><span data-stu-id="54300-109">Maintenance rounds can also be set up on functional locations to be completed on the assets installed on the functional location at the time of creation of the round-based work order.</span></span> <span data-ttu-id="54300-110">Se [Opprette arbeidssteder](../functional-locations/create-functional-locations.md) hvis du vil ha mer informasjon om oppsettet av vedlikeholdsrunder på arbeidssteder.</span><span class="sxs-lookup"><span data-stu-id="54300-110">Refer to [Create functional locations](../functional-locations/create-functional-locations.md) for more information on the setup of maintenance rounds on functional locations.</span></span>

## <a name="set-up-a-maintenance-round"></a><span data-ttu-id="54300-111">Sette opp en vedlikeholdsrunde</span><span class="sxs-lookup"><span data-stu-id="54300-111">Set up a maintenance round</span></span>

1. <span data-ttu-id="54300-112">Klikk på **Aktivastyring** > **Oppsett** > **Forebyggende vedlikehold** > **Vedlikeholdsrunder**.</span><span class="sxs-lookup"><span data-stu-id="54300-112">Click **Asset management** > **Setup** > **Preventive maintenance** > **Maintenance rounds**.</span></span>

2. <span data-ttu-id="54300-113">Klikk på **Ny** for å opprette en ny vedlikeholdsrunde.</span><span class="sxs-lookup"><span data-stu-id="54300-113">Click **New** to create a new maintenance round.</span></span>

3. <span data-ttu-id="54300-114">Sett inn en ID i **Vedlikeholdsrunde**-feltet og et navn på vedlikeholdsrunden i **Navn**-feltet.</span><span class="sxs-lookup"><span data-stu-id="54300-114">Insert and ID in the **Maintenance round** field, and a name for the maintenance round in the **Name** field.</span></span>

4. <span data-ttu-id="54300-115">Velg en startdato for runden i **Startdato**-feltet.</span><span class="sxs-lookup"><span data-stu-id="54300-115">Select a start date for the round in the **Start date** field.</span></span>

5. <span data-ttu-id="54300-116">I feltene **Fullfør innen dager** og **Fullfør innen timer** kan du sette inn forventet sluttdato i dager eller timer.</span><span class="sxs-lookup"><span data-stu-id="54300-116">In the **Finish within days** and **Finish within hours** fields, you can insert expected end date in days or hours.</span></span> <span data-ttu-id="54300-117">Den forventede sluttdatoen beregnes i forhold til startdatoen, som beregnes når vedlikeholdsplanlinjer opprettes.</span><span class="sxs-lookup"><span data-stu-id="54300-117">The expected end date is calculated relative to the start date, which is calculated when maintenance schedule lines are created.</span></span> <span data-ttu-id="54300-118">Du kan for eksempel sette inn 7 i feltet **Fullfør innen dager** for å angi at den tilknyttede jobben skal fullføres innen en uke fra startdatoen.</span><span class="sxs-lookup"><span data-stu-id="54300-118">For example, you can insert "7" in the **Finish within days** field to indicate that the related job should be completed within a week from the start date.</span></span>

6. <span data-ttu-id="54300-119">Velg Ja på **Opprett automatisk**-veksleknappen hvis arbeidsordrer skal opprettes automatisk fra vedlikeholdsplanlinjer som er opprettet fra vedlikeholdsrunden.</span><span class="sxs-lookup"><span data-stu-id="54300-119">Select "Yes" on the **Auto create** toggle button if work orders should automatically be created from maintenance schedule lines that are created from this maintenance round.</span></span>

7. <span data-ttu-id="54300-120">I **Arbeidsordretype**-feltet velger du arbeidsordretypen som skal brukes på arbeidsordrer som opprettes fra denne vedlikeholdsrunden.</span><span class="sxs-lookup"><span data-stu-id="54300-120">In the **Work order type** field, select the work order type to be used on work orders created from this maintenance round.</span></span>

8. <span data-ttu-id="54300-121">I **Servicenivå**-feltet velger du arbeidsordreservicenivået som skal brukes på arbeidsordrer som opprettes fra denne vedlikeholdsrunden.</span><span class="sxs-lookup"><span data-stu-id="54300-121">In the **Service level** field, select the work order service level to be used on work orders created from this maintenance round.</span></span>

9. <span data-ttu-id="54300-122">I hurtigfanen **Aktivalinjer** klikker du på **Legg til** for å legge til et aktivum i vedlikeholdsrunden.</span><span class="sxs-lookup"><span data-stu-id="54300-122">On the **Asset lines** FastTab, click **Add** to add an asset to the maintenance round.</span></span>

10. <span data-ttu-id="54300-123">Et linjenummer settes inn automatisk i **Linjenummer**-feltet for å angi rekkefølgen på aktivaene i vedlikeholdsrunden.</span><span class="sxs-lookup"><span data-stu-id="54300-123">A line number is automatically inserted in the **Line number** field to indicate the sequence of the assets in maintenance round.</span></span>

11. <span data-ttu-id="54300-124">Velg aktivaet i **Aktivum**-feltet.</span><span class="sxs-lookup"><span data-stu-id="54300-124">Select the asset in the **Asset** field.</span></span>

12. <span data-ttu-id="54300-125">Velg vedlikeholdsjobbtypen for aktivaet i **Vedlikeholdsjobbtype**-feltet.</span><span class="sxs-lookup"><span data-stu-id="54300-125">Select the maintenance job type for the asset in the **Maintenance job type** field.</span></span>

13. <span data-ttu-id="54300-126">Velg om nødvendig **Variant av vedlikeholdsjobbtype** og **Handel** som er knyttet til vedlikeholdsjobbtypen.</span><span class="sxs-lookup"><span data-stu-id="54300-126">If required, select **Maintenance job typ variant** and **Trade** related to the maintenance job type.</span></span>

14. <span data-ttu-id="54300-127">Velg gjentakelse (dag, uke osv.) i **Periodetype**-feltet.</span><span class="sxs-lookup"><span data-stu-id="54300-127">Select the recurrence (day, week, etc.) in the **Period type** field.</span></span>

15. <span data-ttu-id="54300-128">I **Periodefrekvens**-feltet setter du inn antall gjentakelser for vedlikeholdsrunden.</span><span class="sxs-lookup"><span data-stu-id="54300-128">In the **Period frequency** field, insert the number of recurrences for the maintenance round.</span></span> <span data-ttu-id="54300-129">Eksempel: Hvis du har valgt Dag i feltet **Periodetype**, og du setter inn tallet 7 i dette feltet, opprettes det nye vedlikeholdsrundelinjer under forebyggende vedlikeholdsplanlegging én gang i uken.</span><span class="sxs-lookup"><span data-stu-id="54300-129">Example: If you have selected "Day" in the **Period type** field, and you insert the number "7" in this field, new maintenance round lines are created during preventive maintenance scheduling once a week.</span></span>

16. <span data-ttu-id="54300-130">Velg en startdato for aktivaet som skal inkluderes i vedlikeholdsrunden, i **Startdato**-feltet.</span><span class="sxs-lookup"><span data-stu-id="54300-130">Select a start date for the asset to be included in the maintenance round in the **Start date** field.</span></span> <span data-ttu-id="54300-131">Denne datoen kan være forskjellig fra startdatoen som er angitt i vedlikeholdsrunden.</span><span class="sxs-lookup"><span data-stu-id="54300-131">This date may differ from the start date set on the maintenance round.</span></span>

17. <span data-ttu-id="54300-132">Gjenta trinn 9–16 for å legge til flere aktiva i vedlikeholdsrunden.</span><span class="sxs-lookup"><span data-stu-id="54300-132">Repeat steps 9-16 to add more assets to the maintenance round.</span></span>

18. <span data-ttu-id="54300-133">I hurtigfanen **Arbeidsstedslinjer** klikker du på **Legg til** for å legge til et arbeidssted i vedlikeholdsrunden.</span><span class="sxs-lookup"><span data-stu-id="54300-133">On the **Functional location lines** FastTab, click **Add** to add a functional location to the maintenance round.</span></span> <span data-ttu-id="54300-134">Se beskrivelsen for de relaterte feltene ovenfor.</span><span class="sxs-lookup"><span data-stu-id="54300-134">Refer to the description of the related fields above.</span></span> <span data-ttu-id="54300-135">De samme feltene er tilgjengelige som for å opprette en aktivalinje, men du kan også velge **Produsent** og **Modell** for et arbeidssted, om nødvendig.</span><span class="sxs-lookup"><span data-stu-id="54300-135">The same fields are available as for creating an asset line, but you can also select **Manufacturer** and **Model** for a functional location, if required.</span></span> <span data-ttu-id="54300-136">Hvis du bare velger et arbeidssted på en linje, men ikke gjør noen valg i **Aktivatype**, **Produsent**, **Modell**, **Vedlikeholdsjobbtype**, **Variant av vedlikeholdsjobbtype** og **Handel**, vil alle aktiva som er knyttet til dette arbeidsstedet på tidspunktet for vedlikeholdsplanlegging, bli inkludert i vedlikeholdsrunden.</span><span class="sxs-lookup"><span data-stu-id="54300-136">If you only select a functional location on a line, but make no selections in **Asset type**, **Manufacturer**, **Model**, **Maintenance job type**, **Maintenance job type variant** and **Trade**, all assets related to that functional location at the time of maintenance scheduling will be included in the maintenance round.</span></span>

19. <span data-ttu-id="54300-137">Klikk på **Legg til** i hurtigfanen **Puljer** for å velge en arbeidsordrepulje som skal tas med i vedlikeholdsrunden.</span><span class="sxs-lookup"><span data-stu-id="54300-137">On the **Pools** FastTab, click **Add** to select a work order pool to be included in the maintenance round.</span></span> <span data-ttu-id="54300-138">Flere arbeidsordrepuljer kan kobles til én vedlikeholdsrunde.</span><span class="sxs-lookup"><span data-stu-id="54300-138">Several work order pools can be connected to one maintenance round.</span></span>

20. <span data-ttu-id="54300-139">Lagre oppsettet.</span><span class="sxs-lookup"><span data-stu-id="54300-139">Save your setup.</span></span>

>[!NOTE]
><span data-ttu-id="54300-140">Feltene **Aktiva** og **Linjer** i **Detaljer**-gruppen i hurtigfanen **Hode** viser antall aktiva og linjer knyttet til den valgte vedlikeholdsrunden.</span><span class="sxs-lookup"><span data-stu-id="54300-140">The **Assets** and **Lines** fields located in the **Details** group on the **Header** FastTab show the total number of assets and lines related to the selected maintenance round.</span></span>

<span data-ttu-id="54300-141">Illustrasjonen nedenfor viser et eksempel på en vedlikeholdsrunding som inneholder tre aktiva.</span><span class="sxs-lookup"><span data-stu-id="54300-141">The illustration below shows and example of a maintenance round containing three assets.</span></span>

![Figur 1](media/13-preventive-maintenance.png)


## <a name="schedule-maintenance-rounds"></a><span data-ttu-id="54300-143">Planlegg vedlikeholdsrunder</span><span class="sxs-lookup"><span data-stu-id="54300-143">Schedule maintenance rounds</span></span>

<span data-ttu-id="54300-144">Når du har definert en vedlikeholdsrunde, kjører du en planleggingsjobb for å planlegge alle jobbene som er knyttet til vedlikeholdsrunden.</span><span class="sxs-lookup"><span data-stu-id="54300-144">When you've set up a maintenance round, you run a schedule job to schedule all the jobs related to the maintenance round.</span></span>

1. <span data-ttu-id="54300-145">Klikk på **Aktivastyring** > **Periodisk** > **Forebyggende vedlikehold** > **Planlegg vedlikeholdsrunder**, eller **Aktivastyring** > **Felles** > **Vedlikeholdsplan** > **Alle vedlikeholdsplaner** eller **Åpne vedlikeholdsplanlinjer** eller **Åpne vedlikeholdsplanpuljer** > velg vedlikeholdsplanlinje i listen > **Vedlikeholdsrunder**-knappen.</span><span class="sxs-lookup"><span data-stu-id="54300-145">Click **Asset management** > **Periodic** > **Preventive maintenance** > **Schedule maintenance rounds**, or **Asset management** > **Common** > **Maintenance schedule** > **All maintenance schedule** or **Open maintenance schedule lines** or **Open maintenance schedule pools** > select maintenance schedule line in the list > **Maintenance rounds** button.</span></span>

2. <span data-ttu-id="54300-146">I feltet **Periode** velger du periodetypen som skal brukes for planleggingsjobben.</span><span class="sxs-lookup"><span data-stu-id="54300-146">In the **Period** field, select the period type to be used for the scheduling job.</span></span>

3. <span data-ttu-id="54300-147">I **Periodefrekvens**-feltet setter du inn antall perioder som skal være med i planleggingsjobben.</span><span class="sxs-lookup"><span data-stu-id="54300-147">In the **Period frequency** field, insert the number of periods to be included in the scheduling job.</span></span> <span data-ttu-id="54300-148">Starten på planleggingen er gjeldende dato.</span><span class="sxs-lookup"><span data-stu-id="54300-148">The start of the scheduling is the current date.</span></span>

4. <span data-ttu-id="54300-149">Velg Ja på veksleknappen **Opprett automatisk** hvis det automatisk skal opprettes en arbeidsordre på grunnlag av en vedlikeholdsrunde.</span><span class="sxs-lookup"><span data-stu-id="54300-149">Select "Yes" on the **Auto create** toggle button if a work order should automatically be created on the basis of a maintenance round.</span></span>

>[!NOTE]
><span data-ttu-id="54300-150">Hvis denne veksleknappen er satt til Ja, og veksleknappen **Opprett automatisk** også er satt til Ja for vedlikeholdsrunden i **Vedlikeholdsrunder**-skjemaet, opprettes arbeidsordrer på grunnlag av vedlikeholdsrundelinjene, og vedlikeholdsplanlinjer med statusen "Arbeidsordre opprettet" opprettes også.</span><span class="sxs-lookup"><span data-stu-id="54300-150">If this toggle button is set to "Yes", and the **Auto create** toggle button is also set to "Yes" on the maintenance round in **Maintenance rounds** form, work orders are created based on the maintenance round lines, and maintenance schedule lines with status "Work order created" are also created.</span></span> <span data-ttu-id="54300-151">Hvis bare en av **Opprett automatisk**-veksleknappene er satt til Ja, i denne rullegardinlisten eller i **Vedlikeholdsrunder**, blir bare vedlikeholdsplanlinjer opprettet med statusen "Opprettet".</span><span class="sxs-lookup"><span data-stu-id="54300-151">If only one of the **Auto create** toggle buttons is set to "Yes", in this drop-down or in **Maintenance rounds**, only maintenance schedule lines are created with status "Created".</span></span> <span data-ttu-id="54300-152">I dette tilfellet opprettes ingen arbeidsordrer.</span><span class="sxs-lookup"><span data-stu-id="54300-152">In that case, no work orders are created.</span></span>

5. <span data-ttu-id="54300-153">Hvis nødvendig, kan du velge bestemte runder eller en annen startdato for planleggingsjobben.</span><span class="sxs-lookup"><span data-stu-id="54300-153">If required, you can select specific rounds or another start date for the schedule job.</span></span> <span data-ttu-id="54300-154">Klikk på **Filter**, og legg til rundene som skal tas med.</span><span class="sxs-lookup"><span data-stu-id="54300-154">Click **Filter**, and add the rounds to be included.</span></span>

6. <span data-ttu-id="54300-155">Klikk **OK**.</span><span class="sxs-lookup"><span data-stu-id="54300-155">Click **OK**.</span></span>

7. <span data-ttu-id="54300-156">Du kan nå vise vedlikeholdsrundejobbene i **Aktivastyring** > **Felles** > **Vedlikeholdsplan** > **Alle vedlikeholdsplaner** eller **Åpne vedlikeholdsplanlinjer**.</span><span class="sxs-lookup"><span data-stu-id="54300-156">You are now able to see the maintenance rounds jobs in **Asset management** > **Common** > **Maintenance schedule** > **All maintenance schedule** or **Open maintenance schedule lines**.</span></span> <span data-ttu-id="54300-157">Hvis de planlagte runden er koblet til en arbeidsordrepulje, kan du også se vedlikeholdsplanlinjer i **Åpne vedlikeholdsplanpuljer**.</span><span class="sxs-lookup"><span data-stu-id="54300-157">If the scheduled rounds are connected to a work order pool, you also see maintenance schedule lines in **Open maintenance schedule pools**.</span></span> <span data-ttu-id="54300-158">Vedlikeholdsplanlinjer som er opprettet fra en runde, har referansetypen Vedlikeholdsrunder.</span><span class="sxs-lookup"><span data-stu-id="54300-158">Maintenance schedule lines created from a round have the reference type "Maintenance rounds".</span></span>

<span data-ttu-id="54300-159">De to illustrasjonene nedenfor viser en planlagt jobb dialogboksen **Planlegg vedlikeholdsrunder** og linjer for vedlikeholdsplan som er opprettet i **Alle vedlikeholdsplaner**, som er basert på den planlagte jobben.</span><span class="sxs-lookup"><span data-stu-id="54300-159">The two illustrations below show a schedule job in the **Schedule maintenance rounds** dialog, and the maintenance schedule lines created in **All maintenance schedule** based on that schedule job.</span></span>

![Figur 2](media/14-preventive-maintenance.png)

![Figur 3](media/15-preventive-maintenance.png)

- <span data-ttu-id="54300-162">Når arbeidsordrer opprettes manuelt for aktiva som dekkes av en leverandørgaranti, vises en dialogboks for å gjøre brukeren oppmerksom på garantien.</span><span class="sxs-lookup"><span data-stu-id="54300-162">When work orders are manually created on assets that are covered by a vendor warranty, a dialog box is shown to make the user aware of the warranty.</span></span> <span data-ttu-id="54300-163">Opprettingen av arbeidsordren kan deretter avbrytes.</span><span class="sxs-lookup"><span data-stu-id="54300-163">The creation of the work order can then be canceled.</span></span> <span data-ttu-id="54300-164">Kontrollen av en garantirelasjon utelates for arbeidsordrer som opprettes automatisk.</span><span class="sxs-lookup"><span data-stu-id="54300-164">The check for a warranty relation is omitted for work orders that are automatically created.</span></span>  
- <span data-ttu-id="54300-165">Du kan sette opp en satsvis jobb i hurtigfanen **Kjør i bakgrunnen** for å planlegge runder med jevne mellomrom.</span><span class="sxs-lookup"><span data-stu-id="54300-165">You can set up a batch job on the **Run in the background** FastTab to schedule rounds at regular intervals.</span></span>  
- <span data-ttu-id="54300-166">Hvis en runde er inkludert i flere arbeidsordrepuljer (se [Arbeidsordrepuljer](../work-orders/work-order-pools.md)), vises én post for hver pulje i **Åpne vedlikeholdsplanpuljer**.</span><span class="sxs-lookup"><span data-stu-id="54300-166">If a round is included in several work order pools (refer to [Work order pools](../work-orders/work-order-pools.md)), one record is shown for each pool in **Open maintenance schedule pools**.</span></span> <span data-ttu-id="54300-167">Dette gjøres for å optimalisere filtreringsalternativene for arbeidsordrepuljer.</span><span class="sxs-lookup"><span data-stu-id="54300-167">This is done to optimize the filtering options for work order pools.</span></span>

