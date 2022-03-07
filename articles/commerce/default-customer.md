---
title: Opprette en standardkunde
description: Dette emnet beskriver hvordan du oppretter en standardkunde som skal brukes ved opprettelse av en kanal i Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: f988732549ce82919f02c87b320623d8d4218735
ms.sourcegitcommit: c88b54ba13a4dfe39b844ffaced4dc435560c47d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/19/2021
ms.locfileid: "5477906"
---
# <a name="create-a-default-customer"></a>Opprette en standardkunde

[!include [banner](includes/banner.md)]

Dette emnet beskriver hvordan du oppretter en standardkunde som skal brukes ved opprettelse av en kanal i Microsoft Dynamics 365 Commerce.

Når du oppretter en kanal, må du angi en standardkunde. En standardkunde kan enkelt opprettes etter at du først har opprettet kundegruppen og kundeadresseboken.

## <a name="create-a-customer-group"></a>Opprette en kundegruppe

Hvis det ikke finnes kundegrupper enda, kan du opprette én. Eksempler kan være grupper for å representere ulike kundegrupper, for eksempel engros, detaljhandel, Internett, ansatte osv.

Hvis du vil opprette en kundegruppe, følger du disse trinnene.

1. I navigasjonsruten går du til **Moduler \> Detaljhandel og handel \> Kunder \> Kundegrupper**.
1. I handlingsruten velger du **Ny**.
1. I **Kundegruppe**-boksen angir du en kundegruppe-ID.
1. I **Beskrivelse**-boksen angir du en passende beskrivelse.
1. I **Betalingsvilkår**-boksen angir du en passende verdi.
1. I **Tid mellom forfallsdato og betalingsdato for faktura**-boksen angir du en passende verdi.
1. I **Standard avgiftsgruppe**-boksen angir du om aktuelt en avgiftsgruppe.
1. Merk om aktuelt av i **Prisene inkluderer salgsavgift**-avmerkingsboksen.
1. I **Standard avskrivingsgrunn**-boksen angir du om aktuelt en passende verdi.

Følgende bilde viser flere konfigurerte kundegrupper.

![Kundegrupper](media/customer-groups.png)

## <a name="create-a-customer-address-book"></a>Opprette en kundeadressebok

En kunde må være knyttet til en adressebok. Hvis dette ikke er opprettet enda, må du opprette én.

Hvis du vil opprette en kundeadressebok, følger du disse trinnene.

1. I navigasjonsruten går du til **Moduler \> Detaljhandel og handel \> Kanaloppsett \> Adressebøker**.
1. I handlingsruten velger du **Ny**.
1. I **Navn**-boksen angir du et navn.
1. I **Beskrivelse**-boksen angir du en beskrivelse.
1. Velg **Lagre** i handlingsruten.

Bildet nedenfor viser et eksempel på en adressebok.

![Adressebok](media/address-book.png)

## <a name="create-a-default-customer"></a>Opprette en standardkunde

Hvis du vil opprette en standardkunde, følger du disse trinnene.

1. I navigasjonsruten går du til **Moduler \> Detaljhandel og handel \> Kunder \> Alle kunder**.
1. I handlingsruten velger du **Ny**.
1. I **Type**-rullegardinlisten velger du "Person".
1. I **Kundekonto**-rullegardinlisten velger du eller skriver inn et kontonummer (for eksempel "100001").
1. I **Fornavn**-rullegardinlisten velger du eller angir et navn (for eksempel "Standard").
1. I **Mellomnavn**-rullegardinlisten velger du eller angir et navn (for eksempel "Detaljhandel").
1. I **Etternavn**-rullegardinlisten velger du eller angir et navn (for eksempel "Kunde").
1. I **Valuta**-rullegardinlisten velger du eller angir en valuta (for eksempel "USD").
1. I **Valuta**-rullegardinlisten velger du kundegruppen som ble opprettet tidligere.
1. I **Adressebøker**-rullegardinlisten velger du en eksisterende kundeadressebok.
1. Velg **Lagre** for å lagre og gå tilbake til Kundedetaljer-skjermbildet for den nye kunden.

> [!NOTE]
> Det er ikke nødvendig å legge til en adresse for en standardkunde.

Bildet nedenfor viser et eksempel på kundeopprettelse.

![Standardkundeopprettelse](media/default-customer-creation.png)

Bildet nedenfor viser en standardkundekonfigurasjon.

![Eksempel på kundekonfigurasjon](media/default-customer-configuration1.png)

De fleste standardverdiene på Kundedetaljer-skjermbildet kan bli slik de er, men to verdier må endres.

1. På Kundedetaljer-skjermbildet utvider du **Standardverdier for salgsordrer**.
1. I **Område**-rullegardinlisten velger du eller angir et forhåndskonfigurert område.
1. I **Lager**-rullegardinlisten velger du eller angir et forhåndskonfigurert lager.

Bildet nedenfor viser et eksempel på kundekonfigurasjon.

![Eksempel på kundekonfigurasjon](media/default-customer-configuration2.png)

## <a name="additional-resources"></a>Tilleggsressurser

[Oversikt over kanaler](channels-overview.md)

[Forutsetninger for kanaloppsett](channels-prerequisites.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
