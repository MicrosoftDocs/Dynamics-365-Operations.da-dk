---
title: Handlingsmeddelelser
description: En aktionsmeddelelse er et systemgenereret forslag om ændring af en eksisterende planlagt eller autoriseret ordre.
author: t-benebo
ms.date: 03/18/2022
ms.topic: article
ms.search.form: ReqGroup, MCRSalesOrderMessages, MCRSalesTableDetailedStatus, TAMItemVendRebateGroup, TAMVendRebate, TAMVendRebateAgreementLineInfoPart, TAMVendRebateGroup, TAMVendRebateTable, TAMVendRebateTrans, ReqTransActionListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19411
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: 10.0.27
ms.openlocfilehash: e6df6cfd038383b3eeaa3659e0af3e469429f81e
ms.sourcegitcommit: 197e6ddee84522fd587c6e4ee4f9089101e301c2
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/13/2022
ms.locfileid: "8570248"
---
# <a name="action-messages"></a>Handlingsmeddelelser

[!include [banner](../includes/banner.md)]

En handlingsmeddelelse er et systemgenereret forslag om ændring af en eksisterende planlagt, godkendt eller autoriseret ordre.

Handlingsmeddelelser genereres af beregningen af behovsplanlægning som reaktion på ændrede behov. For eksempel kan afsendelsesdato eller antal være ændret på en salgsordre, efter at du allerede har oprettet en indkøbsordre for at opfylde behovet for denne salgsordre. I så fald genererer beregning af behovsplanlægning en eller flere handlingsmeddelelser, som foreslår dig at opdatere indkøbsordren. Du bestemmer, om du vil foretage de ændringer, der foreslås.

Du kan konfigurere, hvordan handlingsmeddelelser skal beregnes for en disponeringsgruppe, som du knytter til en vare.

## <a name="select-action-messages"></a>Vælge handlingsmeddelelser

På siden **Disponeringsgrupper** kan du vælge de handlingsmeddelelser, som systemet skal generere, og de disponeringsgrupper eller varer, som meddelelserne skal gælde for. I følgende tabel vises den handlingsmeddelelse, du kan vælge.

| Meddelelse | Beskrivelse |
|---|---|
| Fremskynd | Der oprettes handlingsmeddelelser, når det er nødvendigt, for at flytte ordrer til en tidligere dato. I feltet **Fremskynd margen** kan du også angive det maksimale antal dage, der må gå mellem tilgang og afgang uden fremskyndelseshandling. |
| Udskyd | Der oprettes handlingsmeddelelser, når det er nødvendigt, for at flytte ordrer til en senere dato. I feltet **Udskyd margen** kan du angive det maksimale antal dage, der må gå mellem tilgang og afgang uden en udskydelseshandling. |
| Nedskriv | Der oprettes handlingsmeddelelser, når produktionsordrer, købsordrer og andre tilgangstransaktioner bør mindskes for at undgå høje lagerniveauer. |
| Forøg | Der oprettes handlingsmeddelelser, når produktionsordrer, købsordrer og andre tilgangstransaktioner bør øges for at undgå varemangel på lageret. |
| Afledte handlinger | Handlingsmeddelelser, der oprettes for tilgangsposteringer, overføres til eventuelle afledte behov, og der genereres de nødvendige handlingsmeddelelser for de tilgangsposteringer, der opfylder disse krav. |

Følgende afsnit indeholder nogle få detaljerede scenarier.

## <a name="increase-and-decrease-actions-with-product-default-order-quantities"></a>Forøgelses- og reduceringshandlinger med produktstandardordreantal

På siden **Standardordreindstillinger** for en vare kan du konfigurere et minimumordreantal, et maksimumordreantal og flere værdier. Disse indstillinger tages derefter i betragtning, når der foreslås handlinger, for at sikre, at forslagene aldrig medfører underforsyning.

Du kan f.eks. have et element med følgende indstillinger på siden **Standardordreindstillinger**:

- **Minimalt ordreantal:** *0*
- **Maksimalt ordreantal:** *90*
- **Multiplum:** *20*

Hvis der er behov for et antal på 60 af denne vare, opretter varedisponering et indkøbsordreforslag på et antal af 60. Hvis efterspørgslen øges med 30, foreslår varedisponeringen en stigning på 40, da den vil overholde multiplum af 20 og aldrig forårsage underforsyning.

## <a name="action-messages-for-orders-related-to-safety-stock"></a>Handlingsmeddelelser til ordrer vedrørende sikkerhedslager

Handlingsmeddelelser til ordrer, der forsyner sikkerhedslager, foreslår aldrig, at antallet skal falde under det antal, der er nødvendig for sikkerhedslageret. Med andre ord: Hvis der findes en ordre, der forsyner sikkerhedslager og kundebehov, og efterspørgslen reduceres eller annulleres, vil varedisponering foreslå, at ordreforslaget reduceres med den reducerede efterspørgsel. Den vil dog aldrig foreslå en værdi, der er lavere end det sikkerhedslager, der er brug for.

Systemet foreslår ikke udskydelseshandlinger til forsyning af sikkerhedslager, da det forudsættes, at sikkerhedslageret skal forsynes på det nødvendige tidspunkt og på den påkrævede dato.

### <a name="advance-and-postpone-actions-related-to-boms"></a>Fremskyndelses- og udskydelseshandlinger vedrørende styklister

Handlinger, der er relateret til styklistekomponenter, skal anvendes før handlingerne i deres overordnede varer, da det kan påvirke yderligere ordrer, der er relateret til styklister på højere niveau. Derefter skal du køre varedisponeringen igen for at genberegne og foreslå relevante handlinger.

Du kan f.eks. have følgende situation:

- Endelig god *FG* af typen *produktion* har en stykliste, der indeholder råvarer *RM*.
- Dags dato er 21. januar.
- En eksisterende, frigivet produktionsordre til *FG* er planlagt til 25. januar.
- For at understøtte den eksisterende produktionsordre har varedisponeringen oprettet et indkøbsordreforslag til det nødvendige råmateriale *RM*. Ordren har behovsdato den 25. januar.
- Der oprettes en ny salgsordre for *FG* i dag. Den har en behovsdato i dag (21. januar).
- 21. januar er lukket for levering på *RM*-kalenderen, men 22. januar er åben.

Når der køres varedisponering, genereres der handlingsmeddelelser, der foreslår, at den tidligere planlagte produktion skal flyttes frem, så du kan opfylde dagens ordre.

- For at imødekomme den nye efterspørgsel foreslår programmet, at produktionsordren for *FG* flyttes frem til 21. januar. (Det kommer med dette forslag uden at overveje den lukkede dato for *RM*).
- Da *RM* stadig skal bruges til produktionsordren, foreslår programmet også, at indkøbsordreforslaget flyttes op. Men denne gang kontrolleres kalenderen *RM*. Den foreslår derfor, at indkøbsordreforslaget for *RM* flyttes til 22. januar (fordi 21. januar er lukket).

Som du kan se, vil den påkrævede råvare *RM* nu ankomme for sent til den planlagte produktion af *FG*. Derfor skal du først anvende fremskyndelseshandling på indkøbsordreforslaget til *RM* og derefter køre varedisponeringen igen. På dette tidspunkt genererer varedisponeringen en ny handlingsmeddelelse, der foreslår, at produktionsordren for *FG* flyttes til 22. januar.
