---
title: Legge til et favorittikon
description: Dette emnet forklarer hvordan du legger til et favorittikon på området.
author: bicyclingfool
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 9268bc74a4131256f5a2e88df833104db271b56a
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797725"
---
# <a name="add-a-favicon"></a>Legge til et favorittikon

[!include [banner](includes/banner.md)]

Dette emnet forklarer hvordan du legger til et favorittikon på området.

Et favorittikon er en liten grafikkfil som vises i en webleserkategori, i adressefeltet, i leserloggen og i bokmerker eller favoritter, blant andre steder. Vi anbefaler at du legger til et favorittikon på området, fordi det representerer og forsterker et merke, og bidrar til å identifisere området fra andre områder som kundene besøker.

Selv om du kan legge til flere favorittikoner av forskjellige størrelser og filtyper på området, viser dette emnet hvordan du legger til ett enkelt favorittikon. Den samme prosessen og lokasjonen brukes imidlertid til å legge til flere favorittikoner.

## <a name="upload-a-favicon-to-your-sites-asset-collection"></a>Laste opp et favorittikon til aktivasamlingen på området

Følg denne fremgangsmåten for å laste opp et favorittikon til områdets aktivasamling.

1. Velg **Mediebibliotek** i navigasjonsruten til venstre.
1. Velg **Last opp \> Last opp medieelementer** på kommandolinjen.
1. I filutforskervinduet blar du til favorittikonfilen du vil laste opp, velger den og velger deretter **Åpne**.
1. I dialogboksen **Last opp medieelement** angir du nødvendig tittel og alt-tekst.
1. Hvis du vil publisere bilder like etter opplastingen, merker du av for **Publiser medieelementer etter opplasting**.

    > [!NOTE]
    > Hvis du ikke merker av for **Publiser medieelementer etter opplasting**, må du gå tilbake til siden **Medieelementer** og manuelt publisere favorittikonet senere.

1. Velg **OK**.
1. I egenskapsruten til høyre kopierer du den offentlige URL-adressen til favorittikonet. Du skal bruke denne URL-adressen senere.

## <a name="create-the-html-for-your-favicon"></a>Opprette HTML for favorittikonet ditt

Hvis du vil opprette HTML-koden for favorittikonet, bruker du følgende HTML-streng. For **href**-attributtet erstatter du **Public\_URL\_for\_your\_favicon** med den offentlige URL-adressen du kopierte tidligere.

`<link rel="shortcut icon" href="Public_URL_for_your_favicon">`

## <a name="create-a-fragment-that-contains-a-metatag-for-your-favicon"></a>Opprette et fragment som inneholder en metakode for favorittikon

For å opprette et fragment som inneholder en metakode for favorittikon, følger du disse trinnene.

1. Gå til **Fragmenter**, og velg **Nytt**.
1. I dialogboksen **Nytt fragment** velger du **Metakoder** som modulen som fragmentet er basert på.
1. Angi et navn på fragmentet, og velg deretter **OK**.
1. Velg det underordnede **Standard metakoder** i fragmenthierarkitreet.
1. I ruten til høyre under **Metakoder** velger du **Legg til**, og deretter skriver du inn HTML-strengen du opprettet tidligere for favorittikonet. 
1. Velg **Fullfør redigering**, og velg deretter **Publiser** for å publisere fragmentet.

## <a name="add-the-metatag-fragment-to-the-html-head-section-of-your-pages"></a>Legge til metakodefragmentet i HTML-hodedelen på sidene

For å legge til metakodefragmentet i delen HTML-**hode** på sidene følger du trinnene nedenfor.

1. Gå til **Maler**, og åpne malen for sidene du vil legge til favorittikonet ditt, og velg deretter **Rediger**.
1. I malhierarkitreet velger du ellipser (**...**)-knappen til høyre for **HTML-hode**-beholderen, og deretter velger du **Legg til fragment**.
1. I dialogboksen **Velg fragment** velger du metakodefragmentet du opprettet tidligere, og deretter velger du **OK**.
1. Velg **Fullfør redigering**, og velg deretter **Publiser** for å publisere malen.

> [!NOTE]
> Hvis området bruker mer enn én mal, må du legge til metakodefragmentet i alle.

Når du forhåndsviser sider som er basert på malen som du la til metakodefragmentet i, kan du nå se favorittikonet i leserkategorien.

## <a name="additional-resources"></a>Tilleggsressurser

[Legge til en logo](add-logo.md)

[Velge et områdetema](select-site-theme.md)

[Arbeide med CSS-overstyringsfiler](css-override-files.md)

[Legge til en velkomstmelding](add-welcome-message.md)

[Legge til en opphavsrettserklæring](add-copyright-notice.md)

[Legge til språk på området](add-languages-to-site.md)

[Legge til skript kode i områdes ID-er for å støtte telemetri](add-telemetry.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
