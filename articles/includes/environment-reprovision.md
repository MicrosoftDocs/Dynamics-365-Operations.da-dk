Når du kopierer en database mellem miljøer, skal du køre værktøjet til fornyet klargøring af miljøet, før den kopierede database er fuldt funktionsdygtigt, for at sikre, at alle Commerce-komponenter er opdaterede.

> [!IMPORTANT]
> Det anbefales, at du kører denne procedure, uanset om du bruger Commerce-komponenter eller ej, da Commerce-funktioner er inkluderet i alle miljøer. 

Før du fortsætter, skal du sikre dig, at følgende forudsætninger er opfyldt:
1. Hvis du opgraderer til frigivelsen 7.2.11792.56024 fra juli 2017 (også kaldet 7.2), skal du anvende følgende X++-hotfixes til programmet i destinationsmiljøet, før du kører dataopgraderingen i det pågældende miljø. De kan forhindre forskellige fejl i at opstå under dataopgraderingen:

    - KB 4036156 - lille versionsopgradering til Retail - 'Variantnummerserien er ikke angivet'. Denne programrettelsespakke indeholder også KB 4035399 og KB 4035751. Bemærk, at du mindst skal have installeret Platform Update 9 for at kunne bruge denne pakke. Hvis du ikke er sikker, skal du installere de nyeste binære filer.
    
2. Hvis du opgraderer fra Microsoft Dynamics AX 2012, skal du installere følgende program X++-rettelser til programmet i destinationsmiljøet, før du kører dataopgraderingen:
    - KB 4033183 - Dynamics AX 2012 R2 eller Dynamics AX 2012 R3 Pre-CU8 ikke-detailopgradering mislykkes med fejlen Objektet blev ikke fundet til dbo. RETAILTILLLAYOUTZONE.
    - KB 4040692 - Dynamics AX 2012 R3 til Microsoft Dynamics 365 for Operations 7.2-opgraderingen mislykkes på grund af duplikeret indeks for RetailSalesLine på SalesLineIdx.
    - KB 4035490 - Ydelsesproblem med opgraderingsscriptet til GeneralJournalAccountEntry MainAccount-feltet.


Udfør følgende trin for at køre værktøjet til fornyet klargøring af miljøet.

1. Vælg **Installerbar softwarepakke** i Delt aktivbibliotek.
2. Hent værktøjet til fornyet klargøring af miljøet.
3. Vælg **Installerbar softwarepakke** i det delte aktivbibliotek til dit projekt.
4. Vælg **Ny** for at oprette en ny pakke.
5. Angiv et navn til og en beskrivelse af pakken. Du kan bruge **Værktøjet til fornyet klargøring af miljøet** som pakkenavn.
6. Overfør den pakke, du har hentet tidligere.
7. Vælg **Vedligehold** > **Anvend opdateringer** på siden **Miljøoplysninger**.
8. Vælg det værktøj til fornyet klargøring af miljøet, du har overført tidligere, og vælg derefter **Anvend** for at anvende pakken.
9. Overvåg status for installationen af pakken. 

Du kan finde flere oplysninger om, hvordan du anvender en pakke, der kan installeres, i [Anvende en installerbar pakke](../deployment/create-apply-deployable-package.md). Du kan finde flere oplysninger om, hvordan du manuelt anvender en pakke, der kan installeres, i [Anvende en installerbar pakke](../deployment/install-deployable-package.md).
