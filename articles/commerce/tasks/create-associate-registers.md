---
title: " Opprette og tilknytte kasser"
description: Denne fremgangsmåten beskriver hvordan du oppretter en kasse for et salgssted (POS).
author: rubencdelgado
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: RetailTerminalTable
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ba978a3d895394760687386197dbb3512c62ef98
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5798567"
---
# <a name="create-and-associate-registers"></a><span data-ttu-id="adf23-103"> Opprette og tilknytte kasser</span><span class="sxs-lookup"><span data-stu-id="adf23-103">Create and associate registers</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="adf23-104">Denne fremgangsmåten beskriver hvordan du oppretter en kasse for et salgssted (POS).</span><span class="sxs-lookup"><span data-stu-id="adf23-104">This procedure demonstrates how to create a point of sale (POS) register.</span></span> <span data-ttu-id="adf23-105">Denne prosedyren bruker demonstrasjonsdatafirmaet USRT.</span><span class="sxs-lookup"><span data-stu-id="adf23-105">This procedure uses the demo data company USRT.</span></span>

1. <span data-ttu-id="adf23-106">Gå til Detaljhandel og handel > Kanaloppsett > Salgsstedsoppsett > Kasser.</span><span class="sxs-lookup"><span data-stu-id="adf23-106">Go to Retail and Commerce > Channel setup > POS setup > Registers.</span></span>
2. <span data-ttu-id="adf23-107">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="adf23-107">Click New.</span></span>
3. <span data-ttu-id="adf23-108">I Kassenummer-feltet skriver du inn en ID for den nye kassen.</span><span class="sxs-lookup"><span data-stu-id="adf23-108">In the Register number field, type an ID for the new register.</span></span>
    * <span data-ttu-id="adf23-109">Kasse-ID-en inneholder vanligvis koder som bidrar til å tilordne kassen til butikken den tilhører, og plasseringen i butikken.</span><span class="sxs-lookup"><span data-stu-id="adf23-109">The register ID typically includes codes that help map the register to the store to which it belongs, and the location within the store.</span></span>  
4. <span data-ttu-id="adf23-110">I Navn-feltet skriver du inn et beskrivende navn på kassen.</span><span class="sxs-lookup"><span data-stu-id="adf23-110">In the Name field, type a descriptive name for the register..</span></span>
5. <span data-ttu-id="adf23-111">Angi eller velg en verdi i Butikknummer-feltet.</span><span class="sxs-lookup"><span data-stu-id="adf23-111">In the Store number field, enter or select a value.</span></span>
6. <span data-ttu-id="adf23-112">Angi eller velg en verdi i Maskinvareprofil-feltet.</span><span class="sxs-lookup"><span data-stu-id="adf23-112">In the Hardware profile field, enter or select a value.</span></span>
    * <span data-ttu-id="adf23-113">Maskinvareprofiler brukes til å angi eksterne enheter som skal kobles til kassen, for eksempel kassaskuffen og kvitteringsskriveren.</span><span class="sxs-lookup"><span data-stu-id="adf23-113">Hardware profiles are used to specify the peripherals that will be connected to the register, such as cash drawer and receipt printer.</span></span>  
7. <span data-ttu-id="adf23-114">Angi eller velg en verdi i Visuell profil-feltet.</span><span class="sxs-lookup"><span data-stu-id="adf23-114">In the Visual profile field, enter or select a value.</span></span>
    * <span data-ttu-id="adf23-115">Visuelle profiler brukes til å angi bildene som brukes på bakgrunnen og påloggingssiden for salgsstedet, samt oppsett for salgsstedet.</span><span class="sxs-lookup"><span data-stu-id="adf23-115">Visual profiles are used to specify the images used in the POS background and login page as well as themes for the POS.</span></span>  
8. <span data-ttu-id="adf23-116">Skriv inn en verdi i feltet EFT-registreringsnummer for POS.</span><span class="sxs-lookup"><span data-stu-id="adf23-116">In the EFT POS register number field, type a value.</span></span>
    * <span data-ttu-id="adf23-117">EFT-registreringsnummeret for POS brukes til å informere betalingprosessoren om hvilken betalingsterminal som sender forespørsler om godkjenning.</span><span class="sxs-lookup"><span data-stu-id="adf23-117">The EFT POS register number is used to inform the payment processor which payment terminal is sending authorization requests.</span></span> <span data-ttu-id="adf23-118">Denne verdien kalles ofte Terminal-ID eller TID.</span><span class="sxs-lookup"><span data-stu-id="adf23-118">This value is often called the "Terminal ID" or "TID".</span></span> <span data-ttu-id="adf23-119">TID finnes vanligvis på et klistremerke på betalingsenheten.</span><span class="sxs-lookup"><span data-stu-id="adf23-119">The TID can generally be found on a sticker on the payment device.</span></span>  
9. <span data-ttu-id="adf23-120">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="adf23-120">Click Save.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]