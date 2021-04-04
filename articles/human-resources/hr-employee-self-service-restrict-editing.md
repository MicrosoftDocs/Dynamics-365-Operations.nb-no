---
title: Begrense redigering av personlige opplysninger
description: Du kan hindre at ansatte redigerer kontaktdetaljer i Dynamics 365 Human Resources.
author: andreabichsel
manager: tfehr
ms.date: 03/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: EssWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-03-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d4785232dbb21c5f8a800497fb0cfd3c64dea2d8
ms.sourcegitcommit: 45d10d0c25b3ec585323709bb97ba1895b500429
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/05/2021
ms.locfileid: "5503042"
---
# <a name="restrict-editing-of-personal-information"></a>Begrense redigering av personlige opplysninger

[!include [applies to](../includes/applies-to-hr.md)]
[!include [preview feature](./includes/preview-feature.md)]

Dette emnet beskriver hvordan du begrenser ansatte fra å redigere kontaktdetaljer i Dynamics 365 Human Resources. Det kan hende at du vil hindre at ansatte redigerer bestemte kontaktdetaljer, for eksempel forretningslokasjonen eller e-postadressen.

> [!NOTE]
> Hvis du vil bruke denne funksjonen, må du først aktivere **(Forhåndsvis) Hindre ansatte i å legge til eller redigere adresse- og kontaktinformasjon for utvalgte formål** i Funksjonsstyring. Hvis du vil ha mer informasjon om hvordan du aktiverer forhåndsvisningsfunksjoner, kan du se [Behandle funksjoner](hr-admin-manage-features.md).<br><br>![Aktiver forhåndsvisningsfunksjon](./media/hr-employee-self-service-restrict-enable.png)

## <a name="choose-the-information-an-employee-can-add-or-edit"></a>Velge informasjonen som en ansatt kan legge til eller redigere

1. I Human Resources velger du **Personaladministrasjon**, **Koblinger** og deretter **Personalparametere**.

   ![Gå til Human Resources-parametere](./media/hr-employee-self-service-human-resources-parameters.png)

2. Velg fanen **Selvbetjening for ansatte** på siden **Parametere for Human Resources**.

   ![Velg Selvbetjening for ansatte](./media/hr-employee-self-service-tab.png)

3. I fanen **Selvbetjening for ansatte** fjerner du merket for all informasjon i delen **Adresse- og kontaktinformasjon** som du ikke vil at ansatte skal legge til eller redigere. I dette eksemplet er det ikke merket av for kontaktinformasjonen for **Virksomhet**.

   ![Begrense redigering av forretningskontaktinformasjon](./media/hr-employee-self-service-restrict-business.png)

4. Velg **Lagre**.

   ![Lagre endringer](./media/hr-employee-self-service-restrict-save.png)

## <a name="employee-experience"></a>Ansatterfaring

Når du har begrenset ansatte fra å legge til eller redigere kontaktdetaljer, kan de se informasjonen, men kan ikke endre den.

I dette eksemplet hvor ansatte er begrenset fra å redigere kontaktdetaljer for **Virksomhet**, kan de likevel se informasjonen i Selvbetjening for ansatte:

![Vise detaljer for forretningskontakter](./media/hr-employee-self-service-restrict-view.png)

Når de velger forretningskontaktdetaljene, vises imidlertid ruten **Rediger adresse** som skrivebeskyttet, og de kan ikke endre noen av feltene.

![Forretningskontaktdetaljer vises som skrivebeskyttet](./media/hr-employee-self-service-restrict-read-only.png)

Hvis de i tillegg velger **Legg til** for å legge til en ny adresse, kan de ikke velge **Virksomhet** fra rullegardinlisten **Formål**.

![Den ansatte kan ikke legge til en forretningsadresse](./media/hr-employee-self-service-restrict-add.png)

Ansatte får samme erfaring når de velger **Kontaktdetaljer** på siden **Personalinformasjon** og legger til en ny adresse. Rullegardinlisten **Formål** viser bare informasjonstypene de kan legge til. 

![Den ansatte kan ikke velge rullegardinlisten Virksomhet i Formål](./media/hr-employee-self-service-restrict-purpose.png)

**Kontaktdetaljer** viser nå **Formål** i rutenettet.

![Formål vises i Rutenett for kontaktdetaljer](./media/hr-employee-self-service-restrict-purpose-grid.png)

## <a name="see-also"></a>Se også

[Oversikt over selvbetjening for ansatte og ledere](hr-employee-manager-self-service-overview.md)<br>
[Konfigurere parametere for Human Resources](hr-setup-parameters.md)<br>
[Rediger personlige opplysninger](hr-employee-manager-self-service-edit-personal-information.md)