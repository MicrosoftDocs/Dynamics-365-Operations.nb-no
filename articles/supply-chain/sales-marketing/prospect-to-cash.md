---
title: Kundeemne til kontanter
description: Dette emnet gir en oversikt over Kundeemne til kontanter-løsningen mellom Dynamics 365 Supply Chain Management og Dynamics 365 Sales.
author: ChristianRytt
manager: tfehr
ms.date: 04/25/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustTable, SalesTable, EcoResProductListPage
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: 55c39fac40498488519fcb539b3c3f7560a46b30
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4434336"
---
# <a name="prospect-to-cash"></a>Kundeemne til kontanter

[!include [banner](../includes/banner.md)]

Kundeemne til kontanter-løsningen gir direkte synkronisering på tvers av Dynamics 365 Supply Chain Management og Dynamics 365 Sales. Kundeemne til kontanter-maler som er tilgjengelige med Dataintegrering-funksjonen,tillater flyt av data for kontoer, kontakter, produkter, salgstilbud, salgsordrer og salgsfakturaer. Når dataene flyter, kan du utføre salgs- og markedsaktiviteter i Sales, og du kan håndtere ordrenes oppfyllelse med lagerstyring i Supply Chain Management. 

Hvis du vil ha mer informasjon om Kundeemne til kontanter-integrasjonen, se den korte YouTube-videoen [Kundeemne til kontanter-integrasjon](https://www.youtube.com/watch?v=AVV9x5x-XCg).

I den gjeldende versjonen inneholder Kundeemne til kontanter-løsningen følgende typer direkte synkronisering:

- [Synkronisere kontoer direkte fra Sales til kunder i Supply Chain Management](accounts-template-mapping-direct.md)
- [Synkronisere produkter direkte fra Supply Chain Management til produkter i Sales](products-template-mapping-direct.md)
- [Synkronisere kontakter direkte fra Sales til kontakter eller kunder i Supply Chain Management](contacts-template-mapping-direct.md)
- [Synkronisere salgstilbudshoder og -linjer direkte fra Sales til Supply Chain Management](sales-quotation-template-mapping-sales-fin.md)
- [Synkronisering av salgsordrer direkte mellom Sales og Supply Chain Management](sales-order-template-mapping-direct-two-ways.md)
- [Synkronisere salgsfakturahoder og -linjer direkte fra Supply Chain Management til Sales](sales-invoice-template-mapping-direct.md)

## <a name="system-requirements-for-supply-chain-management"></a>Systemkrav for Supply Chain Management
Kundeemne til kontanter-integrasjon støttes i følgende versjoner:

### <a name="microsoft-dynamics-365-for-finance-and-operations-enterprise-edition-73-december-2017"></a>Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition 7.3 (desember 2017)

- Dynamics 365 for Finance and Operations Enterprise Edition (desember 2017) – programbygg 7.3.11971.56116 med plattformoppdatering 12 (7.0.4709.41129)

### <a name="dynamics-365-for-finance-and-operations-enterprise-edition-july-2017"></a>Dynamics 365 for Finance and Operations Enterprise Edition (juli 2017)

- Dynamics 365 for Finance and Operations Enterprise Edition (juli 2017) – med plattformoppdatering 8 (programbygg 7.2.11792.56024 med plattformbygg 7.0.4565.16212).
- Følgende hurtigreparasjoner vil kreves:

  - **[KB4045570](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4045570&bugId=3851320&qc=ac1145034fd04ab71ccc4d14aa012f245176712c9af7c36bb77a118726d46160)** – Denne hurtigreparasjonen gjør det mulig å synkronisere salgsordre via dataintegreringsfunksjonen fra Sales til Supply Chain Management. I tillegg inneholder den flere forbedringer.
  - **[KB4036524](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036524&bugId=3847504&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** – Denne hurtigreparasjonen gjør det mulig å synkronisere salgsordrelinje via dataintegreringsfunksjonen fra Supply Chain Management til Sales.
  - **[KB4036461](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036461&bugId=3847029&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** – Denne hurtigreparasjonen gjør det mulig å synkronisere salgsordre via dataintegreringsfunksjonen fra Supply Chain Management til Sales.

    > [!NOTE]
    > Du trenger bare å installere KB4045570 fordi installasjonen inkluderer endringene fra de andre hurtigreparasjonene. 

### <a name="dynamics-365-for-finance-and-operations-version-1611-november-2016"></a>Dynamics 365 for Finance and Operations versjon 1611 (november 2016)

- Dynamics 365 for Finance and Operations versjon 1611 (november 2016) med plattformoppdatering 8 eller høyere

- Følgende hurtigreparasjoner vil kreves:

  - **[KB4051266](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4051266&bugId=3863566&qc=ee80faaa7bc6c77b368d5eaf456c9c08e0b9fba5903a7b6fd8c13756c3a4b757)** – Aktiver salgsordresynkronisering med dataintegrator fra Supply Chain Management til Sales. 
  - **[KB4037542](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4037542&bugId=3848253&qc=8323b93c15280172c5ab4159e0256e37104ced1729462c91ab2f7d00cb8d419c)** – Aktiver salgsordrehode- og linjesynkronisering med dataintegrator fra Supply Chain Management til Sales.
  - **[KB4033093](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4033093&bugId=3824604&qc=bd7e15e1fb56066b3a82ce48b691cf1ffbc934a7473fa888545b2211a8d416c5)** - Støtte for kundeemne til kontanter-integrering gjennom dataenheter, kreves.
    
    > [!NOTE]
    > Når du har installert hurtigreparasjonene, må du starte den følgende kjørselen fra skjemaet **SalesPopulateProspectToCash**. Dette skjemaet skjules siden du bare trenger det én gang. For å få tilgang til skjemaet, må du logge på miljøet og legge til følgende i URL-adressen i nettleseradressen: *&mi=action:SalesPopulateProspectToCash*, for eksempel `https://ax123456.cloud.test.dynamics.com/?cmp=USMF&mi=action:SalesPopulateProspectToCash`. Når skjemaet åpnes, klikker du på OK. Dette vil fylle ut et nytt felt **LineCreationSequnceNumber** i tabellen **SalesLine**, **SalesQuotationLine** og **CustInvoiceTrans** med unike verdier og oppdatere varelisten. Dette er nødvendig for at kundeemne til kontanter-integrasjonen skal fungere.


## <a name="system-requirements-for-sales"></a>Systemkrav for Sales

For å bruke Kundeemne til kontanter-løsningen må du installere følgende komponenter:

- Dynamics 365 Sales versjon 1612 (8.2.1.207) (DB 8.2.1.207) online eller en nyere versjon.
- Kundeemne til kontanter-løsning for Dynamics 365 Sales versjon 1.15.0.0 eller en nyere versjon. Løsningen er tilgjengelig for nedlasting fra AppSource. [Last ned Dynamics 365, kundeemne til kontanter](https://appsource.microsoft.com/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]