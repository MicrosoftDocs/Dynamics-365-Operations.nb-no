---
title: Oversikt over kanaler
description: Denne artikkelen viser en oversikt over kanaler i Microsoft Dynamics 365 Commerce.
author: samjarawan
ms.date: 01/27/2020
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.assetid: ''
ms.openlocfilehash: ad31f466563aeb38f28f9761828e6708895005b8
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/12/2022
ms.locfileid: "9280427"
---
# <a name="channels-overview"></a>Oversikt over kanaler


[!include [banner](includes/banner.md)]

Denne artikkelen viser en oversikt over kanaler i Microsoft Dynamics 365 Commerce. Den inneholder informasjon om oppgavene du må fullføre både før og etter at du har definert hver kanal.

## <a name="types-of-channels"></a>Typer kanaler

Dynamics 365 Commerce støtter tre ulike kanaltyper: detaljhandel, telefonsenter og Internett-kanaler.

### <a name="retail-channels"></a>Detaljhandelskanaler

Detaljhandelskanaler representerer standard fysiske butikker. Hver detaljhandelsbutikk kan ha sine egne salgsstedsregistre, inntekts- og utgiftskontoer og ansatte. 

### <a name="call-center-channels"></a>Telefonsenterkanaler

Telefonsenterkanaler representerer ordre- og kundestyring i et telefonsenter.

### <a name="online-channels"></a>Internett-kanaler

Internett-kanaler representerer butikkfasader for e-handel på nettet. Når en Internett-kanal er opprettet, må det opprettes et område ved hjelp av områdebyggeren i Microsoft Dynamics 365 Commerce eller en annen tredjepartsløsning for e-handel.

## <a name="channel-setup-basics"></a>Grunnleggende om kanaloppsett

Kanaloppsett utføres i Commerce-verktøyet. Hver kanal kan ha sine egne betalingsmåter, prisgrupper, produkthierarkier, sortimenter og produktsett. Når du har opprettet en kanal, tilordner du produktene du vil den skal føre og selge. Hver kanaltype har et unikt sett av funksjoner som kanskje må konfigureres. En detaljhandelskanal trenger for eksempel tilordnede ansatte, journaler og kunder. Når en ny kanal er opprettet, må den tilordnes et organisasjonshierarki.

## <a name="channel-setup-prerequisites"></a>Forutsetninger for kanaloppsett

Før du kan definere en kanal, må du fullføre noen nødvendige oppgaver basert på kanaltypen. Hvis du vil ha mer informasjon, kan du se [Forutsetninger for kanaloppsett](channels-prerequisites.md).

## <a name="set-up-a-channel"></a>Definere en kanal

Når du har fullført de nødvendige oppgavene, bruker du følgende koblinger for ytterligere instruksjoner for installasjon.

- [Definere en detaljhandelskanal](channel-setup-retail.md)
- [Definere en telefonsenterkanal](channel-setup-callcenter.md)
- [Definere en Internett-kanal](channel-setup-online.md)

<!--
## Post-channel configuration

After you create a channel, you may need to complete some of the below tasks:

- [Add channel to an organizational hierarchy](add-channel-org-hierarchy.md)
- Set up fulfillment groups. (LINK TBD)
- Configure the POS registers for the store. (LINK TBD)
- Assign product assortments to the store. (LINK TBD)
- Process assortments to generate the list of products that are included in the assortment and to make the products available in the retail store. (LINK TBD)
- Send data such as number sequences, hardware profiles, and POS screen layouts to the Retail POS registers.(LINK TBD)
- Publish the retail store to send store data to Retail POS. (LINK TBD)
- Run the jobs to send the store data to Retail POS. (LINK TBD)
-->

## <a name="additional-resources"></a>Tilleggsressurser

[Forutsetninger for kanaloppsett](channels-prerequisites.md)

[Definere en detaljhandelskanal](channel-setup-retail.md)
    
[Definere en Internett-kanal](channel-setup-online.md)

[Definere en telefonsenterkanal](channel-setup-callcenter.md)

[Definere organisasjonshierarkier](channels-org-hierarchies.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
