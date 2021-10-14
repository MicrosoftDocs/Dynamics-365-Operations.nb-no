---
title: Lastmaler
description: Dette emnet beskriver hvordan du konfigurerer lastmaler og hvordan du knytter en lastmal til en ny last.
author: Henrikan
ms.date: 10/30/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WHSLoadTemplate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: henrikan
ms.search.validFrom: 2020-10-30
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 694860d1ade74f9fd51a8ac579aa69fe7fb673a8
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/29/2021
ms.locfileid: "7569919"
---
# <a name="load-templates"></a>Lastmaler

[!include [banner](../../includes/banner.md)]

Når du oppretter en ny last, kan du tilordne en lastmal. Lastmalen inneholder informasjon om utstyr og om mål, for eksempel høyde, bredde, dybde og mengde for lasten.

Dette emnet beskriver hvordan du konfigurerer lastmaler og hvordan du knytter en lastmal til en ny last.

## <a name="set-up-a-load-template"></a>Konfigurere en lastmal

1. Gå til **Transportstyring \> Oppsett \> Lastplanlegging \> Lastmal**.
1. Velg **Ny** i handlingsruten for å legge til en ny mal eller **Rediger** for å redigere en eksisterende mal.
1. I raden for den nye eller eksisterende malen angir du følgende felt:

    - **Lastmal-ID** – Angi en unik identifikator (ID) for lastmalen.
    - **Utstyr** – Velg utstyret som skal brukes til å levere lasten.
    - **Lasthøyde**, **Lastbredde** og **Lastdybde** – Angi dimensjonene for lasten.
    - **Maks. tillatte lastvolum** og **Maks. tillatte lastvekt** – Angi maksimalt tillatt volum og vekt for lasten.
    - **Maksimalt tillatte bruttovekt** – Angi den maksimale tillatte bruttovekten for lasten. En lasts bruttovekt inkluderer både taravekten og lastvekten.
    - **Maksimalt antall fraktdeler som er tillatt** – Angi det største antallet fraktdeler som lasten kan inneholde.
    - **Stable last på gulv** – Merk av i denne avmerkingsboksen for å bruke gulvlasting. I et scenario med gulvlasting stables bokser fra gulv til tak og vegg til vegg i containeren for å utnytte plassen maksimalt.

1. Velg **Lagre** i handlingsruten.

## <a name="associate-a-load-template-with-a-new-load"></a>Knytt en lastmal til en ny last

1. Gå til **Transportstyring \> Planlegging \> Arbeidsområde for lastplanlegging**.
1. I den øvre delen av siden velger du én av følgende kategorier, avhengig av hvilken type kilde dokument du oppretter en last for: **Leveringer**, **Salgslinjer**, **Overføringslinjer** eller **Bestillingslinjer**. 
1. Velg det bestemte dokumentet du vil planlegge lasten for.
1. I handlingsruten, på **Forsyning og behov**-fanen, i **Legg til**-gruppen, velg **Til ny last**.
1. I dialogboksen **Lastmal**, i **Lastmal-ID**-feltet, velger du malen som skal brukes.
1. Velg **OK** for å bruke malen.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]