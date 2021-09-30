---
title: Konfigurere fraværsbehandlingsrollen
description: Dette emnet beskriver hvordan du konfigurerer fraværsbehandlingsrollen for administrasjon av ansattpermisjon.
author: hasrivas
ms.date: 08/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace, LeaveAbsenceManager
audience: Application User
ms.search.scope: Human Resources
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: hasrivas
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 7f2a2fd0a1ad1cca19625ff1029962f608251f1d
ms.sourcegitcommit: a73df4ddc7f8ddc9e37269c0236dc1bb9b7c7966
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/09/2021
ms.locfileid: "7485760"
---
# <a name="configure-the-absence-manager-role"></a>Konfigurere fraværsbehandlingsrollen

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

I noen organisasjoner kan det hende at ledere ikke administrerer permisjonen for gruppen. I stedet kan en fraværsleder håndtere denne prosessen for gruppemedlemmer på tvers av flere avdelinger og grupper. Fraværsledere har følgende funksjoner for permisjonsbehandling:

- Gjennomgå og godkjenne fridager, basert på et alternativt hierarki.
- Vise gruppemedlemsaldoer.
- Vise fraværskalenderen.

## <a name="turn-on-the-feature"></a>Aktivere funksjonen

1. I arbeidsområdet **Systemadministrasjon** velger du **Funksjonsbehandling**.

2. I kategorien **Funksjonsbehandling** aktiverer du funksjonen **Fraværsbehandling for å administrere permisjon**.

## <a name="define-a-custom-hierarchy"></a>Definere et egendefinert hierarki

Funksjonen for fraværsbehandling bruker et egendefinert hierarki som må konfigureres.

1. I arbeidsområdet **Organisasjonsstyring** velger du **Stillingshierarkityper**.

2. Opprett en stillingshierarkitype som kalles **Permisjon**.

3. I arbeidsområdet **Permisjon og fravær**, under **Koblinger**, velger du **Permisjons- og fraværsparametere**.

4. I kategorien **Generelt** i rullegardinlisten **Fraværshierarki** velger du **Permisjon**-hierarkitypen du opprettet tidligere. Denne Permisjonshierarki-tilknytningen må fullføres for hver juridiske enhet der funksjonaliteten for fraværsansvarlig skal brukes.

Når hierarkitypen er definert, må stillingshierarkirapporten tilordnes til stillingen.

1. I arbeidsområdet **Organisasjonsstyring** velger du **Alle stillinger**.

2. Velg stillingen du vil legge til permisjonshierarkiet i.

3. Velg **Legg til** i fanen **Relasjoner**.

4. I **Hierarkinavn**-feltet velger du **Permisjon**.

5. Velg en stilling i feltet **Rapporter til stilling**. Arbeidsnavnet fylles ut automatisk når du velger en stilling.

## <a name="assign-the-absence-manager-role-to-a-user"></a>Tilordne fraværsbehandlingsrollen til en bruker

Fraværsbehandlingsrollen må tilordnes ansatte slik at de kan godkjenne eller avslå permisjonsforespørsler.

1. I arbeidsområdet **Systemadministrator** velger du **Koblinger**.

2. Velg **Brukere**-koblingen i **Brukere**-delen.

3. Velg brukeren du vil tilordne fraværsbehandlingsrollen til, i listen over brukere.

4. I kategorien **Brukerens rolle** velger du **Tilordne roller**.

5. Velg rollen **Fraværsbehandling** i listen. Velg deretter **OK**.

    > [!IMPORTANT]
    > Kontroller at ansattrollen også er tilordnet brukeren du tilordner fraværsbehandlingsrollen til. Hvis ikke kan ikke arbeideren bruke funksjonen.

6. Når du har opprettet permisjonshierarkiet, kan du vise det ved å følge denne fremgangsmåten:

    1. I arbeidsområdet **Organisasjonsstyring** velger du **Stillingshierarki**.
    
    2. I **Hierarkitype**-feltet velger du **Permisjon**.

## <a name="absence-manager-workspace"></a>Arbeidsområde for fraværsleder

I arbeidsområdet **Ansattselvbetjening** viser fanen **Fraværsbehandling** fraværsinformasjon om de ansatte som er tilordnet til fraværsbehandlingen i permisjonshierarkiet. Fraværsbehandling har flere alternativer: 
 - Se gjennom forespørsler om fridager.</br>
 - Send en forespørsel om fravær på vegne av en ansatt.</br>
 - Vis alle ansatte som er tilordnet dem som en del av permisjonshierarkiet.</br>
 - Vis fraværslederkalenderen.</br>

I arbeidsområdet for **Fraværsbehandling** finnes det to kategorier:
 - **Forespørsler om fridager**: Denne fanen viser alle ventende avslagsforespørsler som fraværsansvarlig kan godkjenne. Fraværsansvarlig kan velge flere poster og gjøre noe med dem samtidig. Hvis permisjonsvisning på tvers av firmaer er aktivert, vil denne listen vise ventende fraværsforespørsler på tvers av alle juridiske enheter som de har tilgang til. Ellers vil den vise ventende fraværsforespørsler for den juridiske enheten som er valgt. </br>
 - **Alle ansatte**: Denne fanen viser alle de ansatte som er tilordnet fraværslederen i permisjonshierarkiet. Det finnes et par tilgjengelige alternativer for hver ansatt:
    - **Be om fri** – Send en ny fraværsforespørsel for den valgte ansatte.</br>
    - **Fridager** – Vis saldoer, godkjente fridager og forespørsler om fridager for den valgte ansatte.</br>

## <a name="approve-time-off-requests"></a>Godkjenne fritidsforespørsler

Fraværsledere kan godkjenne eller avslå fraværsforespørsler for ansatte. 

> [!IMPORTANT]
> Før fraværsledere kan godkjenne eller avslå forespørsler om fridager, må arbeidsflyten for permisjonsforespørsel være konfigurert til å tilordne arbeidselementer for permisjonsforespørsel til dem for gjennomgang.
>
> 1. På siden **Arbeidsflyter for Human Resources** velger eller oppretter du arbeidsflyten for permisjonsforespørsel.
> 2. Velg alternativet **Tilknytt hierarki**, og velg deretter **Permisjon** i **Hierarkinavn**-feltet.
> 3. Oppdater arbeidsflyten i arbeidsflytdesigneren. Under **Tilordningstype** velger du alternativet **Hierarki**, og deretter velger du **Konfigurerbart hierarki** i kategorien **Hierarkivalg**.
>
> Hvis du vil ha mer informasjon om hvordan du oppretter arbeidsflyten for permisjonsforespørsel, kan du se [Opprette en permisjonsforespørsel](hr-leave-and-absence-workflow.md).

1. I arbeidsområdet **Ansattselvbetjening** velger du fanen **Fraværsbehandling**.

2. Velg fraværsforespørsler som du vil gjøre noe med, i fanen **Fraværsforespørsler**. Du kan velge flere poster i denne listevisningen.

3. Bruk handlingsknappene øverst i rutenettet til å godkjenne, avslå eller delegere fraværsforespørselen. 

Brukeren kan også bruke flisen **Fraværsforespørsler** til venstre for å navigere til listen over alle arbeidselementer for fraværsforespørsler. 

## <a name="view-time-off-in-the-calendar"></a>Vise fridager i kalenderen

Brukere i fraværsbehandlingsrollen kan vise tidsforespørsler i kalenderen. Hvis du vil ha tilgang til fraværskalenderen, kan du følge disse trinnene.

> [!IMPORTANT]
> En systemadministrator må konfigurere visningsalternativene for kalenderen for fraværsansvarlig. På siden **Permisjons- og fraværsparametere** i **Kalender**-kategorien finnes det alternativer for å skjule eller vise fødselsdager, fravær uten detaljer, fravær og ventende permisjonsforespørsler. Det finnes også et alternativ for å filtrere kalendervisningsalternativet etter arbeidertype.

1. I arbeidsområdet **Ansattselvbetjening** velger du **Fraværsbehandling** og deretter **Fraværsbehandlingskalender**.

2. Angi ønskede datoer i **Dato**-feltet.

3. Oppdater visningsalternativene etter behov.

Fraværsbehandlingskalenderen viser alle postene for de ansatte som rapporterer til fraværslederen i permisjonshierarkiet.

## <a name="see-also"></a>Se også

- [Oversikt over permisjon og fravær](hr-leave-and-absence-overview.md)
- [Opprette arbeidsflyt for permisjonsforespørsel](hr-leave-and-absence-workflow.md)
- [Vise team- og firmakalendere](hr-employee-self-service-calendar.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
