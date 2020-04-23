---
title: Import leverandørkataloger
description: Dette emnet beskriver prosessen for å importere leverandørkatalogdata.
author: mkirknel
manager: tfehr
ms.date: 03/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendProspectiveVendorRegistrationRequests
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: mkirknel
ms.search.validFrom: 2018-04-20
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: 35b8e2a87708c88b12c5c7605a7977712a35a0f4
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/02/2020
ms.locfileid: "3207384"
---
# <a name="import-vendor-catalogs"></a>Import leverandørkataloger
[!include[banner](../includes/banner.md)]

## <a name="vendor-catalogs-import"></a>Import av leverandørkataloger

I Dynamics 365 Supply Chain Management kan innkjøpere opprette og vedlikeholde kataloger som firmaets ansatte kan bruke når de bestiller varer og tjenester til internt bruk. Hvis du vil opprette en innkjøpskatalog, kan du legge til varene og tjenestene som du vil gjøre tilgjengelig for ansatte, enten ved å importere produktkatalogdata eller ved å legge til produktkatalogdata manuelt til produktstandarden. 

Du kan laste opp katalogdataene som sendes av en leverandør, fra Microsoft Dynamics 365-klienten.

Produktdataene som en leverandøre sender til deg, i form av en PriKat-fil, må være i XML-filformat. PriKat-filen bør inneholde detaljene for produktene som leverandøren leverer til firmaet.
''''
## <a name="import-vendor-catalog-data"></a>Import leverandørkatalogdata
'' Du må utføre følgende oppgaver for å importere leverandørkatalogdata:

1.  Definer et prosjekt i arbeidsområdet Databehandling der du har definert regler for tilordning av data. Velg **Databehandling**, og velg deretter **Definer roller for dataprosjekter**. 
    ''
2.  Definer et innkjøpskategorihierarki, og tilordne leverandører til innkjøpskategoriene. Hvis du bruker varekoder, kan du legge til varekodene i innkjøpskategoriene. Hvis du vil ha informasjon om hvordan du definerer et innkjøpskategorihierarki, se [Definer et innkjøpskategorihierarki](../procurement/tasks/set-up-procurement-category-hierarchy.md).
    ''
3.  Konfigurer leverandøren for katalogimport. Velg en leverandør, og velg deretter **Innkjøp** > **Oppsett** > **Konfigurer leverandør for katalogimport**.
''''
4.  Konfigurer arbeidsflyt for katalogimport. Opprett en mal for PriKat-filen, og del den med leverandøren.

5.  Velg **Innkjøp og leverandører** \> **Felles** \> **Kataloger** \> **Leverandørkataloger** for å opprette en leverandørkatalog. PriKat-filene du mottar fra leverandøren, er gruppert i denne katalogen. 

6.  Last opp PriKat-filen.

7.  Gå gjennom, godkjenn eller avvis produktene i leverandørkatalogen. Produktene tilordnes automatisk til innkjøpskategoriene. 
    
Godkjente produkter legges til i produktstandarden og frigis til de valgte juridiske enhetene. Bare godkjente produkter kan legges til i innkjøpskatalogen.

## <a name="generate-a-catalog-import-file-template"></a>Generere en filmal for katalogimport

Filmalen for katalogimport er en XSD-fil som bruker til å opprette en PriKat-fil for produktene til en leverandør. Du kan bruke PriKat-filen til å opprette en ny katalog, erstatte en eksisterende katalog eller endre en eksisterende katalog.

1.  Velg **Innkjøp og leverandører** \> **Kataloger** \> **Leverandørkataloger**, og dobbeltklikk katalogen du vil arbeide med.

2.  Last ned en gjeldende katalogmportmal (XSD-fil). På siden **Oppdater katalog**, i **handlingsruten** i kategorien **Kataloger** i gruppen **Beslektet informasjon**, klikker du **Generer katalogmal**, og velger **Innkjøpskategori**.

    -   I **innkjøpskategorien** kan du generere en katalogmal som omfatter innkjøpskategoriene der leverandøren er autorisert til å levere produkter.

3. Velg plasseringen der du vil lagre katalogfilmalen og filen, i dialogboksen **Lagre som**.

Hvis du vil ha mer informasjon og eksempler, kan du se dette blogginnlegget: [Leverandørkataloger i Dynamics AX](https://blogs.msdn.microsoft.com/dynamicsaxscm/2016/05/25/vendor-catalogs-in-dynamics-ax/).
