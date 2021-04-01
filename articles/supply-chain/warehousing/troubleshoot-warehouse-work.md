---
title: Feilsøke lagerarbeid
description: Dette emnet beskriver hvordan du løser vanlige problemer som kan oppstå mens du arbeider med lagerarbeid i Microsoft Dynamics 365 Supply Chain Management.
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
ms.openlocfilehash: b1814f7b23efda2cabdb7bfc7bea4de6e3d6ec2f
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5237065"
---
# <a name="troubleshoot-warehouse-work"></a>Feilsøke lagerarbeid

[!include [banner](../includes/banner.md)]

Dette emnet beskriver hvordan du løser vanlige problemer som kan oppstå mens du arbeider med lagerarbeid i Microsoft Dynamics 365 Supply Chain Management.

## <a name="i-cant-move-license-plates-that-have-serial-number-items-when-blank-issue-and-blank-receipt-are-allowed-on-the-tracking-dimension-group"></a>Jeg kan ikke flytte nummerskilter som har serienummervarer når det er en tom avgang, og det er tillatt med tomt mottak på sporingsdimensjonsgruppen.

### <a name="issue-description"></a>Problembeskrivelse

Du kan ikke flytte et nummerskilt ved hjelp av et **Flytting**-menyelement hvis serienummeret har innstillinger for *Tom avgang tillatt* og *Tomt mottak tillatt* på sporingsdimensjonsgruppen, og hvis det er flere nummerskilter på samme sted, kan noe av disse ha serienumre og noen av dem ikke ha det.

### <a name="issue-resolution"></a>Problemløsning

Dette problemet vil løses ved hjelp av endringer som er distribuert i [KB 4571546](https://fix.lcs.dynamics.com/Issue/Details?kb=4571546&bugId=467880&dbType=3&qc=5b46d7faa9cc326cebfe9854cb30be8ea30b21ef33d3572c325fbb21202de687). Disse endringene gjør **Serienummer**-feltet valgfritt når det er tillatt med tomt mottak og tom avgang.

## <a name="i-receive-the-following-error-message-in-the-warehouse-app-when-i-process-movements-the-inventory-owner-1-is-not-allowed-in-this-process"></a>Jeg får følgende feilmelding i lagerappen når jeg behandler flyttinger: Lagereieren %1 er ikke tillatt i denne prosessen.

### <a name="issue-description"></a>Problembeskrivelse

**Eier**-sporingsdimensjonen mangler når lagerappen brukes til å lage bevegelser. En vanlig lageroverføringsjournal fra Supply Chain Management-klienten ser ut til å fungere som tiltenkt og kan bare posteres hvis **Eier**-dimensjonen er fylt ut.

### <a name="issue-resolution"></a>Problemløsning

Microsoft har evaluert dette problemet og har funnet ut at det er en funksjonsbegrensning. For øyeblikket støtter lagerstyringsprosesser bare lager som eies av den juridiske enheten.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]