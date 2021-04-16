---
title: Bruke Power Portal med partdatamodellen
description: Dette emnet beskriver endringene i webrollene i Power Portal på grunn av partdatamodellen i dobbel skriving.
author: RamaKrishnamoorthy
ms.date: 03/22/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2021-03-22
ms.openlocfilehash: a2ea914344341ee26138e853727c551bdd5d733e
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5833096"
---
# <a name="using-power-portal-with-the-party-data-model"></a><span data-ttu-id="f6980-103">Bruke Power Portal med partdatamodellen</span><span class="sxs-lookup"><span data-stu-id="f6980-103">Using Power Portal with the Party data model</span></span>

[!INCLUDE[banner](../../includes/banner.md)]

[!INCLUDE[rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="f6980-104">Versjon 2.0.999.0 og senere av løsningen for orkestrering av apper med dobbel skriving inkluderer endringer i datamodeller for parter og global adressebok tabellene Konto og Kontakt.</span><span class="sxs-lookup"><span data-stu-id="f6980-104">The Dual-write application orchestration solution version 2.0.999.0 and later includes data model changes to party and global address book for the Account and Contact tables.</span></span> <span data-ttu-id="f6980-105">Endringene tillater mange-til-mange-relasjoner som støtter avanserte forretningsscenarier.</span><span class="sxs-lookup"><span data-stu-id="f6980-105">The changes allow many-to-many relationships that support advanced business scenarios.</span></span> <span data-ttu-id="f6980-106">Disse endringene støttes ikke av webroller for portaler, inkludert kundeportalen, som følger med som standard, eller som allerede fantes i miljøet ditt før du installerte dobbel skriving.</span><span class="sxs-lookup"><span data-stu-id="f6980-106">These changes are not supported by portal web roles, including the customer portal, that are shipped out-of-the-box or that existed in your environment before you installed dual-write.</span></span> <span data-ttu-id="f6980-107">For at webrollene skal fungere som forventet, må du opprette nye webroller ved hjelp av den nye datamodellen.</span><span class="sxs-lookup"><span data-stu-id="f6980-107">For the web roles to work as expected, you need to create new web roles using the new data model.</span></span> 

<span data-ttu-id="f6980-108">Kort sagt er måten tabellene fungerer på endret, men tabelltillatelsene i kundeportalen er ikke endret.</span><span class="sxs-lookup"><span data-stu-id="f6980-108">In summary, the way the tables interact has changed, but the table permissions in the customer portal haven't changed.</span></span> <span data-ttu-id="f6980-109">Dette emnet beskriver hvordan du oppretter nye webroller som arbeider med den nye avanserte datamodellen.</span><span class="sxs-lookup"><span data-stu-id="f6980-109">This topic explains how to create new web roles that work with the new advanced data model.</span></span>

<span data-ttu-id="f6980-110">Dette diagrammet viser tabellrelasjonen **uten** parten og den globale adressebokdatamodellen:</span><span class="sxs-lookup"><span data-stu-id="f6980-110">This diagram shows the table relationship **without** the party and global address book data model:</span></span>

   ![uten partmodell](media/without-party-model.PNG)

<span data-ttu-id="f6980-112">Dette diagrammet viser tabellrelasjonen **med** parten og den globale adressebokdatamodellen:</span><span class="sxs-lookup"><span data-stu-id="f6980-112">This diagram shows the table relationship **with** the party and global address book data model:</span></span>

   ![med partmodell](media/with-party-model.png)

## <a name="create-a-new-table-permission"></a><span data-ttu-id="f6980-114">Opprette en ny tabelltillatelse</span><span class="sxs-lookup"><span data-stu-id="f6980-114">Create a new table permission</span></span>

<span data-ttu-id="f6980-115">Følg denne fremgangsmåten for å opprette disse nye tabelltillatelsene:</span><span class="sxs-lookup"><span data-stu-id="f6980-115">To create these new table permissions, follow these steps:</span></span>

1. <span data-ttu-id="f6980-116">Logg deg på [Power Apps](https://make.powerapps.com), og gå til appene.</span><span class="sxs-lookup"><span data-stu-id="f6980-116">Sign in to [Power Apps](https://make.powerapps.com), and go to your apps.</span></span>
2. <span data-ttu-id="f6980-117">Velg Portal Management-appen.</span><span class="sxs-lookup"><span data-stu-id="f6980-117">Select your Portal Management app.</span></span>
3. <span data-ttu-id="f6980-118">Velg **Sikkerhet > Tabelltillatelser** i sidefeltet.</span><span class="sxs-lookup"><span data-stu-id="f6980-118">In the side bar, select **Security > Table permissions**.</span></span>

    <span data-ttu-id="f6980-119">Du må opprette tre nye tillatelser:</span><span class="sxs-lookup"><span data-stu-id="f6980-119">You must create three new permissions:</span></span>

    + <span data-ttu-id="f6980-120">Kontakt til part-tilkobling</span><span class="sxs-lookup"><span data-stu-id="f6980-120">Contact to Party connection</span></span>
    + <span data-ttu-id="f6980-121">Part til konto-tilkobling</span><span class="sxs-lookup"><span data-stu-id="f6980-121">Party to Account connection</span></span>
    + <span data-ttu-id="f6980-122">Konto til ordre-tilkobling</span><span class="sxs-lookup"><span data-stu-id="f6980-122">Account to Order connection</span></span>

4. <span data-ttu-id="f6980-123">Opprett og lagre en ny tillatelse for Kontakt til part-tilkoblingen ved å angi disse parameterne:</span><span class="sxs-lookup"><span data-stu-id="f6980-123">Create and save a new permission for the Contact to Party connection, setting these parameters:</span></span>

    + <span data-ttu-id="f6980-124">**Navn:** Part til konto-tilkobling (eller ditt valg)</span><span class="sxs-lookup"><span data-stu-id="f6980-124">**Name**: Party to Account Connection (or your choice)</span></span>
    + <span data-ttu-id="f6980-125">**Tabellnavn**: msdyn_contactforparty</span><span class="sxs-lookup"><span data-stu-id="f6980-125">**Table Name**: msdyn_contactforparty</span></span>
    + <span data-ttu-id="f6980-126">**Nettsted**: Kundeportal</span><span class="sxs-lookup"><span data-stu-id="f6980-126">**Website**: Customer Portal</span></span>
    + <span data-ttu-id="f6980-127">**Omfang:** Kontakt</span><span class="sxs-lookup"><span data-stu-id="f6980-127">**Scope**: Contact</span></span>
    + <span data-ttu-id="f6980-128">**Rettigheter**: Velg alle</span><span class="sxs-lookup"><span data-stu-id="f6980-128">**Privileges**: Select all</span></span>
    + <span data-ttu-id="f6980-129">**Webroller**: Godkjente brukere, Kunderepresentant (eller ditt valg)</span><span class="sxs-lookup"><span data-stu-id="f6980-129">**Web roles**: Authenticated Users, Customer Representative (or your choice)</span></span>

5. <span data-ttu-id="f6980-130">Opprett og lagre en ny tillatelse for Part til konto-tilkoblingen ved å angi disse parameterne:</span><span class="sxs-lookup"><span data-stu-id="f6980-130">Create and save a new permission for the Party to Account connection, setting these parameters:</span></span>

    + <span data-ttu-id="f6980-131">**Navn:** Part til konto-tilkobling (eller ditt valg)</span><span class="sxs-lookup"><span data-stu-id="f6980-131">**Name**: Party to Account Connection (or your choice)</span></span>
    + <span data-ttu-id="f6980-132">**Tabellnavn**: Konto</span><span class="sxs-lookup"><span data-stu-id="f6980-132">**Table Name**: account</span></span>
    + <span data-ttu-id="f6980-133">**Nettsted**: Kundeportal</span><span class="sxs-lookup"><span data-stu-id="f6980-133">**Website**: Customer Portal</span></span>
    + <span data-ttu-id="f6980-134">**Omfang:** Overordnet</span><span class="sxs-lookup"><span data-stu-id="f6980-134">**Scope**: Parent</span></span>
    + <span data-ttu-id="f6980-135">**Rettigheter**: Velg alle</span><span class="sxs-lookup"><span data-stu-id="f6980-135">**Privileges**: Select all</span></span>
    + <span data-ttu-id="f6980-136">**Overordnet tabelltillatelse**: Kontakt til part-tilkobling</span><span class="sxs-lookup"><span data-stu-id="f6980-136">**Parent Table Permission**: Contact to Party Connection</span></span>

6. <span data-ttu-id="f6980-137">Opprett og lagre en ny tillatelse for Konto til ordre-tilkoblingen ved å angi disse parameterne:</span><span class="sxs-lookup"><span data-stu-id="f6980-137">Create and save a new permission for the Account to Order connection, setting these parameters:</span></span>

    + <span data-ttu-id="f6980-138">**Navn:** Konto til ordre-tilkobling (eller ditt valg)</span><span class="sxs-lookup"><span data-stu-id="f6980-138">**Name**: Account to Order Connection (or your choice)</span></span>
    + <span data-ttu-id="f6980-139">**Tabellnavn**: salgsordre</span><span class="sxs-lookup"><span data-stu-id="f6980-139">**Table Name**: salesorder</span></span>
    + <span data-ttu-id="f6980-140">**Nettsted**: Kundeportal</span><span class="sxs-lookup"><span data-stu-id="f6980-140">**Website**: Customer Portal</span></span>
    + <span data-ttu-id="f6980-141">**Omfang:** Overordnet</span><span class="sxs-lookup"><span data-stu-id="f6980-141">**Scope**: Parent</span></span>
    + <span data-ttu-id="f6980-142">**Rettigheter**: Velg alle</span><span class="sxs-lookup"><span data-stu-id="f6980-142">**Privileges**: Select all</span></span>
    + <span data-ttu-id="f6980-143">**Overordnet tabelltillatelse**: Part til konto-tilkobling</span><span class="sxs-lookup"><span data-stu-id="f6980-143">**Parent Table Permission**: Party to Account Connection</span></span>

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
