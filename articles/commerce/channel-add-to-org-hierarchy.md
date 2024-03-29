---
title: Legge til en kanal i et organisasjonshierarki
description: Denne artikkelen beskriver hvordan du legger til en kanal i et organisasjonshierarki i Microsoft Dynamics 365 Commerce.
author: samjarawan
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: 9def2d7c3cf17ecd9b74ce41f56bc3220a754597
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/12/2022
ms.locfileid: "9278604"
---
# <a name="add-a-channel-to-an-organizational-hierarchy"></a>Legge til en kanal i et organisasjonshierarki


[!include [banner](includes/banner.md)]

Denne artikkelen beskriver hvordan du legger til en kanal i et organisasjonshierarki i Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Oversikt

Kanaler må knyttes til ett eller flere organisasjonshierarkier. Før du oppretter kanaler, må du kontrollere at organisasjonshierarkiene er definert.  

Se [Organisasjonshierarkier](channels-org-hierarchies.md) for mer informasjon om hvordan du oppretter organisasjonshierarkier.

## <a name="select-a-hierarchy"></a>Velge et hierarki

Følg denne fremgangsmåten for å velge et hierarki.

1. I navigasjonsruten går du til **Moduler \> Detaljhandel og handel \> Kanaloppsett \> Organisasjonshierarkier**.
1. Velg organisasjonshierarkiet du vil legge til kanalen i, fra listen.
1. I handlingsruten velger du **Vis** for å vise hierarkidetaljer.

Følgende bilde viser detaljer om organisasjonshierarki for det valgte hierarkiet.

![Detaljer om organisasjonshierarki for det valgte hierarkiet.](media/channel-add-to-org-hierarchy-1.png)

## <a name="add-a-channel-to-a-hierachy-node"></a>Legge til en kanal i en hierarkinode

Hvis du vil legge til en kanal i en hierarkinode, følger du disse trinnene.

1. I handlingsruten velger du **Rediger**.
1. Velg hierarkinoden du vil at kanalen skal legges til i, og gå deretter til rullegardinlisten **Sett inn** og velg **Detaljhandelskanal**. 
1. Velg kanalen som skal legges til, og klikk deretter **OK**-knappen.
1. Velg **Lagre** i handlingsruten.
1. Velg **Publiser** i handlingsruten, og oppgi en **gyldig dato** i fortiden for at denne handlingen skal tre i kraft umiddelbart.

Bildet nedenfor viser hvordan du velger en kanal som skal legges til i en hierarkinode.

![Velge en kanal som skal legges til i en hierarkinode.](media/channel-add-to-org-hierarchy-2.png)

Det følgende bildet viser et hierarki der ulike kanaler er lagt til.

![Et hierarki med ulike kanaler lagt til.](media/channel-add-to-org-hierarchy-3.png)

## <a name="additional-resources"></a>Tilleggsressurser

[Oversikt over kanaler](channels-overview.md)

[Kanaloppsettsforutsetninger](channels-prerequisites.md)

[Oversikt over organisasjoner og organisasjonshierarkier](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[Planlegge organisasjonshierarkiet](../fin-ops-core/fin-ops/organization-administration/plan-organizational-hierarchy.md?toc=/dynamics365/commerce/toc.json)

[Organisasjonshierarkier](channels-org-hierarchies.md)

[Definere en detaljhandelskanal](channel-setup-retail.md)
    
[Definere en Internett-kanal](channel-setup-online.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
