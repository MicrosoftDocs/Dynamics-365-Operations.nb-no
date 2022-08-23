---
title: Konfigurer Azure-ressurser for elektronisk fakturering
description: Denne artikkelen gir en oversikt over prosessen for oppsett av Microsoft Azure-ressurser for elektronisk fakturering.
author: gionoder
ms.date: 01/26/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: gionoder
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.search.form: ''
ms.openlocfilehash: f11e4eac831d54a6cac765a5adc4e4ffddbe0a22
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/12/2022
ms.locfileid: "9283093"
---
# <a name="set-up-azure-resources-for-electronic-invoicing"></a>Konfigurer Azure-ressurser for elektronisk fakturering

[!include [banner](../includes/banner.md)]

Prosessen for oppsett av Microsoft Azure-ressurser for elektronisk fakturering har tre trinn. De to første trinnene, «Opprette et Azure-nøkkelhvelv i Azure-portalen» og «Opprette en Azure-lagringskonto i Azure-portalen», er obligatoriske. Det tredje trinnet, «Konfigurere en SharePoint-tilkobling», er valgfritt.

## <a name="create-an-azure-key-vault-in-the-azure-portal"></a>Opprette et Azure-nøkkelhvelv i Azure-portalen

Opprett et nøkkelhvelv i Azure-abonnementet. Vi anbefaler at du oppretter et separat nøkkelhvelv for elektronisk fakturering, og at du ikke kombinerer hemmeligheter med andre programmer. Opprett så hemmeligheter og sertifikater du trenger, for scenarioene i elektroniske dokumenter. Du må opprette minst én hemmelighet for å lagre tokenet for signatur for delt tilgang (SAS) for Azure-lagringskontoen du skal opprette i neste trinn.

Hvis du vil ha informasjon om hvordan du fullfører dette trinnet, kan du se [Opprette et Azure-nøkkelhvelv i Azure-portalen](e-invoicing-create-azure-key-vault-azure-portal.md).

## <a name="create-an-azure-storage-account-in-the-azure-portal"></a>Opprette en Azure-lagringskonto i Azure Portal

Du eier alle de elektroniske dokumentene og filene som genereres av tjenesten for elektronisk fakturering eller går inn på tjenesten. Disse dokumentene og filene lagres på en Azure-lagringskonto du oppretter i Azure-abonnementet. Tjenesten får tilgang til lagringskontoen din ved hjelp av SAS-tokenet som tas fra Key Vault-hemmeligheten.

Hvis du vil ha informasjon om hvordan du fullfører dette trinnet, kan du se [Opprette en Azure-lagringskonto i Azure Portal](e-invoicing-create-azure-storage-account-azure-portal.md).

## <a name="configure-a-sharepoint-connection"></a>Konfigurere en SharePoint-tilkobling

I noen scenarioer må du kanskje lagre elektroniske filer i SharePoint og hente dem fra SharePoint. Hvis du vil sikre at tjenesten for elektronisk fakturering har tilgang til SharePoint-mappene, konfigurerer du tilgang til SharePoint.

Hvis du vil ha informasjon om hvordan du fullfører dette trinnet, kan du se [Konfigurere en SharePoint-tilkobling](e-invoicing-create-sharepoint-connection.md).
