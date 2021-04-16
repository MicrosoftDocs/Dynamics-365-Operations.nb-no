---
title: Identifisere og løse konflikter i arbeidsdeling
description: Dette emnet forklarer hvordan du identifiserer og løser konflikter i arbeidsdelinger.
author: peakerbl
ms.date: 01/04/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysSecSegregationOfDutiesConflict, SysSecSegregationOfDutiesRule
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0ebd59c7018a50e01253697d792698664a981566
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745819"
---
# <a name="identify-and-resolve-conflicts-in-segregation-of-duties"></a><span data-ttu-id="69963-103">Identifisere og løse konflikter i arbeidsdeling</span><span class="sxs-lookup"><span data-stu-id="69963-103">Identify and resolve conflicts in segregation of duties</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="69963-104">Dette emnet forklarer hvordan du identifiserer og løser konflikter i arbeidsdelinger.</span><span class="sxs-lookup"><span data-stu-id="69963-104">This topic explains how to identify and resolve conflicts in segregation of duties.</span></span> <span data-ttu-id="69963-105">Du kan definere regler for å skille plikter som må utføres av forskjellige brukere.</span><span class="sxs-lookup"><span data-stu-id="69963-105">You can set up rules to separate duties that must be performed by different users.</span></span> <span data-ttu-id="69963-106">Dette konseptet kalles arbeidsdeling.</span><span class="sxs-lookup"><span data-stu-id="69963-106">This concept is named segregation of duties.</span></span> <span data-ttu-id="69963-107">Når definisjonen av en sikkerhetsrolle eller rolletildelingene til en bruker bryter reglene, logges konflikten.</span><span class="sxs-lookup"><span data-stu-id="69963-107">When the definition of a security role or the role assignments of a user violate the rules, the conflict is logged.</span></span> <span data-ttu-id="69963-108">Alle konflikter må løses av administratoren.</span><span class="sxs-lookup"><span data-stu-id="69963-108">All conflicts must be resolved by the administrator.</span></span> <span data-ttu-id="69963-109">Fullfør fremgangsmåten nedenfor for å identifisere og løse konflikter.</span><span class="sxs-lookup"><span data-stu-id="69963-109">Complete the following procedure to identify and resolve conflicts.</span></span>

<span data-ttu-id="69963-110">Etter at en regel er lagt til, kontrollerer du at alle eksisterende roller samsvarer med reglene.</span><span class="sxs-lookup"><span data-stu-id="69963-110">After a rule has been added, verify that all existing roles are compliant.</span></span> 

## <a name="verify-that-existing-roles-and-duties-comply-with-new-rules-for-segregation-of-duties"></a><span data-ttu-id="69963-111">Kontrollere at eksisterende roller og plikter følger nye regler for arbeidsdeling</span><span class="sxs-lookup"><span data-stu-id="69963-111">Verify that existing roles and duties comply with new rules for segregation of duties</span></span>
1. <span data-ttu-id="69963-112">Gå til **Systemadministrasjon** > **Sikkerhet** > **Arbeidsdeling** > **Arbeidsdelingsregler**.</span><span class="sxs-lookup"><span data-stu-id="69963-112">Go to **System administration** > **Security** > **Segregation of duties** > **Segregation of duties rules**.</span></span>
3. <span data-ttu-id="69963-113">Velg **Valider plikter og roller**.</span><span class="sxs-lookup"><span data-stu-id="69963-113">Select **Validate duties and roles**.</span></span> <span data-ttu-id="69963-114">Hvis en rolle bryter reglene, vises en melding som inneholder navnet på regelen og rollen og navnene på pliktene som er i konflikt med hverandre.</span><span class="sxs-lookup"><span data-stu-id="69963-114">If any roles violate the rules, a message is displayed that contains the name of the rule, the role, and the names of the conflicting duties.</span></span> <span data-ttu-id="69963-115">Roller i konflikt må endres ved hjelp av **Sikkerhetskonfigurasjon** og kan ikke inneholde plikter i konflikt.</span><span class="sxs-lookup"><span data-stu-id="69963-115">Conflicting roles must be modified using **Security configuration** and can't include conflicting duties.</span></span> <span data-ttu-id="69963-116">Hvis ingen roller bryter en valgt regel, får du en melding som angir at alle roller er i samsvar.</span><span class="sxs-lookup"><span data-stu-id="69963-116">If no roles violate the selected rule, a message indicates that all roles comply.</span></span>   

> [!NOTE]
> <span data-ttu-id="69963-117">Valideringen utføres bare for den valgte regelen.</span><span class="sxs-lookup"><span data-stu-id="69963-117">The validation is only performed for the selected rule.</span></span> <span data-ttu-id="69963-118">Det er viktig å validere samsvar for hver regel.</span><span class="sxs-lookup"><span data-stu-id="69963-118">It is important to validate compliance for each rule.</span></span>   

<span data-ttu-id="69963-119">Når du oppretter eller endrer en rolle, blir reglene for arbeidsdeling håndhevet automatisk.</span><span class="sxs-lookup"><span data-stu-id="69963-119">When you create or modify a role, the rules for segregation of duties are automatically enforced.</span></span> <span data-ttu-id="69963-120">Du kan ikke tilordne plikter i konflikt til en rolle.</span><span class="sxs-lookup"><span data-stu-id="69963-120">You cannot assign conflicting duties to a role.</span></span>

<span data-ttu-id="69963-121">Kontroller deretter alle eksisterende rolletilordninger er i samsvar.</span><span class="sxs-lookup"><span data-stu-id="69963-121">Next, verify that all existing role assignments are compliant.</span></span>

## <a name="verify-that-user-role-assignments-comply-with-new-rules-for-segregation-of-duties"></a><span data-ttu-id="69963-122">Bekrefte at brukerrolletilordninger samsvarer med nye regler for arbeidsdeling</span><span class="sxs-lookup"><span data-stu-id="69963-122">Verify that user role assignments comply with new rules for segregation of duties</span></span>
1. <span data-ttu-id="69963-123">Gå til **Systemadministrasjon > Sikkerhet > Arbeidsdeling > Bekreft overholdelse av brukerrolletilordninger**.</span><span class="sxs-lookup"><span data-stu-id="69963-123">Go to **System administration > Security > Segregation of duties > Verify compliance of user-role assignments**.</span></span>
2. <span data-ttu-id="69963-124">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="69963-124">Select **OK**.</span></span> <span data-ttu-id="69963-125">En varsling viser resultatet av valideringen.</span><span class="sxs-lookup"><span data-stu-id="69963-125">A notification displays the results of the validation.</span></span> <span data-ttu-id="69963-126">Konflikter logges på siden **Uløste konflikter for arbeidsdeling**.</span><span class="sxs-lookup"><span data-stu-id="69963-126">Conflicts are logged on the **Segregation of duties unresolved conflicts** page.</span></span>   

<span data-ttu-id="69963-127">Når du tilordner brukere til roller, blir reglene for arbeidsdeling håndhevet automatisk.</span><span class="sxs-lookup"><span data-stu-id="69963-127">When you assign users to roles, the rules for segregation of duties are automatically enforced.</span></span> <span data-ttu-id="69963-128">Hvis du prøver å tilordne en bruker til roller som inneholder plikter i konflikt, får du en feilmelding.</span><span class="sxs-lookup"><span data-stu-id="69963-128">If you try to assign a user to roles that contain conflicting duties, you receive an error message.</span></span> <span data-ttu-id="69963-129">Du må deretter løse konflikten ved å avslå eller tillate den ekstra rolletilordningen.</span><span class="sxs-lookup"><span data-stu-id="69963-129">You must then resolve the conflict by denying or allowing the additional role assignment.</span></span> <span data-ttu-id="69963-130">Den ekstra rollen tilordnes etter at tilordningen har blitt tillatt.</span><span class="sxs-lookup"><span data-stu-id="69963-130">The additional role will be assigned after the assignment is allowed.</span></span> 

> [!NOTE]
> <span data-ttu-id="69963-131">Konflikter kontrolleres for øyeblikket ikke for brukere som får tilordnet roller basert på Active Directory Domain-gruppene.</span><span class="sxs-lookup"><span data-stu-id="69963-131">Conflicts are currently not verified for users that are assigned roles based on the Active Directory Domain groups.</span></span>

## <a name="view-and-resolve-conflicting-user-role-assignments"></a><span data-ttu-id="69963-132">Vise og løse tilordninger av brukerroller i konflikt</span><span class="sxs-lookup"><span data-stu-id="69963-132">View and resolve conflicting user role assignments</span></span>
1. <span data-ttu-id="69963-133">Gå til **Systemadministrasjon** > **Sikkerhet** > **Arbeidsdeling** > **Uløste konflikter for arbeidsdeling**.</span><span class="sxs-lookup"><span data-stu-id="69963-133">Go to **System administration** > **Security** > **Segregation of duties** > **Segregation of duties unresolved conflicts**.</span></span> 
2. <span data-ttu-id="69963-134">Velg en konflikt, og velg deretter én av følgende handlinger:</span><span class="sxs-lookup"><span data-stu-id="69963-134">Select a conflict, and then select one of the following actions:</span></span> 

  - <span data-ttu-id="69963-135">**Avslå tilordning**: Dette avslår tilordningen av brukeren til den ekstra sikkerhetsrollen.</span><span class="sxs-lookup"><span data-stu-id="69963-135">**Deny assignment**: This will deny the assignment of the user to the additional security role.</span></span> <span data-ttu-id="69963-136">Hvis du nekter en automatisk rolletilordning, merkes brukeren som utelatt fra rollen.</span><span class="sxs-lookup"><span data-stu-id="69963-136">If you deny an automatic role assignment, the user is marked as excluded from the role.</span></span> <span data-ttu-id="69963-137">Den utelatte brukeren får ikke tilgangen som er knyttet til rollen, og kan ikke tilordnes til rollen før administratoren fjerner utelatelsen.</span><span class="sxs-lookup"><span data-stu-id="69963-137">The excluded user isn't granted the access associated with the role and can't be assigned to the role until the administrator removes the exclusion.</span></span> 
-  <span data-ttu-id="69963-138">**Tillat tilordning**: Dette overstyrer konflikten og lar brukeren bli tilordnet til den ekstra sikkerhetsrollen.</span><span class="sxs-lookup"><span data-stu-id="69963-138">**Allow assignment**: This will override the conflict and allow the user to be assigned to the additional security role.</span></span> <span data-ttu-id="69963-139">Hvis du overstyrer en konflikt, må du angi en årsak i feltet **Årsak til overstyring**.</span><span class="sxs-lookup"><span data-stu-id="69963-139">If you override a conflict, you must enter a reason in the **Reason for override** field.</span></span> <span data-ttu-id="69963-140">Alle overstyrte rolletilordninger kan vises på siden **Arbeidsdelingskonflikter**.</span><span class="sxs-lookup"><span data-stu-id="69963-140">All overridden role assignments can be viewed on the **Segregation of duties conflicts** page.</span></span>  

> [!NOTE]
> <span data-ttu-id="69963-141">Hvis det vises flere konflikter for samme bruker, velger du brukerposten og evaluerer tilordnede roller på **Brukere**-siden.</span><span class="sxs-lookup"><span data-stu-id="69963-141">If several conflicts are listed for the same user, select the user record and evaluate assigned roles on the **Users** page.</span></span> <span data-ttu-id="69963-142">For å unngå denne konflikten validerer du hver regel etter at den er lagt til eller endret.</span><span class="sxs-lookup"><span data-stu-id="69963-142">To avoid this conflict, validate each rule after it's added or modified.</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]