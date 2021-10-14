---
title: Oprette og behandle uoverensstemmelser
description: Dette emne beskriver, hvordan du håndterer uoverensstemmelser baseret på en eksisterende kvalitetsordre.
author: yufeihuang
ms.date: 03/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 032f5b712c2be5312524129cd25e655e778f5f44
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/29/2021
ms.locfileid: "7580858"
---
# <a name="create-and-process-nonconformances"></a>Oprette og behandle uoverensstemmelser

[!include [banner](../../includes/banner.md)]

Dette emne beskriver, hvordan du håndterer uoverensstemmelser baseret på en eksisterende kvalitetsordre. Normalt håndteres uoverensstemmelser af en kvalitetsassistent. Du skal som en forudsætning have en kvalitetsordre til rådighed. (Du kan finde oplysninger om oprettelse af en kvalitetsordre i [Inspicere varers kvalitet](inspect-quality-goods.md).)

Før en bruger kan behandle godkendelsen af en uoverensstemmelse, skal en arbejder tildeles i feltet **Person** på siden **Brugere**. Derudover skal indstillingen **Aktivér dokumenthåndtering** angives til *Ja* i brugerindstillinger, før brugeren kan bruge dokumentbemærkningerne.

## <a name="create-a-nonconformance"></a>Oprette en uoverensstemmelse

Benyt denne fremgangsmåde for at oprette en uoverensstemmelse.

1. Gå til **Lagerstyring \> Periodiske opgaver \> Kvalitetsstyring \> Uoverensstemmelser**.
1. Vælg **Ny** i handlingsruden.
1. Vælg den problemtype, der blev fundet i inspektionsprocessen,I feltet **Problemtype** i dialogboksen **Opret uoverensstemmelse**.
1. Vælg **OK**.

## <a name="approve-or-reject-a-nonconformance"></a>Godkende eller afvise en uoverensstemmelse

Hvis du vil godkende eller afvise en uoverensstemmelse, skal du benytte følgende fremgangsmåde.

1. Gå til **Lagerstyring \> Periodiske opgaver \> Kvalitetsstyring \> Uoverensstemmelser**.
1. På listen skal du vælge den uoverensstemmelse, du vil opdatere.

    > [!NOTE]
    > Du kan kun føje en rettelse til uoverensstemmelser, der er godkendte.

1. Vælg **Funktioner \> Godkend uoverensstemmelse** i handlingsruden for at godkende uoverensstemmelsen, eller **Funktioner \> Afvis uoverensstemmelse** for at afvise den. Du kan knytte godkendte uoverensstemmelser til [relaterede operationer](../quality-operations.md). På denne måde kan du registrere arbejde, der er udført som en del af håndteringen af uoverensstemmelser og rettelser.
1. Du bliver bedt om at bekræfte dit valg. Vælg **Ja** for at fortsætte.

## <a name="add-operations-and-other-details-to-nonconformances"></a>Føje operationer og andre detaljer til uoverensstemmelser

Når du har oprettet en uoverensstemmelse, kan du begynde at tilføje relaterede operationer og angive yderligere oplysninger om disse operationer. Du kan kun føje relaterede operationer til uoverensstemmelser, der er godkendte.

Udover de grundlæggende oplysninger kan du føje følgende detaljer til en operation:

- **Varer** – Du kan oprette en liste over forbrugte varer for at udføre rettelsen. Varerne kan f.eks. være produkter, der skal bruges til reparation af udstyr eller ingredienser, der er nødvendige for at reparere et færdigt produkt.
- **Kvalitetsgebyrer** – Du kan oprette en liste over gebyrer, der påløber eller faktureres til eksterne kilder.
- **Timeseddel** – Du kan oprette en logfil over den tid, hver arbejder bruger på operationen.

De resterende indstillinger er valgfrie. Omkostningerne for hver vare, kvalitetsgebyrer og timesedlen lægges sammen og vises i operationen. Du kan ikke redigere feltet **Omkostning** direkte i operationen.

### <a name="create-an-operation-for-a-nonconformance"></a>Oprette en operation for en uoverensstemmelse

Benyt denne fremgangsmåde for at oprette en operation for en uoverensstemmelse.

1. Gå til **Lagerstyring \> Periodiske opgaver \> Kvalitetsstyring \> Uoverensstemmelser**.
1. På listen skal du vælge den uoverensstemmelse, du vil opdatere.

    > [!NOTE]
    > Du kan kun tilføje eller opdatere operationer for uoverensstemmelser, der er godkendte.

1. Vælg **Relaterede operationer** i handlingsruden.
1. På siden **Relaterede operationer** i handlingsruden skal du vælge **Ny** for at føje en række til gitteret. Angiv følgende felter til den nye række:

    - **Operation** – Vælg koden for den operation, der skal udføres for uoverensstemmelsen.
    - **Årsag** – Angiv en detaljeret beskrivelse, der forklarer, hvorfor operationen er påkrævet.
    - **Salgsordre** – Hvis den valgte operationskode er knyttet til salgsordretypen, skal du vælge den salgsordre, som operationen skal tilknyttes.
    - **Indkøbsordre** – Hvis den valgte operationskode er knyttet til indkøbsordretypen, skal du vælge den indkøbsordre, som operationen skal tilknyttes.

1. Luk siderne.

### <a name="add-items-to-an-operation"></a>Føje varer til en operation

Benyt følgende fremgangsmåde for at føje varer til en operation.

1. Gå til **Lagerstyring \> Periodiske opgaver \> Kvalitetsstyring \> Uoverensstemmelser**.
1. På listen skal du vælge den uoverensstemmelse, du vil opdatere.

    > [!NOTE]
    > Du kan kun tilføje eller opdatere operationer for uoverensstemmelser, der er godkendte.

1. Vælg **Relaterede operationer** i handlingsruden.
1. Vælg den operation på siden **Relaterede operationer**, som du vil føje varer til.
1. Vælg **Varer** i handlingsruden.
1. På siden **Relaterede operationer** i handlingsruden skal du vælge **Ny** for at føje en række til gitteret. Angiv følgende felter for den nye række:

    - **Varenummer** – Vælg det produkt, der skal bruges som del af den valgte operation.
    - **Antal** – Angiv antallet af varer, der vil blive brugt.

    > [!NOTE]
    > Du kan få vist omkostningen for varen i feltet **Omkostning** under fanen **Generelt**. Den viste omkostning hentes fra den omkostning, der er angivet på siden **Frigivet produkt**. Omkostningen kan ikke opdateres direkte på siden **Relateret operationsvare**. Omkostningerne for alle varer, der er tilføjet på siden **Relaterede operationsvarer**, føjes automatisk til feltet **Omkostning** på siden **Relaterede operationer**.

1. Gentag forrige trin for hver ekstra vare, du skal tilføje.
1. Luk siderne.

### <a name="add-quality-charges-to-an-operation"></a>Føje kvalitetsgebyrer til en operation

Benyt følgende fremgangsmåde for at føje kvalitetsgebyrer til en operation.

1. Gå til **Lagerstyring \> Periodiske opgaver \> Kvalitetsstyring \> Uoverensstemmelser**.
1. På listen skal du vælge den uoverensstemmelse, du vil opdatere.

    > [!NOTE]
    > Du kan kun tilføje eller opdatere operationer for uoverensstemmelser, der er godkendte.

1. Vælg **Relaterede operationer** i handlingsruden.
1. Vælg den operation, du vil føje kvalitetsgebyrer til, på siden **Relaterede operationer**.
1. Vælg **Kvalitetsgebyrer** i handlingsruden.
1. På siden **Relaterede operationsgebyrer** i handlingsruden skal du vælge **Ny** for at føje en række til gitteret. Angiv følgende felter til den nye række:

    - **Gebyrkode** – Vælg det kvalitetsgebyr, du vil tilføje.
    - **Beskrivelse** – Indtast en detaljeret beskrivelse af gebyret.
    - **Gebyrværdi** – Angiv beløbet for gebyret.

1. Gentag forrige trin for hvert ekstra gebyr, du skal tilføje.
1. Luk siderne.

> [!NOTE]
> Beløbet i feltet **Gebyrværdi** lægges automatisk sammen for alle kvalitetsgebyrer og føjes til eventuelle andre beløb i feltet **Omkostning** på siden **Relaterede operationer**.

### <a name="create-a-timesheet-on-an-operation"></a>Oprette en timeseddel for en operation

Benyt følgende fremgangsmåde for at føje en timeseddel til en operation.

1. Gå til **Lagerstyring \> Periodiske opgaver \> Kvalitetsstyring \> Uoverensstemmelser**.
1. På listen skal du vælge den uoverensstemmelse, du vil opdatere.

    > [!NOTE]
    > Du kan kun tilføje eller opdatere operationer for uoverensstemmelser, der er godkendte.

1. Vælg **Relaterede operationer** i handlingsruden.
1. Vælg den operation, du vil føje en timeseddel til, på siden **Relaterede operationer**.
1. Vælg **Timeseddel** i handlingsruden.
1. På siden **Timesedler for relaterede operationer** i handlingsruden skal du vælge **Ny** for at føje en række til gitteret. Angiv følgende felter til den nye række:

    - **Dato** – Angiv den dato, hvor arbejdet blev udført. Dette felt er som standard indstillet til dags dato.
    - **Arbejder** – Vælg den arbejder, som udførte arbejdet. Dette felt er som standard angivet til den arbejder, der er tildelt den aktuelle bruger.
    - **Operationstimer** – Angiv antallet af timer, hvor der blev arbejdet på den valgte operation.
    - **Faktureret** – Markér dette afkrydsningsfelt, hvis tiden er blevet debiteret en debitor eller kreditor på en faktura.

    > [!NOTE]
    > Du kan få vist omkostningerne i feltet **Omkostning** under fanen **Generelt**. Omkostningen beregnes ved hjælp af den sats, du definerer på siden **Lagerstyringsparametre**.

1. Gentag forrige trin for hvert ekstra timeseddellinje, du skal tilføje.
1. Luk siderne.

> [!NOTE]
> Beløbet i feltet **Omkostning** lægges automatisk sammen for alle timeseddellinjer og føjes til eventuelle andre beløb i feltet **Omkostning** på siden **Relaterede operationer**.

## <a name="add-a-correction-to-a-nonconformance"></a>Føje en rettelse til en uoverensstemmelse

Hvis du vil tilføje en rettelse til en uoverensstemmelse, skal du benytte følgende fremgangsmåde.

1. Gå til **Lagerstyring \> Periodiske opgaver \> Kvalitetsstyring \> Uoverensstemmelser**.
1. På listen skal du vælge den uoverensstemmelse, du vil opdatere.

    > [!NOTE]
    > Du kan kun føje en rettelse til uoverensstemmelser, der er godkendte.

1. Vælg **Rettelser** i handlingsruden.
1. Vælg **Ny** på siden **Rettelser** i handlingsruden for at føje en række til gitteret. Angiv følgende felter til den nye række:

    - **Diagnosticering** – Vælg den diagnosticeringstype, der identificerer den type rettelse, du er ved at oprette.
    - **Arbejder** – Vælg den person, der er ansvarlig for rettelsen.
    - **Rettelsesprioritet** – Vælg en indstilling for at angive, hvordan rettelsen skal prioriteres (*Lav*, *Normal* eller *Høj*).
    - **Ønsket dato** – Angiv den dato, hvor der blev anmodet om den korrigerende handling.
    - **Planlagt dato** – Angiv den dato, hvor rettelsen forventes at være fuldført.
    - **Kortsigtet løsning** – Markér dette afkrydsningsfelt, hvis den korrigerende handling kun retter uoverensstemmelsen i en kort periode.

1. Luk siderne.

## <a name="mark-a-correction-as-completed"></a>Markere en rettelse som fuldført

Hvis du vil markere en rettelse af en uoverensstemmelse som fuldført, skal du benytte følgende fremgangsmåde.

1. Gå til **Lagerstyring \> Periodiske opgaver \> Kvalitetsstyring \> Uoverensstemmelser**.
1. På listen skal du vælge den uoverensstemmelse, du vil opdatere.

    > [!NOTE]
    > Du kan kun føje en rettelse til uoverensstemmelser, der er godkendte.

1. Vælg **Rettelser** i handlingsruden.
1. Vælg den rettelse, der skal markeres som fuldført, på siden **Rettelser** i gitteret.
1. Vælg **Markér som fuldført** i handlingsruden.
1. Du bliver bedt om at bekræfte dit valg. Vælg **OK** for at fortsætte. Feltet **Færdiggørelsesdato og -klokkeslæt** er indstillet til dags dato og og det aktuelle klokkeslæt, og afkrydsningsfeltet **Fuldført** er markeret.
1. Luk siden.

## <a name="reopen-a-completed-correction"></a>Genåbne en fuldført rettelse

Hvis du vil genåbne en fuldført rettelse, skal du benytte følgende fremgangsmåde.

1. Gå til **Lagerstyring \> Periodiske opgaver \> Kvalitetsstyring \> Uoverensstemmelser**.
1. På listen skal du vælge den uoverensstemmelse, du vil opdatere.
1. Vælg **Rettelser** i handlingsruden.
1. Vælg den rettelse, du vil genåbne, på siden **Rettelser** i gitteret.
1. Vælg **Genåbn** i handlingsruden.
1. Du bliver bedt om at bekræfte dit valg. Vælg **OK** for at fortsætte. Værdien fjernes fra feltet **Færdiggørelsesdato og -klokkeslæt**, og markeringen i afkrydsningsfeltet **Fuldført** fjernes.
1. Luk siden.

Du kan nu redigere eller opdatere rettelsen yderligere. Når du er færdig, kan du markere rettelsen som fuldført igen.

## <a name="close-a-nonconformance"></a>Luk en uoverensstemmelse

Benyt denne fremgangsmåde for at lukke en uoverensstemmelse.

1. Gå til **Lagerstyring \> Periodiske opgaver \> Kvalitetsstyring \> Kvalitetsordrer**.
1. Vælg en kvalitetsordre i gitteret.
1. Vælg **Forespørgsler \> Uoverensstemmelser** i handlingsruden.
1. Vælg måluoverensstemmelsen i gitteret på siden **Uoverensstemmelser**.
1. Vælg **Funktioner \> Luk uoverensstemmelse** i handlingsruden.
1. Du bliver bedt om at bekræfte dit valg. Vælg **Ja** for at fortsætte.
1. Luk siderne.

## <a name="additional-resources"></a>Yderligere ressourcer

- [Oversigt over kvalitetsstyring](../quality-management-processes.md)
- [Aktivere styring af kvalitet og uoverensstemmelse](../enable-quality-management.md)
- [Arbejdere, der er ansvarlige for godkendelse af uoverensstemmelser](../quality-responsible-workers.md)
- [Karantænezoner for uoverensstemmelser](../quality-quarantine-zones.md)
- [Diagnosticeringstyper for uoverensstemmelser](../quality-diagnostic-types.md)
- [Kvalitetsgebyrer for uoverensstemmelser](../quality-charges.md)
- [Operationer for uoverensstemmelser](../quality-operations.md)
- [Kvalitetsstyring for lagerstedsprocesser.](../quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
