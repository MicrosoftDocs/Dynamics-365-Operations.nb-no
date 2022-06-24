---
title: Begrense redigering av personlige opplysninger
description: Du kan hindre at ansatte redigerer kontaktdetaljer i Dynamics 365 Human Resources.
author: twheeloc
ms.date: 08/26/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EssWorkspace
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-03-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: c82114f6600345ee5e2eb9c1c0629ae6c8f0b9a7
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8877692"
---
# <a name="restrict-editing-of-personal-information"></a>Begrens redigering av personlige opplysninger


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [applies to](../includes/applies-to-hr.md)]
[!include [preview feature](./includes/preview-feature.md)]

Denne artikkelen beskriver hvordan du begrenser ansatte fra å redigere kontaktdetaljer i Dynamics 365 Human Resources. Det kan hende at du vil hindre at ansatte redigerer bestemte kontaktdetaljer, for eksempel forretningslokasjonen eller e-postadressen.

> [!NOTE]
> Hvis du vil bruke denne funksjonen, må du først aktivere **(Forhåndsvis) Hindre ansatte i å legge til eller redigere adresse- og kontaktinformasjon for utvalgte formål** i Funksjonsstyring. Hvis du vil ha mer informasjon om hvordan du aktiverer forhåndsvisningsfunksjoner, kan du se [Behandle funksjoner](hr-admin-manage-features.md).<br><br>![Aktiver forhåndsvisningsfunksjon.](./media/hr-employee-self-service-restrict-enable.png)

## <a name="choose-the-information-an-employee-can-add-or-edit"></a>Velge informasjonen som en ansatt kan legge til eller redigere

1. I Human Resources velger du **Personaladministrasjon**, **Koblinger** og deretter **Personalparametere**.

   ![Gå til Human Resources-parametere.](./media/hr-employee-self-service-human-resources-parameters.png)

2. Velg fanen **Selvbetjening for ansatte** på siden **Parametere for Human Resources**.

   ![Velg Selvbetjening for ansatte.](./media/hr-employee-self-service-tab.png)

3. I fanen **Selvbetjening for ansatte** fjerner du merket for all informasjon i delen **Adresse- og kontaktinformasjon** som du ikke vil at ansatte skal legge til eller redigere. I dette eksemplet er det ikke merket av for kontaktinformasjonen for **Virksomhet**.

   ![Begrense redigering av forretningskontaktinformasjon.](./media/hr-employee-self-service-restrict-business.png)

4. Velg **Lagre**.

   ![Lagre endringer.](./media/hr-employee-self-service-restrict-save.png)

## <a name="employee-experience"></a>Ansatterfaring

Når du har begrenset ansatte fra å legge til eller redigere kontaktdetaljer, kan de se informasjonen, men kan ikke endre den.

I dette eksemplet hvor ansatte er begrenset fra å redigere kontaktdetaljer for **Virksomhet**, kan de likevel se informasjonen i **Selvbetjening for ansatte**:

![Vise detaljer for forretningskontakter.](./media/hr-employee-self-service-restrict-view.png)

Når de velger forretningskontaktdetaljene, vises imidlertid ruten **Rediger adresse** som skrivebeskyttet, og de kan ikke endre noen av feltene.

![Forretningskontaktdetaljer vises som skrivebeskyttet.](./media/hr-employee-self-service-restrict-read-only.png)

Hvis de i tillegg velger **Legg til** for å legge til en ny adresse, kan de ikke velge **Virksomhet** fra rullegardinlisten **Formål**.

![Den ansatte kan ikke legge til en forretningsadresse.](./media/hr-employee-self-service-restrict-add.png)

Ansatte får samme erfaring når de velger **Kontaktdetaljer** på siden **Personalinformasjon** og legger til en ny adresse. Rullegardinlisten **Formål** viser bare informasjonstypene de kan legge til. 

![Den ansatte kan ikke velge rullegardinlisten Virksomhet i Formål.](./media/hr-employee-self-service-restrict-purpose.png)

**Kontaktdetaljer** viser nå **Formål** i rutenettet.

![Formål vises i Rutenett for kontaktdetaljer.](./media/hr-employee-self-service-restrict-purpose-grid.png)

## <a name="see-also"></a>Se også

[Oversikt over selvbetjening for ansatte og ledere](hr-employee-manager-self-service-overview.md)<br>
[Konfigurer parametere for Human Resources](hr-setup-parameters.md)<br>
[Rediger personlige opplysninger](hr-employee-manager-self-service-edit-personal-information.md)
