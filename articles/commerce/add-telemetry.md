---
title: Legge til skript kode i områdes ID-er for å støtte telemetri
description: Dette emnet beskriver hvordan du kan legge til skriptkode på klientsiden på områdesidene dine for å støtte innsamling av telemetri på klientsiden.
author: bicyclingfool
manager: annbe
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 674d00faf1b30f87a0b0062129e1b9fbff955dd4
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/01/2020
ms.locfileid: "3001283"
---
# <a name="add-script-code-to-site-pages-to-support-telemetry"></a>Legge til skript kode i områdes ID-er for å støtte telemetri


[!include [banner](includes/banner.md)]

Dette emnet beskriver hvordan du kan legge til skriptkode på klientsiden på områdesidene dine for å støtte innsamling av telemetri på klientsiden.

## <a name="overview"></a>Oversikt

Web Analytics er et viktig verktøy når du vil forstå hvordan kundene samhandler med området og tar avgjørelser som vil bidra til å optimalisere opplevelsen for maksimal konvertering. Mange Web Analytics-pakker er tilgjengelige for å hjelpe deg med å oppnå disse målene, for eksempel Google Analytics, Clicky, Moz Analytics og KISSMetrics. De fleste Web Analytics-pakker krever at du legger til skriptkode på klientsiden i **\<hode\>**-elementet på HTMLen for alle sidene på området.

> [!NOTE]
> Instruksjonene i dette emnet gjelder også for annen tilpasset funksjonalitet på klientsiden som Microsoft Dynamics 365 Commerce ikke tilbyr.

## <a name="create-a-reusable-fragment-for-your-script-code"></a>Opprette et gjenbrukbart fragment for skriptkoden

Når du har opprettet et fragment for skriptkoden, kan det brukes på nytt på alle sider på området.

1. Gå til **Fragmenter \> Nytt sidefragment**.
2. Velg **Eksternt skript**, skriv inn et navn på fragmentet, og velg deretter **OK**.
3. I fragmenthierarkiet velger du den underordnede **skriptinnsetting**-modulen for fragmentet som du nettopp opprettet.
4. I egenskapsruten til høyre legger du til skriptet på klientsiden, og deretter angir du andre konfigurasjonsalternativer etter behov.

## <a name="add-the-fragment-to-templates"></a>Legge til fragmentet i maler

1. Gå til **Maler**, og åpne malen for sidene du vil legge til skriptkoden i.
2. I venstre rute utvider du malhierarkiet slik at det viser **HTML-hode**-sporet.
3. Velg ellipseknappen (**...**) for **HTML-hode**-sporet, og velg deretter **Legg til fragment**.
4. Velg fragmentet du opprettet for skriptkoden.
5. Lagre malen, og sjekk den inn.

> [!NOTE]
> Når du er ferdig, må du publisere fragmentet og malen. 

## <a name="additional-resources"></a>Tilleggsressurser

[Legge til en logo](add-logo.md)

[Velge et områdetema](select-site-theme.md)

[Arbeide med CSS-overstyringsfiler](css-override-files.md)

[Legge til et favorittikon](add-favicon.md)

[Legge til en velkomstmelding](add-welcome-message.md)

[Legge til en opphavsrettserklæring](add-copyright-notice.md)

[Legge til språk på området](add-languages-to-site.md)

