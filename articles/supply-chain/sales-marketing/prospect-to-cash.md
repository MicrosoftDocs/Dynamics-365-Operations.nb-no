---
title: Kundeemne til kontanter
description: Dette emnet gir en oversikt over Kundeemne til kontanter mellom Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition og Microsoft Dynamics 365 for Sales.
author: ChristianRytt
manager: AnnBe
ms.date: 11/17/2017
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
ms.sourcegitcommit: 788e64476094e84eb4d438890776306c05b20582
ms.openlocfilehash: 762699cf68ec8a9df5db20d7dd33bc9248f0a36e
ms.contentlocale: nb-no
ms.lasthandoff: 12/11/2017

---

# <a name="prospect-to-cash"></a>Kundeemne til kontanter

[!include[banner](../includes/banner.md)]

Løsningen Kundeemne til kontanter gir direkte synkronisering på tvers av Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition og Microsoft Dynamics 365 for Sales. Kundeemne til kontanter-maler som er tilgjengelige med Dataintegrering-funksjonen,tillater flyt av data for kontoer, kontakter, produkter, salgstilbud, salgsordrer og salgsfakturaer mellom Finance and Operations og Sales. Når dataene flyter mellom Finance and Operations og Sales kan du utføre salgs- og markedsaktiviteter i Sales, og du kan håndtere ordrenes oppfyllelse med lagerstyring i Finance and Operations.

I den gjeldende versjonen inneholder Kundeemne til kontanter-løsningen følgende typer direkte synkronisering:

- [Beholde kontoer i Sales og synkroniser dem direkte fra Sales til Finance and Operations](accounts-template-mapping-direct.md)
- [Beholde produkter i Finance and Operations og synkroniser dem til direkte til Sales](products-template-mapping-direct.md)
- [Beholde kontakter i Sales og synkroniser dem direkte til kontakter eller kunder i Finance and Operations](contacts-template-mapping-direct.md)
- [Synkronisere salgstilbud direkte fra Sales til Finance and Operations](sales-quotation-template-mapping-sales-fin.md)
- [Synkronisere salgsordrer direkte fra Finance and Operations til Sales](sales-order-template-mapping-direct.md)
- [Synkronisere salgsordrer direkte mellom Sales og Finance and Operations](sales-order-template-mapping-direct-two-ways.md)
- [Synkronisere salgsfaktura direkte fra Finance and Operations til Sales](sales-invoice-template-mapping-direct.md)

I tidligere versjoner inneholder Kundeemne til kontanter-løsningen følgende typer ikke-direkte synkronisering:

- [Behold kontoer i Sales og synkroniser dem til Finance and Operations](accounts-template-mapping.md)
- [Behold kontakter i Sales og synkroniser dem til Finance and Operations](contacts-template-mapping.md)
- [Behold produkter i Sales og synkroniser dem til Finance and Operations](products-template-mapping.md)
- [Opprett salgstilbud i Sales og synkroniser dem til Finance and Operations](sales-quotation-template-mapping.md)
- [Opprett salgsordrer i Finance and Operations og synkroniser dem til Sales](sales-order-template-mapping.md)
- [Opprett salgsfakturaer i Finance and Operations og synkroniser dem til Sales](sales-invoice-template-mapping.md)

## <a name="system-requirements-for-finance-and-operations"></a>Systemkrav for Finance and Operations

For å bruke Kundeemne til kontanter-løsningen må du installere følgende komponenter:

### <a name="july-2017"></a>Juli 2017 

- Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition (juli 2017) med plattformoppdatering 8 (programbygg 7.2.11792.56024 med plattformbygg 7.0.4565.16212)
- Følgende hurtigreparasjoner for Finance and Operations:

    - **[KB4045570](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4045570&bugId=3851320&qc=ac1145034fd04ab71ccc4d14aa012f245176712c9af7c36bb77a118726d46160)** – Denne hurtigreparasjonen gjør det mulig å synkronisere salgsordre via dataintegreringsfunksjonen fra Sales til Finance and Operations. I tillegg inneholder den flere forbedringer.
    - **[KB4036524](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036524&bugId=3847504&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** – Denne hurtigreparasjonen gjør det mulig å synkronisere salgsordrelinjer via dataintegreringsfunksjonen fra Finance and Operations til Sales.
    - **[KB4036461](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036461&bugId=3847029&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** – Denne hurtigreparasjonen gjør det mulig å synkronisere salgsordre via dataintegreringsfunksjonen fra Finance and Operations til Sales.

    > [!NOTE]
    > Du trenger bare å installere KB4045570 fordi installasjonen inkluderer endringene fra de andre Microsoft Knowledge Base (KB)-artiklene.

### <a name="november-2016-version-1611"></a>November 2016 (versjon 1611)

- Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (november 2016) med plattformoppdatering 8 eller høyere

- Følgende hurtigreparasjoner for Finance and Operations:

    - **[KB4051266](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4051266&bugId=3863566&qc=ee80faaa7bc6c77b368d5eaf456c9c08e0b9fba5903a7b6fd8c13756c3a4b757)** - Aktiver salgsordresynkronisering med dataintegrator fra Microsoft Dynamics 365 for Finance and Operations til Sales 
    - **[KB4037542](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4037542&bugId=3848253&qc=8323b93c15280172c5ab4159e0256e37104ced1729462c91ab2f7d00cb8d419c)** - Aktiver salgsordrehode- og salgsordrelinjesynkronisering med dataintegrator fra Microsoft Dynamics 365 for Finance and Operations til Sales
    - **[KB4033093](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4033093&bugId=3824604&qc=bd7e15e1fb56066b3a82ce48b691cf1ffbc934a7473fa888545b2211a8d416c5)** - Støtte for kundeemne til kontanter-integrering gjennom dataenheter, kreves
    
    > [!NOTE]
    > Når du har installert hurtigreparasjonene, må du starte den følgende kjørselen fra skjemaet SalesPopulateProspectToCash. Dette skjemaet skjules siden du bare trenger det én gang. For å få tilgang til det, legger du til følgende i webleseradressen når du er logget på miljøet: &mi=action:SalesPopulateProspectToCash, for eksempel https://ax123456.cloud.test.dynamics.com/?cmp=USMF&mi=action:SalesPopulateProspectToCash I skjemaet som åpnes, klikk OK.
    Dette vil fylle ut et nytt felt "LineCreationSequnceNumber" i tabellen "SalesLine", "SalesQuotationLine" og "CustInvoiceTrans" med unike verdier og oppdatere varelisten. Dette er nødvendig for at P2C-integreringen skal fungere på 7.1


## <a name="system-requirements-for-sales"></a>Systemkrav for Sales

For å bruke Kundeemne til kontanter-løsningen må du installere følgende komponenter:

- Microsoft Dynamics 365 for Sales versjon 1612 (8.2.1.207) (DB 8.2.1.207) online
- Kundeemne til kontanter-løsningen for Microsoft Dynamics 365 for Sales, versjon 1.15.0.0 (v15) 

   > [!NOTE]
   >
   > Maler med versjon 1.0.0.0 og 1.0.0.1 støttes for Kundeemne til kontanter-løsningen for Microsoft Dynamics 365 for Sales, versjon 1.14.1.0
   >
   > Maler med versjon 2.0.0.0 og 2.1.0.0 støttes for Kundeemne til kontanter-løsningen for Microsoft Dynamics 365 for Sales, versjon 1.15.0.0

### <a name="install-the-prospect-to-cash-solution-for-sales"></a>Installere Kundeemne til kontanter-løsningen for Sales

1. Last ned [Kundeemne til kontanter for Dynamics 365 for Sales, løsningspakke zip-fil](https://mbs.microsoft.com/customersource/Global/365Enterprise/downloads/product-releases/MD365FNOPENTProspectToCash) fra CustomerSource.
2. Kontroller at zip-filen ikke er blokkert. Ellers, når du prøver å installere løsningspakken, får du følgende feilmelding: "Finner ingen importpakker". Hvis du vil fjerne blokkeringen av ZIP-filen, høyreklikker du den og velger **Egenskaper**. Velg deretter **Fjern blokkering**.
3. Pakk ut og kjør **PackageDeployer.exe**.
4. Installer Kundeemne til kontanter-løsningen på forekomsten din av Sales:

    1. Velg **Office 365** som implementasjonstype.
    2. Velg **Vis avansert**.
    3. For en hurtiginstallasjon, velg et område. Hvis du velger **Vet ikke** vil systemet søke alle områder, og det vil ta lengre tid å installere.
    4. Skriv inn brukernavn og passord for en administratorbruker som har installasjonsrettigheter.

