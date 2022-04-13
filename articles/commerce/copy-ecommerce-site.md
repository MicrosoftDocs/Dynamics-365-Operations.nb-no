---
title: Kopiere et e-handelsområde
description: Dette emnet beskriver hvordan du kopierer et eksisterende e-handelsområde i eller mellom e-handelsmiljøer i Microsoft Dynamics 365 Commerce-områdebyggeren.
author: psimolin
ms.date: 03/03/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: a23f544cbd1e960cb704d2b9666b7db4c3894b5e
ms.sourcegitcommit: c0f7ee7f8837fec881e97b2a3f12e7f63cf96882
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/22/2022
ms.locfileid: "8462332"
---
# <a name="copy-an-e-commerce-site"></a>Kopiere et e-handelsområde

[!include [banner](../includes/banner.md)]

Dette emnet beskriver hvordan du kopierer et eksisterende e-handelsområde i eller mellom e-handelsmiljøer i Microsoft Dynamics 365 Commerce-områdebyggeren.

Dynamics 365 Commerce støtter kopiering eller kloning av områder som en selvbetjent operasjon i Commerce-områdebyggeren. Områder kan kopieres innenfor ett e-handelsmiljø eller mellom to e-handelsmiljøer. Brukeren som starter kopieringen av området, må være en leieradministrator i både kilde- og målmiljøet for e-handel.

Når området kopieres, blir alt e-handelsinnholdet på kildeområdet kopiert. Dette innholdet omfatter sider, fragmenter, maler, nettadresser og aktiva. Før et nytt område kan brukes, må det initialiseres via prosessen for opplevelse ved førstegangskjøring. Kanaler kan tilordnes og administreres i områdebyggeren i **Områdeinnstillinger \> Kanaler**.

Hvor lang tid kopieringen tar, avhenger hovedsakelig av antallet aktiva på kildeområdet. Når det gjelder uvanlig store områder, anbefaler vi at du i stedet vurderer å bruke miljøkopiering. (Denne operasjonen kan også kalles dataoverførbarhetsoperasjon).

> [!NOTE]
> - Kildeområdet er skrivebeskyttet mens områdekopieringen utføres.
> - Bare publiserte versjoner av dokumenter blir kopiert. Hvis ingen versjoner er publisert, blir bare de siste versjonene kopiert.
> - Versjonshistorikk for innhold blir ikke tilgjengelig på målområdet.

## <a name="copy-a-site-within-an-e-commerce-environment"></a>Kopiere et område innenfor et e-handelsmiljø

Følg denne fremgangsmåten hvis du vil kopiere et område innenfor et e-handelsmiljø.

1. Logg deg på områdebyggeren for miljøet der du vil foreta kopieringen.
1. Åpne områdelistevisningen ved å velge **Områdeveksling** øverst til høyre, og velg deretter **Administrer områder**.
1. Finn området du vil kopiere eller klone, og velg det ved å merke av for navnet på området.
1. Velg **Kopier område** i handlingsruten.
1. I dialogboksen **Kopier område** skriver du inn et navn for det nye området i feltet **Navn på nytt område**. Navnet på det nye området må være unikt i e-handelsmiljøet. Feltene **Kildeleier** og **Kildeområde** settes automatisk til informasjonen for gjeldende leier og valgt område.
1. Velg **Opprett kopi**.

Etter at informasjonen er validert, angir en melding at det er opprettet en kopieringsjobb for nytt område. Du kan overvåke fremdriften til jobben i [høyre rute på siden **Leierjobber**](#monitor-the-site-copy-operation). Når kopieringen er fullført, vises det nye området i listen over områder i områdelistevisning.

Følgende illustrasjon viser et eksempel på dialogboksen **Kopier område** i områdebyggeren.

![Dialogboksen Kopier område i områdebyggeren.](media/site-copy_1.png)

## <a name="copy-a-site-between-two-e-commerce-environments"></a>Kopiere et område mellom to e-handelsmiljøer

Følg denne fremgangsmåten hvis du vil kopiere et område mellom to e-handelsmiljøer.

1. Logg deg på områdebyggeren for målmiljøet for e-handel.
1. Velg **Kopier område** i handlingsruten.
1. I dialogboksen **Kopier område** skriver du inn et navn for det nye området i feltet **Navn på nytt område**. Navnet på det nye området må være unikt i e-handelsmiljøet.
1. Velg navnet på kildeleieren i feltet **Kildeleier**.
1. Velg kildeområdet i feltet **Kildeområde**.
1. Velg **Opprett kopi**.

> [!NOTE]
> Du må ha leieradministratortillatelser for både kilde- og målmiljøet for e-handel.

Etter at informasjonen er validert, angir en melding at det er opprettet en kopieringsjobb for nytt område. Du kan overvåke fremdriften til jobben i [høyre rute på siden **Leierjobber**](#monitor-the-site-copy-operation). Når kopieringen er fullført, vises det nye området i listen over områder i områdelistevisning.

## <a name="monitor-the-site-copy-operation"></a>Overvåke kopieringen av området

Følg denne fremgangsmåten hvis du vil overvåke fremdriften til kopieringen av området.

1. Logg deg på områdebyggeren for målmiljøet for e-handel.
1. Velg **Leierjobber** i venstre rute.
1. På siden **Leierjobber** finner og velger du områdekopieringsjobben i listen. Det vises en rute til høyre, der statusen og detaljene for den valgte jobben vises.

Du kan avbryte en jobb med statusen **Pågår**. Velg jobben i listen, og velg deretter **Avbryt** i handlingsruten.

Hvis en jobb har statusen **Mislykket** eller **Fullført med feil**, kan du prøve den på nytt. Velg jobben i listen, og velg deretter **Prøv på nytt** i handlingsruten.

> [!NOTE]
> Behandling av videoaktiva kan fortsette etter at en områdekopieringsjobb er fullført.

Den følgende illustrasjonen viser et eksempel på den høyre ruten på siden **Leierjobber** i områdebyggeren.

![Jobbdetaljer i høyre rute på siden Leierjobber i områdebyggeren.](media/site-copy_2.png)

## <a name="initialize-a-new-site-by-using-the-fre-process"></a>Initialisere et nytt område ved hjelp av prosessen for opplevelse ved førstegangskjøring

Før det nye området kan brukes, må det initialiseres via prosessen for opplevelse ved førstegangskjøring.

Følg denne fremgangsmåten for å initialisere et nytt område ved hjelp av prosessen for opplevelse ved førstegangskjøring.

1. Logg deg på områdebyggeren for det nye området.
1. Åpne områdelistevisningen ved å velge **Områdeveksling** øverst til høyre, og velg deretter **Administrer områder**.
1. Finn og velg det nye området du vil initialisere.
1. Velg et domene i feltet **Velg et domene** i dialogboksen **Konfigurer område**. Alle domener som ble knyttet til e-handelsmiljøet under initialisering, kan velges.
1. Velg den tilknyttede kanalen for nettbutikk i feltet **Velg en standardkanal**. Den valgte kanalen gir sortimenter og annen informasjon som er lagret i Commerce Headquarters.
1. Velg standard redigeringsspråk i feltet **Velg et standardspråk**. Alle språkene som ble konfigurert for den valgte kanalen for nettbutikk, er tilgjengelige for valg.
1. I **Bane**-feltet består verdien av basisdomenet og en valgfri nettadressebane du kan angi. Du kan la nettadressebanen stå tom hvis kanalen blir betjent fra domeneroten, eller hvis du vil angi denne informasjonen senere i kanalkonfigurasjonsvisningen i områdebyggeren. Områdebanen må være unik i e-handelsmiljøet.
1. Velg **OK**. Området initialiseres med informasjonen du oppgav, og du blir sendt til visningen for områdeadministrasjon.

Følgende illustrasjon viser et eksempel på dialogboksen **Konfigurer område** i områdebyggeren.

![Dialogboksen Konfigurer område i områdebyggeren.](media/site-copy_3.png)

## <a name="additional-resources"></a>Tilleggsressurser

[Konfigurere domenenavnet](configure-your-domain-name.md)

[Distribuere en ny e-handelsleier](deploy-ecommerce-site.md)

[Knytte et Dynamics 365 Commerce-nettsted til en nettkanal](associate-site-online-store.md)

[Administrere robots.txt-filer](manage-robots-txt-files.md)

[Laste opp masseomdirigeringer for URL-adresse](upload-bulk-redirects.md)

[Konfigurere en B2C-leier i Commerce](set-up-b2c-tenant.md)

[Definere egendefinerte sider for brukerpålogginger](custom-pages-user-logins.md)

[Konfigurere flere B2C-leiere i et Commerce-miljø](configure-multi-b2c-tenants.md)

[Legge til støtte for et innholdsleveringsnettverk (CDN)](add-cdn-support.md)

[Aktivere stedsbasert butikkregistrering](enable-store-detection.md)
