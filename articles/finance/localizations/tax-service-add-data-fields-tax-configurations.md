---
title: Legge til datafelt i avgiftskonfigurasjoner
description: Dette emnet beskriver hvordan du tilpasser avgiftskonfigurasjoner ved å legge til datafelt.
author: Kai-Cloud
ms.date: 09/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: fb10fb5feb317dca5253eea6e5694a3960a58a7d
ms.sourcegitcommit: ecd4c148287892dcd45656f273401315adb2805e
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/18/2021
ms.locfileid: "7500152"
---
# <a name="add-data-fields-in-tax-configurations"></a>Legge til datafelt i avgiftskonfigurasjoner

[!include [banner](../includes/banner.md)]

Dette emnet beskriver hvordan du tilpasser avgiftskonfigurasjoner ved hjelp av [datafelt som legges til i avgiftsintegrasjon](tax-service-add-data-fields-tax-integration-by-extension.md).

## <a name="customize-the-tax-data-model"></a>Tilpasse avgiftsdatamodellen

1. I Microsoft  Dynamics 365 Finance går du til **Elektronisk rapportering** > **Avgiftskonfigurasjoner**.
2. I konfigurasjonstreet velger du **Avgiftsdatamodell – Europa**. Velg deretter **Opprett konfigurasjon** i handlingsruten.
3. I rullegardinlisten velger du **Modell for avgiftsbelagte dokumenter utledet fra navnet: Avgiftsdatamobell – Europa, Microsoft**, skriver inn et navn på den nye avgiftsdatamodellen og velger deretter **Opprett konfigurasjon**.
4. Velg avgiftsdatamodellen du akkurat opprettet, og velg deretter **Utforming** i handlingsruten.
5. Utvid datamodelltreet, velg **Linjer**, og velg deretter **Ny**.
6. I dialogboksen **Opprett node** angir du et navn, angir varetypen og velger **Legg til**.
7. Legg til eventuelle nødvendige kolonner.
8. Velg **Lagre** i handlingsruten , og velg deretter **Fullfør**.
9. Lukk siden, og vis den fullførte versjonen av avgiftsdatamodellen.

## <a name="customize-the-tax-configuration"></a>Tilpasse avgiftskonfigurasjonen

1. I Finance går du til **Elektronisk rapportering** > **Avgiftskonfigurasjoner**.
2. I konfigurasjonstreet velger du **Avgiftskonfigurasjon – Europa**. Velg deretter **Opprett konfigurasjon** i handlingsruten.
3. I rullegardinlisten velger du **Konfigurasjon av avgiftstjeneste utledet fra navnet: Avgiftskonfigurasjon – Europa, Microsoft**, skriver inn et navn på den nye avgiftskonfigurasjonen og velger deretter **Opprett konfigurasjon**.
4. Velg avgiftskonfigurasjonen du akkurat opprettet, og velg deretter **Utforming** i handlingsruten.
5. I **Egenskaper**-delen i **Datamodell**-feltet velger du den tilpassede avgiftsdatamodellen du opprettet tidligere.
6. I feltet **Datamodellversjon** velger du den fullførte versjonen av avgiftsdatamodellen.
7. Velg **Legg til**, og legg til de nødvendige avgiftsmålene.
8. Velg **Lagre** i handlingsruten , og velg deretter **Fullfør**.
9. Lukk siden, og vis den fullførte versjonen av avgiftskonfigurasjonen.

## <a name="implement-tax-features-in-the-customized-tax-configuration"></a>Implementere avgiftsfunksjoner i den tilpassede avgiftskonfigurasjonen

1. I Regulatory Configuration Service (RCS) går du til **Globaliseringsfunksjoner** > **Avgift**.
2. Velg **Legg til**, angi informasjon om den nye funksjonen, og velg deretter **Opprett funksjon**.
3. Velg funksjonen på **Versjoner**-fanen, og velg deretter **Rediger**.
4. På **Generelt**-fanen i **Konfigurasjonsversjon**-feltet velger du den tilpassede avgiftskonfigurasjonen og versjonen.
5. I dialogboksen **Administrer kolonner** velger du overskriften og linjekolonnene du vil inkludere i det tilpassede avgiftsmålet, og deretter velger du pil høyre for å legge dem til i listen **Valgte kolonner**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
