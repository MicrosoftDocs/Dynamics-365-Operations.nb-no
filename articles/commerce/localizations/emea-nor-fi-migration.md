---
title: Overfør fra eldre Commerce-funksjonalitet for Norge
description: Denne artikkelen beskriver hvordan du går over fra den eldre løsningen for digital signering i Microsoft Dynamics 365 Commerce-lokaliseringen for Norge til løsningen som er basert på rammeverket for regnskapsintegrering i Commerce.
author: EvgenyPopovMBS
ms.date: 08/23/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Norway
ms.author: josaw
ms.search.validFrom: 2022-8-1
ms.openlocfilehash: c4dbaae11db885cd62b9039c568ba3d6570f38d8
ms.sourcegitcommit: 1dbff0b5fa1f4722a1720fac35cce94606fa4320
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/24/2022
ms.locfileid: "9346369"
---
# <a name="migrate-from-legacy-commerce-functionality-for-norway"></a>Overfør fra eldre Commerce-funksjonalitet for Norge

[!include [banner](../includes/banner.md)]

Denne artikkelen beskriver hvordan du går over fra den [eldre løsningen for digital signering](./emea-nor-loc-deployment-guidelines.md) i Microsoft Dynamics 365 Commerce-lokaliseringen for Norge til løsningen som er basert på [rammeverket for regnskapsintegrering i Commerce](./emea-nor-fi-deployment.md).

Hvis du bruker den [eldre løsningen for digital signering for Norge](./emea-nor-loc-deployment-guidelines.md) i Commerce versjon 10.0.28 eller tidligere, må du gå over til den [gjeldende regnskapsintegreringsløsningen i Commerce](./emea-nor-fi-deployment.md) versjon 10.0.29 eller nyere for å ta endringene i bruk og motta regelmessige oppdateringer for fremtidige funksjoner som spesifikt gjelder Norge. Ingen store endringer kreves i utvidelseslogikken som du opprettet. Siden denne oppdateringen er omfattende, kommer imidlertid noen av tilpassingene dine til slutte å fungere med mindre du gjør endringer hos deg. Du bør derfor planlegge, forberede deg på og fullføre innføringen i miljøet ditt.

## <a name="migration-process"></a>Migreringsprosess

Overgangsprosessen fra den eldre løsningen for digital signering til den gjeldende regnskapsintegreringsløsningen er basert på en gradvis oppdatering. Alle Commerce headquarters- og Commerce Scale Unit-komponenter bør med andre ord allerede være oppdatert før du begynner å oppdatere salgsstedet.

Hvis du vil ha hjelp til å forhindre scenarioer der en hendelse eller transaksjon signeres to ganger (både av den tidligere utvidelsen og av den gjeldende utvidelsen), eller der en hendelse eller transaksjon ikke kan signeres på grunn av en feil eller ufullstendig konfigurasjon, anbefaler vi at du deaktiverer alle salgsstedsenheter som bruker den tidligere løsningen, og deretter oppdaterer alle samtidig. Du kan for eksempel foreta denne samtidige oppdateringen butikk for butikk ved å oppdatere funksjonalitetsprofilen til hver butikk.

Følg fremgangsmåten nedenfor for å fullføre overføringsprosessen.

1. Oppdater Commerce Headquarters-komponentene.
1. [Konfigurer funksjonaliteten for regnskapsintegrering for Norge](#configure-fiscal-integration) i Commerce headquarters.
1. Kontroller at alle frakoblede transaksjoner lastes opp fra frakoblede Modern POS-enheter til kanaldatabasen.
1. Lukk skift, og logg deg av alle salgsstedsenheter.
1. Oppdater Commerce Scale Unit-komponentene.
1. Oppdater salgsstedskomponentene.
1. [Konfigurere kanalkomponenter](./emea-nor-fi-deployment.md#configure-channel-components).
1. [Aktiver funksjoner som spesifikt gjelder Norge](./emea-nor-cash-registers.md#enable-features-for-norway) i Commerce headquarters.
1. [Juster kvitteringsformater](#adjust-receipt-formats) slik at de bruker oppdaterte egendefinerte felter.
1. [Aktiver funksjonaliteten for regnskapsintegrering](#enable-fiscal-integration).
1. Start salgsstedet på nytt.

### <a name="configure-fiscal-integration"></a>Konfigurer regnskapsintegrering

Du kan konfigurere funksjonaliteten for regnskapsintegrering for Norge ved å følge trinnene i [Definer regnskapsregistrering](./emea-nor-fi-deployment.md#set-up-fiscal-registration-for-norway) og [Konfigurer parametere for digital signatur](./emea-nor-fi-deployment.md#configure-the-digital-signature-parameters).

> [!IMPORTANT]
> Ikke aktiver regnskapsintegrering på siden **Delte handelsparametere** ennå.

### <a name="adjust-receipt-formats"></a>Juster kvitteringsformater

Du må justere kvitteringsformatene slik at de bruker oppdaterte egendefinerte felter. Hvis du vil ha oppdatert informasjon om egendefinerte felter for Norge, kan du se [Konfigurere egendefinerte felter, slik at de kan brukes i kvitteringsformater for salgskvitteringer](./emea-nor-cash-registers.md#configure-custom-fields-so-that-they-can-be-used-in-receipt-formats-for-sales-receipts).

### <a name="enable-fiscal-integration"></a>Aktiver regnskapsintegrering

Når du er klar til å aktivere funksjonaliteten for regnskapsintegrering i Commerce headquarters, gjør du følgende.

1. Gå til **Detaljhandel og handel \> Hovedkvarteroppsett \> Parametere \> Delte handelsparametere**.
1. På **Generelt**-fanen angir du **Aktiver regnskapsintegrering**-alternativet til **Ja**.
1. Gå til **Retail og Commerce \> Kanaloppsett \> Salgsstedsoppsett \> Salgsstedsprofiler \> Funksjonalitetsprofiler**.
1. Velg en funksjonsprofil som er koblet til butikken der registreringsprosessen skal aktiveres.
1. I hurtigfanen **Regnskapsregistreringsprosess** velger du regnskapsregistreringsprosessen du opprettet tidligere.
1. I hurtigganen **Regnskapstjenester** velger du den tekniske profilen for koblingen som du opprettet tidligere.
1. Gå til **Detaljhandel og handel \> IT for detaljhandel og handel \> Distribusjonsplan**.
1. Åpne distribusjonsplanen, og velg jobbene **1070** og **1090** for å overføre data til kanaldatabasen.

> [!WARNING]
> Etter at du har fullført de foregående trinnene, slutter de tidligere tilpassingene av funksjonaliteten for digital signering å fungere.
