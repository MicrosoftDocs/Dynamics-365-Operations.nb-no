## <a name="currencies-to-transactioncurrencies"></a><span data-ttu-id="9e106-101">Valutaer til transactioncurrencies</span><span class="sxs-lookup"><span data-stu-id="9e106-101">Currencies to transactioncurrencies</span></span>

<span data-ttu-id="9e106-102">Denne malen synkroniserer data mellom Finance and Operations-apper og Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="9e106-102">This template synchronizes data between Finance and Operations apps and Common Data Service.</span></span>

<span data-ttu-id="9e106-103">Kildefilter: ((CURRENCYCODE != "999"))</span><span class="sxs-lookup"><span data-stu-id="9e106-103">Source filter: ((CURRENCYCODE != "999"))</span></span>

<span data-ttu-id="9e106-104">Finance and Operations-felt</span><span class="sxs-lookup"><span data-stu-id="9e106-104">Finance and Operations field</span></span> | <span data-ttu-id="9e106-105">Tilordningstype</span><span class="sxs-lookup"><span data-stu-id="9e106-105">Map type</span></span> | <span data-ttu-id="9e106-106">Annet Dynamics 365-felt</span><span class="sxs-lookup"><span data-stu-id="9e106-106">Other Dynamics 365 field</span></span> | <span data-ttu-id="9e106-107">Standardverdi</span><span class="sxs-lookup"><span data-stu-id="9e106-107">Default value</span></span>
---|---|---|---
<span data-ttu-id="9e106-108">CURRENCYCODE</span><span class="sxs-lookup"><span data-stu-id="9e106-108">CURRENCYCODE</span></span> | = | <span data-ttu-id="9e106-109">isocurrencycode</span><span class="sxs-lookup"><span data-stu-id="9e106-109">isocurrencycode</span></span> | 
<span data-ttu-id="9e106-110">NAME</span><span class="sxs-lookup"><span data-stu-id="9e106-110">NAME</span></span> | = | <span data-ttu-id="9e106-111">currencyname</span><span class="sxs-lookup"><span data-stu-id="9e106-111">currencyname</span></span> | 
<span data-ttu-id="9e106-112">SYMBOL</span><span class="sxs-lookup"><span data-stu-id="9e106-112">SYMBOL</span></span> | = | <span data-ttu-id="9e106-113">currencysymbol</span><span class="sxs-lookup"><span data-stu-id="9e106-113">currencysymbol</span></span> | 
<span data-ttu-id="9e106-114">none</span><span class="sxs-lookup"><span data-stu-id="9e106-114">none</span></span> | >> | <span data-ttu-id="9e106-115">exchangerate</span><span class="sxs-lookup"><span data-stu-id="9e106-115">exchangerate</span></span> | <span data-ttu-id="9e106-116">1</span><span class="sxs-lookup"><span data-stu-id="9e106-116">1</span></span>