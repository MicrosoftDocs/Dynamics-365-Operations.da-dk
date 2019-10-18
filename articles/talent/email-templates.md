---
title: Mailskabeloner
description: Dette emne indeholder oplysninger om de mailskabeloner, du kan oprette og bruge i Microsoft Dynamics 365 Talent - Attract.
author: andreabichsel
manager: AnnBe
ms.date: 10/19/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: 7174fd96e5ddc9ba5a91eb423d08afd1daa45f48
ms.sourcegitcommit: 434dd21450bddcd891aba0555b9853d9ba0afb6f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/23/2019
ms.locfileid: "2008030"
---
# <a name="email-templates"></a>Mailskabeloner
[!include[banner](../includes/banner.md)]

Ved hjælp af mailskabelonbiblioteket kan administratorer oprette et ensartet tema og branding til alle mails, der sendes via Microsoft Dynamics 365 Talent: Attract og Tilbud. Administratorer kan også organisere en samling mailskabeloner, som andre brugere kan bruge. Ansættelsesteamet kan bruge disse skabeloner i deres arbejdsproces til at sende mails mere effektivt. Nogle mails er konfigureret til at blive sendt automatisk, og administratoren kan bruge biblioteket med mailskabeloner til at tilpasse indholdet for disse mails.

> [!NOTE]
> Hvis du vil bruge e-mailskabeloner, skal din organisation have tilføjelsesprogrammet til omfattende ansættelser.

## <a name="global-template-configurations"></a>Globale skabelonkonfigurationer

Hvis du vil oprette en ensartet branding til al mailkommunikation, skal administratoren først angive det globale sidehoved og den globale sidefod til alle mailskabeloner. I administration under fanen **Mailskabelonindstillinger** i afsnittet **Sidehoved** kan administratoren overføre et billede, der kan bruges som sidehoved eller banner i alle mails. Billedet kan være et firmalogo, et brevhoved eller andre repræsentative billeder. Det anbefales, at bredden er mellem 25 og 800 pixel, og at højden er mellem 25 og 150 pixel, fordi disse dimensioner er velegnet til de fleste mailklienter, f.eks. Microsoft Outlook. Billedet skal være en JPEG-, JPG-, PNG- eller SVG-fil, og filens størrelse skal være mindre end 1 megabyte (MB). Når et billede er overført, oprettes og vises sidehovedet som eksempel. Hvis billedet af sidehovedet skal fjernes eller erstattes, kan administratoren bruge indstillingen **Fjern** ovenfor eksemplet.

I afsnittet **Sidefod** kan administratoren angive links til firmaets politik for beskyttelse af personlige oplysninger for kommunikation og til vilkår og betingelser. Disse links er indbygget i en sidefod, der genereres automatisk. Derefter vises et eksempel på denne sidefod. Administratoren kan også vælge et bestemt sprog, som mailsidefødder skal sendes på som en del af alle mails. Den samme sprogkonfiguration vil også blive brugt til sammensætning af tabellen med samtaleoversigten. 

Sørg for at gemme ændringerne, før du lukker administration.

> [!NOTE] 
> Sidehovedet og sidefoden er globale indstillinger for alle mails. Derfor vises de i alle mails, der sendes via Attract. Hvis indstillingerne ikke er konfigureret, bliver sidehoved og sidefod udeladt af alle mails.

## <a name="email-template-library"></a>Mailskabelonbibliotek 

Når du har oprettet de globale skabelonkonfigurationer, kan administratoren begynde at oprette og organisere skabeloner til alle mails, der sendes fra Attract og Tilbud. Mailskabelonbiblioteket er kun tilgængeligt for administratorer. For at åbne biblioteket skal du i hovednavigationsmenuen vælge fanen **Mailskabeloner**. Biblioteket er inddelt efter de forskellige aktiviteter i Attract, der skal sendes mails for, f.eks. planlægning, vurdering, joboprettelse og tilbud. Administratoren kan vælge en kategori for at få vist alle de mailtyper, der er tilknyttet aktiviteten. Vælg f.eks. **Planlægning** for at få vist de forskellige typer af mail, der sendes under planlægningsprocessen, og alle de skabeloner, der er tilgængelige for hver type mail. Hver underafdeling i en kategori repræsenterer en mailtype.

Nogle mailtyper kan have mere end én modtager. I f.eks. kategorien **Planlægning** sendes de mails, der sendes, når oversigten over samtaletidsplanen er påkrævet, til både kandidater og interviewere. De enkelte afsnit indeholder to primære kolonner: **Skabelontitel** og **Modtager**. Hver række i et afsnit repræsenterer en enkelt skabelon for en mailtype. Der vises et symbol med en lås i rækken for hver skabelon. Dette symbol angiver, at skabelonen er den standardskabelon i Attract, og at den ikke kan slettes. Administratoren bruge på ellipseknappen (**...**) til at kopiere en skabelon, indstille den som standardskabelon eller slette den. Når en skabelon er indstillet som standardskabelon, kan den fungere på en af to måder. Funktionsmåden angives ved hjælp af det eller de kort, der vises i rækken for skabelonen:

- **Standard** – Dette kort angiver, at skabelonen er standardskabelon for mail, der sendes, og at oplysninger angives i den, når en bruger sender mails af den pågældende type.
- **Standard** + **Sendt automatisk** – Denne kombination af kort angiver, at skabelonen er den aktive skabelon for systemgenererede mails, der sendes automatisk.

Markér rækken for en skabelon for at redigere den, og foretag ændringerne af skabelonen.

> [!NOTE]
> Hver modtager af en bestemt type mail er en standardskabelon. Alle standard Attract-skabeloner er indstillet som standardskabeloner, indtil administratoren opretter en ny skabelon til en bestemt type mail og indstiller den som standardskabelonen.

## <a name="create-a-template"></a>Opret en skabelon

Hvis du vil oprette en skabelon, skal du i øverste højre hjørne af mailskabelonbiblioteket vælge **+ Ny skabelon**. For at vælge den type mail, som du opretter skabelonen til, skal du vælge modtageren, processen og den hændelse, mailen skal sendes i forbindelse med. Vælg derefter **Opret**.

Skabelonen åbnes i redigeringstilstand, og du kan give den et navn. Hvis skabelonen f.eks. er beregnet til kandidater fra et universitet i USA, men indholdet er skrevet på fransk, kan du angive **Universitet\_USA\_fransk** som titel. Titel, emne og brødtekst til en skabelon kan understøtte andre sprog end engelsk.

Feltet **Til** for en skabelon ikke kan redigeres, fordi du allerede valgte modtageren, da du oprettede skabelonen.

Du kan tilføje personer som **Rekrutteringsmedarbejder** eller **Ansvarlig for ansættelse** på Cc-linjen. Når mailen sendes, erstattes disse roller automatisk med de relevante brugere, baseret på konteksten for jobbet.

Emnelinjen og brødteksten understøtter pladsholdere. Du kan indsætte pladsholdere ved at skrive **\#** og derefter vælge den relevante pladsholder på rullelisten med automatisk fuldførelse. Listen over tilgængelige pladsholdere vises i højre side af siden. Når mailen sendes, erstattes pladsholderne automatisk, baseret på konteksten for jobbet og modtageren. For eksempel indeholder en skabelon til en mail, der sendes til kandidater, pladsholderen \#{kandidat\_navn}. Når mailen sendes til en kandidat med navnet Cameron, erstattes denne pladsholder med navnet Cameron.

Brødteksteditoren er en RTF-editor, hvor du kan vælge typografi og format for teksten. Du kan også indsætte hyperlinks og ankre.

Når der er oprettet en skabelon for en bestemt type mail, kan du vælge på ellipseknappen (**...**) i rækken for skabelonen og angive den som standardskabelon.

## <a name="consume-templates"></a>Bruge skabeloner

Når ansættelsesteamet sender en mail, kan den bruge de skabeloner, der er oprettet af administratoren. Hvis der er oprettet flere skabeloner til den mail, som en bruger sender, vises en rulleliste i kompositionsarbejdsgangen for mailen. Standardskabelonen angives automatisk, men brugeren kan vælge en anden skabelon.

> [!NOTE] 
> Du kan oprette flere skabeloner til mails, der sendes automatisk. Kun én skabelon kan dog angives som den aktive skabelon. Da denne proces udløses af hændelser, er det kun administratoren, der kan bestemme, hvilken skabelon der skal bruges, på baggrund af kombinationen af **Standard**- og **Sendt automatisk**-kort i skabelonbiblioteket.
