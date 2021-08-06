---
title: Konfigurere fraværsbehandlingsrollen
description: Dette emnet beskriver hvordan du konfigurerer fraværsbehandlingsrollen for administrasjon av ansattpermisjon.
author: hasrivas
ms.date: 07/19/2021
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
ms.openlocfilehash: e8a8250b36d2774ac308637253b780592df316cd
ms.sourcegitcommit: 86d38cf57abe768e5bccde48b28280bc2224080c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/19/2021
ms.locfileid: "6639612"
---
# <a name="configure-the-absence-manager-role"></a>Konfigurere fraværsbehandlingsrollen

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [preview feature](./includes/preview-feature.md)]

I noen organisasjoner kan det hende at ledere ikke administrerer permisjonen for gruppen. I stedet kan en fraværsleder håndtere denne prosessen for gruppemedlemmer på tvers av flere avdelinger og grupper. Fraværsledere har følgende funksjoner for permisjonsbehandling:

- Gjennomgå og godkjenne fridager, basert på et alternativt hierarki.
- Vise gruppemedlemsaldoer.
- Vise fraværskalenderen.

## <a name="turn-on-the-feature"></a>Aktivere funksjonen

1. I arbeidsområdet **Systemadministrasjon** velger du **Funksjonsbehandling**.

2. I kategorien **Funksjonsbehandling** aktiverer du funksjonen **(Forhåndsversjon) Fraværsbehandling for å administrere permisjon**.

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

I arbeidsområdet **Ansattselvbetjening** viser fanen **Fraværsbehandling** fraværsinformasjon om de ansatte som er tilordnet til fraværsbehandlingen i permisjonshierarkiet.

I kategorien **Permisjon og fravær** er følgende alternativer tilgjengelige for hver ansatt:

- **Fridager** – Vis saldoer, godkjente fridager og forespørsler om fridager for den valgte ansatte.
- **Permisjonssaldoer** – Vis en liste over saldoene for de ulike permisjonsplanene for den valgte ansatte.

## <a name="approve-time-off-requests"></a>Godkjenne fritidsforespørsler

Fraværsledere kan godkjenne eller avslå fraværsforespørsler for ansatte. De kan også opprette forespørsler på vegne av ansatte etter behov.

> [!IMPORTANT]
> Før fraværsledere kan godkjenne eller avslå forespørsler om fridager, må arbeidsflyten for permisjonsforespørsel være konfigurert til å tilordne arbeidselementer for permisjonsforespørsel til dem for gjennomgang.
>
> 1. På siden **Arbeidsflyter for Human Resources** velger eller oppretter du arbeidsflyten for permisjonsforespørsel.
> 2. Velg alternativet **Tilknytt hierarki**, og velg deretter **Permisjon** i **Hierarkinavn**-feltet.
> 3. Oppdater arbeidsflyten i arbeidsflytdesigneren. Under **Tilordningstype** velger du alternativet **Hierarki**, og deretter velger du **Konfigurerbart hierarki** i kategorien **Hierarkivalg**.
>
> Hvis du vil ha mer informasjon om hvordan du oppretter arbeidsflyten for permisjonsforespørsel, kan du se [Opprette en permisjonsforespørsel](hr-leave-and-absence-workflow.md).

1. I arbeidsområdet **Ansattselvbetjening** velger du kategorien **Fraværsbehandling**.

2. Velg ønsket ansatt i kategorien **Fraværsbehandling**.

3. Velg **Detaljer** og deretter **Fridager**.

4. Finn fritidsforespørselen, og velg **Godkjenning**-alternativet. Du kan deretter velge et alternativ for å godkjenne eller avbryte fritidsforespørselen.

Statusen **Avbryt** angir at forespørselen er avslått. Statusen **Fullført** angir at forespørselen er godkjent.

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
