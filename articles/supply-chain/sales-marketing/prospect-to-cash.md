---
title: Kundeemne til kontanter
description: Emnet gir en oversikt over Kundeemne til kontanter mellom Dynamics 365 for Finance and Operations, Enterprise Edition og Dynamics 365 for Sales.
author: ChristianRytt
manager: AnnBe
ms.date: 10/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.intro: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 674d2e1f2c5cdbccf43618a9083ca01abed0735a
ms.openlocfilehash: 2accf77c5241adff7ad1648737dde451153fde46
ms.contentlocale: nb-no
ms.lasthandoff: 11/14/2017

---

# <a name="prospect-to-cash"></a>Kundeemne til kontanter  

[!include[banner](../includes/banner.md)]

Kundeemne til kontanter-løsningen bruker [Dataintegrasjon](/common-data-service/entity-reference/dynamics-365-integration) for å synkronisere data på tvers av Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition og Dynamics 365 for Sales via Common Data Service (CDS). Kundeemne til kontanter-maler som er tilgjengelige med dataintegrasjon-funksjonen, gjør det mulig å flytte kontoer, kontakter, produkter, salgstilbud, salgsordrer og salgsfakturaer mellom Finance and Operations og Sales. Når dataene flyter mellom Finance and Operations og Sales kan du utføre salgs- og markedsaktiviteter i Sales og håndtere ordrenes oppfyllelse med lagerstyring i Finance and Operations. 

Denne løsningen gir integrasjon i følgende områder: 

-   [Behold kontoer i Sales og synkroniser dem til Finance and Operations](accounts-template-mapping.md)
-   [Behold kontakter i Sales og synkroniser dem til Finance and Operations](contacts-template-mapping.md)
-   [Behold produkter i Sales og synkroniser dem til Finance and Operations](products-template-mapping.md)
-   [Opprett salgstilbud i Sales og synkroniser dem til Finance and Operations](sales-quotation-template-mapping.md)
-   [Opprett salgsordrer i Finance and Operations og synkroniser dem til Sales](sales-order-template-mapping.md)
-   [Opprett salgsfakturaer i Finance and Operations og synkroniser dem til Sales](sales-invoice-template-mapping.md)

Denne løsningen gir direkte synkronisering i følgende områder:

-   [Beholde kontoer i Sales og synkroniser dem direkte fra Sales til Finance and Operations](accounts-template-mapping-direct.md)
-   [Beholde produkter i Finance and Operations og synkroniser dem til direkte til Sales](products-template-mapping-direct.md)
-   [Beholde kontakter i Sales og synkroniser dem direkte til kontakter eller kunder i Finance and Operations](contacts-template-mapping-direct.md)
-   [Synkronisere salgstilbudshoder og -linjer direkte fra Sales til Finance and Operations](sales-quotation-template-mapping-sales-fin.md)
-   [Opprette salgsordrer i Finance and Operations og synkroniser dem direkte til Sales](sales-order-template-mapping-direct.md)
-  [Synkronisere salgsordrehoder og -linjer direkte mellom Sales og Finance and Operations](sales-order-template-mapping-between-sales-fin.md)
-   [Synkronisere salgsordrer direkte mellom Sales og Finance and Operations](sales-order-template-mapping-direct-two-ways.md)
-   [Opprette salgsfakturaer i Finance and Operations og synkroniser dem direkte til Sales](sales-invoice-template-mapping-direct.md)


## <a name="system-requirements-for-dynamics-365-for-finance-and-operations-enterprise-edition"></a>Systemkrav for Dynamics 365 for Finance and Operations, Enterprise Edition

For å bruke Kundeemne til kontanter-løsningen må du installere følgende:

- Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition (juli 2017) med plattformoppdatering 8 (App 7.2.11792.56024 m/ Platform 7.0.4565.16212)

- Hurtigreparasjoner for Dynamics 365 for Finance and Operations, Enterprise Edition (juli 2017)
        
    -  [KB4045570](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4045570&bugId=3851320&qc=ac1145034fd04ab71ccc4d14aa012f245176712c9af7c36bb77a118726d46160) – Denne hurtigreparasjonen gjør det mulig å synkronisere salgsordre med dataintegreringsfunksjonen fra Sales til Finance and Operations, sammen med en rekke andre forbedringer.

    -  [KB4036524](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036524&bugId=3847504&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2) – Denne hurtigreparasjonen gjør det mulig å synkronisere salgsordreline med dataintegreringsfunksjonen fra Finance and Operations til Sales.
        
    -  [KB4036461](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036461&bugId=3847029&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2) – Denne hurtigreparasjonen gjør det mulig å synkronisere salgsordre med dataintegreringsfunksjonen fra Finance and Operations til Sales.

**Obs!** Du trenger bare å installere KB4045570 fordi installasjonen inkluderer endringene fra de andre KB-ene.
 
## <a name="system-requirements-for-dynamics-365-for-sales"></a>Systemkrav for Dynamics 365 for Sales

For å bruke Kundeemne til kontanter-løsningen må du installere følgende:

- Dynamics 365 for Sales versjon 1612 (8.2.1.207) (DB 8.2.1.207) online.
- Kundeemne til kontanter-løsningen for Dynamics 365 for Sales, versjon 1.14.0.0 (v14) eller senere.

### <a name="install-the-prospect-to-cash-solution-for-sales"></a>Installere Kundeemne til kontanter-løsningen for Sales

- Last ned [Kundeemne til kontanter for Dynamics 365 for Sales, løsningspakke zip-fil](https://mbs.microsoft.com/customersource/Global/365Enterprise/downloads/product-releases/MD365FNOPENTProspectToCash) på CustomerSource.

- Sørge for at zip-filen ikke er blokkert, så du ikke får feilmeldingen «No import packages were found», når du installer løsningspakken. Gjør følgende for å sørge for at filen ikke er blokkert:

    -  Høyreklikk zip-filen.
    -  Velg **Egenskaper** og velg deretter **Opphev blokkering**. 

- Pakk ut og kjøre PackageDeployer.exe

- Installer Kundeemne til kontanter-løsningen for forekomsten din av Sales.

    - Velg **Office 365** Implementasjonstype
    - Velg **Vis avansert**.
    - For en hurtiginstallasjon, velg en **Region**. Hvis du velger **Vet ikke** vil systemet søke alle regioner, og det vil ta lengre tid å installere.
    - Skriv inn **Brukernavn** og **Passord** for en administratorbruker som har brukerrettigheter til å installere.

