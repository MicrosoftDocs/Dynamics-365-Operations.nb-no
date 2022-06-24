---
title: Avinstaller løsninger for appverksettingspakke med dobbel skriving
description: Denne artikkelen beskriver hvordan du avinstallerer løsninger for appiverksetting med dobbel skriving.
author: RamaKrishnamoorthy
ms.date: 03/16/2022
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2022-01-21
ms.openlocfilehash: 676802ddabac69db4947cf806e9103f67cece3de
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8870381"
---
# <a name="uninstall-dual-write-application-orchestration-solutions"></a>Avinstaller løsninger for appverksettingspakke med dobbel skriving

[!include [banner](../../includes/banner.md)]

Denne artikkelen beskriver hvordan du avinstallerer løsninger for appiverksetting med dobbel skriving.

Enkelte kunder installerer utilsiktet appiverksettingspakken med dobbel skriving, som installerer flere løsninger i Microsoft Dataverse-miljøet. Installasjon av overflødige løsninger i pakken kan forårsake uventede og uønskede problemer.

For å løse problemer som er knyttet til installasjon av appiverksettingspakken med dobbel skriving, må du avinstallere de uønskede løsningene for dobbel skriving i denne rekkefølgen:

1. Dynamics365FinanceAndOperationsAnchor_managed
1. msdyn_OneFSSCM_managed (hvis den finnes)
1. Dynamics365FinanceAndOperationsDualWriteEntityMaps_managed
1. Dynamics365Notes_managed (Hvis du vil avinstallere denne løsningen, må du åpne en støtteforespørsel hos Microsoft.)
1. DualWriteCore_managed
1. Dynamics365AssetManagementApp_managed
1. Dynamics365AssetManagement_managed
1. Dynamics365SupplyChainExtended_managed
1. Dynamics365FinanceExtended_managed
1. HCMCommon_managed
1. Dynamics365FinanceAndOperationsCommon_managed
1. Dynamics365Company_managed
1. CurrencyExchangeRates_managed
1. msdyn_AssetCommon_managed
1. FieldServiceCommon_managed

Hvis løsninger for parter og globale adressebøker ble installert, avinstallerer du løsningene i følgende rekkefølge:

1. Dynamics365FinanceAndOperationsAnchor
1. Dynamics365FinanceAndOperationsDualWriteEntityMaps
1. msdyn_DualWriteCore
1. Dynamics365AssetManagementApp
1. Dynamics365AssetManagement
1. Dynamics365SupplyChainExtended
1. Dynamics365FinanceExtended
1. HCMCommon
1. Dynamics365FinanceAndOperationsCommon
1. Part
1. Dynamics365Company_managed
1. CurrencyExchangeRates
1. msdyn_AssetCommon
1. FieldServiceCommon
