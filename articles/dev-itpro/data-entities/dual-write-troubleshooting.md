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
ms.openlocfilehash: 5e71729dafd2ad85a01b055363d1c7056b5558b2
ms.sourcegitcommit: 3f05ede8b8acdf0550240a83a013e093b4ad043d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/13/2019
ms.locfileid: "1873111"
---
# <a name="troubleshooting-guide-for-data-integration"></a>Feilsøkingsveiledning for dataintegrering

## <a name="enable-plug-in-trace-logs-in-common-data-service-and-inspect-the-dual-write-plug-in-error-details"></a>Aktivere sporingslogger for plugin-modul i Common Data Service og sjekke feildetaljene for dobbel skriving

[!include [banner](../includes/banner.md)]

[!include [preview](../includes/preview-banner.md)]

Hvis det oppstår et problem eller en feil med synkronisering av dobbel skriving, følger du denne fremgangsmåten for å kontrollere feilene i sporingsloggen.

1. Før du kan kontrollere feilene, må du aktivere sporingslogger for plugin-modul. Hvis du vil ha instruksjoner, kan du se delen "Vise sporingslogger" i [Opplæring: Skrive og registrere en plugin-modul](https://docs.microsoft.com/powerapps/developer/common-data-service/tutorial-write-plug-in#view-trace-logs).

    Nå kan du inspisere feilene.

2. Logg på Microsoft Dynamics 365 for Sales.
3. Velg **Innstillinger**-knappen (tannhjulsymbolet), og velg deretter **Avanserte innstillinger**.
4. I **Innstillinger**-menyen velger du **Tilpassing \> Sporingslogg for plugin-modul**.
5. Velg **Microsoft.Dynamics.Integrator.CrmPlugins.Plugin** som typenavn for å vise feildetaljene.

## <a name="inspect-dual-write-synchronization-errors-in-finance-and-operations"></a>Sjekke feil ved synkronisering av dobbel skriving i Finance and Operations

Følg disse trinnene for å undersøke feil under testing.

1. Logg på Microsoft Dynamics Lifecycle Services (LCS).
2. Åpne LCS-prosjektet for å utføre testing av dobbelt skriving.
3. Velg **Skybaserte miljøer**.
4. Opprett en eksternt skrivebord-tilkobling til den virtuelle maskinen for Dynamics 365 for Finance and Operations ved hjelp av den lokale kontoen som vises i LCS.
5. Åpne hendelseslisten. 
6. Gå til **Program- og tjenestelogger \> Microsoft \> Dynamics \> AX-DualWriteSync \> Drift**. Feilene og detaljene vises.

## <a name="unlink-one-common-data-service-environment-from-finance-and-operations-and-link-another-environment"></a>Fjerne en tilknytning til Common Data Service-miljøet fra Finance and Operations og koble til et annet miljø

Gjør følgende for å oppdatere koblinger:

1. Gå til Finance and Operations-miljøet.
2. Åpne Databehandling.
3. Velg **Kobling til CDS for Apps**.
4. Velg alle tilordningene som kjører, og velg deretter **Stopp**.
5. Velg alle tilordningene, og velg deretter **Slett**.

    > [!NOTE]
    > Alternativet **Slett** vises ikke hvis malen **CustomerV3-Account** er valgt. Fjern valget av denne malen etter behov. **CustomerV3-Account** er en eldre klargjort mal og fungerer med Kundeemne til kontanter-løsningen. Fordi den er globalt lansert, viser den under alle maler.

6. Klikk **Koble fra miljø**.
7. Velg **Ja** for å bekrefte operasjonen.
8. Hvis du vil koble til det nye miljøet, følger du trinnene i [installasjonsveiledningen](https://aka.ms/dualwrite-docs).
