---
title: Synkronisere produkter direkte fra Supply Chain Management til produkter i Sales
description: Dette emnet beskriver malene og de underliggende oppgavene som brukes til å synkronisere produkter fra Dynamics 365 Supply Chain Management til Dynamics 365 Sales.
author: ChristianRytt
ms.date: 06/10/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: 8976bc69f63fe5b05ab7dcb8d415515436902658
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/16/2021
ms.locfileid: "5909090"
---
# <a name="synchronize-products-directly-from-supply-chain-management-to-products-in-sales"></a>Synkronisere produkter direkte fra Supply Chain Management til produkter i Sales

[!include [banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

> [!NOTE]
> Før du kan bruke kundeemnet til kontanter løsning må du ha kjennskap til [Integrere data til Microsoft Dataverse for Apps](/powerapps/administrator/data-integrator).

Dette emnet beskriver malene og de underliggende oppgavene som brukes til å synkronisere produkter direkte fra Dynamics 365 Supply Chain Management til Dynamics 365 Sales.

## <a name="data-flow-in-prospect-to-cash"></a>Dataflyt i Kundeemne til kontanter

Løsningen Kundeemne til kontanter bruker Dataintegrering-funksjonen til å synkronisere data på tvers av forekomster av Supply Chain Management og Sales. Kundeemne til kontanter-maler som er tilgjengelige med Dataintegrering-funksjonen,tillater flyt av data om kontoer, kontakter, produkter, salgstilbud, salgsordrer og salgsfakturaer mellom Supply Chain Management og Sales. Illustrasjonen nedenfor viser hvordan dataene blir synkronisert mellom Supply Chain Management og Sales.

[![Dataflyt i Kundeemne til kontanter](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)

## <a name="templates-and-tasks"></a>Maler og oppgaver

Hvis du vil ha tilgang til de tilgjengelige malene, kan du åpne [administrasjonssenteret for Power Apps](https://admin.powerapps.com/dataintegration). Velg **Prosjekter**, og velg deretter **Nytt prosjekt** til øverst til høyre for å velge offentlig maler.

Malen nedenfor og de underliggende oppgavene brukes til å synkronisere produkter fra Supply Chain Management til Sales.

- **Navnet på malen i Dataintegrering:** Produkter (Supply Chain Management til Sales) – direkte
- **Navnet på oppgaven i Dataintegrasjonprosjektet**: Produkter

Ingen synkroniseringsoppgaver kreves før produktsynkronisering kan utføres.

## <a name="entity-set"></a>Enhetssett

| Supply Chain Management    | Salg    |
|----------------------------|----------|
| Salgbare frigitte produkter | Produkter |

## <a name="entity-flow"></a>Enhetsflyt

Produkter administreres i Supply Chain Management og synkroniseres til Sales. Sataenheten **Salgbare frigitte produkter** i Supply Chain Management eksporterer bare produkter som er *salgbare*. salgbare produkter er produkter som inneholder informasjon som kreves for å kunne brukes på en salgsordre. De samme reglene gjelder når et produkt er bekreftet ved å bruke **Valider**-funksjonen på siden **Frigitt produkt**.

Produktnummeret brukes som en nøkkel. Når produktvarianter synkroniseres til Sales, har hver produktvariant én enkelt produkt-ID.

## <a name="prospect-to-cash-solution-for-sales"></a>Kundeemnet til kontanter løsning for Sales

I Sales legges det til et nytt **Vedlikeholdes eksternt**-felt på produktene for å angi at et bestemt produkt vedlikeholdes eksternt. Verdien er satt til **Ja** som standard under import til Sales. Følgende verdier er tilgjengelige:

- **Ja** – Produktet kommer fra Supply Chain Management og kan ikke redigeres i Sales.
- **Nei** – Produktet ble lagt inn direkte i Sales.
- **(Tom)** – Produktet fantes i Sales før løsningen Kundeemne til kontanter ble aktivert.

Informasjonen i feltet **Vedlikeholdes eksternt** brukes til å sikre at bare tilbud og salgsordrer med eksternt vedlikeholdte produkter synkroniseres til Supply Chain Management.

Eksternt vedlikeholdte produkter legges automatisk til den første gyldige prislisten med samme valuta. Prislister er ordnet alfabetisk etter navn. Produktets salgspris fra Supply Chain Management brukes som prisen på prislisten. Derfor må det være en prisliste i Sales for alle produktsalgsvaluta i Supply Chain Management. Valutaen på frigitte salgbare produkter er satt til regnskapsvalutaen i den juridiske enheten som produktet er eksportert fra.

> [!NOTE]
> - Produktsynkronisering lykkes ikke hvis det ikke er en prisliste som har en tilhørende valuta.
> - Du kan kontrollere den brukte prislisten med integreringen ved å tilordne pricelevelid.name [standard prisliste (navn)] i dataintegrasjonsprosjektet. Inndataene må være med bare små bokstaver. Standardverdien for en prisliste i Sales med navnet Standard, er for eksempel: Målfelt: pricelevelid.name [standard prisliste (navn)] og tilordningstype: [ { "transformType": "Standard", "defaultValue": "standard" } ].

## <a name="preconditions-and-mapping-setup"></a>Forutsetninger og tilordningsdefinisjon

- Før du kjører synkroniseringen for første gang, må du fylle ut den spesifikke produkttabellen for eksisterende produkter i Supply Chain Management. Eksisterende produkter vil ikke bli synkronisert før denne jobben er fullført.

    1. I Supply Chain Management kan du bruke Søk til å søke etter **Fyll ut tabell for spesifikt produkt**.
    2. Velg **Fyll ut tabell for spesifikt produkt** for å kjøre jobben. Jobben må kjøres bare én gang.

- Pass på at den nødvendige verditilordningen for selgende måleenheten mellom Supply Chain Management og Sales finnes i tilordningen for **SalesUnitSymbol** til **DefaultUnit (Name)**.
- Oppdater verditilordningen for **enhetsgruppen** (**defaultuomscheduleid.name**), slik at den samsvarer med **enhetsgruppene** i Sales.

    Standard malverdi er **Standardenhet**.

- Kontroller at målenheter for alle produkter fra Supply Chain Management finnes i Sales.
- Kontroller at prislister finnes i Sales for alle produktsalgsvaluta i Supply Chain Management.
- Når produkter opprettes i Sales, får de statusen **Utkast** eller **Aktiv**. Virkemåten kontrolleres under **Innstillinger** > **Administrasjon** > **Systeminnstillinger** > **Salg** i Sales.

    Produkter som har statusen **Utkast** når de opprettes, må aktiveres før de kan legges til i tilbud eller salgsordrer.

## <a name="template-mapping-in-data-integration"></a>Maltilordning i Dataintegrering

Illustrasjonen nedenfor viser et eksempel på en tilordning av malen i Dataintegrering. 

> [!NOTE]
> Tilordningen viser hvilken feltinformasjon som vil bli synkronisert fra Sales til Supply Chain Management.

![Maltilordning i Dataintegrator](./media/products-direct-template-mapping-data-integrator-1.png)


## <a name="related-topics"></a>Relaterte emner

[Kundeemne til kontanter](prospect-to-cash.md)

[Synkronisere kontoer direkte fra Sales til kunder i Supply Chain Management](accounts-template-mapping-direct.md)

[Synkronisere kontakter direkte fra Sales til kontakter eller kunder i Supply Chain Management](contacts-template-mapping-direct.md)

[Synkronisering av salgsordrer direkte mellom Sales og Supply Chain Management](sales-order-template-mapping-direct-two-ways.md)

[Synkronisere salgsfakturahoder og -linjer direkte fra Supply Chain Management til Sales](sales-invoice-template-mapping-direct.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]