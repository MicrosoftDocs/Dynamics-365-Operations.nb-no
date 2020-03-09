## <a name="withholding-tax-codes-to-msdyn_withholdingtaxcodes"></a><span data-ttu-id="4ef40-101">Kildeskattkoder til msdyn_withholdingtaxcodes</span><span class="sxs-lookup"><span data-stu-id="4ef40-101">Withholding tax codes to msdyn_withholdingtaxcodes</span></span>

<span data-ttu-id="4ef40-102">Denne malen synkroniserer data mellom Finance and Operations-apper og Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="4ef40-102">This template synchronizes data between Finance and Operations apps and Common Data Service.</span></span>

<span data-ttu-id="4ef40-103">Finance and Operations-felt</span><span class="sxs-lookup"><span data-stu-id="4ef40-103">Finance and Operations field</span></span> | <span data-ttu-id="4ef40-104">Tilordningstype</span><span class="sxs-lookup"><span data-stu-id="4ef40-104">Map type</span></span> | <span data-ttu-id="4ef40-105">Annet Dynamics 365-felt</span><span class="sxs-lookup"><span data-stu-id="4ef40-105">Other Dynamics 365 field</span></span> | <span data-ttu-id="4ef40-106">Standardverdi</span><span class="sxs-lookup"><span data-stu-id="4ef40-106">Default value</span></span>
---|---|---|---
<span data-ttu-id="4ef40-107">WITHHOLDINGCODE</span><span class="sxs-lookup"><span data-stu-id="4ef40-107">WITHHOLDINGCODE</span></span> | = | <span data-ttu-id="4ef40-108">msdyn_name</span><span class="sxs-lookup"><span data-stu-id="4ef40-108">msdyn_name</span></span> | 
<span data-ttu-id="4ef40-109">WITHHOLDINGTAXNAME</span><span class="sxs-lookup"><span data-stu-id="4ef40-109">WITHHOLDINGTAXNAME</span></span> | = | <span data-ttu-id="4ef40-110">msdyn_description</span><span class="sxs-lookup"><span data-stu-id="4ef40-110">msdyn_description</span></span> | 
<span data-ttu-id="4ef40-111">WITHHOLDINGTAXROUNDOFF</span><span class="sxs-lookup"><span data-stu-id="4ef40-111">WITHHOLDINGTAXROUNDOFF</span></span> | = | <span data-ttu-id="4ef40-112">msdyn_roundoff</span><span class="sxs-lookup"><span data-stu-id="4ef40-112">msdyn_roundoff</span></span> | 
<span data-ttu-id="4ef40-113">WITHHOLDINGTAXROUNDOFFTYPE</span><span class="sxs-lookup"><span data-stu-id="4ef40-113">WITHHOLDINGTAXROUNDOFFTYPE</span></span> | >< | <span data-ttu-id="4ef40-114">msdyn_roundofftype</span><span class="sxs-lookup"><span data-stu-id="4ef40-114">msdyn_roundofftype</span></span> | 
<span data-ttu-id="4ef40-115">CURRENCYCODEID</span><span class="sxs-lookup"><span data-stu-id="4ef40-115">CURRENCYCODEID</span></span> | = | <span data-ttu-id="4ef40-116">msdyn_currency.isocurrencycode</span><span class="sxs-lookup"><span data-stu-id="4ef40-116">msdyn_currency.isocurrencycode</span></span> | 
<span data-ttu-id="4ef40-117">WITHHOLDINGTAXBASE</span><span class="sxs-lookup"><span data-stu-id="4ef40-117">WITHHOLDINGTAXBASE</span></span> | >< | <span data-ttu-id="4ef40-118">msdyn_taxableamountorigin</span><span class="sxs-lookup"><span data-stu-id="4ef40-118">msdyn_taxableamountorigin</span></span> | 