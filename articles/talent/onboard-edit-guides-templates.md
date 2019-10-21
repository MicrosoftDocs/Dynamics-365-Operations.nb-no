---
title: Redigere veiledninger og maler for jobbintroduksjon i Dynamics 365 Talent – Onboard
description: Dette emnet forklarer hvordan du legger til aktiviteter og annen informasjon i veiledninger og maler for jobbintroduksjon i Microsoft Dynamics 365 Talent – Onboard.
author: andreabichsel
manager: ''
ms.date: 06/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: HcmCourseType, HcmCourseTypeGroup, HRMCourseTable
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-06-19
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 7803c7cd2c58b8544d2c8dd711c295d6882f9fca
ms.sourcegitcommit: 434dd21450bddcd891aba0555b9853d9ba0afb6f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/23/2019
ms.locfileid: "2010804"
---
# <a name="edit-onboarding-guides-and-templates"></a>Redigere veiledninger og maler for jobbintroduksjon

[!include [banner](includes/banner.md)]

Når du har opprettet en veiledning eller mal for jobbintroduksjon i Microsoft Dynamics 365 Talent: Onboard, må du legge til en innledning, aktiviteter, kontakter og ressurser. I Onboard kan du ta med rikt innhold i jobbintroduksjonsveiledningene, inkludert:

- YouTube-videoer
- Microsoft Sway-presentasjoner
- Microsoft PowerApps-apper
- Microsoft Stream-videoer
- Microsoft Forms-skjemaer
- Iframe som inneholder webinnhold

## <a name="edit-introductions-or-activities-imported-from-a-template"></a>Redigere introduksjoner eller aktiviteter som er importert fra en mal

Hvis du oppretter en jobbintroduksjonsveiledning fra en mal, eller hvis du importerer aktiviteter fra én mal til en annen, vil du se en **låseknapp** på de importerte aktivitetene. Disse kalles *administrerte aktiviteter*.

[![Administrerte aktiviteter](./media/onboard-edit-guide-managed-activities.png)](./media/onboard-edit-guide-managed-activities.png)

Når du velger en administrert aktivitet, kan du se kildemalen øverst i aktiviteten.

[![Kilde for administrert aktivitet](./media/onboard-edit-guide-managed-activity-source.png)](./media/onboard-edit-guide-managed-activity-source.png)

Hvis du redigerer en aktivitet i en mal, vil Onboard overføre endringene til alle maler og usendte veiledninger som er basert på denne malen. Hvis du velger en usendt veiledning basert på en mal du har redigert, og velger deretter **Aktiviteter**-kategorien i veiledningen, vil du se en melding om at veiledningen er endret. Velg **OK** for å forkaste varselet. 

[![Endringsvarsel](./media/onboard-edit-guide-change-notification.png)](./media/onboard-edit-guide-change-notification.png)

Du ser en svart prikk ved siden av de oppdaterte aktivitetene.

[![Endret aktivitet](./media/onboard-edit-guide-changed-activity.png)](./media/onboard-edit-guide-changed-activity.png)

Du kan ikke redigere administrerte aktiviteter utenfor den opprinnelige malen, bortsett fra å legge til en tilordnet person, forfallsdato eller annen informasjon i den høyre delen av aktiviteten.

Hvis du vil redigere en administrert aktivitet, eller hvis du ikke vil at en aktivitet skal motta oppdateringer fra malen den kom fra, velger du **Lås**-knappen for denne aktiviteten. **Lås**-knappen vil forsvinne. Aktiviteten blir ikke lenger administrert av den opprinnelige malen, og den vil ikke lenger motta oppdateringer fra denne malen. Oppdateringer du gjør i en aktivitet, påvirker ikke den opprinnelige malen.

Hvis du sletter en aktivitet fra en veiledning og overfører endringer fra malen for denne veiledningen, vil aktiviteten forbli slettet i veiledningen.

> [!NOTE]
> Kontakter og ressurser administreres ikke av maler. I tillegg administreres ikke inndelinger, så hvis du legger til eller redigerer en inndeling i en mal, blir ikke endringene overført til noen veiledninger eller maler som bruker denne malen.
> 
> Hvis du legger til nye aktiviteter i en mal, overføres de nye aktivitetene til veiledninger og maler basert på denne malen, og de nye aktivitetene vises øverst.

## <a name="import-activities-from-another-template"></a>Importere aktiviteter fra en annen mal

Du kan importere aktiviteter fra én eller flere maler til en veiledning eller mal.

1. Velg veiledningen eller malen du vil redigere.

2. Velg fanen **Aktiviteter**.

3. Velg kategorien **Importer** i delen til høyre.

   [![Importere aktiviteter](./media/onboard-edit-guide-import-activities.png)](./media/onboard-edit-guide-import-activities.png)

4. Hvis du vil forhåndsvise oppgavene i en ny fane i nettleseren, velger du knappen **Åpne i en ny kategori** i en mal.

   [![Importere aktiviteter](./media/onboard-edit-guide-preview-activities.png)](./media/onboard-edit-guide-preview-activities.png)

5. Dra og slipp den ønskede malen på stedet i veiledningsmalen der du vil at aktivitetene skal vises. Fortsett å redigere veiledningen eller malen.

De importerte aktivitetene vil inneholde en **låseknapp**, som angir at disse aktivitetene administreres av malen du importerte fra. Når du gjør endringer i malen du importerte, oppdateres disse aktivitetene i malen du importerte dem til. Endringene vil imidlertid ikke bli overført automatisk til veiledninger som er opprettet fra malen du importerte til.

## <a name="push-changes-from-a-template-to-other-templates-or-guides"></a>Overføre endringer fra en mal til andre maler eller veiledninger

Hvis du redigerer en mal som inneholder aktiviteter som brukes i andre maler eller veiledninger, må du overføre endringene hvis du vil at de skal vises i de andre malene eller veiledningene.

Hvis du ikke er sikker på om malens aktiviteter brukes i andre maler eller veiledninger, velger du **Brukt i**-kategorien for å vise hvor disse aktivitetene vises.

   [![Vise hvor aktiviteter for veiledninger og maler brukes](./media/onboard-edit-guide-view-used-in.png)](./media/onboard-edit-guide-view-used-in.png)

Slik overfører du endringene:

1. Lagre endringene ved å velge **Lagre**-knappen. Hvis du ikke gjør dette, blir du bedt om å lagre endringene i neste trinn.

2. Velg **Overfør disse endringene**.

   
## <a name="add-or-edit-an-introduction"></a>Legge til eller redigere en innledning

1. I kategorien **Innledning** skriver du inn en tittel for veiledningen og en innledningsmelding. Hvis du vil bruke eksempelteksten, velger du **Bruk denne meldingen**.

    [![Innledning-fanen i en Onboard-mal](./media/onboard-template-introduction.png)](./media/onboard-template-introduction.png)

2. Bruk formateringsknappene til å fremheve tekst etter behov, eller for å legge til bilder eller koblinger.
3. Velg **Lagre** for å lagre arbeidet.

## <a name="add-or-edit-activities"></a>Legge til eller redigere aktiviteter

1. Dra elementer fra høyre til redigeringsområdet i kategorien **Aktiviteter**.
2. Hvis du vil organisere veiledningen i inndelinger, drar du **Ny seksjon**-elementet til redigeringsområdet og skriver inn et navn og en valgfri beskrivelse for inndelingen.

    ![[Legge til en ny inndeling i en veiledning eller mal for jobbintroduksjon](./media/onboard-edit-add-section.png)](./media/onboard-edit-add-section.png)

3. Hvis du vil legge til aktiviteter som den nyansatte skal fullføre, drar du elementet **Ny aktivitet** til redigeringsområdet og skriver inn et navn og en beskrivelse for aktiviteten.

    ![[Legge til en ny aktivitet i en veiledning eller mal for jobbintroduksjon](./media/onboard-edit-add-activity.png)](./media/onboard-edit-add-activity.png)

4. Legge til rikt innhold i veiledningen for jobbintroduksjon:

    - Hvis du vil legge til en YouTube-video, drar du **YouTube**-elementet til redigeringsområdet, skriver inn et navn og en beskrivelse for aktiviteten, og skriver inn URL-adressen for YouTube-videoen.
    - Hvis du vil legge til en Sway-presentasjon eller et nyhetsbrev, drar du **Sway**-elementet til redigeringsområdet, skriver inn et navn og en beskrivelse for aktiviteten og skriver inn den innebygde URL-adressen for Sway-presentasjonen eller -nyhetsbrevet.
    - Hvis du vil legge til en PowerApps-app, drar du **PowerApps**-elementet til redigeringsområdet, skriver inn et navn og en beskrivelse for aktiviteten og velger PowerApps-appen eller angir ID-en for PowerApps-appen.
    - Hvis du vil legge til en Microsoft Stream-video, drar du **Microsoft Stream**-elementet til redigeringsområdet, skriver inn et navn og en beskrivelse for aktiviteten, og skriver inn URL-adressen for Microsoft Stream-videoen.
    - Hvis du vil legge til et Microsoft Forms-skjema, drar du **Microsoft Forms**-elementet til redigeringsområdet, skriver inn et navn og en beskrivelse for aktiviteten, skriver inn URL-adressen for Microsoft Forms-skjemaet og angir størrelsen på skjermområdet.
    - Hvis du vil legge til en iframe som inneholder webinnhold, drar du **Webinnhold (iframe)**-elementet til redigeringsområdet, skriver inn et navn og en beskrivelse for aktiviteten, skriver inn URL-adressen for webinnholdet og angir størrelsen på skjermområdet.

    ![[Legge til rikt innhold i en veiledning eller mal for jobbintroduksjon](./media/onboard-edit-add-rich-content.png)](./media/onboard-edit-add-rich-content.png)

2. Valgfritt: I området til høyre for hver aktivitet tilordner du aktiviteten til en bestemt person eller rolle, legger til en forfallsdato og kontaktperson og tilordner en kategorifarge. Når du tilordner en aktivitet til en person eller rolle, opprettes en oppgave for hver enkelt. Denne oppgaven vises på **Oppgaver**-menyen i Onboard.

    [![Tilordne en aktivitet i en veiledning eller mal for jobbintroduksjon](./media/onboard-assign-activity.png)](./media/onboard-assign-activity.png)

3. Velg **Lagre** for å lagre arbeidet.

Hvis du vil slette en aktivitet eller en inndeling, velger du **Slett**-knappen (papirkurvsymbolet) øverst i høyre hjørne av aktiviteten eller inndelingen.

Hvis du vil omorganisere aktiviteter og inndelinger, drar du dem til en ny plassering.

## <a name="add-or-edit-contacts"></a>Legge til eller redigere kontakter

Du kan legge til kontaktpersoner som kan hjelpe den nyansatte med å lykkes fra dag én. Disse kontaktene kan være rekrutterere, teammedlemmer, jobbintroduksjonskontakter, mentorer, administratorer og IT-støttepersonale.

1. Velg **Ny kontakt** i fanen **Kontakter**.
2. Skriv inn kontaktpersonens navn eller e-postadresse i dialogboksen **Legg til teammedlem,** skriv inn en kort beskrivelse som forklarer hvordan kontaktpersonen kan hjelpe den nyansatte, og velg deretter **Legg til** . 

    ![[Legge til kontakter i en veiledning eller mal for jobbintroduksjon](./media/onboard-edit-add-contact.png)](./media/onboard-edit-add-contact.png)

    Du kan eventuelt velge én eller flere kontakter under **Forslag**.

3. Velg **Lagre** for å lagre arbeidet.

Hvis du vil slette en kontakt, velger du **Slett**-knappen (papirkurvsymbolet) til høyre for kontakten.

Hvis du vil redigere en kontakt, velger du **Rediger**-knappen (blyantsymbolet) til høyre for kontakten.

## <a name="add-or-edit-resources"></a>Legge til eller redigere ressurser

Du kan legge til nyttige filer, kart og koblinger i **Ressurser**-delen i jobbintroduksjonsveiledningen.

1. Velg **Ny ressurs** i fanen **Ressurser**.
2. Følg ett av disse trinnene:

    - Hvis du vil legge til en fil, velger du kategorien **Fil** og drar filen til det angitte området. (Du kan også klikke hvor som helst i området for å søke etter filen på datamaskinen, eller velge **Bla gjennom OneDrive**.) Skriv inn et navn på filen, og velg deretter **Legg til**.
    - Hvis du vil legge til en kobling , velger du kategorien **Kobling**, skriver inn et navn og en adresse for koblingen og velger deretter **Legg til**.
    - Hvis du vil legge til et kart , velger du kategorien **Kart**, skriver inn et navn og en adresse for kartet og velger deretter **Legg til**. Onboard vil ta med et kart over adressen du angir.

    ![[Legge til en ressurs i en veiledning eller mal for jobbintroduksjon](./media/onboard-edit-add-resource.png)](./media/onboard-edit-add-resource.png)

3. Velg **Lagre** for å lagre arbeidet.

Hvis du vil slette en ressurs, velger du **Slett**-knappen (papirkurvsymbolet) til høyre for ressursen.

Hvis du vil redigere en kontakt, velger du **Rediger**-knappen (blyantsymbolet) til høyre for ressursen.

## <a name="next-steps"></a>Neste trinn

- [Dele innhold med andre bidragsytere](./onboard-share-template.md)
- [Vise statusen for oppgaver og jobbintroduksjonsmedarbeidere](./onboard-view-status.md)
- [Opprette ansettelsesteam i Onboard](./onboard-create-team.md)

### <a name="see-also"></a>Se også

- [Prøve eller kjøpe Onboard-appen](https://dynamics.microsoft.com/talent/onboard/)
- [Hva er nytt](./whats-new.md)
- [Produktmerknader](https://docs.microsoft.com/business-applications-release-notes/index)
- [Få kundestøtte](./talent-support.md)
