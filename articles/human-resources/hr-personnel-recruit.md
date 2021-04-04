---
title: Rekruttere jobbkandidater
description: Dette emnet beskriver hvordan du rekrutterer kandidater i Dynamics 365 Human Resources.
author: andreabichsel
manager: tfehr
ms.date: 12/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-12-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 6aca285133495dfe023dfd18bdeb050aabcafee6
ms.sourcegitcommit: c88b54ba13a4dfe39b844ffaced4dc435560c47d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/19/2021
ms.locfileid: "5478290"
---
# <a name="recruit-job-candidates"></a>Rekruttere jobbkandidater

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dynamics 365 Human Resources hjelper deg med å administrere rekrutteringsforespørsler. Den hjelper deg også med overgangen fra jobbkandidater til ansatte på en sømløs måte. Hvis organisasjonen bruker et separat rekrutteringsprogram, kan rekrutteringsprosessen omfatte følgende trinn:

- Angi rekrutteringsforespørselen i Human Resources.
- Motta kandidatreferanser i Human Resources fra rekrutteringsprogrammet.
- Fullfør kandidatgodkjenningsprosessen i Human Resources.

Hvis du ikke bruker et eget rekrutteringsprogram, kan du også administrere kandidater manuelt i Human Resources.

>[!NOTE]
>Hvis du er administrator eller utvikler og vil integrere Human Resources med et tredjeparts rekrutteringsprogram, kan du se [Konfigurer Dataverse-integrering](hr-admin-integration-common-data-service.md) og [Konfigurer virtuelle Dataverse-tabeller](hr-admin-integration-common-data-service-virtual-entities.md)
>
> Du kan også finne rekrutteringsintegreringsprogrammer på [AppSource](https://appsource.microsoft.com/marketplace/apps?search=recruiting%20dynamics).
>
> Hvis du vil teste forhåndsversjonen for integrering med LinkedIn Talent Hub, kan du se [Integrer med LinkedIn Talent Hub](hr-admin-integration-linkedin.md).

## <a name="enable-recruiting-requests"></a>Aktiver rekrutteringsforespørsler

Hvis du vil sende rekrutteringsforespørsler i Human Resources, må du først aktivere funksjonaliteten i **Delte parametere for Human Resources**.

1. I arbeidsområdet **Personaladministrasjon** velger du **Koblinger**.

2. Under **Oppsett** velger du **delte parametere for Human Resources**.

3. I fanen **Rekruttering**, under **REKRUTTERING** setter **Aktiver rekrutteringsforespørsler** til **Ja**.

## <a name="add-a-recruiting-request-location"></a>Legg til en rekrutteringsforespørselssted

Hvis organisasjonen har flere steder, kan du legge dem til slik at anmodere kan velge et sted der den nye rekrutten skal fungere. Stedet vil bli inkludert i prosjektbokføringen.

1. Angi **rekrutteringsforespørselssted** i søkefeltet.

2. Velg **Ny**.

3. I feltet **Rekrutteringsforespørselssted** angir du stedsnavnet.

   ![Legg til en rekrutteringsforespørselssted](./media/hr-recruit-0a-add-location.png)

4. I **beskrivelsen** skriver du inn en beskrivelse for stedet.

5. Under **Sted** velger du **Legg til**. Hvis den meldingen **Ny adresse** vises, angir du adressen til stedet.

   ![Angi adresse](./media/hr-recruit-0b-address.png)

6. Angi informasjonen for stedets kontakt under **Kontaktinformasjon**.

7. Velg **Lagre**.

## <a name="add-a-recruiting-request"></a>Legg til en rekrutteringsforespørsel

Ledere kan sende inn rekrutteringsforespørsler i Human Resources. Hvis du bruker et separat rekrutteringsprogram, vil denne fremgangsmåten sende en rekrutteringsforespørsel og starte rekrutteringsprosessen i dette programmet. Hvis ikke kan du fullføre denne fremgangsmåten for å starte arbeidsflyten for din egen interne rekrutteringsprosess.

1. Velg **Selvbetjening for ansatte**.

2. Velg fanen **Mitt team**.

3. Velg **Forespørsel om å rekruttere**.

   ![Start en rekrutteringsforespørsel](./media/hr-recruit-1-request-to-recruit.png)

4. Fyll ut feltene **Beskrivelse**, **Jobb** og **Beregnet startdato**.

   ![Fullfør rekrutteringsforespørselen](./media/hr-recruit-2-request-to-recruit.png)

5. Velg **Fortsett**. Rekrutteringsforespørselen for stillingen din vises.

6. Under **Generelt** velger du en rekrutterer fra rullegardinlisten **Rekrutterer**, og deretter velger du et sted fra rullegardinlisten **Rekrutteringsforespørselssted**.

7. Endre eventuell informasjon etter behov under **Jobb**, og velg deretter **Opprett detaljer fra jobb**.

   ![Opprett detaljer fra jobb](./media/hr-recruit-3-create-details-from-job.png)

   Resten av rekrutteringsforespørselen vil bli fylt ut med standardinformasjonen for jobben du angav.

8. Under **Ekstern beskrivelse** angir du en ekstern jobbeskrivelse.

9. Under **Stillinger** velger du **Legg til**, og deretter velger du en stilling for denne rekrutteringsforespørselen.

   ![Legg til en stilling](./media/hr-recruit-4-select-position.png)

10. Under **Ferdigheter** velger du **Legg til** og velger deretter en ferdighet.

11. Under **Krav til utdannelse** velger du **Legg til**, og deretter velger du verdier fra rullegardinlistene **Utdanning** og **Utdanningsnivå**.

   ![Legg til krav til utdanning](./media/hr-recruit-5-select-educational-requirements.png)

12. Legg til kommentarer etter behov under **Kommentar**.

13. Under **Kompensasjon** velger du et nivå fra rullegardinlisten **Nivå**, og justerer deretter **Lav terskel**, **Kontrollpunkt** og **Høy terskel** etter behov.

14. Når rekrutteringsforespørselen er fullført og du er klar til å starte rekrutteringsprosessen, velger du **Aktiver** på menylinjen.

   ![Aktiver rekrutteringsforespørsel](./media/hr-recruit-6-activate-recruit-request.png)

15. Velg **Lagre**.

## <a name="view-and-edit-your-recruiting-requests"></a>Vis og rediger rekrutteringsforespørsler

Hvis du er en leder og ønsker å vise dine egne forespørsler:

1. Velg **Selvbetjening for ansatte**.

2. Velg fanen **Mitt team**.

3. Under **Informasjon om mitt team** velger du kategorien **Rekrutteringsforespørsler**.

   ![Velg fanen Rekrutteringsforespørsler](./media/hr-recruit-7-recruiting-requests.png)

4. Hvis du vil vise eller redigere en rekrutteringsforespørsel, velger du den i rutenettet.

Hvis du er en HR Pro og ønsker å vise alle rekrutteringsforespørslene:

1. Velg **Personaladministrasjon**.

2. Velg fanen **Rekrutteringsforespørsler**.

   ![Vise rekrutteringsforespørsler i Personaladministrasjon](./media/hr-recruit-8-recruiting-requests-personnel-management.png)

3. Hvis du vil vise eller redigere en rekrutteringsforespørsel, velger du den i rutenettet.

## <a name="add-or-edit-a-candidate-profile"></a>Legg til eller rediger en kandidatprofil

Hvis organisasjonen har integrert med et annet program for å administrere rekrutteringsforespørsler, blir rekrutteringsforespørsler videresendt til dette programmet. Rekrutteringsprogrammet sender deretter kandidatinformasjon tilbake til Human Resources. Hvis ikke kan du følge dine egne interne rekrutteringsprosesser og legge inn kandidatinformasjon manuelt.

1. Velg **Personaladministrasjon**.

2. Velg **Koblinger**.

3. Under **Rekruttering** velger du **Kandidater**.

   ![Vis kandidater](./media/hr-recruit-9-candidates.png)

4. Velg **Ny** for å legge til en kandidat. Hvis du vil redigere en eksisterende kandidat fra listen, merker du adressen og velger **Rediger**. Kandidatprofilen vises.

5. Under **Kandidatsammendrag** legger du inn eller redigerer kandidatinformasjonen etter behov.

6. Under **Rekrutteringsforespørsel** velger du en rekrutteringsforespørsel du vil koble kandidaten til. Deretter fyller du ut feltene **Beregnet startdato**, **Ansettelsessjef**, **Stilling** og **Beskrivelse** etter behov.

   ![Koble til rekrutteringsforespørsel](./media/hr-recruit-10-link-to-recruiting-request.png)

7. Fyll ut all informasjonen i følgende områder som du vil ta med i kandidatens post:
   - **Kommentarer**
   - **Yrkeserfaring**
   - **Kontaktinformasjon**
   - **Utdanning**
   - **Kompetanse**
   - **Attester**
   - **Screeninger**

8. Velg **Lagre**.

## <a name="hire-a-candidate"></a>Ansett en kandidat

Når du er klar til å ansette en kandidat, følger du denne fremgangsmåten for overgang fra kandidat til ansatt.

1. Velg **Ansett** i kandidatskjemaet.

   ![Ansett en kandidat](./media/hr-recruit-11-hire.png)

2. Fyll ut alle feltene under **Detaljer** i skjemaet **Ansett ny arbeider**.

   ![Angi detaljer for ny ansettelse](./media/hr-recruit-12-hire-new-worker.png)

3. Under **Stillingsdetaljer** kan du bekrefte og endre informasjon etter behov.

4. Under **Sjekklister for jobbintroduksjon** velger du de relevante sjekklistene for den ansatte.

5. Velg **Fortsett** for å opprette ansattposten.

   >[!NOTE]
   >Kandidatposten kan gå gjennom flere godkjenningstrinn før den blir til en ansattpost, avhengig av arbeidsflytene i organisasjonen.

## <a name="decide-not-to-hire-a-candidate"></a>Bestemme deg for ikke å ansette en kandidat

Hvis du bestemmer deg for ikke å ansette en kandidat, kan du følge denne fremgangsmåten for å fjerne dem fra gjennomgangsprosessen. 

1. Velg **Ikke ansett** i kandidatskjemaet.

   ![Ikke ansett kandidat](./media/hr-recruit-13-do-not-hire.png)

2. Velg en **årsakskode**, og ta med eventuelle kommentarer.

3. Velg **OK**.

## <a name="dismiss-a-candidate"></a>Forkast en kandidat

Om nødvendig kan du forkaste en kandidat etter å ha ansatt vedkommende. En kandidat kan for eksempel avvise tilbudet eller ikke dukke opp den første dagen.

- Velg **Forkast kandidat** i kandidatskjemaet.

  ![Forkast kandidat](./media/hr-recruit-14-dismiss-candidate.png)

## <a name="see-also"></a>Se også

[Konfigurere virtuelle Dataverse-tabeller](hr-admin-integration-common-data-service-virtual-entities.md)<br>
[Organisere arbeidsstyrken](hr-personnel-departments-jobs-positions.md)<br>
[Definere komponentene for en jobb](hr-personnel-jobs.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
