---
title: Legge til skript kode i områdes ID-er for å støtte telemetri
description: Dette emnet beskriver hvordan du kan legge til skriptkode på klientsiden på områdesidene dine for å støtte innsamling av telemetri på klientsiden.
author: bicyclingfool
manager: annbe
ms.date: 03/20/2020
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
ms.openlocfilehash: 4f26ed5b6674566f579e801f4b7be63c2d0dc38d
ms.sourcegitcommit: 81f162f2d50557d7afe292c8d326618ba0bc3259
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/11/2020
ms.locfileid: "3686820"
---
# <a name="add-script-code-to-site-pages-to-support-telemetry"></a>Legge til skript kode i områdes ID-er for å støtte telemetri

[!include [banner](includes/banner.md)]

Dette emnet beskriver hvordan du kan legge til skriptkode på klientsiden på områdesidene dine for å støtte innsamling av telemetri på klientsiden.

## <a name="overview"></a>Oversikt

Web Analytics er et viktig verktøy når du vil forstå hvordan kundene samhandler med området og tar avgjørelser som vil bidra til å optimalisere opplevelsen for maksimal konvertering. Mange Web Analytics-pakker er tilgjengelige for å hjelpe deg med å oppnå disse målene, for eksempel Google Analytics, Clicky, Moz Analytics og KISSMetrics. De fleste Web Analytics-pakker krever at du legger til skriptkode på klientsiden i **\<head\>**-elementet i HTML-koden for alle sidene på området.

> [!NOTE]
> Instruksjonene i dette emnet gjelder også for annen tilpasset funksjonalitet på klientsiden som Microsoft Dynamics 365 Commerce ikke tilbyr.

## <a name="create-a-reusable-page-fragment-for-your-script-code"></a>Opprette et gjenbrukbart sidefragment for skriptkoden

Ved hjelp av et sidefragment kan du bruke innebygd eller ekstern skriptkode på nytt på alle sidene på området, uansett hvilken mal de bruker.

### <a name="create-a-reusable-page-fragment-for-your-inline-script-code"></a>Opprette et gjenbrukbart sidefragment for den innebygde skriptkoden

Hvis du vil opprette et gjenbrukbart sidefragment for den innebygde skriptkoden i områdebygger, følger du disse trinnene.

1. Gå til **Fragmenter**, og velg deretter **Nytt**.
1. I dialogboksen **Nytt sidefragment** velger du **Innebygd skript**.
1. Under **Navn på sidefragment** angir du et navn på fragmentet, og deretter velger du **OK**.
1. Under sidefragmentet du opprettet, velger du modulen **Standard innebygd skript**.
1. I egenskapsruten til høyre, under **Innebygd skript**, angir du skriptet på klientsiden. Deretter konfigurerer du andre alternativer etter behov.
1. Velg **Lagre**, og velg deretter **Fullfør redigering**.
1. Velg **Publiser**.

### <a name="create-a-reusable-page-fragment-for-your-external-script-code"></a>Opprette et gjenbrukbart sidefragment for den eksterne skriptkoden

Hvis du vil opprette et gjenbrukbart sidefragment for den eksterne skriptkoden i områdebygger, følger du disse trinnene.

1. Gå til **Fragmenter**, og velg deretter **Nytt**.
1. I dialogboksen **Nytt sidefragment** velger du **Eksternt skript**.
1. Under **Navn på sidefragment** angir du et navn på fragmentet, og deretter velger du **OK**.
1. Under sidefragmentet du opprettet, velger du modulen **Standard eksternt skript**.
1. I egenskapsruten til høyre, under **Skriptkilde**, legger du til en ekstern eller relativ URL-adresse for den eksterne skriptkilden. Deretter konfigurerer du andre alternativer etter behov.
1. Velg **Lagre**, og velg deretter **Fullfør redigering**.
1. Velg **Publiser**.

## <a name="add-a-page-fragment-that-includes-script-code-to-a-template"></a>Legge til et sidefragment som inneholder skript kode, i en mal

Hvis du vil legge til et sidefragment som inneholder skriptkode, i en mal i områdebygger, følger du disse trinnene.

1. Gå til **Maler**, og åpne malen for sidene du vil legge til skriptkoden i.
1. I venstre rute utvider du malhierarkiet slik at det viser **HTML-hode**-sporet.
1. Velg ellipseknappen (**...**) for **HTML-hode**-sporet, og velg deretter **Legg til sidefragment**.
1. Velg fragmentet du opprettet for skriptkoden.
1. Velg **Lagre**, og velg deretter **Fullfør redigering**.
1. Velg **Publiser**.

## <a name="add-an-external-script-or-inline-script-directly-to-a-template"></a>Legge til et eksternt skript eller innebygd skript direkte i en mal

Hvis du vil sette inn et innebygd eller eksternt skript direkte i et sett med sider som styres av en enkelt mal, trenger du ikke å opprette et sidefragment først.

### <a name="add-an-inline-script-directly-to-a-template"></a>Legge til et innebygd skript direkte i en mal

Hvis du vil legge til et innebygd skript direkte i en mal i områdebygger, følger du disse trinnene.

1. Gå til **Maler**, og åpne malen for sidene du vil legge til skriptkoden i.
1. I venstre rute utvider du malhierarkiet slik at det viser **HTML-hode**-sporet.
1. Velg ellipseknappen (**...**) for **HTML-hode**-sporet, og velg deretter **Legg til modul**.
1. I dialogboksen **Legg til modul** velger du **Innebygd skript**.
1. I egenskapsruten til høyre, under **Innebygd skript**, angir du skriptet på klientsiden. Deretter konfigurerer du andre alternativer etter behov.
1. Velg **Lagre**, og velg deretter **Fullfør redigering**.
1. Velg **Publiser**.

### <a name="add-an-external-script-directly-to-a-template"></a>Legge til et eksternt skript direkte i en mal

Hvis du vil legge til et eksternt skript direkte i en mal i områdebygger, følger du disse trinnene.

1. Gå til **Maler**, og åpne malen for sidene du vil legge til skriptkoden i.
1. I venstre rute utvider du malhierarkiet slik at det viser **HTML-hode**-sporet.
1. Velg ellipseknappen (**...**) for **HTML-hode**-sporet, og velg deretter **Legg til modul**.
1. I dialogboksen **Legg til modul** velger du **Eksternt skript**.
1. I egenskapsruten til høyre, under **Skriptkilde**, legger du til en ekstern eller relativ URL-adresse for den eksterne skriptkilden. Deretter konfigurerer du andre alternativer etter behov.
1. Velg **Lagre**, og velg deretter **Fullfør redigering**.
1. Velg **Publiser**.

## <a name="additional-resources"></a>Tilleggsressurser

[Legge til en logo](add-logo.md)

[Velge et områdetema](select-site-theme.md)

[Arbeide med CSS-overstyringsfiler](css-override-files.md)

[Legge til et favorittikon](add-favicon.md)

[Legge til en velkomstmelding](add-welcome-message.md)

[Legge til en opphavsrettserklæring](add-copyright-notice.md)

[Legge til språk på området](add-languages-to-site.md)
