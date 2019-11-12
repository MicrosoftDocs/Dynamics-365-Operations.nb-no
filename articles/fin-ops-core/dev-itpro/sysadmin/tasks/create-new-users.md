---
title: Opprette nye brukere
description: Brukere er interne ansatte i din organisasjon, eller eksterne kunder og leverandører, som trenger tilgang til systemet for å utføre jobbene sine.
author: maertenm
manager: AnnBe
ms.date: 10/08/2019
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
ms.openlocfilehash: 3c347a34a389c32d005cc8086c4a1349ecb8a698
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/10/2019
ms.locfileid: "2570527"
---
# <a name="create-new-users"></a>Opprette nye brukere

[!include [task guide banner](../../includes/task-guide-banner.md)]

Brukere er interne ansatte i din organisasjon, eller eksterne kunder og leverandører, som trenger tilgang til systemet for å utføre jobbene sine.

## <a name="associate-a-user-with-a-license-new-license-types-only"></a>Knytte en bruker til en lisens (bare nye lisenstyper)
For kunder som har én av de nye lisenstypene som ble lagt til i oktober 2019, må brukere være knyttet til en lisens. Brukere som er knyttet til en lisens, legges automatisk til som systembrukere som ikke har noen roller første gang de logger på. Brukere som ikke er knyttet til en lisens, får en advarsel.

Systemadministratorer kan [tilordne lisenser til brukere](https://docs.microsoft.com/office365/admin/subscriptions-and-billing/assign-licenses-to-users?view=o365-worldwide) i [administrasjonssenteret for Microsoft 365](https://docs.microsoft.com/office365/admin/admin-overview/about-the-admin-center?view=o365-worldwide).

## <a name="add-a-new-user"></a>Legge til en ny bruker
1. Gå til **Systemadministrasjon \> Brukere \> Brukere**.
2. Velg **Ny** i handlingsruten.
3. I **Bruker-ID**-feltet angir du en unik ID for brukeren. En bruker-ID er nødvendig.  
4. Angi navnet på brukeren i **Brukernavn**-feltet.  
5. I **Domene**-feltet angir du brukerens domene.  
6. Angi brukerens alias i **Alias**-feltet.  
7. Velg ønsket firma i **Firma**-feltet. 
8. Velg **Tilordne roller** i hurtigfanen **Brukerroller** for å [tilordne brukere til sikkerhetsroller](assign-users-security-roles.md)
9. Velg **OK**.
10. Velg **Lagre**.

## <a name="import-users"></a>Importer brukere
1. Velg **Importer brukere** i handlingsruten.
2. Merk den valgte raden i listen.
3. Velg **Importer brukere**.
4. Velg **Lukk**.

