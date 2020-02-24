---
title: Definere et lager
description: Dette emnet beskriver hvordan du definerer et lager som skal brukes med en ny kanal i Microsoft Dynamics 365 Commerce.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: fe785e3bfd503193a588958ae5df0d1c0fdb9e52
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/01/2020
ms.locfileid: "3002318"
---
# <a name="warehouse-set-up"></a>Lageroppsett


[!include [banner](includes/banner.md)]

Dette emnet beskriver hvordan du definerer et lager som skal brukes med en ny kanal i Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Oversikt

Hver handelskanal krever at et konfigurert lager er tilknyttet. Fremgangsmåtene nedenfor angir minimumskonfigurasjonen som kreves for å definere et lager for en handelskanal. Hvis du vil ha mer informasjon om lageroppsett, kan du se [Oversikt over lagerstyring](https://docs.microsoft.com/en-us/dynamics365/supply-chain/warehousing/warehouse-management-overview).

## <a name="configure-a-warehouse-site"></a>Konfigurere et lagerområde

Før du setter opp et lager, må du konfigurere et lagerområde.

Følg denne fremgangsmåten for å konfigurere et lagerområde.

1. I navigasjonsruten går du til **Moduler \> Detaljhandel og handel \> Kanaloppsett \> Områder**.
1. I handlingsruten velger du **Ny**.
1. Angi en verdi i feltet **Område**.
1. Angi en verdi i feltet **Navn**.
1. I **Generelt**-delen angir du aktuell **Tidssone**.
1. Angi en adresse i **Addresser**-delen.
1. Velg **Lagre** i handlingsruten.

Bildet nedenfor viser et eksempel på et lagerområde.

![Eksempel på lagerområde](media/warehouse-site.png)

## <a name="set-up-a-warehouse"></a>Definere et lager

Følg denne fremgangsmåten for å definere et lager.

1. I navigasjonsruten går du til **Moduler \> Detaljhandel og handel \> Kanaloppsett \> Lagre**.
1. I handlingsruten velger du **Ny**.
1. Angi en verdi i feltet **Lager**.  Hvis dette er en 1:1-tilordning til en detaljhandelsbutikk, kan du vurdere å bruke butikknavnet eller navnet på et regionalt distribusjonssenter.
1. Angi en verdi i feltet **Navn**.
1. I rullegardinlisten **Område** velger du lagerområdet som ble opprettet tidligere.
1. I feltet **Type** velger du **Standard**.
    - Hvis du vil angi et **Karantenelager**, må du først følge disse trinnene for å opprette et ekstra lager, der **Type** er satt til **Karantene**.
    - Hvis du vil angi et **Transittlager**, må du først følge disse trinnene for å opprette et ekstra lager, der **Type** er satt til **Transitt**.
1. Velg **Lagre** i handlingsruten.

## <a name="set-up-inventory-aisles"></a>Definer lagerganger

Hvis du vil konfigurere lagerganger, følger du disse trinnene.

1. I navigasjonsruten går du til **Moduler \> Detaljhandel og handel \> Kanaloppsett \> Lokasjonsoppsett \> Lagerganger**.
1. I handlingsruten velger du **Ny**.
1. I rullegardinlisten **Lager** velger du lageret som ble opprettet tidligere.
1. I **Gang**-feltet skriver du inn et navn (for eksempel "Std").
1. I **Navn**-feltet skriver du inn et navn (for eksempel "Standard gang").
1. Velg **Lagre** i handlingsruten.

## <a name="set-up-warehouse-inventory-locations"></a>Konfigurere lagerbeholdningslokasjoner

Følg denne fremgangs måten for å definere lagerbeholdningslokasjoner for standard, skadet og returnert beholdning.

1. I navigasjonsruten går du til **Moduler \> Detaljhandel og handel \> Kanaloppsett \> Lagre**.
1. Velg lageret du opprettet tidligere.
1. I handlingsruten velger du **Rediger**.
1. I handlingsruten velger du **Lager** og deretter **Beholdningssted**.
1. I handlingsruten velger du **Ny**. Rullegardinlisten **Lager** skal vise det nye lageret som standard.
    1. I **Gang**-boksen skriver du inn navnet på gangen du angav tidligere. 
    1. Sett **Manuell oppdatering** til **Ja**
    1. I **Sted**-boksen angir du navnet på lageret.
    1. Velg **Lagre** i handlingsruten.
 1. I handlingsruten velger du **Ny**.  Rullegardinlisten **Lager** skal vise det nye lageret som standard.
    1. I **Gang**-boksen skriver du inn navnet på gangen du angav tidligere.  
    1. Sett **Manuell oppdatering** til **Ja**
    1. I **Sted**-boksen angir du "Skadet".
    1. Velg **Lagre** i handlingsruten.
 1. I handlingsruten velger du **Ny**.  Rullegardinlisten **Lager** skal vise det nye lageret som standard.
    1. I **Gang**-boksen skriver du inn navnet på gangen du angav tidligere. 
    1. Sett **Manuell oppdatering** til **Ja**
    1. I **Sted**-boksen angir du "Returer".
    1. Velg **Lagre** i handlingsruten.
    
Følgende bilde viser et oppsett av en lagerlokasjon i San Francisco.

![Eksempel på lagerlokasjonsoppsett](media/warehouse-inventory-locations.png)
    
## <a name="complete-warehouse-setup"></a>Komplett lageroppsett

Følg fremgangsmåten nedenfor for å fullføre lageroppsettet.

1. I navigasjonsruten går du til **Moduler \> Detaljhandel og handel \> Kanaloppsett \> Lagre**.
1. Velg lageret du opprettet tidligere.
1. I handlingsruten velger du **Rediger**.
1. Under **Lagerstyring**:
    1. Angi **Standard tilgangssted** til standardstedet som er opprettet ovenfor.
    1. Angi **Standard avgangssted** til standardstedet som er opprettet ovenfor.
1. Under **Adresser**-delen angir du en lageradresse.
1. Under **Detaljhandel**-delen: 
    1. I boksen **Standardreturlokasjon** angir du returlokasjonen som ble opprettet tidligere.
    1. Sett **Butikk** til **Ja**.
    1. Sett **Vekt** til **1,00**. 
    1. I boksen **Lagringsdimensjoner** angir du standardlokasjonen som ble opprettet tidligere.
1. Under **Lager**-delen setter du **Fysisk negativt lager** til **Ja**.
1. Velg **Lagre** i handlingsruten.

Følgende bilde viser detaljer for et konfigurert lager.

![Eksempel på konfigurert lager](media/warehouse-sample.png)

## <a name="additional-resources"></a>Tilleggsressurser

[Oversikt over lagerstyring](https://docs.microsoft.com/en-us/dynamics365/supply-chain/warehousing/warehouse-management-overview)

[Oversikt over kanaler](channels-overview.md)

[Forutsetninger for kanaloppsett](channels-prerequisites.md)

[Definere en detaljhandelskanal](channel-setup-retail.md)
    
[Definere en Internett-kanal](channel-setup-online.md)

[Definere en telefonsenterkanal](channel-setup-callcenter.md)





