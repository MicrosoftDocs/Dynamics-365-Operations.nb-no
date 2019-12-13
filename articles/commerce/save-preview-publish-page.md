---
title: Lagre, forhåndsvise og publisere en side
description: Dette emnet beskriver hvordan du lagrer, forhåndsviser og publiserer en side i Microsoft Dynamics 365 Commerce.
author: psimolin
manager: annbe
ms.date: 10/01/2019
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
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 8c1b82b1b8423c63d442ee581ed0cc8789ee63fd
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697894"
---
# <a name="save-preview-and-publish-a-page"></a>Lagre, forhåndsvise og publisere en side

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Dette emnet beskriver hvordan du lagrer, forhåndsviser og publiserer en side i Microsoft Dynamics 365 Commerce.

## <a name="save-a-page"></a>Lagre en side

Hvis du vil lagre en side, må du sjekke den ut til deg selv og åpne den i redigeringsprogrammet. Du bør lagre en side umiddelbart etter at du har endret den, for å bidra til å sikre at endringene lagres.

Når du lagrer en side, er endringene bare synlige for deg. Lagringsoperasjonen er primært ment å lagre endringer mens siden ennå ikke er klar til å sjekkes inn. Når du er ferdig med å endre siden, anbefaler vi at du sjekker den inn, slik at endringene blir synlige for andre. På dette tidspunktet kan siden også sjekkes ut av andre brukere som må endre den.

## <a name="preview-a-page"></a>Forhåndsvise en side

Redigeringsverktøyet har to typer forhåndsvisningsfunksjoner: en WYSIWYG-forhåndsvisningsrute ("hva du ser, er hva du får") i sideredigeringsprogrammet og et eget forhåndsvisningsvindu.

Når du bruker sideredigeringsprogrammet, vises det en WYSIWYG-forhåndsvisning i den midtre ruten. Denne forhåndsvisningen oppdateres automatisk hver gang du lagrer siden. Du kan også oppdatere den manuelt ved å velge **Oppdater** på kommandolinjen. WYSIWYG-forhåndsvisning gjengir siden på samme måte som områdets brukere vil se den, men redigeringshjelpere gjengis oppå den.

Når du er ferdig med å endre siden, kan det være lurt å forhåndsvise den for å se hva kundene vil se. Velg **Forhåndsvisning** på kommandolinjen for å forhåndsvise en side. Forhåndsvisningen vil vises i et eget leservindu. Siden i forhåndsvisningsvinduet vises på samme måte som områdets bruker vil se den. Du kan endre størrelsen på vinduet for å kontrollere at svarmoduler gjengis riktig i alle visningsporter.

> [!NOTE]
> Godkjenning og riktige tillatelser kreves for å forhåndsvise upublisert innhold. Hvis du deler URL-adressen for forhåndsvisningen med noen, må vedkommende derfor ha de riktige tillatelsene for å få tilgang til innholdet.

## <a name="publish-a-page"></a>Publisere en side

Når siden er klar, er det neste trinnet å publisere den, slik at eksterne brukere kan vise innholdet. Før du kan publisere en side må du sjekke den inn.

Du kan publisere og oppheve publiseringen av sidene enten fra sideinspeksjonen eller sideredigeringen. Sideinspeksjonen viser en liste over sider og tillater masseoperasjoner. Sideredigeringsprogrammet kan brukes til å publisere eller oppheve publiseringen av bare den ene siden som er åpen i den.

Hvis du vil publisere én eller flere sider fra sideinspeksjonen, merker du sidene, kontrollerer at de er sjekket inn, og deretter velger **Publiser** på kommandolinjen. Sidene publiseres, og du mottar en melding om operasjonen i redigeringsverktøyet.

Fremgangsmåten er lik for publisering av en enkelt side fra sideredigeringsprogrammet. Mens siden er åpen i redigeringsprogrammet for side, må du kontrollere at den er sjekket inn og deretter velge **Publiser** på kommandolinjen. Siden publiseres, og du mottar en melding om operasjonen.

Når du publiserer en side, publiseres bare sideinnholdet. Du og andre brukere kan gå til siden og vise den bare etter at en URL-adresse er tilknyttet. Nettadressen må publiseres separat.

> [!IMPORTANT]
> Før du kan publisere en side må alle bilder eller fragmenter som siden refererer til, allerede være publisert.

## <a name="save-preview-and-publish-a-home-page"></a>Lagre, forhåndsvise og publisere en startside

Følg denne fremgangsmåten for å lagre, forhåndsvise og publisere en startside.

1. Under **Områder** velger du **Fabrikam** (eller navnet på området).
1. Velg **Sider**i navigasjonsruten til venstre.
1. Finn og velg startsside for å åpne den i sideredigeringsprogrammet.
1. Velg **Sjekk ut**.
1. Endre siden slik du vil ha den.
1. Velg **Lagre**, og velg deretter **Sjekk inn**.
1. Skriv inn en merknad om endringene du har gjort, i feltet **Kommentar**, og velg deretter **OK**.
1. Velg **Forhåndsvisning** for å forhåndsvise siden. Når du er ferdig, lukker du forhåndsvisningskategorien for å gå tilbake til redigeringsverktøyet.
1. Velg **Publiser**.

## <a name="publish-a-url"></a>Publisere en URL-adresse

Hvis du vil publisere en URL-adresse, følger du disse trinnene.

1. Under **Områder** velger du **Fabrikam** (eller navnet på området).
1. Velg **URL-adresser**i navigasjonsruten til venstre.
1. Finn og velg URL-adressen du vil publisere.
1. På kommandolinjen velger du **Publiser**.

## <a name="additional-resources"></a>Tilleggsressurser

[Endre en eksisterende områdeside](modify-existing-page.md)

[Legg til en ny områdeside](add-new-page.md)

[Velge sideoppsett](select-page-layouts.md)

[Behandle metadata for søkemotor](manage-seo-metadata.md)

[Supplere en produktside](enrich-product-page.md)

[Supplere en kategorimålside](enrich-category-page.md)

