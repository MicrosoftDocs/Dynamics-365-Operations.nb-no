---
title: Innsjekking for plukkmodul
description: Dette emnet beskriver innsjekking for plukkmodul og forklarer hvordan du konfigurerer den i Microsoft Dynamics 365 Commerce.
author: bicyclingfool
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ROBOTS: ''
audience: Application user
ms.reviewer: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.author: stuharg
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 0baa922afc72778dd6e4836398a280cbe6abaec2
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/17/2021
ms.locfileid: "6270589"
---
# <a name="check-in-for-pickup-module"></a><span data-ttu-id="0787b-103">Innsjekking for plukkmodul</span><span class="sxs-lookup"><span data-stu-id="0787b-103">Check-in for pickup module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="0787b-104">Dette emnet beskriver innsjekking for plukkmodul og forklarer hvordan du konfigurerer den i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="0787b-104">This topic covers the check-in for pickup module and explains how to configure it in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="0787b-105">Innsjekkingen for plukkmodulen gir en bekreftelsesside for kunder som bruker Dynamics 365 Commerce-muligheten til å sjekke inn kunder for å varsle en butikk om ankomsten.</span><span class="sxs-lookup"><span data-stu-id="0787b-105">The check-in for pickup module provides a confirmation page for customers who use the Dynamics 365 Commerce customer check-in capabilities to notify a store about their arrival.</span></span> <span data-ttu-id="0787b-106">Ved hjelp av innsjekkingen for plukkmodulen kan du også konfigurere et skjema som samler inn tilleggsinformasjon fra kunder for å legge til rette for ordrelevering.</span><span class="sxs-lookup"><span data-stu-id="0787b-106">The check-in for pickup module also lets you configure a form that collects additional information from customers to facilitate order delivery.</span></span> <span data-ttu-id="0787b-107">Denne informasjonen omfatter kundens parkeringsplassnummer og merke og modell for kjøretøyet.</span><span class="sxs-lookup"><span data-stu-id="0787b-107">This information includes a customer's parking spot number, and the make and model of their vehicle.</span></span> 

## <a name="module-properties"></a><span data-ttu-id="0787b-108">Modulegenskaper</span><span class="sxs-lookup"><span data-stu-id="0787b-108">Module properties</span></span>

| <span data-ttu-id="0787b-109">Egenskapsnavn</span><span class="sxs-lookup"><span data-stu-id="0787b-109">Property name</span></span> | <span data-ttu-id="0787b-110">Verdier</span><span class="sxs-lookup"><span data-stu-id="0787b-110">Values</span></span> | <span data-ttu-id="0787b-111">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="0787b-111">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="0787b-112">Bekreftelsestekst</span><span class="sxs-lookup"><span data-stu-id="0787b-112">Confirmation text</span></span> | <span data-ttu-id="0787b-113">Tekststreng</span><span class="sxs-lookup"><span data-stu-id="0787b-113">Text string</span></span> | <span data-ttu-id="0787b-114">Innhold for overskriften som vises på bekreftelsessiden for innsjekking.</span><span class="sxs-lookup"><span data-stu-id="0787b-114">Content for the heading that appears on the check-in confirmation page.</span></span> |
| <span data-ttu-id="0787b-115">Vise QR-kode</span><span class="sxs-lookup"><span data-stu-id="0787b-115">Show QR code</span></span> | <span data-ttu-id="0787b-116">**Sann** eller **Usann**</span><span class="sxs-lookup"><span data-stu-id="0787b-116">**True** or **False**</span></span> | <span data-ttu-id="0787b-117">Når denne egenskapen er satt til **Sann**, viser innsjekkingsbekreftelsessiden en QR-kode som representerer ordrebekreftelses-IDen.</span><span class="sxs-lookup"><span data-stu-id="0787b-117">When this property is set to **True**, the check-in confirmation page shows a QR code that represents the order confirmation ID.</span></span> |
| <span data-ttu-id="0787b-118">Ekstra informasjonsoverskrift</span><span class="sxs-lookup"><span data-stu-id="0787b-118">Additional information heading</span></span> | <span data-ttu-id="0787b-119">Tekststreng</span><span class="sxs-lookup"><span data-stu-id="0787b-119">Text string</span></span> | <span data-ttu-id="0787b-120">Innhold for overskriften som vises når ekstra informasjonsfelt er konfigurert.</span><span class="sxs-lookup"><span data-stu-id="0787b-120">Content for the heading that appears when additional information fields have been configured.</span></span> |
| <span data-ttu-id="0787b-121">Ekstra informasjonsnøkler</span><span class="sxs-lookup"><span data-stu-id="0787b-121">Additional information keys</span></span> | <span data-ttu-id="0787b-122">Ressurs-ID/ressursverdipar</span><span class="sxs-lookup"><span data-stu-id="0787b-122">Resource ID/resource value pair</span></span> | <span data-ttu-id="0787b-123">Hver nøkkel oppretter et skjemafelt og en tilknyttet etikett som brukes til å samle inn tilleggsinformasjon fra kunder.</span><span class="sxs-lookup"><span data-stu-id="0787b-123">Each key creates a form field and an associated label that are used to collect additional information from customers.</span></span> |
| <span data-ttu-id="0787b-124">Ekstra informasjonsnøkler \> Ressurs-ID</span><span class="sxs-lookup"><span data-stu-id="0787b-124">Additional information keys \> Resource ID</span></span> | <span data-ttu-id="0787b-125">Tekststreng</span><span class="sxs-lookup"><span data-stu-id="0787b-125">Text string</span></span> | <span data-ttu-id="0787b-126">Hver informasjonsnøkkel oppretter et skjemafelt og en tilknyttet etikett som brukes til å samle inn tilleggsinformasjon fra kunder.</span><span class="sxs-lookup"><span data-stu-id="0787b-126">Each information key creates a form field and an associated label that are used to collect additional information from customers.</span></span> <span data-ttu-id="0787b-127">Denne egenskapen identifiserer den ekstra informasjonsnøkkelen.</span><span class="sxs-lookup"><span data-stu-id="0787b-127">This property identifies the additional information key.</span></span> <span data-ttu-id="0787b-128">I oppgaven som opprettes på salgsstedet (POS), vises verdien for denne egenskapen som etiketten i instruksjonene i feltet.</span><span class="sxs-lookup"><span data-stu-id="0787b-128">In the task that is created in point of sale (POS), the value of this property is shown as the label in the instructions field.</span></span> |
| <span data-ttu-id="0787b-129">Ekstra informasjonsnøkler \> Ressursverdi</span><span class="sxs-lookup"><span data-stu-id="0787b-129">Additional information keys \> Resource value</span></span> | <span data-ttu-id="0787b-130">Tekststreng</span><span class="sxs-lookup"><span data-stu-id="0787b-130">Text string</span></span> | <span data-ttu-id="0787b-131">Etiketten for tekstfeltet i oppgaven på salgsstedet.</span><span class="sxs-lookup"><span data-stu-id="0787b-131">The label for the text field in the task in POS.</span></span> |
| <span data-ttu-id="0787b-132">Ekstra informasjonsnøkler \> Påkrevd</span><span class="sxs-lookup"><span data-stu-id="0787b-132">Additional information keys \> Required</span></span> | <span data-ttu-id="0787b-133">**Sann** eller **Usann**</span><span class="sxs-lookup"><span data-stu-id="0787b-133">**True** or **False**</span></span> | <span data-ttu-id="0787b-134">Denne egenskapen angir om kunder må fylle ut skjemafeltet før de kan fortsette.</span><span class="sxs-lookup"><span data-stu-id="0787b-134">This property specifies whether customers must fill in the form field before they can continue.</span></span> <span data-ttu-id="0787b-135">Når denne egenskapen er satt til **Sann**, lages det en stjerne ved siden av skjemaetiketten, og det utføres en nullkontroll for å hindre at kundene fortsetter hvis ingen verdi angis.</span><span class="sxs-lookup"><span data-stu-id="0787b-135">When this property is set to **True**, an asterisk is rendered next to the form label, and a null check is done to prevent customers from continuing if no value is entered.</span></span> |

## <a name="add-the-check-in-for-pickup-module-to-a-page"></a><span data-ttu-id="0787b-136">Legge til innsjekkingen for plukkmodulen på en side</span><span class="sxs-lookup"><span data-stu-id="0787b-136">Add the check-in for pickup module to a page</span></span>

<span data-ttu-id="0787b-137">Innsjekkingen for plukkmodulen skal legges til på den nye siden du oppretter for innsjekkingsbekreftelse.</span><span class="sxs-lookup"><span data-stu-id="0787b-137">The check-in for pickup module should be added to the new page that you create for check-in confirmation.</span></span> <span data-ttu-id="0787b-138">Denne siden fungerer som innsjekkingsbekreftelseserfaring for kunder som velger **Jeg er her**-kobling eller -knapp i e-posten.</span><span class="sxs-lookup"><span data-stu-id="0787b-138">That page will serve as the check-in confirmation experience for customers who select the **I am here** link or button in their email.</span></span> 

## <a name="configure-the-additional-information-form"></a><span data-ttu-id="0787b-139">Konfigurere ekstra informasjonsskjema</span><span class="sxs-lookup"><span data-stu-id="0787b-139">Configure the additional information form</span></span>

<span data-ttu-id="0787b-140">Hvis ingen tilleggsinformasjonsnøkler er konfigurert, viser modulen som standard kundenes innsjekkingsbekreftelsesside.</span><span class="sxs-lookup"><span data-stu-id="0787b-140">By default, if no additional information keys are configured, the module shows customers the check-in confirmation page.</span></span> <span data-ttu-id="0787b-141">Når innsjekkingsbekreftelsen vises, opprettes det en oppgave på salgsstedet for butikken der ordren plukkes opp.</span><span class="sxs-lookup"><span data-stu-id="0787b-141">As the check-in confirmation is shown, a task is created in POS for the store where the order is being picked up.</span></span>

<span data-ttu-id="0787b-142">Når én eller flere informasjonsnøkler er konfigurert, blir kunder først bedt om å angi informasjon.</span><span class="sxs-lookup"><span data-stu-id="0787b-142">When one or more additional information keys are configured, customers are first prompted to enter information.</span></span> <span data-ttu-id="0787b-143">Når de velger **Send** ser de innsjekkingsbekreftelsen, og en oppgave blir opprettet på salgsstedet.</span><span class="sxs-lookup"><span data-stu-id="0787b-143">When they select **Submit**, they are shown the check-in confirmation, and a task is created in POS.</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="0787b-144">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="0787b-144">Additional resources</span></span>

[<span data-ttu-id="0787b-145">Aktivere innsjekkingsmeldinger for kunde på salgsstedet</span><span class="sxs-lookup"><span data-stu-id="0787b-145">Enable customer check-in notifications in point of sale (POS)</span></span>](enable-customer-check-in.md)
