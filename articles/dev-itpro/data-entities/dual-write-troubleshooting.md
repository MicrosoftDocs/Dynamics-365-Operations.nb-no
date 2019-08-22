---
title: Feilsøkingsveiledning for dataintegrering
description: Dette emnet inneholder feilsøkingsinformasjon om dataintegrasjon mellom Microsoft Dynamics 365 for Finance and Operations og Common Data Service.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: ca62a6b3aa64ec2383ee3ded3b7bbf4650a41166
ms.sourcegitcommit: efcc0dee8bde5f8f93f6291e7f059ad426843e57
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/31/2019
ms.locfileid: "1797281"
---
# <a name="troubleshooting-guide-for-data-integration"></a>Feilsøkingsveiledning for dataintegrering

## <a name="enable-plugin-trace-in-common-data-service-and-check-the-dual-write-plugin-error-details"></a>Aktivere Sporing for plugin-modul i Common Data Service og sjekke feildetaljene for dobbel skriving

Hvis du står overfor et problem eller en feil med dobbel skriving-synkronisering, kan du undersøke feilene i sporingsloggen:

1. Før du kan inspisere feilene, må du aktivere sporing for plugin-modul ved hjelp av instruksjonene i [Registrere plugin](https://docs.microsoft.com/en-us/powerapps/developer/common-data-service/tutorial-write-plug-in#view-trace-logs) for å aktivere sporing for plugin-modul. Nå kan du inspisere feilene.
2. Logg på Dynamics 365 for Sales.
3. Klikk på innstillinger-ikonet (et tannhjul), og velg **Avanserte innstillinger**.
4. I **Innstillinger**-menyen velger du **Tilpassing > Sporingslogg for plugin-modul**.
5. Klikk på typenavnet **Microsoft.Dynamics.Integrator.CrmPlugins.Plugin** for å vise feildetaljene.

## <a name="check-dual-write-synchronization-errors-in-finance-and-operations"></a>Sjekke feil ved synkronisering av dobbel skriving i Finance and Operations

Du kan kontrollere feilene under testing ved å følge disse trinnene:

+ Logg på LifeCycle Services (LCS).
+ Åpne LCS-prosjektet du har valgt til å utføre testing av dobbelt skriving.
+ Gå til Skybaserte miljøer.
+ Eksternt skrivebord til Finance and Operations VM ved hjelp av lokal konto som vises i LCS.
+ Åpne hendelseslisten. 
+ Naviger til **Program- og tjenestelogger > Microsoft > Dynamics > AX-DualWriteSync > Drift**. Feilene og detaljene vises.

## <a name="how-to-unlink-and-link-another-common-data-service-environment-from-finance-and-operations"></a>Slik fjerner du tilknytningen til og kobler til et annet Common Data Service-miljø fra Finance and Operations

Du kan oppdatere koblinger ved å følge disse trinnene:

+ Naviger til Finance and Operations-miljøet.
+ Åpne Databehandling.
+ Klikk på **Kobling til CDS for apper**.
+ Velg alle kjørende tilordninger, og klikk på **Stopp**. 
+ Velg alle tilordningene, og klikk på **Slett**.

    > [!NOTE]
    > Alternativet **Slett** vises ikke hvis malen **CustomerV3-Account** er valgt. Opphev merkingen om nødvendig. **CustomerV3-Account** er en eldre klargjort mal og fungerer med Kundeemne til kontanter-løsningen. Fordi den er globalt lansert, viser den under alle maler.

+ Klikk **Koble fra miljø**.
+ Klikk **Ja** for bekreftelse.
+ Hvis du vil koble til det nye miljøet, følger du trinnene i [installasjonsveiledningen](https://aka.ms/dualwrite-docs).

