---
title: Betalingsseddelrapport for Europa
description: Dette emnet gir informasjon om betalingsseddelrapport for Europa.
author: EvgenyPopovMBS
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: OMLegalEntities, ProjFormletterParameters, CustFormletterParameters
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 264604
ms.search.region: Belgium, Denmark, Finland, Norway, Switzerland
ms.author: epopov
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 213cabd17b24471cfc4657a433c7ad02ac03b24a
ms.contentlocale: nb-no
ms.lasthandoff: 04/13/2018

---

# <a name="payment-slip-report-for-europe"></a><span data-ttu-id="d9376-103">Betalingsseddelrapport for Europa</span><span class="sxs-lookup"><span data-stu-id="d9376-103">Payment slip report for Europe</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="d9376-104">Dette emnet gir informasjon om betalingsseddelrapport for Europa.</span><span class="sxs-lookup"><span data-stu-id="d9376-104">This topic provides information about payment slip reports for Europe.</span></span>

<span data-ttu-id="d9376-105">Funksjonaliteten for betalingsseddelrapport er tilgjengelig for juridiske enheter som har den primære adressen i Danmark, Belgia, Norge, Sveits og Finland.</span><span class="sxs-lookup"><span data-stu-id="d9376-105">The functionality for payment slip reports is available for legal entities that have their primary address in Denmark, Belgium, Norway, Switzerland, or Finland.</span></span> <span data-ttu-id="d9376-106">Bedrifter knytter ofte utskrevne betalingsbilag til fakturaer som skal gi en betalingsreferanse for postering og utligning.</span><span class="sxs-lookup"><span data-stu-id="d9376-106">Businesses often attach printed payment slips to invoices to provide a payment reference for posting and settlement.</span></span> <span data-ttu-id="d9376-107">Betalingsbilaget kan brukes til prosjekt- eller tjenestefakturaer, purringer, rentenotaer og kontoutdrag, i tillegg til salgsfakturaer og fritekstfakturaer.</span><span class="sxs-lookup"><span data-stu-id="d9376-107">The payment slip can be used for project or service invoices, collection letters, interest notes, and account statements, in addition to sales invoices and free text invoices.</span></span>

## <a name="set-up-a-creditor-id-number-denmark-only"></a><span data-ttu-id="d9376-108">Definere et ID-nummer for kreditor (bare Danmark)</span><span class="sxs-lookup"><span data-stu-id="d9376-108">Set up a creditor ID number (Denmark only)</span></span>
<span data-ttu-id="d9376-109">Følg disse trinnene for å angi firmakreditorens identifikasjonsnummer.</span><span class="sxs-lookup"><span data-stu-id="d9376-109">Follow these steps to enter your company's creditor identification (ID) number.</span></span> <span data-ttu-id="d9376-110">Finansinstitusjonen gir dette nummeret.</span><span class="sxs-lookup"><span data-stu-id="d9376-110">Your financial institution provides this number.</span></span> <span data-ttu-id="d9376-111">Dette nummeret brukes som referanse når du mottar kundebetalinger via finansinstitusjoner.</span><span class="sxs-lookup"><span data-stu-id="d9376-111">It's used as a reference when customer payments are received through financial institutions.</span></span>

1.  <span data-ttu-id="d9376-112">Klikk **Organisasjonsstyring** &gt; **Oppsett** &gt; **Organisasjon** &gt; **Juridiske enheter**.</span><span class="sxs-lookup"><span data-stu-id="d9376-112">Click **Organization administration** &gt; **Setup** &gt; **Organization** &gt; **Legal entities**.</span></span>
2.  <span data-ttu-id="d9376-113">På hurtigfanen **Bankkontoinformasjon** i feltet **ID for FI-kreditor** angir du det unike 8-sifrede ID-nummeret for kreditoren.</span><span class="sxs-lookup"><span data-stu-id="d9376-113">On the **Bank account information** FastTab, in the **FI-Creditor ID** field, enter your unique eight-digit creditor ID number.</span></span>
3.  <span data-ttu-id="d9376-114">Lukk skjemaet for å lagre endringene.</span><span class="sxs-lookup"><span data-stu-id="d9376-114">Close the form to save your changes.</span></span>

## <a name="set-up-a-payment-slip-attachment-format-for-invoices-interest-notes-collection-letters-and-account-statements"></a><span data-ttu-id="d9376-115">Definere et format for betalingsseddelvedlegg for fakturaer, rentenotaer, purrebrev og kontoutdrag</span><span class="sxs-lookup"><span data-stu-id="d9376-115">Set up a payment slip attachment format for invoices, interest notes, collection letters, and account statements</span></span>
<span data-ttu-id="d9376-116">Følg denne fremgangsmåten for å definere et format for et betalingsbilagsvedlegg for salgsfakturaer, fritekstfakturaer, rentenotaer, purringer og kontoutdrag.</span><span class="sxs-lookup"><span data-stu-id="d9376-116">Follow these steps to set up a format for payment slip attachments that accompany sales invoices, free text invoices, interest notes, collection letters, and account statements.</span></span>

1.  <span data-ttu-id="d9376-117">Klikk **Kunder** &gt; **Oppsett** &gt; **Skjemaer** &gt; **Skjemaoppsett**.</span><span class="sxs-lookup"><span data-stu-id="d9376-117">Click **Accounts receivable** &gt; **Setup** &gt; **Forms** &gt; **Form setup**.</span></span>
2.  <span data-ttu-id="d9376-118">Velg format for betalingsseddelvedlegg i **Faktura**-kategorien i feltet **Tilknyttet betalingsvedlegg på kundefaktura**.</span><span class="sxs-lookup"><span data-stu-id="d9376-118">On the **Invoice** tab, in the **Associated payment attachment on customer invoice** field, select the payment slip attachment format.</span></span>
3.  <span data-ttu-id="d9376-119">Velg et format for betalingsseddelvedlegg for hver dokumenttype i kategoriene **Fritekstfaktura**, **Rentenota**, **Purring** og **Kontoutdrag**.</span><span class="sxs-lookup"><span data-stu-id="d9376-119">On the **Free text invoice**, **Interest note**, **Collection letter**, and **Account statement** tabs, select a payment slip attachment format for each document type.</span></span>
4.  <span data-ttu-id="d9376-120">Lukk skjemaet for å lagre endringene.</span><span class="sxs-lookup"><span data-stu-id="d9376-120">Close the form to save your changes.</span></span>

<span data-ttu-id="d9376-121">Følg denne fremgangsmåten for å definere et format for et betalingsseddelvedlegg som skal følge prosjektfakturaer.</span><span class="sxs-lookup"><span data-stu-id="d9376-121">Follow these steps to set up a format for payment slip attachments that accompany project invoices.</span></span>

1.  <span data-ttu-id="d9376-122">Klikk på **Prosjektstyring og regnskap** &gt; **Oppsett** &gt; **Skjemaer** &gt; **Skjemaoppsett**.</span><span class="sxs-lookup"><span data-stu-id="d9376-122">Click **Project management and accounting** &gt; **Setup** &gt; **Forms** &gt; **Form setup**.</span></span>
2.  <span data-ttu-id="d9376-123">I feltet **Tilknyttet betalingsvedlegg** velger du format for betalingsseddelvedlegg.</span><span class="sxs-lookup"><span data-stu-id="d9376-123">In the **Associated payment attachment** field, select the payment slip attachment format.</span></span>

## <a name="assign-a-payment-slip-attachment-format-to-a-customer-account"></a><span data-ttu-id="d9376-124">Tilordne et format for betalingsseddelvedlegg til en kundekonto</span><span class="sxs-lookup"><span data-stu-id="d9376-124">Assign a payment slip attachment format to a customer account</span></span>
<span data-ttu-id="d9376-125">Når du har satt opp formatet for betalingsseddelvedlegg for salgsfakturaer, fritekstfakturaer, rentenotaer, purringer, kontoutdrag og prosjektfakturaer, kan du tilordne bestemte formater for en valgt kunde.</span><span class="sxs-lookup"><span data-stu-id="d9376-125">After you set up the payment slip attachment format for sales invoices, free text invoices, interest notes, collection letters, account statements, and project invoices, you can assign specific formats for a selected customer.</span></span>

1.  <span data-ttu-id="d9376-126">Klikk **Kunder** &gt; **Felles** &gt; **Kunder** &gt; **Alle kunder**.</span><span class="sxs-lookup"><span data-stu-id="d9376-126">Click **Accounts receivable** &gt; **Common** &gt; **Customers** &gt; **All customers**.</span></span>
2.  <span data-ttu-id="d9376-127">Opprett en ny kunde, eller velg en eksisterende kunde.</span><span class="sxs-lookup"><span data-stu-id="d9376-127">Create a new customer, or select an existing customer.</span></span>
3.  <span data-ttu-id="d9376-128">På hurtigfanen **Faktura og levering** i feltene **På en kundefaktura**, **På en fritekstfaktura**, **På en rentenota**, **På en purring**, **På en prosjektfaktura** og **På et kontoutdrag**, velger du formatet for betalingsseddelvedlegg som skal følge dokumenter for hver type som sendes til den valgte kunden.</span><span class="sxs-lookup"><span data-stu-id="d9376-128">On the **Invoice and delivery** FastTab, in the **On a customer invoice**, **On a free text invoice**, **On an interest note**, **On a collection letter**, **On a project invoice**, and **On an account statement** fields, select the format for payment slip attachments that will accompany documents of each type that are sent to the selected customer.</span></span>
4.  <span data-ttu-id="d9376-129">Lukk skjemaet for å lagre endringene.</span><span class="sxs-lookup"><span data-stu-id="d9376-129">Close the form to save your changes.</span></span>





