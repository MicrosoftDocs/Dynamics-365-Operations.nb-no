---
title: Hva er nytt eller endret i mobilappen Warehouse Management
description: Dette emnet inneholder en liste over de nye og endrede funksjonene for hver utgitte versjon av mobilappen Warehouse Management for Microsoft Dynamics 365 Supply Chain Management.
author: ivanv-microsoft
ms.date: 06/07/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ivanv
ms.search.validFrom: 2021-06-07
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 61124728942c0b8162de9f687ae752773c47d07e
ms.sourcegitcommit: 4cbd83e21a78459e4711a2dedba0f5a7acc3c841
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/15/2021
ms.locfileid: "6261792"
---
# <a name="whats-new-or-changed-in-the-warehouse-management-mobile-app"></a><span data-ttu-id="6d51b-103">Hva er nytt eller endret i mobilappen Warehouse Management</span><span class="sxs-lookup"><span data-stu-id="6d51b-103">What's new or changed in the Warehouse Management mobile app</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6d51b-104">Dette emnet inneholder en liste over nye funksjoner, reparasjoner, forbedringer og kjente problemer for hver utgitte versjon av mobilappen Warehouse Management for Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="6d51b-104">This topic lists new features, fixes, improvements, and known issues for each released version of the Warehouse Management mobile app for Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="version-2060"></a><span data-ttu-id="6d51b-105">Versjon 2.0.6.0</span><span class="sxs-lookup"><span data-stu-id="6d51b-105">Version 2.0.6.0</span></span>

### <a name="new-features-fixes-and-improvements-in-version-2060"></a><span data-ttu-id="6d51b-106">Nye funksjoner, reparasjoner og forbedringer i versjon 2.0.6.0</span><span class="sxs-lookup"><span data-stu-id="6d51b-106">New features, fixes, and improvements in version 2.0.6.0</span></span>

<span data-ttu-id="6d51b-107">Denne versjonen inneholder følgende nye funksjoner, reparasjoner og forbedringer:</span><span class="sxs-lookup"><span data-stu-id="6d51b-107">This version introduces the following new features, fixes, and improvements:</span></span>

- <span data-ttu-id="6d51b-108">Demomodus viser nå alle etikettene på enhetsspråket.</span><span class="sxs-lookup"><span data-stu-id="6d51b-108">Demo mode now shows all labels in the device language.</span></span>
- <span data-ttu-id="6d51b-109">Det er mindre sannsynlig at du får følgende feilmelding: "Finner ikke en passende visning for den angitte størrelsen."</span><span class="sxs-lookup"><span data-stu-id="6d51b-109">You're less likely to receive the following error message: "Cannot find a suitable view for the specified size."</span></span>
- <span data-ttu-id="6d51b-110">Minimumshøyden for arbeidskort er økt (for tilfeller der tre eller færre felt er konfigurert til å vises i arbeidslisten).</span><span class="sxs-lookup"><span data-stu-id="6d51b-110">The minimum height for work cards has been increased (for cases where three or fewer fields are configured to appear in the work list).</span></span>
- <span data-ttu-id="6d51b-111">Margene (tones ut) nederst på detaljkortene er forbedret.</span><span class="sxs-lookup"><span data-stu-id="6d51b-111">Margins (fade out) at the bottom of details cards have been improved.</span></span>
- <span data-ttu-id="6d51b-112">Ugyldige symboler i XML-filer som utveksles med serveren, håndteres nå på en elegant måte.</span><span class="sxs-lookup"><span data-stu-id="6d51b-112">Invalid symbols in XML files that are exchanged with the server are now handled gracefully.</span></span> <span data-ttu-id="6d51b-113">(Tegn som ikke kan skrives ut, håndteres nå elegant og fører ikke lenger til at appen slutter å svare.)</span><span class="sxs-lookup"><span data-stu-id="6d51b-113">(For example, non-printable characters are now handled gracefully and no longer cause the app to stop responding.)</span></span>
- <span data-ttu-id="6d51b-114">HTTP-feil (for eksempel "feil 503") når en serverforespørsel sendes, håndteres nå på en elegant måte.</span><span class="sxs-lookup"><span data-stu-id="6d51b-114">HTTP errors (such as "error 503") when a server request is submitted are now handled gracefully.</span></span>
- <span data-ttu-id="6d51b-115">Når det vises en feil, vises ikke lenger alternativlisten automatisk for kombinasjonsbokskontroller.</span><span class="sxs-lookup"><span data-stu-id="6d51b-115">While an error is being shown, the options list is no longer automatically shown for combo box controls.</span></span>
- <span data-ttu-id="6d51b-116">Appen slutter ikke lenger å svare på grunn av skjermretningen som er valgt i brukerinnstillinger.</span><span class="sxs-lookup"><span data-stu-id="6d51b-116">The app no longer stops responding because of the display orientation that is selected in user settings.</span></span>
- <span data-ttu-id="6d51b-117">Produktbilder vises nå i selvbetjeningsmiljøer.</span><span class="sxs-lookup"><span data-stu-id="6d51b-117">Product images are now shown in self-service environments.</span></span> <span data-ttu-id="6d51b-118">(Denne endringen gjelder bare versjoner med lav oppløsning.</span><span class="sxs-lookup"><span data-stu-id="6d51b-118">(This change applies to low-resolution versions only.</span></span> <span data-ttu-id="6d51b-119">Filbehandlingstjenesten støtter ikke bilder i full størrelse i selvbetjeningsmiljøer.)</span><span class="sxs-lookup"><span data-stu-id="6d51b-119">The file management service doesn't support full-sized images in self-service environments.)</span></span>
- <span data-ttu-id="6d51b-120">Et problem som involverte korte plukkinger med null antall, er løst.</span><span class="sxs-lookup"><span data-stu-id="6d51b-120">An issue that involved zero-quantity short picks has been fixed.</span></span>
- <span data-ttu-id="6d51b-121">Appen slutter ikke lenger å svare når et detaljkort viser flere identiske felt.</span><span class="sxs-lookup"><span data-stu-id="6d51b-121">The app no longer stops responding when a details card shows multiple identical fields.</span></span>

### <a name="known-issues-in-version-2060"></a><span data-ttu-id="6d51b-122">Kjente problemer i versjon 2.0.6.0</span><span class="sxs-lookup"><span data-stu-id="6d51b-122">Known issues in version 2.0.6.0</span></span>

<span data-ttu-id="6d51b-123">Følgende kjente problemer finnes i denne versjonen:</span><span class="sxs-lookup"><span data-stu-id="6d51b-123">The following known issues exist in this version:</span></span>

- <span data-ttu-id="6d51b-124">Appen (spesielt arbeidslisten) blir tregere over tid.</span><span class="sxs-lookup"><span data-stu-id="6d51b-124">The app (especially the work list) becomes slower over time.</span></span>
- <span data-ttu-id="6d51b-125">**Windows-versjon:** Når et USB-drev brukes til skanning på Windows, fører inkonsekvente resultater til at skannede symboler blandes sammen.</span><span class="sxs-lookup"><span data-stu-id="6d51b-125">**Windows version:** When a USB gun is used for scanning on Windows, inconsistent results cause scanned symbols to be mixed up.</span></span>

## <a name="version-2050"></a><span data-ttu-id="6d51b-126">Versjon 2.0.5.0</span><span class="sxs-lookup"><span data-stu-id="6d51b-126">Version 2.0.5.0</span></span>

<span data-ttu-id="6d51b-127">Denne versjonen inneholder følgende nye funksjoner, reparasjoner og forbedringer:</span><span class="sxs-lookup"><span data-stu-id="6d51b-127">This version introduces the following new features, fixes, and improvements:</span></span>

- <span data-ttu-id="6d51b-128">Klienthemmeligheten er ikke lenger skjult i installasjonsprogrammet for tilkoblingsinnstillinger.</span><span class="sxs-lookup"><span data-stu-id="6d51b-128">The client secret is no longer hidden in the connection settings setup.</span></span>
- <span data-ttu-id="6d51b-129">Du kan nå trykke lenge på hvilken som helst tekst for å se den fullt ut.</span><span class="sxs-lookup"><span data-stu-id="6d51b-129">You can now long-press on any text to see it fully.</span></span>
- <span data-ttu-id="6d51b-130">Feilmeldingen når lagringstillatelser mangler, er forbedret.</span><span class="sxs-lookup"><span data-stu-id="6d51b-130">The error message when storage permissions are missing has been improved.</span></span>
- <span data-ttu-id="6d51b-131">Nye kontrollsekvenser er lagt til for noen flyter.</span><span class="sxs-lookup"><span data-stu-id="6d51b-131">New control sequences have been added for some flows.</span></span>
- <span data-ttu-id="6d51b-132">Send-knappen blir ikke lenger tilgjengelig ved en feil på grunn av vindusstørrelsen.</span><span class="sxs-lookup"><span data-stu-id="6d51b-132">The submit button no longer incorrectly becomes available because of the window size.</span></span>
- <span data-ttu-id="6d51b-133">Glidebrytere kan nå fortsette på mindre skjermer når større knappestørrelser brukes.</span><span class="sxs-lookup"><span data-stu-id="6d51b-133">Sliders can now proceed on smaller screens when larger button sizes are used.</span></span>
- <span data-ttu-id="6d51b-134">Fireknappsoverlegget er ikke lenger avskåret.</span><span class="sxs-lookup"><span data-stu-id="6d51b-134">The four-button overlay is no longer cut off.</span></span>
- <span data-ttu-id="6d51b-135">Tastaturet støtter nå sletteknappen.</span><span class="sxs-lookup"><span data-stu-id="6d51b-135">The keyboard now supports the delete button.</span></span>
- <span data-ttu-id="6d51b-136">Et problem med lysstyrken som kan oppstå når du trykker på tastaturet, er løst.</span><span class="sxs-lookup"><span data-stu-id="6d51b-136">A brightness issue that could occur when the keyboard is pressed has been fixed.</span></span>
- <span data-ttu-id="6d51b-137">Ulike demodataproblemer er løst.</span><span class="sxs-lookup"><span data-stu-id="6d51b-137">Various demo data issues have been fixed.</span></span>
- <span data-ttu-id="6d51b-138">Et problem som påvirket numeriske felt på detaljsiden, er løst.</span><span class="sxs-lookup"><span data-stu-id="6d51b-138">An issue that affected numeric fields on the details page has been fixed.</span></span>
- <span data-ttu-id="6d51b-139">Skjermtastaturet forsvinner ikke lenger enkelte ganger på noen enheter.</span><span class="sxs-lookup"><span data-stu-id="6d51b-139">The screen keyboard no longer occasionally disappears on some devices.</span></span>
- <span data-ttu-id="6d51b-140">Ulike brukergrensesnittfeil er rettet, for eksempel feil som påvirket bakgrunnsfargen og plasseringen.</span><span class="sxs-lookup"><span data-stu-id="6d51b-140">Various user interface (UI) bugs have been fixed, such as bugs that affected the background color and positioning.</span></span>
- <span data-ttu-id="6d51b-141">Det russiskspråklige brukergrensesnittet er forbedret.</span><span class="sxs-lookup"><span data-stu-id="6d51b-141">The Russian-language UI has been improved.</span></span>
- <span data-ttu-id="6d51b-142">Ulike problemer som førte til at systemet sluttet å svare, er løst.</span><span class="sxs-lookup"><span data-stu-id="6d51b-142">Various issues that caused the system to stop responding have been fixed.</span></span>
- <span data-ttu-id="6d51b-143">Et problem som var relatert til å åpne kalkulatoren på nytt, er løst.</span><span class="sxs-lookup"><span data-stu-id="6d51b-143">An issue that was related to reopening the calculator has been fixed.</span></span>
- <span data-ttu-id="6d51b-144">**Android-versjon:** Et problem som førte til at Android 4.4 sluttet å svare ved oppstart, er løst.</span><span class="sxs-lookup"><span data-stu-id="6d51b-144">**Android version:** An issue that caused Android 4.4 to stop responding on startup has been fixed.</span></span>
- <span data-ttu-id="6d51b-145">**Android-versjon:** Minimumsskalering er redusert til 50 prosent.</span><span class="sxs-lookup"><span data-stu-id="6d51b-145">**Android version:** Minimum scaling has been reduced to 50 percent.</span></span>

## <a name="version-2040"></a><span data-ttu-id="6d51b-146">Versjon 2.0.4.0</span><span class="sxs-lookup"><span data-stu-id="6d51b-146">Version 2.0.4.0</span></span>

<span data-ttu-id="6d51b-147">Versjon 2.0.4.0 var den første generelt tilgjengelige utgivelsen av Warehouse Management-mobilappen.</span><span class="sxs-lookup"><span data-stu-id="6d51b-147">Version 2.0.4.0 was the first generally available release of the Warehouse Management mobile app.</span></span>

### <a name="new-features-fixes-and-improvements-in-version-2040"></a><span data-ttu-id="6d51b-148">Nye funksjoner, reparasjoner og forbedringer i versjon 2.0.4.0</span><span class="sxs-lookup"><span data-stu-id="6d51b-148">New features, fixes, and improvements in version 2.0.4.0</span></span>

<span data-ttu-id="6d51b-149">Denne versjonen introduserer følgende nye funksjoner, reparasjoner og forbedringer som ikke var tilgjengelige i forhåndsvisningsversjonen:</span><span class="sxs-lookup"><span data-stu-id="6d51b-149">This version introduces the following new features, fixes, and improvements that weren't available in the preview version:</span></span>

- <span data-ttu-id="6d51b-150">Hvis et detaljkort inneholder to etiketter som har identiske data, skjules en av etikettene.</span><span class="sxs-lookup"><span data-stu-id="6d51b-150">If a details card includes two labels that have identical data, one of the labels is hidden.</span></span>
- <span data-ttu-id="6d51b-151">Spesialtegn vises nå som standard, og alternativet for å skjule dem er fjernet fra brukerinnstillingene.</span><span class="sxs-lookup"><span data-stu-id="6d51b-151">Special characters are now shown by default, and the option to hide them has been removed from user settings.</span></span>
- <span data-ttu-id="6d51b-152">Deaktiverte send-knapper vises nå som ikke tilgjengelige i kompakt armholdt visning.</span><span class="sxs-lookup"><span data-stu-id="6d51b-152">Disabled submit buttons are now shown as unavailable in compact arm-held view.</span></span>
- <span data-ttu-id="6d51b-153">En endring i sekvenseringslogikken for kontroller sikrer jevnere skalering på tvers av enheter.</span><span class="sxs-lookup"><span data-stu-id="6d51b-153">A change to the sequencing logic for controls ensures smoother scaling across devices.</span></span> <span data-ttu-id="6d51b-154">Derfor er det mindre behov for å justere skaleringen av skrifter eller knapper.</span><span class="sxs-lookup"><span data-stu-id="6d51b-154">Therefore, there is less need to adjust the scaling of fonts or buttons.</span></span>
- <span data-ttu-id="6d51b-155">Standard fargetema er endret til *Mørk*.</span><span class="sxs-lookup"><span data-stu-id="6d51b-155">The default color theme has been changed to *Dark*.</span></span>
- <span data-ttu-id="6d51b-156">Det manglende ikonet for den deaktiverte Send-knappen er lagt til i båndvisning.</span><span class="sxs-lookup"><span data-stu-id="6d51b-156">The missing icon for the disabled submit button has been added in ribbon view.</span></span>
- <span data-ttu-id="6d51b-157">Tidsavbruddsunntak tar deg nå til tilkoblingssiden i stedet for å vise en innebygd feil.</span><span class="sxs-lookup"><span data-stu-id="6d51b-157">Time-out exceptions now take you to the connection page instead of showing an in-line error.</span></span>
- <span data-ttu-id="6d51b-158">Hvis ingen sendehandling er tilgjengelig (for eksempel **OK**, **Ja**, **Godta**, **Ferdig** eller **Ferdig**), deaktiveres Send-knappen.</span><span class="sxs-lookup"><span data-stu-id="6d51b-158">If no submit action is available (such as **OK**, **Yes**, **Accept**, **Done**, or **Finished**), the submit button will be disabled.</span></span>
- <span data-ttu-id="6d51b-159">Appstabiliteten er forbedret.</span><span class="sxs-lookup"><span data-stu-id="6d51b-159">App stability has been improved.</span></span>
- <span data-ttu-id="6d51b-160">Det finnes en hurtigreparasjon for sikkerhetsproblemet [CVE-2021-26701](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-26701).</span><span class="sxs-lookup"><span data-stu-id="6d51b-160">There is a fix for security vulnerability [CVE-2021-26701](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-26701).</span></span>
- <span data-ttu-id="6d51b-161">**Windows-versjon:** Et problem på Windows, der menyer ikke reagerte etter at vinduet ble endret, er løst.</span><span class="sxs-lookup"><span data-stu-id="6d51b-161">**Windows version:** An issue on Windows, where menus were unresponsive after the window was resized, has been fixed.</span></span>

### <a name="known-issue-in-version-2040"></a><span data-ttu-id="6d51b-162">Kjent problem i versjon 2.0.4.0</span><span class="sxs-lookup"><span data-stu-id="6d51b-162">Known issue in version 2.0.4.0</span></span>

<span data-ttu-id="6d51b-163">Følgende kjente problem finnes i denne versjonen:</span><span class="sxs-lookup"><span data-stu-id="6d51b-163">The following known issue exists in this version:</span></span>

- <span data-ttu-id="6d51b-164">Denne versjonen har et problem med enheter som bruker Android 4.4.</span><span class="sxs-lookup"><span data-stu-id="6d51b-164">This version has an issue with devices that use Android 4.4.</span></span> <span data-ttu-id="6d51b-165">Det kan oppstå problemer når du bruker appen på denne Android-versjonen.</span><span class="sxs-lookup"><span data-stu-id="6d51b-165">You might experience issues when you use the app on this Android version.</span></span>
