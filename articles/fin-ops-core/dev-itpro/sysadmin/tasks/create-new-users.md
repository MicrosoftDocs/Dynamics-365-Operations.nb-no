---
title: Opprette nye brukere
description: Brukere er interne ansatte i din organisasjon, eller eksterne kunder og leverandører, som trenger tilgang til systemet for å utføre jobbene sine.
author: maertenm
manager: AnnBe
ms.date: 06/08/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserManagement, SysDataAreaSelectLookup, SysSecUserAddRoles, SysUserMSODSUserImport
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d126b449074663772549b96b86acb53db971a5d4
ms.sourcegitcommit: 7d943499f302298c6ff127f56cecc34af6cee289
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/08/2020
ms.locfileid: "3435590"
---
# <a name="create-new-users"></a>Opprette nye brukere

[!include [banner](../../includes/banner.md)]

Brukere er interne ansatte i din organisasjon, eller eksterne kunder og leverandører, som trenger tilgang til systemet for å utføre jobbene sine.

## <a name="associate-a-user-with-a-license-new-license-types-only"></a>Knytte en bruker til en lisens (bare nye lisenstyper)
For kunder som har én av de nye lisenstypene som ble lagt til i oktober 2019, må brukere være knyttet til en lisens. Brukere som er knyttet til en lisens, legges automatisk til som systembrukere som ikke har noen roller første gang de logger på.

Systemadministratorer kan [tilordne lisenser til brukere](https://docs.microsoft.com/office365/admin/subscriptions-and-billing/assign-licenses-to-users?view=o365-worldwide) i [administrasjonssenteret for Microsoft 365](https://docs.microsoft.com/office365/admin/admin-overview/about-the-admin-center?view=o365-worldwide).

## <a name="associate-an-external-user-with-a-license-new-license-types-only"></a>Knytte en ekstern bruker til en lisens (bare nye lisenstyper)
Brukere utenfor leieren som miljøet ble distribuert i, må representeres i katalogen for vertsleierkatalogen (Azure Active Directory (Azure AD)) slik at de kan tilordnes lisenser. Disse eksterne brukerne må legges til for leieren i Azure AD som gjestebrukere og deretter tilordnes de aktuelle lisensene. Hvis du vil ha mer informasjon, kan du se [Legge til Azure Active Directory B2B-samarbeidsbrukere i Azure-portalen](https://docs.microsoft.com/azure/active-directory/b2b/add-users-administrator).

## <a name="add-a-new-user"></a>Legge til en ny bruker
1. Gå til **Systemadministrasjon \> Brukere \> Brukere**.
2. Velg **Ny** i handlingsruten.
3. I **Bruker-ID**-feltet angir du en unik ID for brukeren. En bruker-ID er nødvendig.  
4. Angi navnet på brukeren i **Brukernavn**-feltet.  
5. I **Domene**-feltet angir du brukerens domene.  
6. Angi brukerens alias i **Alias**-feltet.  
7. Velg ønsket firma i **Firma**-feltet. 
8. I **Brukerens roller**-hurtigfanen en velger du **Tilordne roller** for å tilordne brukere til sikkerhetsroller. Hvis du vil ha mer informasjon, kan du se [Tilordne brukere til sikkerhetsroller](assign-users-security-roles.md).
9. Velg **OK**.
10. Velg **Lagre**.

## <a name="import-users"></a>Importer brukere
1. Gå til **Systemadministrasjon \> Brukere \> Brukere**.
2. Velg **Importer brukere** i handlingsruten.
3. Merk den valgte raden i listen.
4. Velg **Importer brukere**.
5. Velg **Lukk**.

