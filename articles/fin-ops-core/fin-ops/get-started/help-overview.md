---
title: Hjelpesystem (inneholder video)
description: Denne artikkelen inneholder en oversikt over hjelpesystemet for økonomi- og driftsapper.
author: edupont04
ms.date: 07/20/2021
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: SystemParameters
audience: Application User, Developer, IT Pro
ms.reviewer: tfehr
ms.custom:
- "16381"
- intro-internal
ms.assetid: 018c148c-9cbd-41e0-8186-d75dbf66288f
ms.search.region: Global
ms.author: edupont
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 57c17cab920c531b3eb125260064d01dd8662576
ms.sourcegitcommit: 873d66c03a51ecb7082e269f30f5f980ccd9307f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/06/2022
ms.locfileid: "9124202"
---
# <a name="help-system"></a>Hjelpesystem

[!include [banner](../includes/banner.md)]


[!INCLUDE [PEAP](../../../includes/peap-1.md)]

Brukere av følgende apper kan få tilgang til kontekstavhengig hjelp og annet innhold som er basert på det samme hjelpesystemet:

- Dynamics 365 Commerce
- Dynamics 365 Finance
- Dynamics 365 Human Resources
- Dynamics 365 Supply Chain Management

I alle disse appene kan du få tilgang til produktspesifikk hjelp fra **Hjelp**-ruten.

![Hjelp-rute.](./media/help-pane-ops-help.png)

## <a name="help-on-docsmicrosoftcom"></a>Hjelp på docs.microsoft.com

Nettstedet docs.microsoft.com ([docs.microsoft.com/dynamics365](/dynamics365/)) er standardkilden for produktdokumentasjon for de tidligere oppførte appene. Dette nettstedet tilbyr følgende funksjoner:

- **Tilgang til det mest oppdaterte innholdet** – Området gir Microsoft en raskere og mer fleksibel måte å opprette, levere og oppdatere produktdokumentasjon på. Derfor har du enkel tilgang til den nyeste tekniske informasjonen.
- **Innhold som er skrevet av eksperter** – Innhold på nettstedet er åpent for bidrag av fellesskapsmedlemmer både i og utenfor Microsoft.

Du kan finne innhold på docs.microsoft.com ved å bruke en hvilken som helst søkemotor. For best mulig resultater anbefaler det å bruke områdesøk, for eksempel **site:docs.microsoft.com dynamics 365 "søketerm"**.

## <a name="get-notified-about-changes-through-an-rss-feed"></a>Få beskjed om endringer ved hjelp av en RSS-feed

Hvis du vil abonnere på en RSS-feed for alle oppdateringer som er gjort på innholdet på docs.microsoft.com i alle økonomi- og driftsapper, bruker du følgende kobling:

[RSS-feed](/api/search/rss?$filter=scopes%2fany(t%3A%20t%20eq%20%27dynamics365-finops%27)&locale=en-us)

> [!NOTE]
> RSS-feeden returnerer en liste over de 100 emnene som sist ble oppdatert. Listen sorteres ikke etter dato.  

Alternativt kan du abonnere på en RSS-feed via app:

- [Commerce](/api/search/rss?$filter=scopes%2fany(t%3A%20t%20eq%20%27dynamics365-commerce%27)&locale=en-us)  
- [Finance](/api/search/rss?$filter=scopes%2fany(t%3A%20t%20eq%20%27dynamics365-finance%27)&locale=en-us)  
- [Human Resources](/api/search/rss?$filter=scopes%2fany(t%3A%20t%20eq%20%27dynamics365-hr%27)&locale=en-us)  
- [Forsyningskjede](/api/search/rss?$filter=scopes%2fany(t%3A%20t%20eq%20%27dynamics365-supplychain%27)&locale=en-us)  
- [Talent](/api/search/rss?$filter=scopes%2fany(t%3A%20t%20eq%20%27dynamics365-talent%27)&locale=en-us)  

### <a name="leave-us-feedback"></a>Send tilbakemelding til oss

Hvis du har tilbakemelding eller spørsmål om en artikkel, legger du igjen en kommentar nederst på siden.

1. Velg **Tilbakemelding** for å vise kommentarene nederst på siden. Deretter velger du **Tilbakemelding for produkt** eller **Logg på for å sende tilbakemelding om dokumentasjon**.

2. Skriv inn kommentarene, og velg deretter **Send tilbakemelding**.

    ![Legg inn kommentar.](./media/feedback.png)

> [!NOTE]
> Hvis du vil sende tilbakemelding fra dokumentasjon, må du logge på ved hjelp av en GitHub-konto. Hvis du vil ha mer informasjon, kan du se [Definere og behandle GitHub-profilen](https://help.github.com/github/setting-up-and-managing-your-github-profile).

## <a name="contribute-to-the-documentation"></a>Bidra til dokumentasjonen

Du kan bidra til og redigere i dokumentasjonen. Begynn med å velge knappen **Rediger** (blyantsymbol) for en artikkel. Følgende video viser hvordan du kan bidra til dokumentasjonen vår.

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE36liB]

Videoen [Bidra til dokumentasjonen for Microsoft Dynamics 365](https://youtu.be/m5djioozRbg) (vist ovenfor) er inkluder i Microsoft Dynamics 365-kanalen på YouTube.

Hvis du vil ha mer informasjon, kan du se [veiledningen for dokumentbidragsyter](/contribute), som er publisert av teamet som laget nettstedet docs.microsoft.com.

> [!NOTE]
> Vi godtar for øyeblikket bare bidrag til vårt engelske innhold.

## <a name="task-guides"></a>Oppgaveveiledninger

En oppgaveveiledning er en kontrollert, veiledet, interaktiv opplevelse som leder deg gjennom trinnene for en aktivitet eller forretningsprosess. Du kan åpne (spille av) en oppgaveveiledning fra **Hjelp**-ruten. Når du først velger en oppgaveveiledning, vil **Hjelp**-ruten vise de trinnvise instruksjonene for oppgaven. Lokaliserte oppgaveveiledninger er tilgjengelige.

Microsoft lanserte biblioteker for oppgaveveiledning for produktversjoner i 2017-versjonen av Dynamics 365 Finance and Operations. Delen [Tilgang til oppgaveveiledninger fra Hjelp-ruten](#accessing-task-guides-from-the-help-pane) i denne artikkelen forklarer hvordan du finner de riktige oppgaveveiledningene for produktet.

![Oppgaveveiledning – lesevisning.](./media/task-guide-ops.png)

Hvis du vil starte den veiledede interaktive opplevelsen, velger du **Start oppgaveveiledning** nederst i **Hjelp**-ruten. En svart peker viser deg hvor du skal gå først. Følg instruksjonene som vises i brukergrensesnittet (UI), og legg inn data i henhold til instruksjonene.

![Oppgaveveiledning – trinnvis instruksjon.](./media/task-guide-step-1-ops.png)

> [!IMPORTANT]
> Dataene som du angir når du spiller av en oppgaveveiledning, er ekte. Hvis du er i et produksjonsmiljø, legges dataene inn i firmaet som du bruker for øyeblikket.

Du kan bruke oppgaveopptakeren til å opprette dine egne egendefinerte oppgaveveiledninger. Hvis du vil ha mer informasjon, se [Lage dokumentasjon eller opplæring med Oppgaveopptaker](../../dev-itpro/user-interface/task-recorder-training-docs.md).

## <a name="in-product-help"></a>Hjelp i produktet

Noen felt har feltbeskrivelser som hjelper brukerne å komme til å bli opphevet når de for eksempel er usikker på dataene som feltet inneholder. I tillegg formidler **Hjelp**-ruten i produktet kontekstsensitiv tilgang til innhold som kan hjelpe brukerne med å komme i gang, få opphevet og finne ut mer.

Hvis du vil ha tilgang til hjelpeinnhold, velger du knappen **Hjelp** (**?**), og deretter velger du **Hjelp**. Du kan også trykke på **Ctrl+Skift+?**. I begge tilfeller vises **Hjelp**-ruten. Fra **Hjelp**-ruten får du tilgang til begrepsmessige emner eller oppgavelinjer som er relevante for området i produktet du befinner deg i for øyeblikket.

![Hjelp-rute.](./media/help-pane-ops-help.png)

### <a name="accessing-help-topics-from-the-help-pane"></a>Tilgang til helpeemner fra Hjelp-ruten

Fra **Hjelp**-ruten har du tilgang til emner som gjelder for klienten. Når du første gang åpner **Hjelp**-ruten, viser fanen **Hjelp** emnene som gjelder for siden du befinner deg på. Hvis ingen emner vises, kan du angi nøkkelord for å presisere søket. Når du velger en artikkel i **Hjelp**-ruten, åpnes den i en ny kategori i leseren.

> [!IMPORTANT]
> Denne delen gjelder ikke for Dynamics 365 Human Resources. Hjelpesystemet for Human Resources kobles automatisk til oppgaveveiledningene for produktet. Du kan heller ikke opprette tilpassede oppgaveveiledninger for Human Resources.

### <a name="accessing-task-guides-from-the-help-pane"></a>Tilgang til oppgaveveiledninger fra Hjelp-ruten

Før du får tilgang til oppgaveveiledninger fra **Hjelp**-ruten, må en systemadministrator konfigurere noen innstillinger på siden **Systemparametere** i Finance, Supply Chain Management elle Commerce. Hvis du vil ha mer informasjon, kan du se [Legge til oppgaveveiledninger](help-connect.md#adding-task-guides).

<!-- > [!NOTE]
> - In order to configure Help, you must be signed in with an account in the same tenant as the tenant in which the app is deployed.
> - It is not possible to connect to an LCS library from an instance of the app running in a local virtual hard drive (VHD).

![System Parameters form with Help settings.](./media/system-parameters_ops-1024x437.png)

On the **System parameters** page, follow these steps:

1. **Important:** The first time that you open the Help tab, you must connect to Lifecycle Services. Be sure to select the link in the middle of the form, wait for the connection, close the dialog box, and then select **OK** to get to the parameters form.

    ![Connect to LCS.](./media/connect-to-lcs-crop-1024x365.png)

2. Select the Lifecycle Services project to connect to.
3. Select BPM libraries (within the selected project) to retrieve task recordings from.
4. Set the display order of the BPM libraries. This setting determines the order in which task recordings from the libraries will appear in the Help pane.-->

Etter at en systemadministrator har fullført disse trinnene, kan du åpne **Hjelp**-ruten og velge fanen **Oppgaveveiledninger**. Du vil nå se oppgaveveiledningene som gjelder for siden du er på for øyeblikket. Hvis det ikke finneds noen oppgaveveiledninger, kan du angi nøkkelord for å presisere søket. Når du velger en oppgaveveiledning i **Hjelp**-ruten, viser **Hjelp**-ruten de trinnvise instruksjonene, og du kan spille av oppgaveveiledningen.

![Oppgaveveiledning – lesevisning.](./media/task-guide-ops.png)

### <a name="where-are-the-translated-task-guides-for-microsoft-libraries"></a>Hvor er de oversatte oppgaveveiledningene for Microsoft-biblioteker?

Oversatte oppgaveveiledninger er utgitt i biblioteker som har "Alle språk" i tittelen. Hvis du vil vise lokalisert hjelp for oppgaveveiledninger, må du sjekke at du er koblet til et egnet biblioteket. Hver bruker kan endre språket som en oppgaveveiledning vises i, ved å endre språkinnstillingene under **Alternativer** &gt; **Innstillinger**.

- Hvis en oppgaveveiledning er oversatt, vil all teksten i oppgaveveiledningen vises på det valgte språket når du åpner oppgaveveiledningen.
- Hvis en oppgaveveiledning ikke er oversatt, vil bare teksten til kontrollene vises på det valgte språket når du åpner oppgaveveiledningen.

## <a name="creating-custom-help"></a>Opprette egendefinert hjelp

Du kan opprette hjelp for brukerne ved å opprette egendefinerte oppgaveveiledninger eller koble ditt eget nettsted til **Hjelp**-ruten. Hvis du vil ha mer informasjon, kan du se følgende emner:

- [Ressurser for Oppgaveregistrering](../../dev-itpro/user-interface/task-recorder.md)
- [Oversikt over tilpasset hjelp](../../dev-itpro/help/custom-help-overview.md)

## <a name="additional-resources"></a>Tilleggsressurser

Følgende tabell viser nettstedene våre. Områder med en stjerne (\*) ved siden av navnet, krever at du logger på med en konto som er knyttet til en serviceplan.

| Site | beskrivelse |
|------|-------------|
| [Docs.microsoft.com](/dynamics365/) | Dette nettstedet drifter eller kobler til all produktdokumentasjon for Dynamics 365. |
| [Microsoft Learn](/learn/) | Dette området er et gratis Microsoft eLearning-område. |
| [Microsoft DynamicsLifecycle Services (LCS)](https://lcs.dynamics.com/)\* | Dette området er et skybasert samarbeidsområde som kunder og partnere kan bruke til å administrere prosjekter fra før salg til implementering og operasjoner. Det er nyttig i alle fasene ved implementering. |
| [Kundestøtteblogg](https://aka.ms/AXSupportBlog) | Dette området gir tips som posteres av kundestøtteteamet. |
| [Docs.microsoft.com/tidligere versjoner](/previous-versions/dynamics/) | Dette området har innhold fra tidligere versjoner. |
| [Dynamics-fellesskap](https://community.dynamics.com/) | Dette området har blogger, forum og videoer. |
| [Microsoft.com/dynamics365](https://www.microsoft.com/dynamics365/home) | Dette området formidler informasjon om evaluering og salg. |




[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

