---
title: Serviceobjektrelasjoner
description: Du kan opprette serviceobjektrelasjoner mellom et serviceobjekt og en serviceavtale eller en serviceordre.
author: ShylaThompson
manager: tfehr
ms.date: 02/21/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceObjectRelation
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e2b1b76dffc2751d51c2a25d831fab512b747c15
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/10/2020
ms.locfileid: "3979360"
---
# <a name="service-object-relations"></a>Serviceobjektrelasjoner 

[!include [banner](../includes/banner.md)]

Du kan opprette serviceobjektrelasjoner mellom et serviceobjekt og en serviceavtale eller en serviceordre. Når du oppretter en relasjon, knytter du serviceobjektet til serviceavtalen eller serviceordren.

Når relasjonen er opprettet, kan du knytte serviceobjektet til en hvilken som helst linje i serviceavtalen eller serviceordren.

## <a name="template-boms"></a>Stykklistemaler

Du kan også angi en stykklistemal for objektrelasjonen. Stykklistemalen er en stykkliste for objektet som du utfører service på. Hvis du bytter en del som en del av serviceobjektet under et servicebesøk, kan du registrere denne endringene i servicestykklisten ved hjelp av Serviceobjekter-skjemaet.

## <a name="example"></a>Eksempel

Du oppretter en serviceavtale om å utføre service på to heiser i kundens bygg.
Serviceavtalen har identifikatoren ID SAL-001.

Heisene er definert som objekter i Serviceobjekter-skjemaet med numrene EL-S/1000 og EL-L/1000.

Du knytter serviceobjektene EL-S/1000 og EL-L/1000 til serviceavtalen.

Du vil registrere endringer i stykklisten (SL) for serviceobjektet når du setter inn reservedeler i objektet, så du knytter en servicestykkliste til serviceobjektrelasjonen, som beskrevet i tabellen nedenfor.

| Serviceobjekt | Relasjon – Serviceavtale | Servicestykkliste   |
|----------------|------------------------------|---------------|
| EL-S/1000      | ID SAL-001                   | SL-EL-S/1000 |
| EL-L/1000      | ID SAL-001                   | SL-EL-L/1000 |

Fordi det finnes serviceobjektrelasjoner for avtalen, kan du nå opprette serviceavtalelinjer med disse objektene, som vist i tabellen nedenfor.

| transaksjonstype | Kategori           | Serviceobjekt |
|------------------|--------------------|----------------|
| Time             | Inspeksjon         | EL-S/1000      |
| Time             | Rengjøring av girkasse  | EL-S/1000      |
| Vare             | Rengjøringsmaterialer | EL-S/1000      |
| Time             | Inspeksjon         | EL-L/1000      |
| Time             | Rengjøring av girkasse   | EL-L/1000      |
| Vare             | Rengjøringsmaterialer | EL-L/1000      |

På et servicebesøk må du bytte girkasse i heisen EL-S/1000. Når du skal bytte en del i objektet, kan du åpne stykklistedesigneren ved hjelp av serviceobjektrelasjonen som du definerte for gjeldende serviceavtale.

Åpne stykklistedesigneren ved hjelp av en serviceobjektrelasjon

1. Serviceavtaler
2. Dobbeltklikk en serviceavtale, eller klikk Serviceavtale for å opprette en serviceavtale.
3. Klikk kategorien Oppsett.
4. Klikk Serviceobjekter hvis du vil knytte en stykklistemal til serviceavtalen.
5. I Serviceobjekter-skjemaet klikker du Utforming for å åpne skjemaet Utforming for å endre stykklistemalen.

## <a name="automatically-created-service-orders"></a>Automatisk opprettede serviceordrer

Hvis du oppretter serviceordrer for serviceavtalen automatisk, opprettes også serviceobjektrelasjonene i avtalen, i serviceordrene.

