---
title: Kvalitetsordrer
description: Dette emnet beskriver hvordan du oppretter kvalitetsordrer manuelt eller automatisk, og hvordan du arbeider med dem for å utføre inspeksjoner og registrere testresultater i Microsoft Dynamics 365 Supply Chain Management.
author: yufeihuang
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventQualityOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 69a4a61a599f1279ec7ad68ebb20c7b4b0f37005
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/29/2021
ms.locfileid: "7571863"
---
# <a name="quality-orders"></a>Kvalitetsordrer

[!include [banner](../includes/banner.md)]

Dette emnet beskriver hvordan du oppretter kvalitetsordrer manuelt eller automatisk, og hvordan du arbeider med dem for å utføre inspeksjoner og registrere testresultater i Microsoft Dynamics 365 Supply Chain Management.

## <a name="automatically-created-quality-orders"></a>Automatisk opprettede kvalitetsordrer

Du kan konfigurere systemet slik at det automatisk oppretter kvalitetsordrer basert på vareprøveregler. Hvis du vil ha mer informasjon, kan du se [Vareprøve for kvalitetsstyring](quality-item-sampling.md).

## <a name="manually-create-quality-orders"></a><a name="manual-quality-orders"></a>Opprette kvalitetsordrer manuelt

Hvis du vil opprette en kvalitetsordrer manuelt, følger du disse trinnene.

1. Gå til **Lagerstyring \> Periodiske oppgaver \> Kvalitetsstyring \> Kvalitetsordrer**.
1. Velg **Ny**.
1. I dialogboksen **Kvalitetsordrer**, i **Referansetype**-feltet, velger du lagerreferansen som kvalitetsordren skal knyttes til. Hvis du vil ha en beskrivelse av referansetypene som kan velges, kan du se delen [Referansetyper for kvalitetsordre](#ref-types) senere i dette emnet.

    > [!NOTE]
    > Lager som er knyttet til den valgte referansen, må være tilgjengelig. Hvis lager ikke er tilgjengelig for kombinasjonen av referansetypen, antallet og lagerdimensjonene du velger, får du en feilmelding.

1. Følg ett av disse trinnene, avhengig av verdien du valgte i **Referansetype**-feltet:

    - Hvis du valgte **Lager**, er ingen tilleggsreferanse nødvendig.
    - Hvis du valgte **Salg** eller **Innkjøp**, angir du følgende informasjon:

        - **Kontovalg** – Referanse til kunde- eller leverandørnummeret.
        - **Referansenummer** – Referanse til salgsordren eller bestillingsnummeret.
        - **Referanseparti** – Referanse til den bestemte salgsordrelinjen eller bestillingslinjen.

    - Hvis du valgte **Produksjon**, **Karantene** eller **Koproduktproduksjon** i **Referensenummer**-feltet, refererer du til produksjonsordren, partiordren eller karanteneordrenummeret.
    - Hvis du valgte **Ruteoperasjon**, angir du følgende informasjon:

        - **Referansenummer** – Referanse til produksjonsordren eller partiordrenummeret.
        - **Oper.nr.** – Referanse til det angitte ruteoperasjonsnummeret.
        - **Operasjon** – Referanse til den bestemte ruteoperasjonen.
        - **Ressurs** – Refererer til den bestemte ressursen som må brukes med ruteoperasjonen.

1. Velg testgruppen som må utføres, i **Testgruppe**-feltet.
1. I **Antall**-feltet angir du antall varer som må testes.
1. I **Lagerdimensjoner**-delen angir du eventuelle ekstra lagerdimensjoner som kreves for den valgte varen.
1. Velg **OK**.

Når en kvalitetsordre er opprettet, kan du begynne å kontrollere lageret og registrere testresultatene. Hvis du vil ha mer informasjon om hvordan du registrerer og validerer testresultater, kan du se [Kontrollere varekvaliteten](tasks/inspect-quality-goods.md).

## <a name="quality-order-reference-types"></a><a name="ref-types"></a>Referansetyper for kvalitetsordre

Kvalitetsordrer brukes til å spore detaljene om inspeksjoner og testresultater for en beholdning i lageret. En kvalitetsordre må inneholde en referanse som representerer kilden til beholdningen som testes. Kvalitetsordrer kan være knyttet til følgende referansetyper:

- **Lager** – Denne referansetypen angir at du undersøker lagerbeholdningen. Inspeksjoner av denne typen er vanligvis tilfeldige eller uplanlagte, og utføres når en lagerarbeider finner et problem.
- **Salg** – Denne referansetypen angir at du undersøker lageret som er knyttet til en bestemt salgsordre. Inspeksjoner av denne typen er vanligvis knyttet til kundespesifikasjoner eller generering av et analysesertifikat (CoA) som må leveres til en kunde som del av en forsendelse. (En CoA kalles noen ganger også et samsvarssertifikat \[CoC\].)
- **Innkjøp** – Denne referansetypen angir at du undersøker lageret som er knyttet til en bestilling. Inspeksjoner av denne typen brukes ofte til å kontrollere innkommende varer før de settes på lager eller forbrukes i produksjonsprosesser.
- **Produksjon** – Denne referansetypen angir at du undersøker lageret som er knyttet til en produksjonsordre. Inspeksjoner av denne typen brukes ofte til å kontrollere ferdigvarer før de settes på lager.
- **Karantene** – Denne referansetypen angir at du undersøker lageret som er knyttet til en karanteneordre. Karanteneordrer er en spesiell type ordre som sporer beholdning i et segregert lager eller et segregert område på lageret. Inspeksjoner av denne typen brukes ofte til å kontrollere varer som en kunde har returnert, eller som er satt i karantene for ytterligere analyse. Karanteneordrer kan genereres fra kvalitetsordrer. Alternativt kan de genereres fra andre kilder, og deretter kan kvalitetsordrer være knyttet til karanteneordrene.
- **Ruteoperasjon** – Denne referansetypen angir at du undersøker beholdningen som er knyttet til et bestemt trinn i ruten for en produksjonsordre. Inspeksjoner av denne typen brukes vanligvis til å analysere VIA (varer i arbeid) for et produkt før det går videre til neste trinn i produksjonsprosessen.
- **Koproduktproduksjon** – Denne referansetypen angir at du undersøker lageret som er knyttet til et koprodukt av en produksjonsordre. Inspeksjoner av denne typen brukes vanligvis til å kontrollere koproduktet til en partiordre før koproduktet legges til lager.

## <a name="view-and-create-quality-orders-from-various-parts-of-the-system"></a>Vise og opprette kvalitetsordrer fra forskjellige deler av systemet

Kvalitetsordrer kan opprettes manuelt. Alternativt kan de opprettes automatisk basert på kvalitetstilknytningene du definerer. Hvis du vil ha mer informasjon om hvordan du oppretter og administrerer automatisk oppretting av kvalitetsordrer, kan du se [Kvalitetstilknytninger](quality-associations.md).

Du kan bruke kvalitetsordresiden til å opprette en ny kvalitetsordre manuelt eller vise statusen for en kvalitetsordre som er knyttet til en annen post. Det er flere måter å få tilgang til kvalitetsordresiden på.

### <a name="from-the-quality-orders-page"></a>Fra kvalitetsordresiden

Hvis du vil opprette kvalitetsordrer manuelt og vise alle eksisterende kvalitetsordrer, går du til **Lagerstyring \> Periodiske oppgaver \> Kvalitetsstyring \> Kvalitetsordrer**. De gjenværende delene av dette emnet inneholder mer informasjon om hvordan du arbeider med **Kvalitetsordrer**-siden.

### <a name="from-sales-orders"></a>Fra salgsordrer

Hvis du vil arbeide med kvalitetsordrer som er knyttet til salgsordrene, kan du gå til **Salg og markedsføring \> Salgsordrer \> Alle salgsordrer**, og deretter følger du noen av disse trinnene:

- Åpne en salgsordre, eller velg den i rutenettet. I handlingsruten i kategorien **Plukk og pakk** i **Kvalitetsstyring**-gruppen velger du **Kvalitetsordrer** for å åpne siden **Kvalitetsordrer**. Der kan du vise, opprette eller oppdatere kvalitetsordrer som er knyttet til salgsordren.
- Åpne en salgsordre, og velg deretter hurtigfanen **Generelt** i kategorien **Topptekst**. **Kvalitetsordrestatus**-feltet viser den samlede statusen for alle kvalitetsordrene som er knyttet til salgsordren.
- Åpne en salgsordre, og velg deretter hurtigfanen **Salgsordrelinjer** i kategorien **Linjer**. Kolonnen **Kvalitetsordrestatus** viser statusen for hver linje i salgsordren.

### <a name="from-purchase-orders"></a>Fra bestillinger

Hvis du vil arbeide med kvalitetsordrer som er knyttet til bestillinger, kan du gå til **Innkjøp og leverandører \> Bestillinger \> Alle bestillinger**, og deretter følger du noen av disse trinnene:

- Åpne en bestilling, eller velg den i rutenettet. I handlingsruten i kategorien **Motta** i **Kvalitetsstyring**-gruppen velger du **Kvalitetsordrer** for å åpne siden **Kvalitetsordrer**. Der kan du vise, opprette eller oppdatere kvalitetsordrer som er knyttet til bestillingen.
- Åpne en bestilling, og velg deretter hurtigfanen **Generelt** i kategorien **Topptekst**. **Kvalitetsordrestatus**-feltet viser den samlede statusen for alle kvalitetsordrene som er knyttet til bestillingen.
- Åpne en bestilling, og velg deretter hurtigfanen **Bestillingslinjer** i kategorien **Linjer**. Kolonnen **Kvalitetsordrestatus** viser statusen for hver linje i bestillingen.

### <a name="from-production-orders"></a>Fra produksjonsordrer

Hvis du vil arbeide med kvalitetsordrer som er knyttet til produksjonsordrer, kan du gå til **Produksjonskontroll \> Produksjonsordrer \> Alle produksjonsordrer**, og deretter følger du noen av disse trinnene:

- Åpne en produksjonsordre, eller velg den i rutenettet. I handlingsruten i kategorien **Vis** i **Administrer kvalitet**-gruppen velger du **Kvalitetsordrer** for å åpne siden **Kvalitetsordrer**. Der kan du vise, opprette eller oppdatere kvalitetsordrer som er knyttet til produksjonsordren.
- Åpne en produksjonsordre, eller velg den i rutenettet. Deretter, i handlingsruten i kategorien **Produksjonsordre**, i gruppen **Produksjonsdetaljer**, velger du **Rute** for å åpne **Produksjonsrute**-siden. Følg ett av disse trinnene for å vise kvalitetsordrene som er knyttet til en ruteoperasjon:

    - Velg målruteoperasjonen i rutenettet. I handlingsruten velger du deretter **Forespørsler \> Kvalitetsordrer**.
    - Velg verdien i **Oper. nr.**-feltet for målruteoperasjonen for å åpne **Produksjonsrute**-siden med detaljer. I hurtigfanen **Generelt** viser **Kvalitetsordrestatus**-feltet statusen for kvalitetsordrene som er knyttet til ruteoperasjonen.

- Åpne en produksjonsordre, og velg hurtigfanen **Generelt**. **Kvalitetsordrestatus**-feltet viser den samlede statusen for kvalitetsordrene som er knyttet til produksjonsordren.

### <a name="from-quarantine-orders"></a>Fra karanteneordrer

Hvis du vil arbeide med kvalitetsordrer som er knyttet til karanteneordrer, går du til **Lagerstyring \> Periodiske oppgaver \> Kvalitetsstyring \> Karanteneordrer**, og deretter følger du ett av disse trinnene:

- Gå gjennom verdiene i **Kvalitetsordrestatus**-kolonnen. På denne måten kan du få bedre informasjon om den samlede statusen for alle kvalitetsordrer som er knyttet til hver karanteneordre i rutenett.
- Velg en karanteneordre i rutenettet, og velg deretter **Kvalitetsordrer** i handlingsruten for å vise, opprette eller oppdatere kvalitetsordrer som er knyttet til karanteneordren.

## <a name="advanced-actions-for-quality-orders"></a>Avanserte handlinger for kvalitetsordrer

Du kan utføre flere handlinger for kvalitetsordrer for å styre statusen, generere dokumenter og be om flere detaljer.

### <a name="reopen-a-quality-order"></a>Åpne en kvalitetsordre på nytt

Som standard kan du ikke lenger redigere eller oppdatere en kvalitetsordre etter at den er validert og testene er bestått. I noen tilfeller kan det imidlertid hende at du må åpne en kvalitetsordre på nytt etter at den er fullført.

Hvis du vil åpne en kvalitetsordre på nytt, følger du disse trinnene.

1. Gå til **Lagerstyring \> Periodiske oppgaver \> Kvalitetsstyring \> Kvalitetsordrer**.
1. Åpne den validerte kvalitetsordren, eller velg den i rutenettet.
1. Velg **Åpne kvalitetsordre på nytt** i handlingsruten.

### <a name="create-a-certificate-of-analysis-for-a-quality-order"></a>Opprette et analysesertifikat for en kvalitetsordre

En CoA er en rapport som genereres av en organisasjons kvalitetssikringsteam. Den validerer at et produkt oppfyller bestemte bestemmelser eller krav. Dine kunder eller forskriftsmessige etableringer på stedet der du befinner deg, kan kreve analysesertifikater. De kan også være nødvendige basert på industrien og typen produkter du håndterer, kjøper, produserer eller selger.

Med Supply Chain Management kan du generere en CoA fra en kvalitetsordre. Rapporten inneholder resultatene av eventuelle tester på kvalitetsordren der alternativet **Analysesertifikatrapport** er angitt til *Ja*. Dette alternativet kan angis som standard, basert på testen du definerer på **Tester**-siden. Du kan imidlertid overstyre innstillingen for bestemte tester for en bestemt kvalitetsordre.

Hvis du vil opprette en CoA for en kvalitetsordre, følger du disse trinnene.

1. Gå til **Lagerstyring \> Periodiske oppgaver \> Kvalitetsstyring \> Kvalitetsordrer**.
1. Velg kvalitetsordren du vil opprette en CoA for.
1. Velg **Forespørsler \> Analysesertifikat** i handlingsruten.
1. På siden **Analysesertifikat** i handlingsruten velger du **Ny**.
1. Valgfritt: I **Kontakt**-feltet velger du kontaktpersonen som sertifikatet skal adresseres til.
1. Velg deretter **Skriv ut** i handlingsruten.
1. I dialogboksen **Analysesertifikat** definerer du hvordan rapporten skal skrives ut. Velg deretter **OK** for å skrive ut rapporten til en skriver, på skjermen, til en fil eller til e-post.
1. Lukk sidene.

### <a name="block-or-unblock-inventory-for-a-quality-order"></a>Blokkere eller fjerne blokkering av beholdning for en kvalitetsordre

Når en kvalitetsordre genereres automatisk fra en kvalitettilordning, kan vareprøven som er tilordnet kvalitetstilordningen, konfigureres til å blokkere hele lagerantallet for referansen som testes. Hvis du vil ha mer informasjon om prøvevarer, kan du se [Vareprøve for kvalitetsstyring](quality-item-sampling.md).

Hvis du ikke bruker full blokkering, eller hvis du oppretter en kvalitetsordre manuelt, oppretter systemet automatisk en lagerblokkeringspost for antallet av varen som testes på kvalitetsordren. I posten som opprettes på **Lagerblokkering**-siden, settes feltet **Lagerblokkeringtype** til *Kvalitetsordre*.

Hvis du vil vise og redigere lagerblokkingen for en kvalitetsordre som er valgt på siden **Lagerblokkering**, velger du **Forespørsler \> Lagerblokkering** i handlingsruten. For mer informasjon, se [Lagerblokkering](inventory-blocking.md).

### <a name="inquire-about-the-details-of-a-quality-order"></a>Spør om detaljene i en kvalitetsordre

Bruk følgende knapper i handlingsruten på **Kvalitetsordrer**-siden for å vise mer informasjon om eller relatert til en kvalitetsordre:

- **Forespørsler \> Arbeidsdetaljer** – Åpne en side der du kan vise lagerarbeid som er knyttet til kvalitetsordren.
- **Forespørsler \> Avvik** – Åpne en side der du kan vise eventuelle avvik som er knyttet til kvalitetsordren.
- **Beholdning** – Kommandoene på denne menyen er felles for alle lagertransaksjonene. Du kan bruke dem til å vise eller oppdatere detaljer som transaksjoner, lagerbeholdning, reserveringer og merking.

### <a name="create-cases-related-to-quality-orders"></a>Opprette tilfeller relatert til kvalitetsordrer

Du kan opprette tilfeller som er knyttet til kvalitetsordrer. På denne måten kan du spore detaljer om problemer og arbeide mot en løsning. Du kan deretter bruke arbeidsflytfunksjonene i saksbehandling til å rute en sak gjennom en forhåndsdefinert forretningsprosess for å få flere godkjenninger eller få mer informasjon om et bestemt problem. Du kan også bruke kunnskapsartiklene til å opprette et kunnskapsgrunnlag for løsninger for vanlige spørsmål.

## <a name="case-management-examples-for-quality-management"></a>Saksbehandling-eksempler for kvalitetsstyring

### <a name="example-1"></a>Eksempel 1

Du jobber for et produksjonsfirma som må følge strenge bestemmelser som gjelder produksjon av regulerte produkter, for eksempel mat. Kvalitetsordrer brukes til å registrere og spore detaljer om kvaliteten på varer gjennom produksjonsprosessen. Hvis en kvalitetsordre mislykkes i bestemte tester, kan det være et problem med utstyret. Tilfeller brukes til å følge en forretningsprosess og videresende problemet til de riktige ingeniørene, slik at rotårsaken kan fastslås. For å gjøre det lettere å følge forretningsprosesser har firmaet et kunnskapsgrunnlag for vanlige spørsmål som er knyttet til kvalitetsordrer og utstyrsproblemer.

### <a name="example-2"></a>Eksempel 2

Du jobber for et distribusjonsfirma som leverer produkter som kan tilpasses for forskjellige land og områder. Noen kunder har strenge spesifikasjoner som må følges. Hvis ikke, kan det påløpe gebyrer og returer eller tilbakeføringer. Du bruker kvalitetsordrer til å spore detaljene om hver test og resultater som samsvarer med kundekravene. Tilfeller brukes til å gå gjennom og godkjenne detaljene for analysesertifikatet før dokumentet genereres og knyttes til andre forsendelsespapirer.

## <a name="additional-resources"></a>Tilleggsressurser

- [Kvalitetsstyringsprosesser](quality-management-processes.md)
- [Kvalitetstest](quality-tests.md)
- [Kvalitetstestgrupper](quality-test-groups.md)
- [Kvalitetstilknytninger](quality-associations.md)
- [Kvalitetsstyringsprosesser](quality-management-processes.md)
- [Aktivere kvalitets- og avviksstyring](enable-quality-management.md)
- [Kvalitetsstyring for lagerprosesser](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
