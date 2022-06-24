---
title: Endre leveringsmodus i salgssted
description: Denne artikkelen beskriver hvordan du konfigurerer og bruker endre leveringsmodus i POS.
author: hhainesms
ms.date: 03/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: hhaines
ms.search.validFrom: 2020-02-20
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: 583f568164d0de70e22998bf5ded5f4616b00bd2
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8855827"
---
# <a name="change-mode-of-delivery-in-pos"></a>Endre leveringsmodus i salgssted

[!include [banner](includes/banner.md)]

Denne artikkelen beskriver hvordan du konfigurerer og bruker funksjonen "endre leveringsmodus" i salgsstedsmiljøer. 

I Dynamics 365 Commerce versjon 10.0.10 og senere er **Endre leveringsmodus** (647) tilgjengelig for å legge til i skjermoppsett for POS.

Med funksjonen for endring av leveringsmåte kan du endre leveringsmåten for én eller flere forsendelseskonfigurerte salgslinjer på POS-transaksjonen. I tidligere versjoner av Commerce måtte du gå gjennom de fullstendige konfigurasjonsflytene **Send alle** eller **Valgt for forsendelse** hvis du ville endre leveringsmåten for en eksisterende linje som ble konfigurert for forsendelse. Denne prosessen var tidkrevende, og kunne føre til utilsiktede endringer i leveringsopprinnelsen eller leveringsdatoen for linjen. De nye funksjonene gir en alternativ metode for effektiv oppdatering av leveringsmåten på disse salgslinjene.

Hvis du vil ha mer informasjon om hvordan du legger til en operasjon på en knapp i POS-rutenettet, kan du se [Skjermoppsett for salgssted](pos-screen-layouts.md).

Når denne funksjonen er konfigurert i POS-feltet og du velger **Endre leveringsmåte**, åpnes en listeside som gir deg muligheten til å velge linjene i transaksjonen du vil endre leveringsmåten for. Du kan velge noen av eller alle linjene, eller avslutte uten å gjøre noen endringer. Salgslinjene som tidligere ble konfigurert for forsendelse, er de eneste linjene i listen som du kan endre. Hvis du vil endre en linje som er utpekt til plukking eller utlevering, må du bruke operasjonene **Send alle** eller **Valgt for forsendelse**. Hvis du derimot vil endre en linje som er utpekt som en forsendelse til en plukking eller utlevering, må du bruke operasjonene **Plukk alle**, **Plukk valgte produkter**, **Utlevering av alle** eller **Utlevering av valgte**.

Når du har valgt linjene du vil endre, klikker du **Endre leveringsmåte** for å bli bedt om å velge alternativer for leveringmåte. Hvis du valgte flere linjer som skal endres, viser salgssted bare leveringsmåter som er konfigurert som tillatt for alle de valgte varene. Leveringsmåter kan konfigureres til å støtte bestemte produkter og leveringsadresser. Hvis det finnes en leveringsmåte som er akseptabel for én produkt- og adressekombinasjon, men ikke er akseptabel for en annen valgt produkt- og adressekombinasjon, er ikke leveringsmåten tilgjengelig. Det kan hende at du må velge linjer én etter én og endre leveringsmåten for hver linje separat hvis du vil velge en leveringsmåte for ett produkt som ikke støttes av et annet produkt.  

Når du har valgt den nye leveringsmåten, vises transaksjonssiden. Hvis du vil se gjennom de nye valgene for leveringsmodus, velger du kategorien **Levering** i transaksjonslisten.

## <a name="additional-resources"></a>Tilleggsressurser

[Opprette telefonsenterordrer](tasks/create-call-center-orders.md)

[Tilpasse transaksjons-e-poster etter leveringsmåte](customize-email-delivery-mode.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]