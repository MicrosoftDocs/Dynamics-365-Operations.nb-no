---
title: Aktivadokumenter
description: Dette emnet beskriver aktivadokumenter i Aktivastyring.
author: johanhoffmann
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetObjectDocument
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8458c302b506f9f048b7886f55a392d9afceb446
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5808382"
---
# <a name="asset-documents"></a><span data-ttu-id="f0faa-103">Aktivadokumenter</span><span class="sxs-lookup"><span data-stu-id="f0faa-103">Asset documents</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="f0faa-104">Dette emnet beskriver aktivadokumenter i Aktivastyring.</span><span class="sxs-lookup"><span data-stu-id="f0faa-104">This topic explains asset documents in Asset Management.</span></span>

<span data-ttu-id="f0faa-105">I Aktivastyring kan du definere dokumenter slik at de automatisk er knyttet til jobbtyper, aktivaprodusenter, aktivatyper eller aktiva.</span><span class="sxs-lookup"><span data-stu-id="f0faa-105">In Asset Management, you can set up documents so that they are automatically related to job types, asset manufacturers, asset types, or assets, for example.</span></span> <span data-ttu-id="f0faa-106">Denne funksjonaliteten er nyttig når det utgis oppdaterte dokumentversjoner.</span><span class="sxs-lookup"><span data-stu-id="f0faa-106">This functionality is useful when updated document versions are released.</span></span> <span data-ttu-id="f0faa-107">I så fall må du bare plassere det oppdaterte dokumentet på standardstedet du bruker for Supply Chain Management-dokumentene, og knytte dokumentet til aktivadokumentposten du har opprettet.</span><span class="sxs-lookup"><span data-stu-id="f0faa-107">In that case, you just have to put the updated document in the standard location that you use for your Supply Chain Management documents, and attach the document to the asset document record that you've created.</span></span> <span data-ttu-id="f0faa-108">Du får da tilgang til det oppdaterte dokumentet fra menyelementene **Alle aktiva**, **Aktive aktiva**, **Mine aktiva aktiva**, **Alle arbeidsordrer** og **Aktive arbeidsordrejobber**.</span><span class="sxs-lookup"><span data-stu-id="f0faa-108">The updated document can then be accessed from the **All assets**, **Active assets**, **My active assets**, **All work orders**, and **Active work order jobs** menu items.</span></span> <span data-ttu-id="f0faa-109">Prosessen for å knytte dokumenter til en aktivadokumentpost bruker standardsystemet for dokumenthåndtering.</span><span class="sxs-lookup"><span data-stu-id="f0faa-109">The process for attaching documents to an asset document record uses the standard document handling system.</span></span>

<span data-ttu-id="f0faa-110">**Eksempel 1:** Et dokument som er relatert til en jobbtype, kan beskrive en fremgangsmåte for denne jobbtypen.</span><span class="sxs-lookup"><span data-stu-id="f0faa-110">**Example 1:** A document that is related to a job type might describe a procedure for that job type.</span></span>

<span data-ttu-id="f0faa-111">**Eksempel 2:** Et dokument som er knyttet til en kombinasjon av en aktivatype, -produsent og -modell, kan være standardhåndboken for den valgte aktivaleverandørmodellen.</span><span class="sxs-lookup"><span data-stu-id="f0faa-111">**Example 2:** A document that is related to a combination of an asset type, manufacturer, and model might be the standard manual for the selected asset manufacturer model.</span></span>

## <a name="create-asset-document-relation"></a><span data-ttu-id="f0faa-112">Opprett relasjon til aktivadokument</span><span class="sxs-lookup"><span data-stu-id="f0faa-112">Create asset document relation</span></span>

1. <span data-ttu-id="f0faa-113">Velg **Aktivastyring** \> **Oppsett** \> **Aktivadokumenter**.</span><span class="sxs-lookup"><span data-stu-id="f0faa-113">Select **Asset management** \> **Setup** \> **Asset documents**.</span></span>
2. <span data-ttu-id="f0faa-114">Velg **Ny** for å opprette en aktivadokumentpost.</span><span class="sxs-lookup"><span data-stu-id="f0faa-114">Select **New** to create an asset document record.</span></span>
3. <span data-ttu-id="f0faa-115">Avhengig av hvor spesifikk du ønsker dokumentrelasjonen skal være, kan du foreta relevante valg i ett eller flere av følgende felt: **Aktivatype**, **Produsent**, **Modell**, **Aktivum**, **Jobbtypekategori**, **Jobbtype**, **Jobbtypevariant** og **Jobbehov**.</span><span class="sxs-lookup"><span data-stu-id="f0faa-115">Depending on how specific you want the document relation to be, make relevant selections in one or more of the following fields: **Asset type**, **Manufacturer**, **Model**, **Asset**, **Job type category**, **Job type**, **Job type variant**, and **Job requirement**.</span></span> <span data-ttu-id="f0faa-116">Alternativene som er tilgjengelige i feltene **Jobbtypevariant** og **Jobbehov**, avhenger av hva du velger i **Jobbtype**-feltet.</span><span class="sxs-lookup"><span data-stu-id="f0faa-116">The options that are available in the **Job type variant** and **Job requirement** fields depend on your selection in the **Job type** field.</span></span>

    > [!NOTE]
    > <span data-ttu-id="f0faa-117">Når systemet søker etter dokumenter som skal knyttes til et aktivum eller en arbeidsordre, går Aktivastyring gjennom alle aktivadokumentposter for å se etter en mulig match.</span><span class="sxs-lookup"><span data-stu-id="f0faa-117">When the system searches for documents that should be related to an asset or a work order, Asset Management goes through all asset document records to check for a possible match.</span></span> <span data-ttu-id="f0faa-118">Den kontrollerer alltid den mest spesifikke kombinasjonen først.</span><span class="sxs-lookup"><span data-stu-id="f0faa-118">It always checks the most specific combination first.</span></span> <span data-ttu-id="f0faa-119">Med andre ord ser Aktivastyring først etter et treff i **Jobbehov**-feltet.</span><span class="sxs-lookup"><span data-stu-id="f0faa-119">In other words, Asset Management first checks for a match for the **Job requirement** field.</span></span> <span data-ttu-id="f0faa-120">Hvis det ikke blir funnet noe treff, kontrolleres det for et treff i **Jobbtypevariant**-feltet.</span><span class="sxs-lookup"><span data-stu-id="f0faa-120">If no match is found, it checks for a match for the **Job type variant** field.</span></span> <span data-ttu-id="f0faa-121">Hvis det ikke blir funnet noe treff, kontrolleres det for et treff i **Jobbtype**-feltet, og så videre.</span><span class="sxs-lookup"><span data-stu-id="f0faa-121">If no match is found, it checks for a match for the **Job type** field, and so on.</span></span> <span data-ttu-id="f0faa-122">Som du kan se i oppsettet av **Aktivadokumenter**-siden, betyr dette at for å finne den mest spesifikke kombinasjonen, kontrollerer Aktivastyring hver post fra høyre til venstre for et treff.</span><span class="sxs-lookup"><span data-stu-id="f0faa-122">As you can see in the layout of the **Asset documents** page, this behavior means that, to find the most specific combination, Asset Management checks each record from right to left for a match.</span></span> <span data-ttu-id="f0faa-123">Flere dokumenter kan være knyttet til et aktivum eller en arbeidsordre.</span><span class="sxs-lookup"><span data-stu-id="f0faa-123">Several documents might be related to an asset or a work order.</span></span> <span data-ttu-id="f0faa-124">Du kan redigere servicenivået i en melding eller en arbeidsordre etter behov.</span><span class="sxs-lookup"><span data-stu-id="f0faa-124">You can edit the service level on a maintenance request or a work order as you require.</span></span>

4. <span data-ttu-id="f0faa-125">Velg **Vedlegg**.</span><span class="sxs-lookup"><span data-stu-id="f0faa-125">Select **Attachments**.</span></span> <span data-ttu-id="f0faa-126">Standardsiden **Dokumenthåndtering** vises.</span><span class="sxs-lookup"><span data-stu-id="f0faa-126">The standard **Document handling** page appears.</span></span>
5. <span data-ttu-id="f0faa-127">Definer dokumentene eller notatene som skal knyttes til aktivadokumentposten.</span><span class="sxs-lookup"><span data-stu-id="f0faa-127">Set up the documents or notes that should be attached to the asset document record.</span></span> <span data-ttu-id="f0faa-128">Når du har tilknyttet dokumenter, viser **Vedlegg**-feltet antallet dokumenter som er knyttet til posten.</span><span class="sxs-lookup"><span data-stu-id="f0faa-128">After you attach documents, the **Attachments** field shows the number of documents that are related to the record.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]