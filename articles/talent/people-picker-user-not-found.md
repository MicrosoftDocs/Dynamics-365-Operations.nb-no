---
title: Brukeren ble ikke funnet i Personvelger i Attract eller Onboard
description: Dette emnet forklarer hva du gjør når brukere i leieren i selskapet ikke vises i Personvelger i Dynamics 365 Talent – Attract eller Onboard.
author: andreabichsel
manager: AnnBe
ms.date: 01/22/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-01-22
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 2a3c83fcc3f48aa235ffb2db2dc492b34a306c4c
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/24/2019
ms.locfileid: "2024201"
---
# <a name="azure-active-directory-users-not-found-in-people-picker"></a>Fant ikke Azure Active Directory-brukere i Personvelger

[!include [banner](includes/banner.md)]

## <a name="issue"></a>Avgang

Noen gyldige brukere i Microsoft Azure Active Directory (Azure AD) for leier vises ikke når du søker etter navnet i Personvelger i Dynamics 365 Talent: Attract eller Dynamics 365 Talent: Onboard.

## <a name="cause"></a>Årsak

Enkelte brukertyper støttes ikke i Attract og Onboard. Kontroller at brukeren ikke er en Azure AD B2B-gjestebruker (bedrift til bedrift). "Brukertype"-informasjon finnes i Azure Active Directory-bladet på Azure-portalen.

Hvis du vil ha mer informasjon om Azure B2B, se [Hva er gjestebrukertilgang i Azure Active Directory B2B](https://docs.microsoft.com/azure/active-directory/b2b/what-is-b2b).

For ikke-B2B-brukere er det enkelte brukere som kan ha en ufullstendig "Brukertype"-egenskap i **Bruker**-objektet. Dette kan bekreftes og løses ved hjelp av Azure AD Powershell-modulen. Hvis du vil ha mer informasjon, kan du se [Azure AD](https://docs.microsoft.com/powershell/module/azuread/?view=azureadps-2.0).

## <a name="resolution"></a>Oppløsning

For å fullføre fremgangsmåten nedenfor for å løse problemet må du ha "Global administrator"-tillatelser på Azure Active Directory-leieren eller tillatelser for **User.ReadWrite.All**.

For å bekrefte "Brukertype" for den aktuelle brukeren.

```
PS C:\>Get-AzureADUser -ObjectId "testUpn@tenant.com"
```
Kommandoen returnerer følgende informasjon.
```
ObjectId                             DisplayName UserPrincipalName      UserType
--------                             ----------- -----------------      --------
5e8b0f4d-2cd4-4e17-9467-b0f6a5c0c4d0 New user    testUpn@tenant.com     
```
Merk **Brukertype**-egenskapen for brukeren. Hvis **Brukertype** er tom, for eksempel ikke "Medlem" eller "Gjest", kan du oppdatere den **Brukertype** ved hjelp av kommandoen nedenfor.

```
PS C:\>Set-AzureADUser -ObjectId "testUpn@tenant.com" -UserType Member
```
