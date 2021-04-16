---
title: Utvide Talent med Power Apps og Power Automate
description: Denne artikkelen beskriver noen eksempler på scenarioer for utvidelsesmuligheter for Microsoft Dynamics 365 Human Resources som bruker Microsoft Power Apps og Microsoft Power Automate.
author: negudava
ms.date: 02/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: negudava
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: ad55de4b660de89d323f32a1ce2911d880c24ec5
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5793567"
---
# <a name="extend-with-power-apps-and-power-automate"></a><span data-ttu-id="001ce-103">Utvide med Power Apps og Power Automate</span><span class="sxs-lookup"><span data-stu-id="001ce-103">Extend with Power Apps and Power Automate</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="001ce-104">Denne artikkelen beskriver noen eksempler på scenarioer for utvidelsesmuligheter for Microsoft Dynamics 365 Human Resources som bruker Microsoft Power Apps og Microsoft Power Automate.</span><span class="sxs-lookup"><span data-stu-id="001ce-104">This article describes some examples of extensibility scenarios for Microsoft Dynamics 365 Human Resources that use Microsoft Power Apps and Microsoft Power Automate.</span></span> <span data-ttu-id="001ce-105">Du kan importere løsningspakken som er tilknyttet hvert eksempel, i ditt Power Apps-miljø.</span><span class="sxs-lookup"><span data-stu-id="001ce-105">You can import the solution package that is associated with each example into your Power Apps environment.</span></span> <span data-ttu-id="001ce-106">Du kan deretter bruke pakkene som retningslinjer eller som utgangspunkt til å implementere scenarioene som gjelder for organisasjonen din.</span><span class="sxs-lookup"><span data-stu-id="001ce-106">You can then use the packages either as guidance or as starting points to implement scenarios that are applicable to your organization.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="001ce-107">Hvis du vil bruke malene og appene som er beskrevet i dette emnet, "som de er", må du teste dem å være sikker på at de dekker alle scenarioene som er spesifikke for implementeringen.</span><span class="sxs-lookup"><span data-stu-id="001ce-107">If you want to use the templates and apps that are described in this topic "as is," be sure to test them to make sure that they cover all the scenarios that are specific to your implementation.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="001ce-108">Forutsetninger</span><span class="sxs-lookup"><span data-stu-id="001ce-108">Prerequisites</span></span>

- <span data-ttu-id="001ce-109">Hvis du vil importere pakker, må brukerne ha **Miljøskaper**-tillatelsen.</span><span class="sxs-lookup"><span data-stu-id="001ce-109">To import packages, users must have the **Environment Maker** permission.</span></span>
- <span data-ttu-id="001ce-110">Hvis du vil eksportere eller importere apper, må brukerne ha en Power Apps Plan 2-lisens eller en Power Apps Plan 2-prøvelisens.</span><span class="sxs-lookup"><span data-stu-id="001ce-110">To export or import apps, users must have a Power Apps Plan 2 license or a Power Apps Plan 2 trial license.</span></span>

## <a name="integration-with-microsoft-365-power-automate"></a><span data-ttu-id="001ce-111">Integrering med Microsoft 365, Power Automate</span><span class="sxs-lookup"><span data-stu-id="001ce-111">Integration with Microsoft 365, Power Automate</span></span>

<span data-ttu-id="001ce-112">**Integrering med Microsoft 365**-appen kan brukes til å hente teaminformasjon for påloggede brukere fra Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="001ce-112">The **Integration with Microsoft 365** app can be used to extract team information for signed-in users from Microsoft 365.</span></span> <span data-ttu-id="001ce-113">Den refererer til arbeidere i Human Resources for å trekke ut identifikasjonstyper for ansatte.</span><span class="sxs-lookup"><span data-stu-id="001ce-113">It references workers in Human Resources to extract employee identification types.</span></span> <span data-ttu-id="001ce-114">Ledere kan kontrollere utløpsdatoer for ansatt-ID-typer.</span><span class="sxs-lookup"><span data-stu-id="001ce-114">Managers can check expiration dates of employee ID types.</span></span> <span data-ttu-id="001ce-115">De kan også sende en e-postpåminnelse hvis ansatt-ID-typen utløper.</span><span class="sxs-lookup"><span data-stu-id="001ce-115">They can also send an email reminder if the employee ID type is expiring.</span></span> <span data-ttu-id="001ce-116">Power Automate integreres med Power Apps for å sende denne påminnelsen.</span><span class="sxs-lookup"><span data-stu-id="001ce-116">Power Automate integrates with Power Apps to send this reminder.</span></span> <span data-ttu-id="001ce-117">Bekreftelse vil bli sendt tilbake til Power Apps fra Power Automate når påminnelsen sendes.</span><span class="sxs-lookup"><span data-stu-id="001ce-117">Confirmation will be sent back to Power Apps from Power Automate when the reminder is sent.</span></span> <span data-ttu-id="001ce-118">Identifikasjonstyper omfatter førerkort, pass og andre godkjente former for ID.</span><span class="sxs-lookup"><span data-stu-id="001ce-118">Identification types include driver's license, passport, and other acceptable forms of ID.</span></span>

<span data-ttu-id="001ce-119">Du kan utvide denne appen til andre scenarier.</span><span class="sxs-lookup"><span data-stu-id="001ce-119">You can extend this app for other scenarios.</span></span> <span data-ttu-id="001ce-120">Du kan for eksempel bruke den til å vise ferieinformasjon for team, kalenderhendelser og teamspesifikke hendelser.</span><span class="sxs-lookup"><span data-stu-id="001ce-120">For example, you can use it to show team vacation information, calendar events, and any team-specific events.</span></span>

<span data-ttu-id="001ce-121">Du kan laste ned appen for **integrering med Microsoft 365, Power Automate** ved å gå til [Integrering med Microsoft 365](https://go.microsoft.com/fwlink/?linkid=2081787) i Microsoft Download Center.</span><span class="sxs-lookup"><span data-stu-id="001ce-121">To download the **Integration with Microsoft 365, Power Automate** app, go to [Integration with Microsoft 365](https://go.microsoft.com/fwlink/?linkid=2081787) on the Microsoft Download Center.</span></span>

## <a name="power-automate--sql-connect-and-execute"></a><span data-ttu-id="001ce-122">Power Automate – SQL-tilkobling og kjøring</span><span class="sxs-lookup"><span data-stu-id="001ce-122">Power Automate – SQL Connect and execute</span></span>

<span data-ttu-id="001ce-123">Malen **Power Automate – SQL-tilkobling og kjøring** kobler til Microsoft SQL Server og aktiverer SQL-spørringer som skal kjøres.</span><span class="sxs-lookup"><span data-stu-id="001ce-123">The **Power Automate – SQL Connect and execute** template connects to Microsoft SQL Server and enables SQL queries to be run.</span></span>

<span data-ttu-id="001ce-124">Selv om denne malen leser og oppdaterer SQL-tabeller, kan du utvide den og bruke den i andre scenarioer.</span><span class="sxs-lookup"><span data-stu-id="001ce-124">Although this template reads and updates SQL tables, you can extend it and use it for other scenarios.</span></span> <span data-ttu-id="001ce-125">Du kan for eksempel bruke den til å fylle ut en oppsamlingstabell i Dataverse med poster fra SQL Server og synkronisere oppsamlingstabellen jevnlig ved hjelp av en trinnvis push fra SQL Server.</span><span class="sxs-lookup"><span data-stu-id="001ce-125">For example, you can use it to fill a staging table in Dataverse with records from SQL Server, and to periodically synchronize the staging table by using an incremental push from SQL Server.</span></span>

<span data-ttu-id="001ce-126">Avansert spørring integreres med flyt for å muliggjøre datatransformering og trinnvis push.</span><span class="sxs-lookup"><span data-stu-id="001ce-126">Advanced Query is integrated with Flow to enable Data transformation and incremental push.</span></span>

<span data-ttu-id="001ce-127">For å laste ned malen **Power Automate – SQL-tilkobling og kjøring** kan du gå til [Power Automate – SQL-tilkobling og kjøring](https://go.microsoft.com/fwlink/?linkid=2081789) på Microsoft Download Center.</span><span class="sxs-lookup"><span data-stu-id="001ce-127">To download the **Power Automate – SQL Connect and execute** template, go to [Power Automate – SQL Connect and execute](https://go.microsoft.com/fwlink/?linkid=2081789) on the Microsoft Download Center.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="001ce-128">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="001ce-128">Additional resources</span></span>

[<span data-ttu-id="001ce-129">Microsoft Power Platform</span><span class="sxs-lookup"><span data-stu-id="001ce-129">The Microsoft Power Platform</span></span>](https://docs.microsoft.com/power-platform/admin/admin-documentation)</br>

[!INCLUDE[footer-include](../includes/footer-banner.md)]