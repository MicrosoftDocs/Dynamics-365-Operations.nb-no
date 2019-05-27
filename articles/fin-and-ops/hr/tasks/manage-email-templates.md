---
title: Behandle e-postmaler
description: Du kan overføre informasjon fra databasen for organisasjonens til bokmerker i et nytt dokument og bruke det i maler som hjelper deg å kommunisere effektivt med søkere og kandidater.
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HRMApplicationWordBookmark, HRMApplicationEmailTemplate
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4667d0506c5ae6bea87b982c7feebab8963797a6
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/07/2019
ms.locfileid: "1508039"
---
# <a name="manage-email-templates"></a><span data-ttu-id="9e183-103">Behandle e-postmaler</span><span class="sxs-lookup"><span data-stu-id="9e183-103">Manage email templates</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9e183-104">Du kan overføre informasjon fra databasen for organisasjonens til bokmerker i et nytt dokument og bruke det i maler som hjelper deg å kommunisere effektivt med søkere og kandidater.</span><span class="sxs-lookup"><span data-stu-id="9e183-104">You can transfer information from your organization’s database to the bookmarks in a new document and use it in templates that help you communicate efficiently with applicants and candidates.</span></span> <span data-ttu-id="9e183-105">For å gjøre dette, oppretter du en mal som inneholder standardtekst og bokmerker der systemdataene skal settes inn.</span><span class="sxs-lookup"><span data-stu-id="9e183-105">To do this, you create a template that contains standard text and some bookmarks where the system data should be inserted.</span></span> <span data-ttu-id="9e183-106">Du kan for eksempel sette inn adresse- og kontaktinformasjon for en søker i et Microsoft Word-dokument som du kan bruke ved kommunikasjon med denne søkeren.</span><span class="sxs-lookup"><span data-stu-id="9e183-106">For example, you can insert address and contact information for an applicant into a Microsoft Word document that you can use when communicating with that applicant.</span></span> <span data-ttu-id="9e183-107">Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="9e183-107">The demo data company used to create this procedure is USMF.</span></span>


## <a name="select-which-bookmarks-to-use-in-your-email-templates"></a><span data-ttu-id="9e183-108">Velg hvilke bokmerker som skal brukes i dine e-postmaler</span><span class="sxs-lookup"><span data-stu-id="9e183-108">Select which bookmarks to use in your email templates</span></span>
1. <span data-ttu-id="9e183-109">Gå til Søknadsbokmerker.</span><span class="sxs-lookup"><span data-stu-id="9e183-109">Go to Application bookmarks.</span></span>
2. <span data-ttu-id="9e183-110">Finn og velg ønsket korrespondansehandling i listen.</span><span class="sxs-lookup"><span data-stu-id="9e183-110">In the list, find and select the desired correspondence action.</span></span>
3. <span data-ttu-id="9e183-111">Klikk Rediger.</span><span class="sxs-lookup"><span data-stu-id="9e183-111">Click Edit.</span></span>
4. <span data-ttu-id="9e183-112">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="9e183-112">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="9e183-113">Velg feltene du vil kunne bruke i en e-postmal for den valgte korrespondansehandlingen, og flytt dem til Bokmerke-feltene.</span><span class="sxs-lookup"><span data-stu-id="9e183-113">Select the fields you would like to be able to use in an email template for the selected Correspondence action and move them to the Bookmark fields.</span></span>  
5. <span data-ttu-id="9e183-114">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="9e183-114">Close the page.</span></span>

## <a name="create-an-email-template"></a><span data-ttu-id="9e183-115">Opprette en e-postmal</span><span class="sxs-lookup"><span data-stu-id="9e183-115">Create an email template</span></span>
1. <span data-ttu-id="9e183-116">Gå til Personale > Rekruttering > Kommunikasjon > E-postmaler for søknader.</span><span class="sxs-lookup"><span data-stu-id="9e183-116">Go to Human resources > Recruitment > Communication > Application e-mail templates.</span></span>
2. <span data-ttu-id="9e183-117">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="9e183-117">Click New.</span></span>
3. <span data-ttu-id="9e183-118">Velg Intervju i feltet Korrespondansehandling.</span><span class="sxs-lookup"><span data-stu-id="9e183-118">In the Correspondence action field, select 'Interview'.</span></span>
    * <span data-ttu-id="9e183-119">Velg korrespondansehandlingen som inneholder bokmerkene du bruker for denne typen e-postkommunikasjon.</span><span class="sxs-lookup"><span data-stu-id="9e183-119">Select the correspondence action that contains the bookmarks to use for this type of email communication.</span></span>  
4. <span data-ttu-id="9e183-120">Angi en verdi i E-postmal-feltet.</span><span class="sxs-lookup"><span data-stu-id="9e183-120">In the E-mail template field, type a value.</span></span>
5. <span data-ttu-id="9e183-121">Skriv inn en verdi i Emne-feltet.</span><span class="sxs-lookup"><span data-stu-id="9e183-121">In the Subject field, type a value.</span></span>
6. <span data-ttu-id="9e183-122">Skriv inn en verdi i Tekst-feltet.</span><span class="sxs-lookup"><span data-stu-id="9e183-122">In the Text field, type a value.</span></span>
7. <span data-ttu-id="9e183-123">Finn og velg ønsket bokmerkefelt i listen.</span><span class="sxs-lookup"><span data-stu-id="9e183-123">In the list, find and select the desired bookmark field.</span></span>
8. <span data-ttu-id="9e183-124">Fortsett å skrive inn din e-postmelding, og sett inn bokmerkfeltene der du trenger dem.</span><span class="sxs-lookup"><span data-stu-id="9e183-124">Continue typing your email message, inserting the bookmark fields where you need them.</span></span>
    * <span data-ttu-id="9e183-125">Fortsett å skrive inn din e-postmelding, og sett inn bokmerkfeltene der det er ønskelig.</span><span class="sxs-lookup"><span data-stu-id="9e183-125">Continue typing your email message inserting the bookmark fields where desired.</span></span>  
9. <span data-ttu-id="9e183-126">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="9e183-126">Click Save.</span></span>

