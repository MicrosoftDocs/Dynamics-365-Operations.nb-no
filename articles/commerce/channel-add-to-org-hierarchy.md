---
title: Legge til en kanal i et organisasjonshierarki
description: Denne artikkelen beskriver hvordan du legger til en kanal i et organisasjonshierarki i Microsoft Dynamics 365 Commerce.
author: samjarawan
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 8de9242b9d272158dff9c486006a1684f073935e
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8876592"
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