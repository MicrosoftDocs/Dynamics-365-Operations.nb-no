---
title: Åpne finansjournalmaler i Office
description: Dette emnet beskriver problemer som kan oppstå når du oppretter egendefinerte finansjournaler ved hjelp av en Microsoft Excel-mal.
author: kweekley
ms.date: 05/14/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2020-05-14
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 0773f47551b2460ec310b92b67c634b433147749
ms.sourcegitcommit: 8c5b3e872825953853ad57fc67ba6e5ae92b9afe
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/24/2021
ms.locfileid: "6089463"
---
# <a name="open-financial-journal-templates-in-office"></a><span data-ttu-id="090eb-103">Åpne finansjournalmaler i Office</span><span class="sxs-lookup"><span data-stu-id="090eb-103">Open financial journal templates in Office</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="090eb-104">Dette emnet beskriver problemer som kan oppstå når du oppretter egendefinerte finansjournaler ved hjelp av en Microsoft Excel-mal.</span><span class="sxs-lookup"><span data-stu-id="090eb-104">This topic describes issues that might occur when you create custom financial journals by using a Microsoft Excel template.</span></span>

## <a name="symptom"></a><span data-ttu-id="090eb-105">Symptom</span><span class="sxs-lookup"><span data-stu-id="090eb-105">Symptom</span></span>

<span data-ttu-id="090eb-106">Du har opprettet en egendefinert Excel-mal for finansjournaler, men den vises ikke på menyen **Åpne linjer i Excel**.</span><span class="sxs-lookup"><span data-stu-id="090eb-106">You created a custom Excel template for financial journals, but it doesn't appear on the **Open lines in Excel** menu.</span></span> <span data-ttu-id="090eb-107">Hvis det eventuelt vises i menyen, åpnes en annen mal, men når du velger den.</span><span class="sxs-lookup"><span data-stu-id="090eb-107">Alternatively, it does appear on the menu, a different template is opened but when you select it.</span></span>

## <a name="resolution"></a><span data-ttu-id="090eb-108">Løsning</span><span class="sxs-lookup"><span data-stu-id="090eb-108">Resolution</span></span>

<span data-ttu-id="090eb-109">Standardfunksjonen Åpne i Excel bruker rotdatakilden (tabell) på den gjeldende siden til å fastslå hvilke Office-maler eller dataenheter som skal vises som alternativer på menyen **Åpne i Excel**.</span><span class="sxs-lookup"><span data-stu-id="090eb-109">The default Open in Excel functionality uses the root data source (table) of the current page to determine which Office templates or data entities appear as options on the **Open in Excel** menu.</span></span> <span data-ttu-id="090eb-110">Denne virkemåten er ikke en ideell funksjon for finansjournaler fordi finansjournaler bruker de samme tabellene (LedgerJournalTable og LedgerJournalTrans) som rotdatakilden for mange andre journaltyper.</span><span class="sxs-lookup"><span data-stu-id="090eb-110">This behavior isn't an ideal experience for financial journals, because financial journals use the same tables (LedgerJournalTable and LedgerJournalTrans) as the root data source of many other types of journals.</span></span>

<span data-ttu-id="090eb-111">For finansjournaler er Åpne linjer i Excel-funksjonen ment å vise maler som er utformet for journalen du for øyeblikket arbeider i sammenheng med, for eksempel økonomijournalen eller en betalingsjournal.</span><span class="sxs-lookup"><span data-stu-id="090eb-111">For financial journals, the Open Lines in Excel functionality is intended to show templates that are designed for the journal that you're currently working in the context of, such as the general journal or a payment journal.</span></span> <span data-ttu-id="090eb-112">En mal som for eksempel er ment å brukes med en leverandørbetalingsjournal, er utformet for å fremtvinge primærkontoen som en leverandørkonto.</span><span class="sxs-lookup"><span data-stu-id="090eb-112">For example, a template that is intended to be used with a vendor payment journal will be designed to enforce your primary account as a vendor account.</span></span>

<span data-ttu-id="090eb-113">Hvis du vil promotere en mal slik at den er tilgjengelig på menyene **Åpne linjer i Excel** og **Åpne i Excel**, er det en enkel utviklerfunksjon å implementere grensesnittet **LedgerIJournalExcelTemplate** og utvide klassen **DocuTemplateRegistrationBase**.</span><span class="sxs-lookup"><span data-stu-id="090eb-113">If you want to promote a template so that it's available on the **Open lines in Excel** and **Open in Excel** menus, an easy developer experience is to implement the **LedgerIJournalExcelTemplate** interface and extend the **DocuTemplateRegistrationBase** class.</span></span> <span data-ttu-id="090eb-114">Mange eksempler på denne fremgangsmåten er implementert i systemet.</span><span class="sxs-lookup"><span data-stu-id="090eb-114">Many examples of this approach are implemented in the system.</span></span> <span data-ttu-id="090eb-115">Et eksempel som kan brukes som referanse, er grensesnittet **LedgerDailyJournalExcelTemplate** som ble opprettet for økonomijournalen (eller den daglige journalen).</span><span class="sxs-lookup"><span data-stu-id="090eb-115">One example that can be used for reference is the **LedgerDailyJournalExcelTemplate** interface that was created for the general journal (or daily journal).</span></span>

<span data-ttu-id="090eb-116">Når grensesnittet **LedgerIJournalExcelTemplate** er implementert for malen, filtrerer menyen **Åpne linjer i Excel** maler etter journaltypen til journalen din og viser bare malene som er tilgjengelige for den journalen.</span><span class="sxs-lookup"><span data-stu-id="090eb-116">When the **LedgerIJournalExcelTemplate** interface is implemented for your template, the **Open Lines in Excel** menu will filter templates by the journal type of your journal and will show only the templates that are available for that journal.</span></span> <span data-ttu-id="090eb-117">Grensesnittet gir også en valideringsmetode som sikrer at en mal ikke kan åpnes for en journal hvis den ikke oppfyller kontotypekravene.</span><span class="sxs-lookup"><span data-stu-id="090eb-117">The interface also provides a validation method that ensures that a template can't be opened for a journal if it doesn't meet the account type requirements.</span></span> <span data-ttu-id="090eb-118">Du kan for eksempel angi at kontotypen må være av typen **Leverandør** eller **Finans**.</span><span class="sxs-lookup"><span data-stu-id="090eb-118">For example, you can specify that the account type must be of the **Vendor** or **Ledger** type.</span></span>

<span data-ttu-id="090eb-119">Hvis du vil ha mer informasjon om denne funksjonaliteten, kan du se [Legg til maler på menyen Åpne linjer i Excel](../../fin-ops-core/dev-itpro/user-interface/add-templates-open-lines-excel-menu.md).</span><span class="sxs-lookup"><span data-stu-id="090eb-119">For more information about this functionality, see [Add templates to the Open lines in Excel menu](../../fin-ops-core/dev-itpro/user-interface/add-templates-open-lines-excel-menu.md).</span></span>
