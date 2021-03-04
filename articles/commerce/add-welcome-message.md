---
title: Legge til en velkomstmelding
description: Dette emnet beskriver hvordan du legger til en velkomstmelding i Microsoft Dynamics 365 Commerce-webområdet.
author: psimolin
manager: annbe
ms.date: 04/13/2020
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
ms.openlocfilehash: d2a125b4e71016ad620f128af2e3c9f29aa04f4c
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4414596"
---
# <a name="add-a-welcome-message"></a>Legge til en velkomstmelding


[!include [banner](includes/banner.md)]

Dette emnet beskriver hvordan du legger til en velkomstmelding i Microsoft Dynamics 365 Commerce-webområdet.

## <a name="overview"></a>Oversikt

En velkomstmelding på webområdet for e-handel kan informere besøkende om pågående salg, områdeoppdateringer eller tilgjengelighet for sesongsamlinger. Velkomstmeldingen angis ved hjelp av varselmodulen.

Varselmodulen skal legges til i sporet for **Feilmeldinger/Informasjonsmeldinger** i topptekstfragmentet. Ved hjelp av varselmodulen kan du angi teksten som vises, tekstfargen og justeringen. Du kan også angi om gjester på området kan ignorere meldingen.

Når en velkomstmelding blir lagt til i et delt topptekstfragment, vises den på hver side som bruker malen der det delte topptekstfragmentet brukes.

Følg denne fremgangsmåten for å legge til en velkomstmelding på området.

1. Gå til området i Commerce-områdebygger.
1. Velg **Fragmenter**.
1. Velg topptekstfragmentet du vil legge til meldingen i.
1. Utvid **Feilmeldinger/Informasjonsmeldinger** i disposisjonstreet.
1. Velg varselmodulen, og velg deretter **OK**. Hvis det ennå ikke finnes en varselmodul, velger du først ellipseknappen (**...**) ved siden **Feilmeldinger/Informasjonsmeldinger**, og deretter velger du **Legg til modul**.
1. I egenskapsruten til høyre, i kategorien **Data**, velger du **Legg til datakilde**, og deretter velger du **Innhold**.
1. I feltet **Inndatatekst** skriver du inn teksten i velkomstmeldingen.
1. Velg **Lagre**, velg **Fullfør redigering** for å sjekke inn topptekstfragmentet, og velg deretter **Publiser** for å publisere det. 

Velkomstmeldingen vil nå vises øverst på alle områdesider som bruker det valgte topptekstfragmentet.

## <a name="additional-resources"></a>Tilleggsressurser

[Legge til en logo](add-logo.md)

[Velge et områdetema](select-site-theme.md)

[Arbeide med CSS-overstyringsfiler](css-override-files.md)

[Legge til et favorittikon](add-favicon.md)

[Legge til en opphavsrettserklæring](add-copyright-notice.md)

[Legge til språk på området](add-languages-to-site.md)

[Legge til skript kode i områdes ID-er for å støtte telemetri](add-telemetry.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]