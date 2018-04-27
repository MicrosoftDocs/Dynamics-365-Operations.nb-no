---
title: Kundeemne til kontanter
description: Dette emnet gir en oversikt over Kundeemne til kontanter mellom Microsoft Dynamics 365 for Finance and Operations og Microsoft Dynamics 365 for Sales.
author: ChristianRytt
manager: AnnBe
ms.date: 04/03/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustTable, SalesTable, EcoResProductListPage
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: bc0fa8fe3e20ae4be3e572932f99ccc54e3b746b
ms.contentlocale: nb-no
ms.lasthandoff: 04/13/2018

---

# <a name="prospect-to-cash"></a>Kundeemne til kontanter

[!INCLUDE [banner](../includes/banner.md)]

Løsningen Kundeemne til kontanter gir direkte synkronisering på tvers av Dynamics 365 for Finance and Operations og Dynamics 365 for Sales. Kundeemne til kontanter-maler som er tilgjengelige med Dataintegrering-funksjonen,tillater flyt av data for kontoer, kontakter, produkter, salgstilbud, salgsordrer og salgsfakturaer mellom Finance and Operations og Sales. Når dataene flyter mellom Finance and Operations og Sales kan du utføre salgs- og markedsaktiviteter i Sales, og du kan håndtere ordrenes oppfyllelse med lagerstyring i Finance and Operations. 

Hvis du vil ha mer informasjon om kundeemne til kontanter-integrering, se den korte YouTube-videoen:

> [!Video https://www.youtube.com/embed/AVV9x5x-XCg]

I den gjeldende versjonen inneholder Kundeemne til kontanter-løsningen følgende typer direkte synkronisering:

- [Beholde kontoer i Sales og synkroniser dem direkte fra Sales til Finance and Operations](accounts-template-mapping-direct.md)
- [Beholde produkter i Finance and Operations og synkronisere dem til direkte til Sales](products-template-mapping-direct.md)
- [Beholde kontakter i Sales og synkronisere dem direkte til kontakter eller kunder i Finance and Operations](contacts-template-mapping-direct.md)
- [Synkronisere salgstilbud direkte fra Sales til Finance and Operations](sales-quotation-template-mapping-sales-fin.md)
- [Synkronisere salgsordrer direkte mellom Sales og Finance and Operations](sales-order-template-mapping-direct-two-ways.md)
- [Synkronisere salgsfaktura direkte fra Finance and Operations til Sales](sales-invoice-template-mapping-direct.md)

## <a name="system-requirements-for-finance-and-operations"></a>Systemkrav for Finance and Operations
Kundeemne til kontanter-integrasjon støttes i følgende versjoner:

### <a name="microsoft-dynamics-365-for-finance-and-operations-enterprise-edition-73-december-2017"></a>Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3 (desember 2017)

- Dynamics 365 for Finance and Operations, Enterprise edition (desember 2017) - programbygg 7.3.11971.56116 med plattformoppdatering 12 (7.0.4709.41129)

### <a name="dynamics-365-for-finance-and-operations-enterprise-edition-july-2017"></a>Dynamics 365 for Finance and Operations, Enterprise edition (juli 2017)

- Dynamics 365 for Finance and Operations, Enterprise Edition (juli 2017) – plattformoppdatering 8 (programbygg 7.2.11792.56024 med plattformbygg 7.0.4565.16212).
- Følgende hurtigreparasjoner vil kreves:

  - **[KB4045570](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4045570&bugId=3851320&qc=ac1145034fd04ab71ccc4d14aa012f245176712c9af7c36bb77a118726d46160)** – Denne hurtigreparasjonen gjør det mulig å synkronisere salgsordre via dataintegreringsfunksjonen fra Sales til Finance and Operations. I tillegg inneholder den flere forbedringer.
  - **[KB4036524](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036524&bugId=3847504&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** – Denne hurtigreparasjonen gjør det mulig å synkronisere salgsordrelinjer via dataintegreringsfunksjonen fra Finance and Operations til Sales.
  - **[KB4036461](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036461&bugId=3847029&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** – Denne hurtigreparasjonen gjør det mulig å synkronisere salgsordre via dataintegreringsfunksjonen fra Finance and Operations til Sales.

    > [!NOTE]
    > Du trenger bare å installere KB4045570 fordi installasjonen inkluderer endringene fra de andre hurtigreparasjonene. 

### <a name="dynamics-365-for-finance-and-operations-version-1611-november-2016"></a>Dynamics 365 for Finance and Operations versjon 1611 (november 2016)

- Dynamics 365 for Finance and Operations versjon 1611 (november 2016) med plattformoppdatering 8 eller høyere

- Følgende hurtigreparasjoner vil kreves:

  - **[KB4051266](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4051266&bugId=3863566&qc=ee80faaa7bc6c77b368d5eaf456c9c08e0b9fba5903a7b6fd8c13756c3a4b757)** - Aktiver salgsordresynkronisering med dataintegrator fra Finance and Operations til Sales. 
  - **[KB4037542](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4037542&bugId=3848253&qc=8323b93c15280172c5ab4159e0256e37104ced1729462c91ab2f7d00cb8d419c)** - Aktiver salgsordrehode- og linjesynkronisering med dataintegrator fra Finance and Operations til Sales.
  - **[KB4033093](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4033093&bugId=3824604&qc=bd7e15e1fb56066b3a82ce48b691cf1ffbc934a7473fa888545b2211a8d416c5)** - Støtte for kundeemne til kontanter-integrering gjennom dataenheter, kreves.
    
    > [!NOTE]
    > Når du har installert hurtigreparasjonene, må du starte den følgende kjørselen fra skjemaet **SalesPopulateProspectToCash**. Dette skjemaet skjules siden du bare trenger det én gang. For å få tilgang til skjemaet, må du logge på miljøet og legge til følgende i URL-adressen i nettleseradressen: &mi=action:SalesPopulateProspectToCash, for eksempel `https://ax123456.cloud.test.dynamics.com/?cmp=USMF&mi=action:SalesPopulateProspectToCash`. Når skjemaet åpnes, klikker du på OK. Dette vil fylle ut et nytt felt **LineCreationSequnceNumber** i tabellen **SalesLine**, **SalesQuotationLine** og **CustInvoiceTrans** med unike verdier og oppdatere varelisten. Dette er nødvendig for at kundeemne til kontanter-integrasjonen skal fungere.


## <a name="system-requirements-for-sales"></a>Systemkrav for Sales

For å bruke Kundeemne til kontanter-løsningen må du installere følgende komponenter:

- Dynamics 365 for Sales versjon 1612 (8.2.1.207) (DB 8.2.1.207) nett eller en senere versjon.
- Kundeemne til kontanter-løsningen for Dynamics 365 for Sales, versjon 1.15.0.0 eller en senere versjon. Løsningen er tilgjengelig for nedlasting fra AppSource. [Last ned Dynamics 365, kundeemne til kontanter](https://appsource.microsoft.com/en-us/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3).

