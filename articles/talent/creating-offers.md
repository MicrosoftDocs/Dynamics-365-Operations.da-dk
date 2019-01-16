---
title: Oprettelse, godkendelse og signering af tilbud
description: "Dette emne indeholder oplysninger om, hvordan du kan oprette, godkende og underskrive et kandidattilbud ved hjælp af Dynamics 365 for Talent."
author: josaw
manager: AnnBe
ms.date: 12/07/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent, Core
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2018-10-19
ms.dyn365.ops.version: Talent October 2018 update
ms.translationtype: HT
ms.sourcegitcommit: be66d9f95551066bb8bc25445c652d4fa59066d4
ms.openlocfilehash: f189df052ef299a2cca1d92065a7a4d377d25399
ms.contentlocale: da-dk
ms.lasthandoff: 12/07/2018

---

# <a name="creating-approving-and-signing-offers"></a>Oprettelse, godkendelse og signering af tilbud

[!include[banner](../includes/banner.md)]

I mange tilfælde skal forberedelse af en tilbudspakke til en kandidat være en meget hurtig proces.
Ved at bruge de skabeloner, der oprettes af Attract-administratoren, kan den, der udarbejder tilbuddet, spare tid på at forberede og sende tilbud til en kandidat.

## <a name="create-an-offer"></a>Oprette et tilbud

Når appen Tilbudsstyring er aktiveret, kan alle brugere med rollen som ansættelsesansvarlig eller rekrutteringsmedarbejder forberede en tilbudspakke til kandidaten. Gør følgende for at klargøre tilbuddet.

1.  Gå til jobbet og den kandidatansøgning, du opretter et tilbud for.

1.  Gå til **Tilbudsstadie**, og klik på **Forbered tilbud**.

    Du bliver omdirigeret til Tilbud-appen, hvor du kan se kandidaten med status **Ny**. Du kan også se andre tilbud, som du bidrager til, enten som tilbudsopretter eller -godkender.

1.  Klik på **Forbered tilbud**. 
    
    Du kan se et udvalg af forskellige tilbudspakker, der er gjort tilgængelige af administratoren.

1.  Vælg en pakke, og klik på **Udført** for at starte udarbejdelsen af tilbuddet.

    Skabelonen til tilbudspakken indlæses med de samme job- og kandidatoplysninger som er angivet i tilbuddet.

1.  Alle pladsholdere for tilbudsdata, der indgår i tilbudspakken, kan ses på landingssiden. Du kan angive alle værdierne på tværs af pakken på denne side.

    Du kan også se tilbudsdokumentskabeloner, der indgår i pakketilbuddet, på landingssiden.

1.  Du kan nu muligvis redigere indholdet af tilbuddet, afhængigt af hvordan skabelonen er konfigureret af administratoren.

1.  Hvis du vil fjerne dokumenter, der er markeret som ikke-obligatoriske, kan du gøre det.

1. Når alle tilbudsdatapladsholdere er udfyldt, skal du klikke på **Gem** for at gemme en kladde af tilbuddet.

>[!NOTE]
> Når du har gemt en kladde, kan du slette kladdeversionen af tilbuddet eller vælge en ny pakkeskabelon, hvis du har brug for det.


## <a name="approve-an-offer"></a>Godkende et tilbud

De fleste tilbud skal gennemgå en godkendelsesproces for at sikre, at tilbuddet opfylder de nødvendige standarder. Hvis tilbuddet ikke opfylder standarderne, for eksempel hvis den, der har oprettet tilbuddet, ikke har fulgt reglerne for tilbudsdata og har tilsidesat værdierne i tilbuddet, vælges godkendelsesprocessen. Når du vil sende et tilbud til godkendelse, skal du gøre følgende:

1.  Når tilbuddet er i kladdetilstand, skal du tilføje godkendere i **Godkenderpanel**. 
    >[!NOTE]
    > Ansættelsesansvarlige tilføjes som standard som godkender. Du kan vælge enhver bruger i din organisation som godkender for tilbuddet.

1.  Du kan eventuelt tildele godkendere i en sekventiel godkendelsesmetode eller i en parallel godkendelsesmetode. Denne indstilling er kun tilgængelig, hvis den er konfigureret som sådan af administratoren.
    >[!NOTE]
    > Hvis godkendelsesprocessen er sekventiel, kan du redigere rækkefølgen af godkendere, hvis det er nødvendigt.

1.  Når du er færdig med at definere godkendelseskæden, kan du redigere indholdet af godkendelses-e-mailen og derefter sende beskeden til godkenderne. Klik på **Send til godkendere**.
    >[!NOTE]
    > Hvis tilbuddet ikke er standard, skal du angive en begrundelse.

1.  Hvis den, der opretter tilbuddet, fravælger en godkender, kan han eller hun skrive en note og gå til den næste godkender.

Godkendere modtager en e-mail, hvor de bliver bedt om at godkende tilbuddet. De kan klikke på linket i e-mailen for at åbne tilbuddet, gennemse hele tilbudspakken og enten godkende den eller sende den tilbage til tilbudsopretteren. Tilbudsgodkendere skal tilføje endnu en note, hvis de afviser tilbudspakken, fordi den kræver yderligere redigering. 

I tilfælde hvor der er en ny version af tilbuddet, som er oprettet, før godkenderen handler, kan godkenderen ikke godkende eller afvise tilbuddet.

## <a name="offer-versioning"></a>Versioner af tilbud 

Når tilbuddet er godkendt eller sendt tilbage til yderligere redigeringer, kan du vælge indstillingen **Aktivér redigering** for at oprette en ny version af tilbuddet. Den nye version af tilbuddet indeholder alle tilbudsdataværdierne og listen over godkendere, der er overført fra den seneste version. 

Godkenderne kan skifte mellem forskellige tilbudsversioner, hvis versionerne er delt med dem med henblik på godkendelse. En godkender eller tilbudsopretter kan også vælge at slette en bestemt version af en tilbudskladde for at vende tilbage til det tidligere stadie.


## <a name="send-an-offer-to-a-candidate"></a>Sende et tilbud til en kandidat 

Når tilbuddet er gemt, godkendt og klar til at blive sendt til kandidaten, skal du klikke på **Send til kandidat**.

Der er flere handlinger, som du kan udføre, før du sender tilbuddet til kandidaten.
-  Du kan få vist oversigten over dokumenter, der indgår i tilbudspakken, som skal sendes til kandidaten.

-  Du kan angive en udløbsdato for tilbuddet. Kandidater forventes at acceptere eller afvise tilbuddet før udløbsdatoen.  Kandidaten går tilsendt en påmindelse, 48 timer før tilbuddet udløber.

-  Der kan være flere dokumenter, du vil medtage i processen til accept af tilbuddet. Du har mulighed for at angive den dokumenttype, der kræves.

- Indstilling for e-signatur: Hvis Adobe Sign er valgt som den foretrukne e-signaturmetode, skal den, der opretter et tilbud, oprette forbindelse til sin Adobe Sign-licens. Der er to måder at gøre dette på. Gå til **Brugerindstillinger** i **Tilbud**. Under **Forbindelser** skal du oprette forbindelse til **Adobe Sign**. Du kan også blive bedt om at oprette forbindelse fra Send tilbud til kandidatens skærm, hvis forbindelsen ikke allerede blev oprettet ud fra brugerindstillingerne. 

> [!NOTE]
> Brugerne skal blot forbinde deres Adobe Sign-konti én gang. Den samme brugerlicens bruges til alle fremtidige tilbudspakker, der skal sendes ud af den samme bruger. 

-  Du kan få vist og rediger e-mailskabelonen efter behov.

Når tilbuddet er klar, og du klikker på **Send til kandidat**, modtager kandidaten en e-mail om, at et tilbud afventer gennemsyn.


## <a name="candidates-actions-after-receiving-an-offer"></a>Kandidatens handlinger efter modtagelse af et tilbud

Når kandidaten har fået besked om, at der er et delt tilbud, kan han eller hun klikke på linket i sin e-mail for at gå til ansøgningsdashboardet og se tilbuddet. I dashboardet kan kandidaten se de aktiviteter, han eller hun stadig skal udføre.

1.  For at få vist tilbuddet og alle relaterede dokumenter skal kandidaten klikke på **Vis tilbud**.

    Kandidaterne kan også downloade tilbudspakken i .zip-format.

1.  For at acceptere tilbuddet skal kandidaterne klikke på **Gå til underskrift** for hvert dokument, der indgår i tilbudspakken.

1.  Når dokumenterne hver især er underskrevet og accepteret, skal kandidaten vælge at afslutte acceptprocessen ved at klikke på **Acceptér tilbud** øverst på siden.

1.  Hvis kandidaten til afslå tilbuddet, skal han eller hun klikke på **Afvis tilbud** øverst på siden, vælge den relevante årsag, tilføje en kommentar efter behov og derefter klikke på **Afvis**.

1.  Når kandidaten har accepteret eller afvist tilbuddet, kan vedkommende fortsat forblive i tilbudsvisningen eller gå tilbage til ansøgningsdashboardet.

1.  Hvis der blev anmodet om andre dokumenter som et led i processen til accept af tilbuddet, skal kandidaten vælge at overføre de krævede dokumenter og mærke dem til den dokumenttype, der blev anmodet om.

1.  Tilbudsopretteren får besked, når alle dokumenter er overført, og tilbudspakken er underskrevet.


## <a name="withdrawing-an-offer"></a>Trække et tilbud tilbage

Et tilbud kan trækkes tilbage fra en kandidat når som helst og af forskellige årsager. 
1.  Træk tilbuddet tilbage ved at klikke på ellipseknappen (**...**) og derefter klikke på **Træk dette tilbud tilbage**. 

2. Der vises en meddelelse, hvor du bliver spurgt, om kandidaten er blevet kontaktet om ændringen af status. Hvis kandidaten ikke er blevet kontaktet, har du mulighed for at sende en e-mail til kandidaten med oplysninger om yderligere handlinger. 

   Tilbuddet vil ikke længere være tilgængeligt for kandidaten.


## <a name="closing-an-offer"></a>Lukning af et tilbud 

Når et tilbud er blevet accepteret, afvist eller trukket tilbage, uden at der kræves yderligere handlinger, kan du lukke tilbuddet, så der ikke kan foretages yderligere redigeringer af denne tilbudspakke.

