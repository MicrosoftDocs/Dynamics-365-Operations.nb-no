---
title: Vise sider side ved side ved hjelp av funksjonen Åpne i nytt vindu
description: Denne artikkelen forklarer hvordan du viser sider side ved side.
author: aneesmsft
ms.date: 11/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.custom: 17611
ms.assetid: fc589d76-3927-4486-ab83-e86b9b47ba2c
ms.search.region: Global
ms.author: aneesa
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a4c8086d511892f8965dfefca2789742a006f63f
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/31/2022
ms.locfileid: "8068065"
---
# <a name="show-pages-side-by-side-using-the-open-in-new-window-feature"></a>Vise sider side ved side ved hjelp av funksjonen Åpne i nytt vindu

[!include [banner](../includes/banner.md)]


[!INCLUDE [PEAP](../../../includes/peap-1.md)]

Denne artikkelen forklarer hvordan du viser sider side ved side.

Du vil kanskje vise flere sider side ved side for å fullføre en oppgave raskt. Du vil for eksempel kanskje validere eller registrere linjer i flere journaler. For å kunne validere eller registrere linjer i flere journaler, vil du vanligvis måtte gå frem og tilbake mellom siden som viser en liste over journaler, og siden som viser linjer for en bestemt journal. Funksjonen **Åpne i nytt vindu** gjør at du kan vise disse sidene side ved side, slik at du kan gjøre oppgavene raskt.

La oss fortsette med eksemplet ovenfor. Når du viser linjene, kan du klikke ikonet **Åpne i nytt vindu**.

[![Klikk på ikonet for å åpne i nytt vindu.](./media/open-in-new-window-icon.png)](./media/open-in-new-window-icon.png)

Når du klikker ikonet **Åpne i nytt vindu**, åpnes linjesiden i et nytt popup-nettleservindu, og det opprinnelige nettleservinduet navigeres tilbake i historikken til siden der listen over journaler vises. Du kan dermed vise begge sidene side ved side. Etter at du har vist en journal, kan du endre den valgte journalen på journallistesiden, og dermed vises linjene i den nylig valgte journalen automatisk på linjesiden i popup-vinduet.

[![Du kan vise sidene side ved side.](./media/pages-show-side-by-side.png)](./media/pages-show-side-by-side.png)

Den dynamiske koblingen og oppdateringen skjer på grunn av relasjonene mellom dataene som ligger bak disse sidene. Hvis systemet ikke er klar over relasjonen mellom dataene, oppdateres ikke popup-vinduet automatisk som svar på en endring i vinduet det stammer fra.

Noen sider har flere visninger, for eksempel Rutenettvisning, Topptekstvisning og Detaljvisning. Ikonet **Åpne i nytt vindu** gjør at hele siden åpnes i det nye nettleservinduet. Derfor kan du ikke ha to visninger av den samme siden side ved side ved hjelp av funksjonen **Åpne i nytt vindu**. Nesten alle slike sider har en navigasjonsliste du kan bruke til å bytte mellom poster og få en lignende opplevelse.

Før du bruker funksjonen **Åpne i nytt vindu**, konfigurerer du popup-blokkeringen i nettleseren slik at den tillater popup-vinduer fra URL-adressen til området. Du kan for eksempel tillate popup-vinduer fra "\*.dynamics.com".

Funksjonen **Åpne i nytt vindu** er bare tilgjengelig når det er flere sider åpne i vinduet. I tillegg lukkes popup-vinduet automatisk når ingen flere sider er åpne (det vil si når du lukker den siste siden i dette vinduet). Systemet lukker også åpne sider når du går til et annet område i programmet. Hvis du har popup-vinduer åpne og går til et annet område i programmet, lukkes derfor popup-vinduene automatisk fordi systemet lukket sidene i disse vinduene.

Den øverste linjen i popup-vinduene viser informasjon om firmaet siden ble åpnet i, og er skrivebeskyttet. Popup-vinduene er også avhengig av hovednettleservinduet. Hvis hovedvinduet lukkes eller oppdateres, blir alle åpne popup-vinduer skrivebeskyttet. Hvis dette skjer, kan du fortsatt vise informasjonen i disse vinduene, men du kan ikke bruke den.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]