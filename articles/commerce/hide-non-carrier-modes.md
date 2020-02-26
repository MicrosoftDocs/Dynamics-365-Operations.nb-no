---
title: Skjule leveringsmåter som ikke er transportør, fra forsendelsesalternativene på salgssted
description: Dette emnet beskriver et konfigurasjonsalternativ som kan forhindre at leveringsmåter fra ikke-transportører vises for det merkede området når forsendelsesordrer opprettes i salgsstedsprogrammet (POS).
author: hhainesms
manager: annbe
ms.date: 10/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: hhainesms
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 75e7e8f183982f7829db78eb75b8c29c9ab95e89
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/01/2020
ms.locfileid: "3023616"
---
# <a name="hide-non-carrier-delivery-modes-from-the-shipping-options-in-pos"></a>Skjule leveringsmåter som ikke er transportør, fra forsendelsesalternativene på salgssted


[!include [banner](includes/banner.md)]

Dette emnet beskriver et konfigurasjonsalternativ som er tilgjengelig for salgsstedsprogrammet (POS). Dette konfigurasjonsalternativet endrer virkemåten for valg av en leveringsmåte når det opprettes forsendelsesordrer på salgsstedet.

Når brukere oppretter leveringsordrer for kunde på salgsstedet, kan de velge en leveringsmåte for forsendelsen. Denne funksjonaliteten er tilgjengelig uansett om hele ordren sendes eller bare valgte linjer.

Dialogboksen der en leveringsmåte er valgt, viser som standard alle de gyldige leveringsmåtene for kombinasjonen av en kanal, en vare og en leveringsadresse. Disse leveringsmåtene er definert på **Leveringsmåter**-siden i Hovedkontor (**Salg og markedsføring \> Oppsett \> Distribusjon \> Leveringsmåter**). "Ikke-transportør"-modi for levering, for eksempel **Utlevering** eller **Henting**, kan også vises som valg i dialogboksen.

Det er imidlertid lagt til en funksjon som lar deg skjule ikke-transportør-leveringsmåter i dialogboksen. Hvis du vil aktivere denne funksjonen, går du til siden **Handelsparametere**, kategorien **Kundeordrer** og angir alternativet for **Vis bare transportøralternativer for forsendelsesordrer** til **Ja**. Når du har aktivert denne funksjonen og kjørt de aktuelle distribusjonsjobbene for å synkronisere informasjonen til kanaldatabasen, vil ikke leveringsmåter for ikke-transportør vises som valg under oppretting av forsendelsesordrer på salgsstedet.
