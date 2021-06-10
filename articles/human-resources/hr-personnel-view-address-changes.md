---
title: Vise og behandle adresseendringer
description: Dette emnet forklarer hvordan du kan vise og behandle adresseendringer i Dynamics 365 Human Resources.
author: andreabichsel
ms.date: 08/07/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 269074
ms.assetid: 426c6127-42ee-4163-8dd0-b2867f95581d
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-08-07
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 751e903b011b74fad584a1a22b574134610aa3d2
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/18/2021
ms.locfileid: "6051767"
---
# <a name="view-and-manage-address-changes"></a>Vise og behandle adresseendringer

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

I dette emnet finner du informasjon om hvordan du kan vise og behandle adresseendringer på den selvbetjente siden **Rediger personopplysninger** for ansatte eller på **Arbeider**-detaljsiden i Dynamics 365 Human Resources.

Mange organisasjoner vil at de ansatte skal administrere sine egne personopplysninger via selvbetjening. Du kan tillate at brukere oppdaterer adresser i arbeidsområdet **Ansattselvbetjening**. Deretter kan du overvåke disse endringene i arbeidsområdet **Personaladministrasjon**. Hvis du vil bruke denne funksjonen, må du angi hvor mange dager du vil vise endringene, på siden **Personalparametere**.

## <a name="configure-address-change-parameters"></a>Konfigurere parametere for adresseendring

Følg denne fremgangsmåten for å konfigurere antall dager du vil at adresseendringer skal vises i arbeidsområdet **Personaladministrasjon**:

1. I navigasjonsruten velger du **Personaladministrasjon**.

2. Velg **Koblinger**.

3. Velg **Personalparametere**.

4. I feltet **Antall dager** under **Adresseendring** angir du antallet dager du vil at adresseendringer skal vises, i arbeidsområdet **Personaladministrasjon**.

5. Lukk siden.

## <a name="create-or-change-an-employee-address"></a>Opprette eller endre adressen til en ansatt

Ansatte kan oppdatere sine egne adresser i arbeidsområdet **Ansattselvbetjening**. Følg disse trinnene for å opprette eller endre en adresse:

1. Velg flisen **Ansattselvbetjening** på startsiden.

2. Velg **Rediger personlig informasjon**.

3. Klikk **Legg til** for å legge til en adresse. Hvis du vil oppdatere en eksisterende adresse fra listen, merker du adressen og velger **Rediger**.

4. Angi **Navnet eller beskrivelse**.

5. Velg rullegardinlisten **Formål**, og velg deretter adressetypen.

6. Angi **Land/område**.

7. Angi **Postnummer**.

8. Angi **Gate**.

9. Angi **Poststed**, **Delstat** og **Fylke**. Disse feltene angis vanligvis automatisk basert på **Postnummer**-feltet.

10. Hvis du vil, velger du **Primær**-feltet for å angi en primæradresse. Bare én adresse kan merkes som primær. Hvis en annen adresse allerede er merket som primær adresse, må du bekrefte at du vil bruke denne adressen som den primære adressen.

11. Hvis du vil, velger du **Privat**-feltet for å angi at adressen er privat. Bare brukere med eksplisitt tillatelse til å vise informasjon om privatadresser kan vise denne adressen.

12. Velg **OK**.

## <a name="create-or-change-a-worker-address"></a>Opprette eller endre en arbeideradresse

Du kan oppdatere en adresse i arbeidsområdet **Personaladministrasjon**. Følg disse trinnene for å opprette eller endre en adresse:

1. I arbeidsområdet **Personaladministrasjon** velger du **Koblinger** og deretter **Arbeidere**.

3. Velg arbeideren, og velg deretter **Adresser**.

3. Klikk **Legg til** for å legge til en adresse. Hvis du vil oppdatere en eksisterende adresse fra listen, merker du adressen og velger **Rediger**.

4. Angi **Navnet eller beskrivelse**.

5. Velg rullegardinlisten **Formål**, og velg deretter adressetypen.

6. Angi **Land/område**.

7. Angi **Postnummer**.

8. Angi **Gate**.

9. Angi **Poststed**, **Delstat** og **Fylke**. Disse feltene angis vanligvis automatisk basert på **Postnummer**-feltet.

10. Hvis du vil, velger du **Primær**-feltet for å angi en primæradresse. Bare én adresse kan merkes som primær. Hvis en annen adresse allerede er merket som primær adresse, må du bekrefte at du vil bruke denne adressen som den primære adressen.

11. Hvis du vil, velger du **Privat**-feltet for å angi at adressen er privat. Bare brukere med eksplisitt tillatelse til å vise informasjon om privatadresser kan vise denne adressen.

12. Velg **OK**.
 
## <a name="create-a-future-change-for-an-address"></a>Opprette en fremtidig endring for en adresse

I noen tilfeller vil du kanskje oppdatere en adresse for å endre den i fremtiden. Dette kan for eksempel være nyttig hvis en ansatt skal flytte den 15. i neste måned.

1. Åpne siden **Administrer adresser** ved å velge **Flere alternativer > Avansert** fra ethvert adresserutenett.

2. Velg **Ny** for å opprette en ny adresse.

3. Angi detaljene for adressen.

4. Velg hurtigfanen **Generelt**.

5. I feltet **Gyldighetsdato** velger du datoen da den nye adressen skal gjelde.

6. I feltet **Utløpsdato** kan du eventuelt velge når adressen ikke lenger skal være gyldig.

7. Lukk sidene.

## <a name="view-and-monitor-address-changes"></a>Vise og overvåke adresseendringer

HR-personale kan vise og overvåke adresseendringer fra arbeidsområdet **Personaladministrasjon**. Hvis du vil vise adresseendringene, åpner du flisen **Personaladministrasjon** fra **startsiden**. Adresseendringene vises på en flis i øvre høyre hjørne. Nummeret over **Adresseendringer** viser hvor mange adresse endringer som har oppstått i løpet av antallet dager som er angitt på siden **Personalparametere**. 

Når du velger **Adresseendringer**-flisen, viser en ny side detaljene for alle adresseendringer. Du kan også velge **Inkluder fremtidige adresseendringer** i øvre høyre hjørne for å vise adresseendringer med en fremtidig dato.

> [!NOTE]
> Hvis du vil motta et varsel eller en e-postmelding om disse adresseendringene, kan du opprette en ny varslingsregel på **Alternativer**-fanen i handlingsruten. Hvis du vil ha mer informasjon om varslingsregler, kan du se [Opprette varslingsregler](../fin-ops-core/fin-ops/get-started/create-alerts.md).<br><br>

> Hvis du vil konfigurere en arbeidsflyt for adresseendringene, kan du velge alternativet **Send eksternt** i varslingsregelen og deretter bruke Power Automate til å utløse forretningshendelsen og konfigurere en arbeidsflyt. Hvis du vil ha mer informasjon, kan du se [Varsler som forretningshendelser](../fin-ops-core/fin-ops/get-started/create-alerts.md#alerts-as-business-events).


[!INCLUDE[footer-include](../includes/footer-banner.md)]