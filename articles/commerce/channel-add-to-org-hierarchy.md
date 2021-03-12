---
title: Legge til en kanal i et organisasjonshierarki
description: Dette emnet beskriver hvordan du legger til en kanal i et organisasjonshierarki i Microsoft Dynamics 365 Commerce.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 297bd34f9bde23d5cc7de266b8e8f49b1a752662
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "4993707"
---
# <a name="add-a-channel-to-an-organizational-hierarchy"></a>Legge til en kanal i et organisasjonshierarki


[!include [banner](includes/banner.md)]

Dette emnet beskriver hvordan du legger til en kanal i et organisasjonshierarki i Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Oversikt

Kanaler må knyttes til ett eller flere organisasjonshierarkier. Før du oppretter kanaler, må du kontrollere at organisasjonshierarkiene er definert.  

Se [Organisasjonshierarkier](channels-org-hierarchies.md) for mer informasjon om hvordan du oppretter organisasjonshierarkier.

## <a name="select-a-hierarchy"></a>Velge et hierarki

Følg denne fremgangsmåten for å velge et hierarki.

1. I navigasjonsruten går du til **Moduler \> Detaljhandel og handel \> Kanaloppsett \> Organisasjonshierarkier**.
1. Velg organisasjonshierarkiet du vil legge til kanalen i, fra listen.
1. I handlingsruten velger du **Vis** for å vise hierarkidetaljer.

Følgende bilde viser detaljer om organisasjonshierarki for det valgte hierarkiet.

![Detaljer om organisasjonshierarki for det valgte hierarkiet](media/channel-add-to-org-hierarchy-1.png)

## <a name="add-a-channel-to-a-hierachy-node"></a>Legge til en kanal i en hierarkinode

Hvis du vil legge til en kanal i en hierarkinode, følger du disse trinnene.

1. I handlingsruten velger du **Rediger**.
1. Velg hierarkinoden du vil at kanalen skal legges til i, og gå deretter til rullegardinlisten **Sett inn** og velg **Detaljhandelskanal**. 
1. Velg kanalen som skal legges til, og klikk deretter **OK**-knappen.
1. Velg **Lagre** i handlingsruten.
1. Velg **Publiser** i handlingsruten, og oppgi en **gyldig dato** i fortiden for at denne handlingen skal tre i kraft umiddelbart.

Bildet nedenfor viser hvordan du velger en kanal som skal legges til i en hierarkinode.

![Velge en kanal som skal legges til i en hierarkinode](media/channel-add-to-org-hierarchy-2.png)

Det følgende bildet viser et hierarki der ulike kanaler er lagt til.

![Et hierarki med ulike kanaler lagt til](media/channel-add-to-org-hierarchy-3.png)

## <a name="additional-resources"></a>Tilleggsressurser

[Oversikt over kanaler](channels-overview.md)

[Forutsetninger for kanaloppsett](channels-prerequisites.md)

[Oversikt over organisasjoner og organisasjonshierarkier](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[Planlegge organisasjonshierarkiet](../fin-ops-core/fin-ops/organization-administration/plan-organizational-hierarchy.md?toc=/dynamics365/commerce/toc.json)

[Organisasjonshierarkier](channels-org-hierarchies.md)

[Definere en detaljhandelskanal](channel-setup-retail.md)
    
[Definere en Internett-kanal](channel-setup-online.md)
