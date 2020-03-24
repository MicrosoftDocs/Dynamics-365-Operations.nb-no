---
title: Periodiske oppgaver for kredittbehandling
description: Dette emnet beskriver de periodiske oppgavene som er en nødvendig del av prosessen for å behandle kredittgrenser for kunder.
author: mikefalkner
manager: AnnBe
ms.date: 09/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschloma
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 4ca9bb7f77283ec30d4648d6763f4156494050ac
ms.sourcegitcommit: 1d5a4f70a931e78b06811add97c1962e8d93689b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/13/2020
ms.locfileid: "3124168"
---
# <a name="periodic-credit-management-tasks"></a><span data-ttu-id="1371a-103">Periodiske oppgaver for kredittstyring</span><span class="sxs-lookup"><span data-stu-id="1371a-103">Periodic credit management tasks</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1371a-104">Dette emnet beskriver de periodiske oppgavene som er en nødvendig del av prosessen for å behandle kredittgrenser for kunder.</span><span class="sxs-lookup"><span data-stu-id="1371a-104">This topic describes the periodic tasks that are a necessary part of the process of managing credit limits for customers.</span></span>

## <a name="update-risk-scores"></a><span data-ttu-id="1371a-105">Oppdater risikopoeng</span><span class="sxs-lookup"><span data-stu-id="1371a-105">Update risk scores</span></span>

<span data-ttu-id="1371a-106">Ettersom selskaper utvikler seg og forhold endres, kan kredittrisiko for en gitt kunde også endre seg.</span><span class="sxs-lookup"><span data-stu-id="1371a-106">As businesses evolve and circumstances change, the credit risks for a given customer can also change.</span></span> <span data-ttu-id="1371a-107">Hvis du vil ha hjelp til å vedlikeholde riktige kredittgrenser for kundene, må du jevnlig gå gjennom kriteriene for hver risikopoengsum og oppdatere resultatene for hver kunde.</span><span class="sxs-lookup"><span data-stu-id="1371a-107">To help maintain appropriate credit limits for your customers, you must periodically review the criteria for each risk score and update the scores for each customer.</span></span> <span data-ttu-id="1371a-108">Du kan oppdatere følgende resultater ved å bruke siden **Oppdater risikopoeng** (**Kreditt og innkreving \> Periodiske oppgaver \> Kredittbehandling \> Oppdater risikopoeng**).</span><span class="sxs-lookup"><span data-stu-id="1371a-108">You can update the following scores by using the **Update risk scores** page (**Credit and collections \> Periodic tasks \> Credit management \> Update risk scores**).</span></span> <span data-ttu-id="1371a-109">Alle brukerdefinerte beregninger blir også behandlet.</span><span class="sxs-lookup"><span data-stu-id="1371a-109">All user-defined calculations are also processed.</span></span>

- <span data-ttu-id="1371a-110">**Gjennomsnittlig betalingsdager** – Denne poengsummen er gjennomsnittlig antall dager en kunde bruker for å betale fakturaer.</span><span class="sxs-lookup"><span data-stu-id="1371a-110">**Average payment days** – This score is the average number of days that a customer takes to pay invoices.</span></span>
- <span data-ttu-id="1371a-111">**Kunde siden** – Denne poengsummen er antall år en kunde har vært kunde i organisasjonen.</span><span class="sxs-lookup"><span data-stu-id="1371a-111">**Customer since** – This score is the number of years that a customer has been a customer of your organization.</span></span>
- <span data-ttu-id="1371a-112">**Drevet virksomhet siden** – Denne poengsummen er antall år en kunde har drevet virksomhet.</span><span class="sxs-lookup"><span data-stu-id="1371a-112">**In business since** – This score is the number of years that a customer has been in business.</span></span> <span data-ttu-id="1371a-113">Den bruker verdien i feltet **Forretningsstart** på **Kunder**-siden.</span><span class="sxs-lookup"><span data-stu-id="1371a-113">It uses the value of the **Business start** field on the **Customers** page.</span></span>
- <span data-ttu-id="1371a-114">**Dager utestående salg** – Denne poengsummen er basert på kundesaldoen, salgsinntekter og antall dager i forrige 12-månedersperiode.</span><span class="sxs-lookup"><span data-stu-id="1371a-114">**Days sales outstanding** – This score is based on the accounts receivable balance, sales revenue, and number of days for the previous 12-month period.</span></span>
- <span data-ttu-id="1371a-115">**Gjennomsnittlig saldo**– Denne poengsummen er basert på kundesaldoen for forrige 12-månedersperiode.</span><span class="sxs-lookup"><span data-stu-id="1371a-115">**Average balance** – This score is based on the accounts receivable balance for the previous 12-month period.</span></span>
- <span data-ttu-id="1371a-116">**Kredittbehandlingsgruppe**, **Kontostatus** og **Land** – Disse resultatene bruker informasjon fra kunden.</span><span class="sxs-lookup"><span data-stu-id="1371a-116">**Credit management group**, **Account status**, and **Country** – These scores use information from the customer.</span></span>

## <a name="update-customer-balance-statistics"></a><span data-ttu-id="1371a-117">Oppdatere kundesaldostatistikk</span><span class="sxs-lookup"><span data-stu-id="1371a-117">Update customer balance statistics</span></span>

<span data-ttu-id="1371a-118">Du kan kjøre prosessen **Oppdater kundesaldostatistikk** for å oppdatere beregningen av saldostatistikk som vises på siden **Forespørsel om saldostatistikk**.</span><span class="sxs-lookup"><span data-stu-id="1371a-118">You can run the **Update customer balance statistics** process to update the calculation of balance statistics that is shown on the **Balance statistics inquiry** page.</span></span> <span data-ttu-id="1371a-119">Denne informasjonen brukes til å beregne risikoresultater og verdiene som vises i faktaboksene for kredittstatistikk på **Kunde**-siden.</span><span class="sxs-lookup"><span data-stu-id="1371a-119">This information is used to calculate risk scores and the values that are shown in the credit statistics FactBoxes on the **Customer** page.</span></span>

<span data-ttu-id="1371a-120">Når du kjører prosessen, oppdaterer den kundesaldostatistikk for en enkelt kunde.</span><span class="sxs-lookup"><span data-stu-id="1371a-120">When you run the process, it updates customer balance statistics for a single customer.</span></span> <span data-ttu-id="1371a-121">Hvis du vil definere en satsvis jobb for å kjøre prosessen for flere kunder, kan du bruke siden **Beregn saldostatistikk** (**Kredittbehandling \> Periodiske oppgaver \> Beregn saldostatistikk**).</span><span class="sxs-lookup"><span data-stu-id="1371a-121">To set up a batch job to run the process for multiple customers, you can use the **Calculate balance statistics** page (**Credit management \> Periodic tasks \> Calculate balance statistics**).</span></span>
