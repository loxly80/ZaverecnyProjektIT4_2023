
# ZaverecnyProjektIT4_2023

V jazyce C# vytvořte formulářovou aplikaci s datovou základnou v SQL Serveru (může být localDB). 

# Popis programované reality

Realizujte správu firmeních procesů ve výrobě a její administraci. 

Administrativa zadává do systému informace o zaměstnancích a spravuje jejich údaje a přístupy do systému. Dále pracovníci administrativy zadávají údaje o realizovaných zakázkách a definují pracovní úkony, které je možné vykonávat v procesu výroby. 

Zaměstnanci ve výrobě po přihlášení do systému zadávají počty odpracovaných hodin při konkrétní činnosti na konkrétní zakázce. Mají možnost editovat svoje záznamy pouze v aktuálním dnu.

# Struktura aplikace

- Do aplikace bude přístup pouze po přihlášení,
- Uživatelům bude možné přidělovat role (každému právě jednu),
- Role uživatelů budou minimálně admin a user,
- Admin může dělat úpravy nad všemi dostupnými datovými zdroji (zobrazovat, vkládat, upravovat a mazat záznamy),
- User může zobrazovat informace o zakázkách a může vkládat záznamy o odpracovaných hodinách, jím vložené záznamy může mazat pokud jsou z aktuálního dne.

# Objektová struktura

Definovaná struktura je minimální požadovaná.

- User (Name, Password) - ochrana hashováním
- Role (Name)
- Employee (PersonalNumber, FirstName, LastName, BirthDate, Email, PhoneNumber)
- Contract (ContractNumber, Customer, Description)
- WorkType (Name, Description)
- WorkHours (Employee, Contract, WorkType, Hours)

Zákazníka realizujte minimálně jako textový záznam, případně můžete jako samostatnou tabulku.

# Požadovaná funkcionalita

- V databázi realizujte tabulky pro uložení potřebných dat. Doplňte indexace a relace podle souvislostí vyplývajících z předchozího popisu.
- V C# použijte .NET Core nebo .NET Framework dle vlastní volby.
- Vnitřní architekturu realizujte pomocí OOP a snažte se co nejlépe oddělit jednotlivé vrstvy aplikace (DataAccess, Core, FrontEnd)
- U zobrazovaných dat v tabulkách realizujte třídění a vyhledávání.
- Uživatelské rozhraní vytvořte libovolně, snažte se však o přehlednost a uživatelský komfort
- Ošetřete všechny možné výskyty nestabilty aplikace (výjimky) 
- Všechny vstupy do databáze ošetřete proti SQL Injection útoku

