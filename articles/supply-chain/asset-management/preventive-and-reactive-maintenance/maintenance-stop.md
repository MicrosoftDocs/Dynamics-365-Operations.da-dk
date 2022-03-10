---
title: Vedligeholdelsesnedetidsaktiviteter
description: Dette emne beskriver, hvordan vedligeholdelsesnedetid bruges til at få et overblik over den kapacitet, der kræves for at udføre vedligeholdelsesjob på bestemte aktiver i en bestemt periode.
author: johanhoffmann
ms.date: 08/27/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetMaintenanceStopCopy, EntAssetMaintenanceStopObject, EntAssetObjectProductionStop, EntAssetProductionStopType, EntAssetMaintenanceStop
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 0e6168033afb97c6f4f1b8466801a6f16332df82a039927ec1b45e03aa3694b8
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6727912"
---
# <a name="maintenance-downtime-activities"></a>Vedligeholdelsesnedetidsaktiviteter

[!include [banner](../../includes/banner.md)]

Vedligeholdelsesnedetid bruges til at få et overblik over den kapacitet, der kræves for at udføre vedligeholdelsesjob på bestemte aktiver i en bestemt periode. Du kan f.eks. oprette en registrering af vedligeholdelsesnedetid for produktionslinje 10 i produktionshal 29-A på produktionssted 02. Registrering af vedligeholdelsesnedetid har et start- og sluttidspunkt, der angiver den periode, hvor de aktiver, der er tilknyttet vedligeholdelsesstoppet, ikke er tilgængelige for produktionen.

**Aktiviteter med vedligeholdelsesnedetid** er en oversigt over vedligeholdelsestidsplanslinjer og vedligeholdelsesjob for arbejdsordrer på relaterede aktiver i en bestemt periode. De linjer, der er knyttet til vedligeholdelsesjob for arbejdsordrer, har alle den forventede startdato i perioden for vedligeholdelsesstop. Du kan udtrække nyttige oplysninger og regulere planlagte vedligeholdelsesjob:

- Få vist en oversigt over de påkrævede lukningsperioder for produktionsudstyr (aktiver).  
- Få et overblik over planlagt vedligeholdelse (timer), grupperet efter kompetencer (ansvarlige vedligeholdelsesarbejdsgrupper eller vedligeholdelsesarbejdere), f.eks. kapacitetsbelastning for elektrikere, smede eller andre vedligeholdelsesarbejdsgrupper, der kræves for at udføre de planlagte vedligeholdelsesjob.  
- Foretag justeringer af vedligeholdelsestidsplanslinjer eller vedligeholdelsesjob for arbejdsordrer, der er knyttet til aktiverne, f.eks. rediger forventede start- og sluttidspunkter på en linje, eller vælg andre vedligeholdelsesarbejdere for at optimere arbejdsgangen for vedligeholdelsesarbejdere og vedligeholdelsesarbejdsgrupper.

Når der er valgt anlægsaktiver i en registrering af vedligeholdelsesnedetid, medtages alle åbne vedligeholdelsestidsplanslinjer og arbejdsordrevedligeholdelsesjob for aktive arbejdsordrer i registrering af vedligeholdelsesnedetid.

## <a name="maintenance-downtime-activities"></a>Vedligeholdelsesnedetidsaktiviteter

Klik på **Styring af aktiver** > **Almindeligt** > **Aktiviteter med vedligeholdelsesnedetid** > **Alle aktiviteter med vedligeholdelsesnedetid** for at åbne en liste over alle aktiviteter med vedligeholdelsesnedetid og se nogle af de oplysninger, der er relateret til aktiviteterne. Klik på et link i kolonnen **Aktiviteter med vedligeholdelsesnedetid** for at åbne detaljevisningen. I følgende illustration vises et eksempel på listen **Vedligeholdelsesnedetidsaktiviteter**.

![Figur 1.](media/19-preventive-maintenance.png)


## <a name="create-a-maintenance-downtime-activity"></a>Oprette en vedligeholdelsesnedetidsaktivitet

1. Klik på **Styring af aktiver** > **Almindeligt** > **Aktiviteter med vedligeholdelsesnedetid** > **Alle vedligeholdelsesaktiviteter** eller **Aktive aktiviteter med vedligeholdelsesnedetid**.

2. Klik på **Ny**.

3. Indsæt et id i feltet **Aktiviteter med vedligeholdelsesnedetid** og et navn i feltet **Navn**.

4. Indsæt perioden for vedligeholdelsesstoppet i felterne **Start dato/klokkeslæt** og **Slutdato/klokkeslæt**.

5. I oversigtspanelet **Aktiviteter med vedligeholdelsesnedetid for aktiver** > skal du klikke på **Tilføj linje** for at føje aktiver ét ad gangen til aktiviteten med vedligeholdelsesnedetid.

6. Klik på **Gem**, når alle aktiver er tilføjet. I nedenstående illustration vises et eksempel på en Vedligeholdelsesnedetidsaktivitet med relaterede aktiver og vedligeholdelsesjob.

7. Vedligeholdelsesjob for arbejdsordrer og åbne vedligeholdelsestidsplanslinjer, der vedrører de valgte aktiver, vises i oversigtspanelerne **Resulterende vedligeholdelsesjob for arbejdsordre** og **Vedligeholdelsestidsplanslinjer**. I oversigtspanelet **Generelt** > gruppen **Arbejdsordrer** feltet **> Vedligeholdelsesprognosetimer** og oversigtspanelet **Generelt** > gruppen **Vedligeholdelsestidsplan** > feltet **Timer i vedligeholdelsesprognose** kan du se det samlede antal budgetterede timer for vedligeholdelsesjob for arbejdsordrer og vedligeholdelsestidsplanlinjer.

I følgende illustration vises et eksempel på detaljevisningen af **Vedligeholdelsesnedetidsaktiviteter**.

![Figur 2.](media/20-preventive-maintenance.png)

>[!NOTE]
>Vedligeholdelsesjob for arbejdsordrer og vedligeholdelsestidsplanslinjerne, der vedrører de valgte aktiver, opdateres automatisk, hvis der oprettes nye arbejdsordrer eller vedligeholdelsestidsplanslinjer, efter at du oprettede aktiviteten med vedligeholdelsesnedetid. Hvis du f.eks. planlægger vedligeholdelsesplaner eller vedligeholdelsesrunder i de relaterede aktiver to dage efter, at aktiviteten med vedligeholdelsesnedetid blev oprettet, føjes der automatisk nye vedligeholdelsestidsplanslinjer til aktiviteten med vedligeholdelsesnedetid.

8. I **Alle aktiviteter for vedligeholdelsesnedetid** > **Aktiviteter med vedligeholdelsesnedetid** > skal du vælge en vedligeholdelsesnedetidsaktivitet på listen og klikke på **Kapacitetsbelastning** for at åbne dialogboksen **Beregn kapacitetsbelastning**. Du kan bruge denne dialogboks til at få vist en oversigt over kapacitetsbelastningen, f.eks. datoer, aktiver, aktivtyper og vedligeholdelsesjobtyper. Bemærk, at de datoer, der vises i dialogboksen, er de start- og slutdatoer, der er valgt i **Aktiviteter med vedligeholdelsesnedetid**. Denne beregning omfatter de aktiver, der er relateret til aktiviteten med vedligeholdelsesnedetid.

9. I dialogboksen **Beregn kapacitetsbelastning** skal du redigere start- og sluttidspunkter, hvis det er nødvendigt, og vælge, om du vil medtage arbejdsordrer og vedligeholdelsestidsplaner i beregningen. Du kan bruge feltet **Niveau** til at angive, hvor detaljeret beregningen af kapacitetsbelastningen skal være i forbindelse med arbejdssteder. Hvis du f.eks. indsætter tallet "1" i feltet, og du har en arbejdsstedsstruktur med flere niveauer, vises alle aktiver for et arbejdssted, som er valgt for aktiviteten med vedligeholdelsesnedetid, på det øverste niveau, og derfor kan timerne på en linje være opsummeret fra arbejdssteder, der findes på et lavere niveau. Hvis du indsætter tallet "0" i feltet **Niveau**, kan du se et detaljeret resultat, der viser alle kapacitetsbelastningslinjer på alle de arbejdsstedsniveauer, de er relateret til.

10. Klik på **OK** for at starte beregningen. Det samlede antal timer vises i oversigten **Kapacitetsbelastning**. Under fanen **Kapacitetsbelastning** > **Grupper efter...** handlingsrudegrupper skal du klikke på de relevante knapper for at få vist et mere detaljeret overblik over fordelingen af budgetterede timer. I illustrationen herunder vises resultaterne af en beregning af **Kapacitetsbelastning**.

![Figur 3.](media/21-preventive-maintenance.png)

11. Når du har overblik over kapacitetsbelastningen, og du vil foretage reguleringer af vedligeholdelsesjob for arbejdsordrer eller linjer til vedligeholdelsestidsplaner, skal du vende tilbage til detaljevisningen **Aktiviteter med vedligeholdelsesnedetid** og vælge de linjer, du vil justere, i oversigtspanelerne **Resulterende vedligeholdelsesjob for arbejdsordre** og **Vedligeholdelsestidsplanslinjer**.

12. Klik på knappen **Juster**, og opdater forventede start-/slutdatoer, serviceniveau eller ansvarlige vedligeholdelsesarbejdere for de valgte vedligeholdelsesjob for arbejdsordrer eller vedligeholdelsestidsplanslinjer.

13. Klik på **OK**, når du har foretaget de nødvendige justeringer. 

>[!NOTE]
>Vedligeholdelsesjob for arbejdsordrer og vedligeholdelsestidsplanslinjer, der ikke er medtaget i perioden for vedligeholdelsesnedetid, efter at du har foretaget justeringer, fjernes automatisk fra **Aktiviteter med vedligeholdelsesnedetid**.

14. I **Alle aktiviteter med vedligeholdelsesnedetid** > **Aktiviteter med vedligeholdelsesnedetid** > skal du vælge en aktivitet med vedligeholdelsesnedetid på listen og klikke på **Varebudget** for at åbne dialogboksen **Beregn varebudget**. Du kan bruge denne dialogboks til at beregne budgetter for varer (reservedele og andre påkrævede varer) og gruppere dem for at få et overblik, f.eks. efter dato, aktiv, aktivtype og vedligeholdelsesjobtype. Bemærk, at de datoer, der vises i dialogboksen, er de start- og slutdatoer, der er valgt i **Aktiviteter med vedligeholdelsesnedetid**. Denne beregning omfatter reservedele og varer, der er relateret til de aktiver, der er valgt i aktiviteten med vedligeholdelsesnedetid.

15. I dialogboksen **Beregne varebudget** skal du redigere start- og sluttidspunkter, hvis det er nødvendigt, og vælge, om du vil medtage arbejdsordrer og vedligeholdelsestidsplaner i beregningen. Du kan bruge feltet **Niveau** til at angive, hvor detaljeret beregningen af kapacitetsbelastningen skal være i forbindelse med arbejdssteder. Hvis du f.eks. indsætter tallet "1" i feltet, og du har en arbejdsstedsstruktur med flere niveauer, vises alle aktiver for et arbejdssted, som er valgt for aktiviteten med vedligeholdelsesnedetid, på det øverste niveau, og derfor kan timerne på en linje være opsummeret fra arbejdssteder, der findes på et lavere niveau. Hvis du indsætter tallet "0" i feltet **Niveau**, kan du se et detaljeret resultat, der viser alle kapacitetsbelastningslinjer på alle de arbejdsstedsniveauer, de er relateret til.

16. Klik på **OK** for at starte beregningen. Det samlede antal varebudgetter vises i oversigten **Varebudget**. Under fanen **Varebudget** > handlingsrudegrupperne **Grupper efter...** skal du klikke på de relevante knapper for at få vist et mere detaljeret overblik over fordelingen af budgetterede varer. I illustrationen herunder vises resultaterne af en beregning af **Varebudget**.

![Figur 4.](media/22-preventive-maintenance.png)

- Du kan kopiere aktiver fra én aktivitet med vedligeholdelsesnedetid til en anden. I **Alle aktiviteter med vedligeholdelsesnedetid** skal du vælge knappen **Kopiér aktiviteter med vedligeholdelsesnedetid** og foretage dine valg i felterne **Fra aktiviteter med vedligeholdelsesnedetid** og **Til aktiviteter med vedligeholdelsesnedetid** og klikke på **OK**.
- I **Alle aktiviteter med vedligeholdelsesnedetid** skal du klikke på knappen **Vedligeholdelsestidsplanslinjer** eller knappen **Aktive arbejdsordrer** for at åbne de relaterede lister og få vist linjer, der er relateret til den valgte aktivitet med vedligeholdelsesnedetid.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]