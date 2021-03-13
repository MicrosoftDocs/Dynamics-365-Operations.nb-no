---
title: Endre en eksisterende områdeside
description: Dette emnet beskriver hvordan du endrer en eksisterende områdeside i Microsoft Dynamics 365 Commerce.
author: psimolin
manager: annbe
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 47a7d17b97631ba469a9b68f5f6cf492ebccde6f
ms.sourcegitcommit: 872600103d2a444d78963867e5e0cdc62e68c3ec
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/01/2021
ms.locfileid: "5097312"
---
# <a name="modify-an-existing-site-page"></a>Endre en eksisterende områdeside


[!include [banner](includes/banner.md)]

Dette emnet beskriver hvordan du endrer en eksisterende områdeside i Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Oversikt

Når du må endre en side, er det første trinnet å åpne den i sideredigeringsprogrammet. Gå til området som inneholder siden, og finn siden du vil bruke, i listen over sider. Hvis du ikke finner siden, kan du bruke redigeringsverktøyets omfattende søkefunksjonalitet. Skriv inn det nøyaktige sidenavnet, eller skriv inn de første bokstavene i objektet og deretter en stjerne (\*). Det vises en filtrert liste over sider. Du kan bruke denne listen til å finne siden du vil bruke. Når du har funnet riktig side, velger du sidenavnet for å åpne siden i sideredigeringsprogrammet.

> [!TIP]
> Hvis siden er synlig i sideinspeksjon, kan du velge **Rediger** og sjekke den ut siden før du åpner den i sideredigeringsprogrammet. På denne måten kan du sjekke ut flere sider samtidig.

Når siden er åpnet i redigeringsprogrammet for side, må du kontrollere at den er sjekket ut til deg. Kommandolinjen i redigeringsverktøyet er dynamisk, kontekstavhengig og tilstandsfølsom. Derfor vises bare handlingene du kan utføre på siden for øyeblikket. Hvis siden for eksempel ikke er sjekket ut til deg, vises ikke knappene **Lagre** og **Fullfør redigering** på kommandolinjen. Tilstanden for siden vises også på høyre side av vinduet.

Hvis siden ikke allerede er sjekket ut til deg, velger du **Rediger** kommandolinjen. Kommandolinjen endres til å gjenspeile den nye statusen for siden. Du får også et varsel som sier at siden ble sjekket ut til deg.

Det neste du gjør, er å utføre de faktiske endringene. Du vil ofte bruke sidedisposisjonstreet til venstre for å finne og velge modulen du vil endre, og deretter gjøre endringer i egenskapsruten til høyre. 

Endringen kan imidlertid noen ganger involvere å legge til eller fjerne modeller eller fragmenter. Hvis du vil legge til et fragment eller en modul, bruker du sidedisposisjonstreet til å finne sporet der du vil legge til modulen eller fragmentet, og deretter velger du ellipseknappen (**...**) for sporet. Det vises en meny som inneholder kommandoer for å legge til en modul eller et fragment. Hvis du vil fjerne en modul eller et fragment, kan du finne og merke den/det i sidedisposisjonstreet, velge ellipseknappen og deretter velge kommandoen for å slette modulen eller fragmentet.

> [!TIP]
> Du kan også vise og redigere egenskapene for en hvilken som helst modul i den visuelle sidebyggerforhåndsvisningen, ved å velge den direkte.

Når du er ferdig med å gjøre endringer og forhåndsvise effekten, bør du sjekke inn siden ved å velge **Fullfør redigering** på kommandolinjen. 

Hvis du vil publisere endringene umiddelbart, velger du **Publiser** på kommandolinjen. Den siste innsjekkede versjonen av siden du endret, publiseres og blir tilgjengelig for eksterne brukere som viser området ditt. 

## <a name="example-change-the-video-on-the-home-page"></a>Eksempel: Endre videoen på startsiden

Følgende eksempel viser hvordan du endrer startsiden ved å endre videoen som vises i videospillermodulen.

1. Under **Områder** velger du **Fabrikam** (eller navnet på området).
1. Velg **Sider** i navigasjonsruten til venstre.
1. Finn og velg startsside for å åpne den i sideredigeringsprogrammet.
1. På kommandolinjen velger du **Rediger**.
1. Velg **Hoved**-spor i sideoppsettet.
1. Utvid alle moduler for flytende containere under **Hoved**-sporet.
1. Finn og velg videospillermodulen.
1. I egenskapsruten til høyre velger du **video**-egenskapen. Aktivavelgeren vises.
1. I aktivavelgeren velger du et tilgjengelig videoaktiva, eller velg **Last opp nytt aktiva** for å laste opp et nytt videoaktiva.
1. Velg **OK**.
1. Velg **Lagre**, og velg deretter **Fullfør redigering**.
1. I feltet **Kommentarer** angir du **Endre videown**, og deretter velger du **OK**.
1. Velg **Forhåndsvisning** for å forhåndsvise den oppdaterte siden. Når du er ferdig, lukker du forhåndsvisningskategorien for å gå tilbake til redigeringsverktøyet.
1. Velg **Publiser**.

## <a name="additional-resources"></a>Tilleggsressurser

[Legg til en ny områdeside](add-new-page.md)

[Velge sideoppsett](select-page-layouts.md)

[Behandle metadata for søkemotor](manage-seo-metadata.md)

[Lagre, forhåndsvise og publisere en side](save-preview-publish-page.md)

[Supplere en produktside](enrich-product-page.md)

[Supplere en kategorimålside](enrich-category-page.md)

[Kontrollere tilgjengelighet for sideinnhold](verify-accessibility.md)

[Opprette dynamiske e-handelssider basert på URL-parametere](create-dynamic-pages.md)
