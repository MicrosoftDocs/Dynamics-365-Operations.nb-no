---
title: Kontrollere at dobbel skriving er konfigurert i apper i Finance and Operations og Dataverse
description: Dette emnet forklarer hvordan du kan finne ut om dobbel skriving er konfigurert i Finance and Operations-apper og i Dataverse.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: f389bcf133cc7e6a086167d5e26c1b8795d0fa30
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/05/2020
ms.locfileid: "4685545"
---
# <a name="verify-that-dual-write-is-configured-in-finance-and-operations-apps-and-dataverse"></a><span data-ttu-id="13084-103">Kontrollere at dobbel skriving er konfigurert i apper i Finance and Operations og Dataverse</span><span class="sxs-lookup"><span data-stu-id="13084-103">Verify that dual-write is configured in Finance and Operations apps and Dataverse</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



<span data-ttu-id="13084-104">Dette emnet inneholder feilsøkingsinformasjon om dobbel skriving-integrasjon mellom Finance and Operations-apper og Dataverse.</span><span class="sxs-lookup"><span data-stu-id="13084-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Dataverse.</span></span> <span data-ttu-id="13084-105">Det forklarer særlig hvordan du kan finne ut om dobbel skriving er konfigurert i Finance and Operations-apper og i Dataverse.</span><span class="sxs-lookup"><span data-stu-id="13084-105">Specifically, it explains how you can determine whether dual-write is configured in Finance and Operations apps and in Dataverse.</span></span>

## <a name="verify-that-dual-write-is-configured-in-a-finance-and-operations-app"></a><span data-ttu-id="13084-106">Kontrollere at dobbel skriving er konfigurert i en Finance and Operations-app</span><span class="sxs-lookup"><span data-stu-id="13084-106">Verify that dual-write is configured in a Finance and Operations app</span></span>

<span data-ttu-id="13084-107">Hvis du vil finne ut om feilene du ser når du prøver å lagre rader for oppdatering, kommer fra dobbel skriving, må du først kontrollere at dobbel skriving er konfigurert.</span><span class="sxs-lookup"><span data-stu-id="13084-107">To determine whether the errors that you see when you try to save rows for update come from dual-write, first verify that dual-write is configured.</span></span>

+ <span data-ttu-id="13084-108">Hvis du har administratorrettigheter i Finance and Operations-appen, går du til **Arbeidsområder \> Databehandling** og velger **Dobbel skriving**-flisen.</span><span class="sxs-lookup"><span data-stu-id="13084-108">If you have admin privileges in the Finance and Operations app, go to **Workspaces \> Data management**, and select the **Dual-write** tile.</span></span> <span data-ttu-id="13084-109">Hvis detaljene for de koblede miljøene og listen over tabelltilordninger som kjører, vises, er dobbel skriving konfigurert.</span><span class="sxs-lookup"><span data-stu-id="13084-109">If the details of the linked environments and the list of table maps that are running are shown, dual-write is configured.</span></span>

    ![Kontrollere Finance and Operations-apptilkoblingen når du har administratorrettigheter](media/verify_fin_ops_1.png)

+ <span data-ttu-id="13084-111">Hvis du ikke har administratorrettigheter, får du feilmeldingen *Kan ikke skrive data til enhet \<entity name\>*.</span><span class="sxs-lookup"><span data-stu-id="13084-111">If you don't have admin privileges, you will receive an error message, *Unable to write data to entity \<entity name\>*.</span></span> <span data-ttu-id="13084-112">I eksemplet i illustrasjonen nedenfor kan du ikke opprette en kunderad i Finance and Operations-appen, fordi dobbel skriving er konfigurert, men referansedataene for kundegruppen og betalingsbetingelsene finnes ikke i Dataverse.</span><span class="sxs-lookup"><span data-stu-id="13084-112">In the example in the following illustration, you can't create a customer row in the Finance and Operations app, because dual-write is configured, but the customer group and payment terms reference data don't exist in Dataverse.</span></span>

    ![Kontrollere Finance and Operations-apptilkoblingen når du ikke har administratorrettigheter](media/verify_fin_ops_2.png)

<span data-ttu-id="13084-114">Hvis du vil ha informasjon om hvordan du løser problemer når du oppretter data i Finance and Operations-apper, kan du se [Feilsøke problemer med direkte synkronisering](dual-write-troubleshooting-live-sync.md).</span><span class="sxs-lookup"><span data-stu-id="13084-114">For information about how to fix issues when you create data in Finance and Operations apps, see [Troubleshoot live synchronization issues](dual-write-troubleshooting-live-sync.md).</span></span>

## <a name="verify-that-dual-write-is-configured-in-dataverse"></a><span data-ttu-id="13084-115">Kontrollere at dobbel skriving er konfigurert i Dataverse</span><span class="sxs-lookup"><span data-stu-id="13084-115">Verify that dual-write is configured in Dataverse</span></span>

<span data-ttu-id="13084-116">Når du oppretter data og ser **Firma**-feltet på sider i Dataverse, er dobbel skriving konfigurert.</span><span class="sxs-lookup"><span data-stu-id="13084-116">When you create data, if you see the **Company** field on pages in Dataverse, dual-write is configured.</span></span>

![Kontrollere Dataverse-tilkoblingen](media/verify_cds.png)

<span data-ttu-id="13084-118">Hvis du vil ha informasjon om hvordan du løser problemer når du oppretter data i Dataverse, kan du se [Feilsøke problemer med direkte synkronisering](dual-write-troubleshooting-live-sync.md).</span><span class="sxs-lookup"><span data-stu-id="13084-118">For information about how to fix issues when you create data in Dataverse, see [Troubleshoot live synchronization issues](dual-write-troubleshooting-live-sync.md).</span></span>

<span data-ttu-id="13084-119">Hvis du vil ha informasjon om hvordan du viser feildetaljer hvis det oppstår feil mens du oppretter data i Dataverse, kan du se [Aktivere og vise sporingsloggen for plugin-modul i Dataverse for å vise feildetaljer](dual-write-troubleshooting.md#enable-view-trace).</span><span class="sxs-lookup"><span data-stu-id="13084-119">For information about how to view error details if you encounter any errors while you create data in Dataverse, see [Enable and view the plug-in trace log in Dataverse to view error details](dual-write-troubleshooting.md#enable-view-trace).</span></span>
