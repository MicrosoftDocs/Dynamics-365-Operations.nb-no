---
title: Registrere mottaket av returnerte varer
description: Du kan registrere at returnerte varer er ankommet, ved å bruke Ankomstoversikt-skjemaet eller Registrering-skjemaet.
author: sorenva
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WMSArrivalOverview, InventTransRegister
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f4942e455350844ac5614e70fef21b37461540a6
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/15/2022
ms.locfileid: "9017296"
---
# <a name="register-the-receipt-of-returned-items"></a>Registrere mottaket av returnerte varer 

[!include [banner](../includes/banner.md)]


Det er to metoder for å registrere mottak av returnerte varer. Den første metoden er en lagermottaksprosess som bruker **Ankomstoversikt**-skjemaet. Den andre bruker **Registrering**-skjemaet.

## <a name="register-the-receipt-of-returned-items-in-the-arrival-overview-form"></a>Registrere mottaket av returnerte varer i Ankomstoversikt-skjemaet.

Du kan bruke **Ankomstoversikt**-skjemaet for å identifisere en returforsendelse ved hjelp av autorisasjonsreturnummeret. Hvis det er angitt et journalnavn i fanen **Oppsett** og det finnes journallinjer som samsvarer med de valgte linjene i **Ankomstoversikt**-skjemaet, blir det opprettete et nytt journalhode når du klikker **Start ankomst**.

1.  Klikk på **Lagerstyring** \> **Periodisk** \> **Ankomstoversikt**.

2.  I feltet **Oppsettsnavn** velger du **Returordre** og klikker deretter **Oppdater**.
    

    > [!TIP]
    > <P>Du kan bruke <STRONG>Område</STRONG>-feltene til å begrense søkeresultatene. Du kan skrive eller velge autorisasjonsreturnummeret i feltet <STRONG>Autorisasjonsreturnummer</STRONG> for å få et nøyaktig resultat. Hvis du vil definere og lagre et sett med filtre som vil begrense hvilke innkommende ankomster som vises, klikker du <STRONG>Oppsett</STRONG>-fanen. Tilgjengelige filtre omfatter typer, lagre og utleveringsporter.</P>

    

    > [!WARNING]
    > <P>Returordre kan ikke blandes med andre ankomsttyper i <STRONG>Ankomstoversikt</STRONG>-skjemaet. Referansen vil derfor alltid være salgsordre, men ingen salgsordre-ID vil være angitt i journalhodet.</P>



3.  I **Mottak**-rutenettet finner du linjen som samsvarer med varen som returneres, og deretter merker du av for avmerkingsboksen i kolonnen **Velg for ankomst**.

4.  Hvis du vil ekskludere visse linjer fra returmottaket, som for eksempel varer fra den opprinnelige ordren som ikke var inkludert i returforsendelsen, kan du fjerne merket i de tilknyttede **Velg for ankomst**-boksene i **Linjer**-tabellen i nederste del av skjemaet.

5.  Klikk på **Start ankomst** for å opprette en ankomstjournal.
    

    > [!NOTE]
    > <P>Du kan velge flere returordrer og inkludere dem i en enkelt ankomstprosess. Hver returordrelinje kopieres til en tilhørende vareankomstjournallinje.</P>

    

    > [!NOTE]
    > <P>Du kan også opprette en ankomstjournal manuelt ved hjelp av <STRONG>Vareankomst</STRONG>-skjemaet. 



6.  Klikk på **Lagerstyring** \> **Journaler** \> **Vareankomst** \> **Vareankomst**.

7.  Velg ankomstjournalen du akkurat opprettet, og klikk deretter **Linjer** for å åpne skjemaet **Journallinjer, lokasjoner**.

8.  I fanen **Generelt** justerer du nummeret i **Antall**-feltet ved behov, og deretter tilordner du en disposisjonskode i **Disposisjonskode**-feltet.
    
    Du kan også merke av for **Karantenestyring** for å sende de returnerte varene gjennom en inspeksjonsprosess i forbindelse med en karanteneordre.
    

    > [!NOTE]
    > <P>Hvis du sender de returnerte varene gjennom karantene, kan du ikke angi en disposisjonskode.</P>



9.  Klikk på **Valider**-knappen.

10. Hvis det ikke er noen feil i valideringsprosessen, klikker du **Poster**.

## <a name="register-the-receipt-of-returned-items-in-the-registration-form"></a>Registrere mottaket av returnerte varer i registreringsskjemaet.

I stedet for å bruke **Ankomstoversikt**-skjemaet kan du bruke **Registrering**-skjemaet til å registrere at returnerte varer er ankommet.

1.  Klikk på **Salg og markedsføring** \> **Salgsreturer** \> **Alle returordrer**. Opprett en ny returordre eller åpne returordren fra listen. Velg returordrelinjen i hurtigfanen **Linjer**. Klikk på **Oppdater linje**, og klikk deretter **Registrering**.

2.  Tilordne en disposisjonskode i **Disposisjonskode**-feltet, og klikk deretter **OK**.
    

    > [!NOTE]
    > <P>Det er ikke mulig å sende varen til inspeksjon som en karanteneordre ved hjelp av <STRONG>Registrering</STRONG>-skjemaet.</P>



3.  I **Transaksjoner**-rutenettet velger du transaksjonen som skal registreres.

4.  I **Registrer nå**-rutenettet klikker du **Legg til**. Gjenta de to forrige trinnene til alle returnerte varer vises i **Registrer nå**-rutenettet.

5.  Klikk på **Poster alle**.

## <a name="see-also"></a>Se også

[Ankomstoversikt (skjema)](https://technet.microsoft.com/library/hh227654\(v=ax.60\))

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]