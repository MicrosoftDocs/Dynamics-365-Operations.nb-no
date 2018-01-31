---
title: Utvide funksjonaliteten i Microsoft Dynamics 365 for Talent
description: Hvis du har opprettet en Microsoft PowerApps, kan du starte disse programmene fra koblinger i Microsoft Dynamics 365 for Talent.
author: rschloma
manager: AnnBe
ms.date: 11/28/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Talent
ms.custom: 17271
ms.assetid: ba1ad49d-8232-400e-b11f-525423506a3f
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2017-11-28
ms.dyn365.ops.version: Talent July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: ceea24519d641c676521771cee274feb64ca7783
ms.openlocfilehash: e1d0bbd71737001579218068e2ab0e02bc973f38
ms.contentlocale: nb-no
ms.lasthandoff: 01/31/2018

---
# <a name="extend-the-functionality-of-microsoft-dynamics-365-for-talent"></a><span data-ttu-id="0a9ec-103">Utvide funksjonaliteten i Microsoft Dynamics 365 for Talent</span><span class="sxs-lookup"><span data-stu-id="0a9ec-103">Extend the functionality of Microsoft Dynamics 365 for Talent</span></span>
<span data-ttu-id="0a9ec-104">Hvis du har opprettet en Microsoft PowerApps, kan du starte disse programmene fra koblinger i Microsoft Dynamics 365 for Talent.</span><span class="sxs-lookup"><span data-stu-id="0a9ec-104">If you’ve created any Microsoft PowerApps, you can start those applications from links within Microsoft Dynamics 365 for Talent.</span></span> <span data-ttu-id="0a9ec-105">Hvis du vil konfigurere tilgang til programmene, må du angi informasjon i Talent på en konfigurasjonsside som kan åpnes fra **Systemadministrasjon**-arbeidsområdet.</span><span class="sxs-lookup"><span data-stu-id="0a9ec-105">To set up access to your applications, you’ll need to set up some information in Talent on a configuration page that you can open from the **System administration** workspace.</span></span>

## <a name="configuring-embedded-powerapps-within-talent"></a><span data-ttu-id="0a9ec-106">Konfigurere innebygd PowerApps i Talent</span><span class="sxs-lookup"><span data-stu-id="0a9ec-106">Configuring embedded PowerApps within Talent</span></span>
<span data-ttu-id="0a9ec-107">Bruk **Angi innebygd Microsoft PowerApps**-siden til å konfigurere Talent-sider for å starte PowerApps-programmer.</span><span class="sxs-lookup"><span data-stu-id="0a9ec-107">Use the **Set embedded Microsoft PowerApps** page to configure Talent pages to start PowerApps applications.</span></span> <span data-ttu-id="0a9ec-108">Hvis du skal åpne **Angi innebygd Microsoft PowerApps**-siden, åpner du **Systemadministrasjon**-arbeidsområdet og åpner deretter **Koblinger**-fanen. Velg **Microsoft PowerApps** fra **Oppsett**-gruppen.</span><span class="sxs-lookup"><span data-stu-id="0a9ec-108">To open the **Set embedded Microsoft PowerApps** page, open the **System administration** workspace and then open the **Links** tab. Select **Microsoft PowerApps** from the **Setup** group.</span></span> 

<span data-ttu-id="0a9ec-109">Følgende informasjon angis på denne siden:</span><span class="sxs-lookup"><span data-stu-id="0a9ec-109">The following information is entered or set on this page:</span></span> 

> - <span data-ttu-id="0a9ec-110">Et beskrivende navn eller en identifikator for hver PowerApps-applikasjon.</span><span class="sxs-lookup"><span data-stu-id="0a9ec-110">A descriptive name or identifier for each PowerApps application.</span></span>
> - <span data-ttu-id="0a9ec-111">En unik identifikator (GUID) for hvert program som du legger til på en Talent-side.</span><span class="sxs-lookup"><span data-stu-id="0a9ec-111">A unique identifier (GUID) for each application that you add to a Talent page.</span></span> <span data-ttu-id="0a9ec-112">Program-ID-en er tilgjengelig på PowerApps-området [powerapps.com](http://powerapps.com/).</span><span class="sxs-lookup"><span data-stu-id="0a9ec-112">The app ID is available on the PowerApps site, [powerapps.com](http://powerapps.com/).</span></span> 
> - <span data-ttu-id="0a9ec-113">Siden som brukere kan åpne et program eller en rapport fra.</span><span class="sxs-lookup"><span data-stu-id="0a9ec-113">The page from which users can open an application or report.</span></span> <span data-ttu-id="0a9ec-114">Ikke alle Talent-sider støtter innebygde PowerApps- og Power BI-rapporter.</span><span class="sxs-lookup"><span data-stu-id="0a9ec-114">Not all Talent pages support embedded PowerApps and Power BI reports.</span></span> 

 > [!NOTE]
 >  <span data-ttu-id="0a9ec-115">Angi det interne navnet på siden, i stedet for visningsnavnet som vises øverst på siden.</span><span class="sxs-lookup"><span data-stu-id="0a9ec-115">Enter the internal name of the page, rather than the display name that appears at the top of the page.</span></span> <span data-ttu-id="0a9ec-116">Hvis du vil finne det interne navnet, åpner du siden som du trenger det interne navnet for, og høyreklikker hvor som helst på siden.</span><span class="sxs-lookup"><span data-stu-id="0a9ec-116">To find the internal name, open the page that you need the internal name of, and right-click anywhere on the page.</span></span> <span data-ttu-id="0a9ec-117">Når menyen åpnes, holder du pekeren over **Skjemainformasjon**-elementet.</span><span class="sxs-lookup"><span data-stu-id="0a9ec-117">When the menu opens, hover over the **Form information** item.</span></span> <span data-ttu-id="0a9ec-118">Det interne skjemanavnet vises ved siden av **Skjemainformasjon**-elementet på menyen.</span><span class="sxs-lookup"><span data-stu-id="0a9ec-118">The internal form name is displayed next to the **Form information** item in the menu.</span></span>
 
> - <span data-ttu-id="0a9ec-119">Angi skjemakontrollen som programmet kan hente kontekstdata fra.</span><span class="sxs-lookup"><span data-stu-id="0a9ec-119">Specify the form control from which the application can retrieve context data.</span></span> <span data-ttu-id="0a9ec-120">Et program kan for eksempel bruke data om en arbeider.</span><span class="sxs-lookup"><span data-stu-id="0a9ec-120">For example, an application might use data about a worker.</span></span> <span data-ttu-id="0a9ec-121">Hvis du angir **Arbeider**-siden i **Kontekst**-feltet, åpnes **Arbeider**-siden når du starter programmet.</span><span class="sxs-lookup"><span data-stu-id="0a9ec-121">If you enter the **Worker** page in the **Context** field, the **Worker** page will open when you start the application.</span></span> <span data-ttu-id="0a9ec-122">En oppføring i **Kontekstfelt** er valgfritt.</span><span class="sxs-lookup"><span data-stu-id="0a9ec-122">An entry in the **Context field** is optional.</span></span> 
> - <span data-ttu-id="0a9ec-123">Angi størrelsen på dialogboksen som PowerApps-programmet skal kjøre.</span><span class="sxs-lookup"><span data-stu-id="0a9ec-123">Set the size of the dialog box on which the PowerApps application will run.</span></span> <span data-ttu-id="0a9ec-124">Dialogboksene angis som "små" eller "stor" for å optimalisere brukergrensesnittet når programmet skal kjøre på en telefon eller en større enhet, henholdsvis.</span><span class="sxs-lookup"><span data-stu-id="0a9ec-124">The dialog boxes are designated as “small” or “large” to optimize the user interface when your application for running on a phone or a larger device, respectively.</span></span> 

<span data-ttu-id="0a9ec-125">Du kan også angi hvilke juridiske enheter et program skal være tilgjengelig for, eller du kan gjøre det tilgjengelig for alle dine juridiske enheter.</span><span class="sxs-lookup"><span data-stu-id="0a9ec-125">You can also specify which legal entities an application will be available for, or you can make it available to all your legal entities.</span></span> <span data-ttu-id="0a9ec-126">PowerApps-programmer er som standard tilgjengelige for alle juridiske enheter.</span><span class="sxs-lookup"><span data-stu-id="0a9ec-126">By default, your PowerApps applications are available to all legal entities.</span></span>

## <a name="opening-an-application"></a><span data-ttu-id="0a9ec-127">Åpne et program</span><span class="sxs-lookup"><span data-stu-id="0a9ec-127">Opening an application</span></span>
<span data-ttu-id="0a9ec-128">Når du har konfigurert innebygde PowerApps-programmer, legges koblinger til programmene du har angitt, på sidene i Talent.</span><span class="sxs-lookup"><span data-stu-id="0a9ec-128">When you’ve configured embedded PowerApps applications, links to the applications that you specified will be added to the pages within Talent.</span></span> <span data-ttu-id="0a9ec-129">Klikk på en kobling for å åpne et program.</span><span class="sxs-lookup"><span data-stu-id="0a9ec-129">Click a link to open an application.</span></span> 



