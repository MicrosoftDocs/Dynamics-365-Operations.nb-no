---
title: Serviceobjektgrupper
description: Objektgrupper er nyttige for å kunne sortere og filtrere data til bruk i rapporter og statistikk.
author: ShylaThompson
manager: tfehr
ms.date: 05/11/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceObjectGroups
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4438487fa234cf093b557bca9455717b2cd3ca0b
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/10/2020
ms.locfileid: "3979238"
---
# <a name="service-object-groups"></a>Serviceobjektgrupper 

[!include [banner](../includes/banner.md)]

Objektgrupper er nyttige for å kunne sortere og filtrere data til bruk i rapporter og statistikk. Du kan for eksempel gruppere objekter etter geografisk plassering eller etter type.

## <a name="group-by-geographical-location"></a>Grupper etter geografisk plassering

Du kan bruke denne grupperingsmetoden for å vise hvor de ulike objektene som firmaet utfører tjenester for, befinner seg. Gruppering av objekter etter geografisk plassering kan også være nyttig hvis du for eksempel må identifisere objektene som firmaet allerede utfører tjenester for, i et bestemt land eller område.

## <a name="example"></a>Eksempel

En kunde fra Belgia ringer ditt servicecenter og vil opprette en en serviceavtale for et objekt, ABC. Du har tilknyttet en objektgruppe for geografisk plassering, Belgia, til alle objekter som betjenes i Belgia. Ved å bruke denne gruppen som et filter, kan du raskt søke for å se om du allerede har en post for ABC i programmet ditt, eller om du må definere et nytt objekt. 

## <a name="group-by-type"></a>Grupper etter type

Du kan bruke denne grupperingsmetoden for å vise hvilke typer av objekter firmaet ditt utfører tjenester for. Gruppering av objekter etter type kan også være nyttig hvis du for eksempel vil opprette et nytt objekt basert på liknende objekter som allerede finnes i programmet.

## <a name="example"></a>Eksempel

En kunde ringer og vil opprette en serviceavtale for en luftkondisjoneringsmaskin, HIJ. Du har ikke allerede en oppføring for denne maskinen. Men du har satt opp en objektgruppe som heter Luftkondisjonering, og du har knyttet denne gruppen til alle luftkondisjoneringsobjekter. Derfor kan du raskt søke etter og identifisere alle andre luftkondisjoneringsmaskiner og bruke malinformasjonen fra disse objektene til å opprette serviceavtalelinjer for HIJ. Ved å bruke objektgrupper på denne måten, kan du raskt definere nye objekter og avgjøre hvilke serviceoppgaver som må utføres på dem. 

## <a name="create-service-object-groups"></a>Opprette serviceobjektgrupper

Opprett grupper som du kan tilordne serviceobjekter til. Serviceobjekter er lagervarer og andre produkter som det utføres tjenester for. Når du grupperer serviceobjekter, kan du opprette rapporter for lignende og relaterte serviceobjekter. En serviceobjektgruppe kan for eksempel bestå av to serviceobjekter: ett serviceobjekt er et sett, og det andre serviceobjektet er tjenesten som skal installere settet.

Hvis du vil opprette serviceobjektgrupper, gjør du følgende:

1. Klikk **Servicestyring > Oppsett > Serviceobjekter > Serviceobjektgrupper** .

2. Klikk **Ny** for å opprette en ny serviceobjektgruppe.

3. Angi et unikt navn for serviceobjektgruppen, og eventuelt en beskrivelse.

Du kan tilordne serviceobjekter til gruppen ved hjelp av **Serviceobjekter** -skjemaet. 

## <a name="see-also"></a>Se også

[Opprette serviceobjekter](create-service-objects.md)


