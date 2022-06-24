---
title: Legg til datafelter i avgiftskonfigurasjoner
description: Denne artikkelen beskriver hvordan du tilpasser avgiftskonfigurasjoner ved å legge til datafelt.
author: Kai-Cloud
ms.date: 10/21/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.custom: ''
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 894c42f444d27b807288b84c7b9c620ad0121fa9
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8872333"
---
# <a name="add-data-fields-in-tax-configurations"></a>Legg til datafelter i avgiftskonfigurasjoner

[!include [banner](../includes/banner.md)]

Denne artikkelen beskriver hvordan du tilpasser avgiftskonfigurasjoner ved hjelp av [datafelt som legges til i avgiftsintegrasjon](tax-service-add-data-fields-tax-integration-by-extension.md).

## <a name="customize-the-tax-data-model"></a>Tilpasse avgiftsdatamodellen

1. I Microsoft Dynamics 365 Finance går du til **Elektronisk rapportering** > **Avgiftskonfigurasjoner**.
2. I konfigurasjonstreet velger du **Datamodell for avgiftsberegning**. Velg deretter **Opprett konfigurasjon** i handlingsruten. 

  > [!NOTE] 
  > Hvis det ikke er noen tilgjengelig konfigurasjonsleverandør, oppretter du en og gjør den aktiv for mva-konfigurasjonen. Hvis du ha mer informasjon, kan du se [Opprette konfigurasjonsleverandører og merke dem som aktive](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).
  
3. I rullegardinlisten velger du **Modell for avgiftsbelagte dokumenter utledet fra navnet: Datamodell for avgiftsberegning, Microsoft**, skriver inn et navn på den nye avgiftsdatamodellen og velger deretter **Opprett konfigurasjon**.
4. Velg avgiftsdatamodellen du akkurat opprettet, og velg deretter **Utforming** i handlingsruten.
5. Utvid datamodelltreet, velg **Linjer**, og velg deretter **Ny**.
6. I dialogboksen **Opprett node** angir du et navn, angir varetypen og velger **Legg til**.
7. Legg til eventuelle nødvendige kolonner.
8. Velg **Lagre** i handlingsruten , og velg deretter **Fullfør**.
9. Lukk siden, og vis den fullførte versjonen av avgiftsdatamodellen.

## <a name="customize-the-tax-configuration"></a>Tilpasse avgiftskonfigurasjonen

1. I Finance går du til **Elektronisk rapportering** > **Avgiftskonfigurasjoner**.
2. I konfigurasjonstreet velger du **Konfigurasjon for avgiftsberegning**. Velg deretter **Opprett konfigurasjon** i handlingsruten.
3. I rullegardinlisten velger du **Konfigurasjon av avgiftstjeneste utledet fra navnet: Konfigurasjon for avgiftsberegning, Microsoft**, skriver inn et navn på den nye avgiftskonfigurasjonen og velger deretter **Opprett konfigurasjon**.
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
