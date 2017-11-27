---
title: Startside for organisasjonsstyring
description: "Dette emnet peker på ressurser som hjelper deg med å bruke Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition i organisasjonen din."
author: sericks007
manager: AnnBe
ms.date: 08/18/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 20421
ms.assetid: 7aa24a03-d172-47e9-81f8-ebd39e80bc60
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: f1cff2388b02ff6dfd52a39b7f3ea90f10807096
ms.contentlocale: nb-no
ms.lasthandoff: 11/03/2017

---

# <a name="organization-administration-home-page"></a><span data-ttu-id="d88da-103">Startside for organisasjonsstyring</span><span class="sxs-lookup"><span data-stu-id="d88da-103">Organization administration home page</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="d88da-104">Dette emnet peker på innhold som vil hjelpe privilegerte brukere og administratorer til å konfigurere Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition.</span><span class="sxs-lookup"><span data-stu-id="d88da-104">This topic points to content that will help power users and administrators configure Microsoft Dynamics 365 for Finance and Operations, Enterprise edition.</span></span> <span data-ttu-id="d88da-105">Dette innholdet vil hjelpe dem å konfigurere systemet så det jobber godt og effektivt for organisasjonen og bedriften din.</span><span class="sxs-lookup"><span data-stu-id="d88da-105">This content will help them configure the system to work smoothly and effectively for your organization and business.</span></span>

<span data-ttu-id="d88da-106">Mye av innholdet som er oppført her gjelder for funksjoner i modulen **Organisasjonsstyring**.</span><span class="sxs-lookup"><span data-stu-id="d88da-106">Much of the content listed here applies to features in the **Organizational administration** module.</span></span> <span data-ttu-id="d88da-107">Det er imidlertid et par oppgaver, for eksempel å opprette og bruke en postmal, som kan utføres i en hvilken som helst modul for å hjelpe organisasjonen din å være mer effektiv.</span><span class="sxs-lookup"><span data-stu-id="d88da-107">However, there are a couple of tasks, such as creating and using a record template, that can be performed in any module to help your organization run more efficiently.</span></span> 

<a name="number-sequences"></a><span data-ttu-id="d88da-108">Nummerserier</span><span class="sxs-lookup"><span data-stu-id="d88da-108">Number sequences</span></span>
----------------
<span data-ttu-id="d88da-109">Nummerserier brukes for å generere lesbare, unike ID-er for hoveddataposter og transaksjonsposter som krever ID-er.</span><span class="sxs-lookup"><span data-stu-id="d88da-109">Number sequences are used to generate readable, unique identifiers for master data records and transaction records that require identifiers.</span></span> <span data-ttu-id="d88da-110">En hoveddatapost eller transaksjonspost som krever en ID kalles en *referanse*.</span><span class="sxs-lookup"><span data-stu-id="d88da-110">A master data record or transaction record that requires an identifier is referred to as a *reference*.</span></span> <span data-ttu-id="d88da-111">Du må konfigurere en nummerserie og tilknytte den referansen før du kan opprette nye poster for en referanse.</span><span class="sxs-lookup"><span data-stu-id="d88da-111">Before you can create new records for a reference, you must set up a number sequence and associate it with the reference.</span></span>

-   [<span data-ttu-id="d88da-112">Oversikt over nummerserie</span><span class="sxs-lookup"><span data-stu-id="d88da-112">Number sequence overview</span></span>](number-sequence-overview.md)
-   <span data-ttu-id="d88da-113">[Konfigurere alle nødvendige nummerserier ved å bruke en veiviser](tasks/set-up-number-sequences-wizard.md) (Oppgaveveiledning)</span><span class="sxs-lookup"><span data-stu-id="d88da-113">[Set up number sequences by using a wizard](tasks/set-up-number-sequences-wizard.md) (Task guide)</span></span>
-   <span data-ttu-id="d88da-114">[Konfigurere nummerserier enkeltvis](tasks/set-up-number-sequences-individual-basis.md) (Oppgaveveiledning)</span><span class="sxs-lookup"><span data-stu-id="d88da-114">[Set up number sequences on an individual basis](tasks/set-up-number-sequences-individual-basis.md) (Task guide)</span></span>

## <a name="organizations"></a><span data-ttu-id="d88da-115">Organisasjoner</span><span class="sxs-lookup"><span data-stu-id="d88da-115">Organizations</span></span>
<span data-ttu-id="d88da-116">En organisasjon er en gruppe personer som jobber sammen for å utføre en forretningsprosess eller oppnå et mål.</span><span class="sxs-lookup"><span data-stu-id="d88da-116">An organization is a group of people who are working together to carry out a business process or achieve a goal.</span></span> <span data-ttu-id="d88da-117">Organisasjonshierarkier representerer relasjonene mellom organisasjonene som utgjør virksomheten.</span><span class="sxs-lookup"><span data-stu-id="d88da-117">Organizational hierarchies represent the relationships between the organizations that make up your business.</span></span>

<span data-ttu-id="d88da-118">Før du oppretter organisasjoner og organisasjonshierarkier i Finance and Operations, må du sørge for at du planlegger hvordan virksomheten din skal modelleres.</span><span class="sxs-lookup"><span data-stu-id="d88da-118">Before you set up organizations and organization hierarchies in Finance and Operations, make sure that you plan how your business will be modeled.</span></span> <span data-ttu-id="d88da-119">Organisasjonsmodellen har en betydelig innvirkning på implementeringen av Finance and Operations og på forretningsprosesser.</span><span class="sxs-lookup"><span data-stu-id="d88da-119">The organization model has a significant effect on the implementation of Finance and Operations and on business processes.</span></span>

-   [<span data-ttu-id="d88da-120">Organisasjoner og organisasjonshierarkier</span><span class="sxs-lookup"><span data-stu-id="d88da-120">Organizations and organizational hierarchies</span></span>](organizations-organizational-hierarchies.md)
-   [<span data-ttu-id="d88da-121">Planlegge organisasjonshierarkiet</span><span class="sxs-lookup"><span data-stu-id="d88da-121">Plan your organizational hierarchy</span></span>](plan-organizational-hierarchy.md)
-   <span data-ttu-id="d88da-122">[Opprette et organisasjonshierarki](tasks/create-organization-hierarchy.md) (Oppgaveveiledning)</span><span class="sxs-lookup"><span data-stu-id="d88da-122">[Create an organization hierarchy](tasks/create-organization-hierarchy.md) (Task guide)</span></span>
-   <span data-ttu-id="d88da-123">[Opprette en juridisk enhet](tasks/create-legal-entity.md) (Oppgaveveiledning)</span><span class="sxs-lookup"><span data-stu-id="d88da-123">[Create a legal entity](tasks/create-legal-entity.md) (Task guide)</span></span>
-   <span data-ttu-id="d88da-124">[Opprette en driftsenhet](tasks/create-operating-unit.md) (Oppgaveveiledning)</span><span class="sxs-lookup"><span data-stu-id="d88da-124">[Create an operating unit](tasks/create-operating-unit.md) (Task guide)</span></span>

## <a name="address-books"></a><span data-ttu-id="d88da-125">Adressebøker</span><span class="sxs-lookup"><span data-stu-id="d88da-125">Address books</span></span>
<span data-ttu-id="d88da-126">Den globale adresseboken er et sentralisert lager for stamdata som må lagres for alle interne og eksterne personer og organisasjoner som selskapet samhandler med.</span><span class="sxs-lookup"><span data-stu-id="d88da-126">The global address book is a centralized repository for master data that must be stored for all internal and external persons and organizations that the company interacts with.</span></span> <span data-ttu-id="d88da-127">Dataene som er knyttet til partsoppføringer inkluderer partens navn, adresse og kontaktinformasjon.</span><span class="sxs-lookup"><span data-stu-id="d88da-127">The data that is associated with party records includes the party's name, address, and contact information.</span></span> 

<span data-ttu-id="d88da-128">Når du oppretter den globale adresseboken, kan du opprette flere adressebøker i henhold til behovet ditt, for eksempel en egen adressebok for hvert firma i organisasjonen din eller for hver bransje.</span><span class="sxs-lookup"><span data-stu-id="d88da-128">After you create the global address book, you can create additional address books as you require, such as a separate address book for each company in your organization or for each line of business.</span></span> 

-   [<span data-ttu-id="d88da-129">Global adressebok</span><span class="sxs-lookup"><span data-stu-id="d88da-129">Global address book</span></span>](overview-global-address-book.md)
-   [<span data-ttu-id="d88da-130">Planlegg hvordan du konfigurerer den globale adresseboken og flere adressebøker</span><span class="sxs-lookup"><span data-stu-id="d88da-130">Plan how to configure the global address book and additional address books</span></span>](plan-configuration-global-address-book-additional-address-books.md)
- [<span data-ttu-id="d88da-131">Konfigurere den globale adresseboken</span><span class="sxs-lookup"><span data-stu-id="d88da-131">Configure the global address book</span></span>](tasks/configure-global-address-book.md)
-   [<span data-ttu-id="d88da-132">Vanlige spørsmål om adressebøker</span><span class="sxs-lookup"><span data-stu-id="d88da-132">Address books FAQ</span></span>](qa-address-books.md)


## <a name="workflow"></a><span data-ttu-id="d88da-133">Arbeidsflyt</span><span class="sxs-lookup"><span data-stu-id="d88da-133">Workflow</span></span>
<span data-ttu-id="d88da-134">Arbeidsflyt er et system som er installert med Finance and Operations, og du kan bruke den for å opprette individuelle arbeidsflyter eller forretningsprosesser.</span><span class="sxs-lookup"><span data-stu-id="d88da-134">Workflow is a system that is installed with Finance and Operations that you can use to create individual workflows, or business processes.</span></span> <span data-ttu-id="d88da-135">Når du oppretter en arbeidsflyt spesifiserer du hvordan et dokument flyter eller flyttes gjennom systemet ved å vise hvem som må fullføre en oppgave, ta en avgjørelse, eller godkjenne et dokument.</span><span class="sxs-lookup"><span data-stu-id="d88da-135">When you create a workflow, you specify how a document flows, or moves, through the system by showing who must complete a task, make a decision, or approve a document.</span></span> 

-   [<span data-ttu-id="d88da-136">Arbeidsflytoversikt</span><span class="sxs-lookup"><span data-stu-id="d88da-136">Workflow overview</span></span>](overview-workflow-system.md)
-   [<span data-ttu-id="d88da-137">Arbeidsflytelementer</span><span class="sxs-lookup"><span data-stu-id="d88da-137">Workflow elements</span></span>](workflow-elements.md)
-   [<span data-ttu-id="d88da-138">Arbeidsflythandlinger</span><span class="sxs-lookup"><span data-stu-id="d88da-138">Workflow actions</span></span>](workflow-actions.md)
-   [<span data-ttu-id="d88da-139">Opprette en arbeidsflyt</span><span class="sxs-lookup"><span data-stu-id="d88da-139">Create a workflow</span></span>](create-workflow.md)

## <a name="electronic-signatures"></a><span data-ttu-id="d88da-140">Elektroniske signaturer</span><span class="sxs-lookup"><span data-stu-id="d88da-140">Electronic signatures</span></span>
<span data-ttu-id="d88da-141">En elektronisk signatur bekrefter identiteten til en person som er i ferd med å starte eller godkjenne en dataprosess.</span><span class="sxs-lookup"><span data-stu-id="d88da-141">An electronic signature confirms the identity of a person who is about to start or approve a computing process.</span></span> <span data-ttu-id="d88da-142">I noen bransjer er en elektronisk signatur like bindende som er håndskrevet signatur.</span><span class="sxs-lookup"><span data-stu-id="d88da-142">In some industries, an electronic signature is as legally binding as a handwritten signature.</span></span> <span data-ttu-id="d88da-143">Elektroniske signaturer er et krav til samsvar med lovgivning for flere regulerte industrier, for eksempel legemiddelindustrien, matvareindustrien og romfarts- og forsvarsindustrien.</span><span class="sxs-lookup"><span data-stu-id="d88da-143">Electronic signatures are a regulations compliance requirement for several regulated industries, such as pharmaceuticals, food and beverage, and aerospace and defense.</span></span>

<span data-ttu-id="d88da-144">I Dynamics 365 for Finance and Operations kan du bruke elektroniske signaturer for viktige forretningsprosesser.</span><span class="sxs-lookup"><span data-stu-id="d88da-144">In Finance and Operations, you can use electronic signatures for critical business processes.</span></span> <span data-ttu-id="d88da-145">Noen prosesser har innebygde funksjoner for elektronisk signatur.</span><span class="sxs-lookup"><span data-stu-id="d88da-145">Some processes have built-in electronic signature capabilities.</span></span> <span data-ttu-id="d88da-146">Du kan også opprette egendefinerte signaturkrav for en hvilken som helst databasetabell og et hvilket som helst felt.</span><span class="sxs-lookup"><span data-stu-id="d88da-146">You can also create custom signature requirements for any database table and field.</span></span>

-   [<span data-ttu-id="d88da-147">Oversikt over elektronisk signatur</span><span class="sxs-lookup"><span data-stu-id="d88da-147">Electronic signature overview</span></span>](electronic-signature-overview.md)
-   <span data-ttu-id="d88da-148">[Definere elektroniske signaturer](tasks/set-up-electronic-signatures.md) (Oppgaveveiledning)</span><span class="sxs-lookup"><span data-stu-id="d88da-148">[Set up electronic signatures](tasks/set-up-electronic-signatures.md) (Task guide)</span></span>

## <a name="case-management"></a><span data-ttu-id="d88da-149">Saksbehandling</span><span class="sxs-lookup"><span data-stu-id="d88da-149">Case management</span></span>
<span data-ttu-id="d88da-150">Når du planlegger, sporer og analyserer tilfeller, kan du utvikle effektive løsninger som kan brukes ved lignende problemer.</span><span class="sxs-lookup"><span data-stu-id="d88da-150">By planning, tracking, and analyzing cases, you can develop efficient resolutions that can be used for similar issues.</span></span> <span data-ttu-id="d88da-151">For eksempel, når kundeservicerepresentanter eller HR-generalister oppretter saker, kan de finne informasjon i kunnskapsartikler for å hjelpe dem med å arbeide med eller løse en sak mer effektivt.</span><span class="sxs-lookup"><span data-stu-id="d88da-151">For example, when customer service representatives or Human Resources generalists create cases, they can find information in knowledge articles to help them work with or resolve a case more efficiently.</span></span> 

-   [<span data-ttu-id="d88da-152">Oversikt over saksbehandling</span><span class="sxs-lookup"><span data-stu-id="d88da-152">Case management overview</span></span>](cases.md)
-   [<span data-ttu-id="d88da-153">Konfigurere sakssikkerhet, prosesser og kategorier</span><span class="sxs-lookup"><span data-stu-id="d88da-153">Configure case security, processes, and categories</span></span>](plan-case-management.md)

## <a name="record-templates"></a><span data-ttu-id="d88da-154">Postmaler</span><span class="sxs-lookup"><span data-stu-id="d88da-154">Record templates</span></span>
<span data-ttu-id="d88da-155">Postmaler kan hjelpe deg å opprette poster mer effektivt.</span><span class="sxs-lookup"><span data-stu-id="d88da-155">Record templates can help you to create records more quickly.</span></span> <span data-ttu-id="d88da-156">Du kan opprette en postmal så feltverdiene som brukes ofte ikke behøver fylles inn eksplisitt for en ny post.</span><span class="sxs-lookup"><span data-stu-id="d88da-156">You can create a record template so that field values that are used often do not have to be entered explicitly for each new record.</span></span> 

-   [<span data-ttu-id="d88da-157">Postmaler</span><span class="sxs-lookup"><span data-stu-id="d88da-157">Record templates</span></span>](record-templates.md)
- <span data-ttu-id="d88da-158">[Opprett en postmal for å fasilitere dataoppføring](../../dev-itpro/data-entities/tasks/create-record-template-facilitate-data-entry.md) (Oppgaveveiledning)</span><span class="sxs-lookup"><span data-stu-id="d88da-158">[Create a record template to facilitate data entry](../../dev-itpro/data-entities/tasks/create-record-template-facilitate-data-entry.md) (Task guide)</span></span>
- <span data-ttu-id="d88da-159">[Bruk en postmal for å fasilitere opprettelse av en ny oppføring](../../dev-itpro/data-entities/tasks/use-record-template-new-record.md) (Oppgaveveiledning)</span><span class="sxs-lookup"><span data-stu-id="d88da-159">[Use a record template to create a new record](../../dev-itpro/data-entities/tasks/use-record-template-new-record.md) (Task guide)</span></span>

## <a name="general-organization-administration"></a><span data-ttu-id="d88da-160">Generell organisasjonsadministrasjon</span><span class="sxs-lookup"><span data-stu-id="d88da-160">General organization administration</span></span>
-   <span data-ttu-id="d88da-161">[Endre banner eller logo](../get-started/tasks/change-banner-or-logo.md) (Oppgaveveiledning)</span><span class="sxs-lookup"><span data-stu-id="d88da-161">[Change the banner or logo](../get-started/tasks/change-banner-or-logo.md) (Task guide)</span></span>
- [<span data-ttu-id="d88da-162">Konfigurere dokumentstyring</span><span class="sxs-lookup"><span data-stu-id="d88da-162">Configure document management</span></span>](configure-document-management.md)
- [<span data-ttu-id="d88da-163">Konfigurere og sende e-post</span><span class="sxs-lookup"><span data-stu-id="d88da-163">Configure and send email</span></span>](configure-email.md)
-   [<span data-ttu-id="d88da-164">Dato-/klokkeslettdata og tidssoner</span><span class="sxs-lookup"><span data-stu-id="d88da-164">Date/time data and time zones</span></span>](date-time-zones.md)








