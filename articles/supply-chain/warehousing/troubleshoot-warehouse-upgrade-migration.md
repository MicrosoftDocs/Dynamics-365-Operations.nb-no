---
title: Feilsøke oppgradering og overføring til avansert lagerstyring
description: Dette emnet beskriver hvordan du løser vanlige problemer som kan oppstå mens du oppgraderer og overføre til avansert lagerstyring.
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: f5bfee31ce27e919086f978fb3ff88ca61a65eba
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5208093"
---
# <a name="troubleshoot-upgrade-and-migration-to-advanced-warehouse-management"></a>Feilsøke oppgradering og overføring til avansert lagerstyring

[!include [banner](../includes/banner.md)]

Dette emnet beskriver hvordan du løser vanlige problemer som kan oppstå mens du oppgraderer og overføre til avansert lagerstyring.

## <a name="i-receive-the-following-error-message-javasecuritycertcertpathvalidatorexception-trust-anchor-for-certification-path-is-not-found"></a>Jeg får følgende feilmelding: java.security.cert.certPathValidatorException: Finner ikke klareringsanker for sertifiseringsbane.

### <a name="issue-description"></a>Problembeskrivelse

Du får denne feilmeldingen i lagerappen, fordi selvsignerte sertifikater ikke er klarerte i lokale Android 8+-miljøer.

### <a name="issue-resolution"></a>Problemløsning

Bruk en ekstern (offentlig) sertifiseringsinstans (CA). En hurtigreparasjon for dette problemet er tilgjengelig i versjon 1.9.0.0 av lagerappen. Hvis du vil ha mer informasjon om dette problemet og hvordan du løser det, kan du se [Feilsøke tilkoblingsproblemer for lagerapp](troubleshoot-warehouse-app-connection.md).

## <a name="what-is-the-approved-process-for-moving-from-basic-warehousing-to-advanced-warehousing"></a>Hva er den godkjente prosessen for flytting fra grunnleggende lager til avansert lagerstyring?

### <a name="issue-description"></a>Problembeskrivelse

Du kjører nå under lagerstyring og bruker grunnleggende lagerfunksjoner, og du vil gå over til avansert lager for å dra nytte av mobilenheter, bølger og arbeid. Det oppstår imidlertid problemer når du prøver å utføre denne flyttingen. Du kan for eksempel ikke endre produktene, slik at de bruker lagerdimensjoner (område, lager og lokasjon), fordi produktene har transaksjoner mot dem. Derfor må du lære den godkjente prosessen for flytting fra grunnleggende lager til avansert lagerstyring.

### <a name="issue-resolution"></a>Problemløsning

Hvis du vil ha mer informasjon om prosessen for flytting fra grunnleggende lager til avansert lagerstyring, kan du se følgende blogginnlegg og dokumentasjon:

- [Aktiver lagerstyringsprosess for eksisterende varer og lagre](https://cleverax.wordpress.com/2017/12/06/d365fo-enable-warehouse-management-process-for-existing-items-and-warehouses/)
- [Overføring av Microsoft Dynamics AX WMS til ny R3-lager- og transportfunksjonalitet](https://cloudblogs.microsoft.com/dynamics365/no-audience/2015/08/17/migration-of-microsoft-dynamics-ax-wms-to-new-r3-warehouse-and-transportation-functionality/)
- [WMSI/WMS2-vareoverføring](https://cloudblogs.microsoft.com/dynamics365/no-audience/2018/05/03/wmsiwms2-item-migration/)
- [Oppgradere lagerstyring fra Microsoft Dynamics AX 2012 til Supply Chain Management](https://docs.microsoft.com/dynamics365/supply-chain/warehousing/upgrade-migration-warehouse-management-processes)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]