---
title: Legge til et favorittikon
description: Dette emnet forklarer hvordan du legger til et favorittikon på området.
author: bicyclingfool
manager: annbe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 58cb6c592351a96876532ef53d5d477ff93fafa1
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/01/2019
ms.locfileid: "2696997"
---
# <a name="add-a-favicon"></a>Legge til et favorittikon

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Dette emnet forklarer hvordan du legger til et favorittikon på området.

## <a name="overview"></a>Oversikt

Et favorittikon er en liten grafikkfil som vises i en webleserkategori, i adressefeltet, i leserloggen og i bokmerker eller favoritter, blant andre steder. Vi anbefaler at du legger til et favorittikon på området, fordi det representerer og forsterker et merke, og bidrar til å identifisere området fra andre områder som kundene besøker.

Selv om du kan legge til flere favorittikoner av forskjellige størrelser og filtyper på området, viser dette emnet hvordan du legger til ett enkelt favorittikon. Den samme prosessen og lokasjonen brukes imidlertid til å legge til flere favorittikoner.

## <a name="upload-a-favicon-to-your-sites-asset-collection"></a>Laste opp et favorittikon til aktivasamlingen på området

Følg denne fremgangsmåten for å laste opp et favorittikon til områdets aktivasamling.

1. Gå til **Aktiva \> Last opp \> Last opp aktiva**.
1. Finn og velg favorittikon på det lokale filsystemet.
1. Skriv inn en tittel, og velg deretter **OK**. 
1. I egenskapsruten til høyre kopierer du den offentlige URL-adressen til favorittikonet.

> [!NOTE]
> Hvis du ikke velger alternativet **Publiser aktiva etter opplasting**, må du gå tilbake til siden **Aktiva** og manuelt publisere favorittikonet senere.

## <a name="create-the-html-for-the-favicon"></a>Opprette HTML for favorittikonet

Hvis du vil opprette HTML-koden for favorittikonet, bruker du følgende HTML-kodesnutt. For **href**-attributtet erstatter du **"Public\_URL\_for\_your\_favicon"** " med den offentlige URL-adressen du kopierte tidligere.

`<link rel="shortcut icon" href="Public_URL_for_your_favicon">`

## <a name="add-the-html-for-the-favicon-to-the-head-element-of-your-pages"></a>Legge HTML-koden til favorittikonet i \<hode\>-elementet på sidene

Hvis du vil legge til et favorittikon på området, bruker du den samme fremgangsmåte som brukes til å legge til en hvilken som helst type HTML eller skript i elementet **\<hode\>** på områdesidene.

## <a name="additional-resources"></a>Tilleggsressurser

[Legge til en logo](add-logo.md)

[Velge et områdetema](select-site-theme.md)

[Legge til en velkomstmelding](add-welcome-message.md)

[Legge til en opphavsrettserklæring](add-copyright-notice.md)

[Legge til språk på området](add-languages-to-site.md)

[Legge til skript kode i områdes ID-er for å støtte telemetri](add-telemetry.md)

