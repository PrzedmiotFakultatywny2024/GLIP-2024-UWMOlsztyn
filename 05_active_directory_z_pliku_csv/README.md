# Zadanie 5 - Zasilenie Katalogu Użytkowników

> Cel zadania: zasilenie platformy GLPi informacjami o użytkownikach i grupach.

## Sposób dostarczenia informacji o użytkownikach może być

- manualny (na zaliczenie)
- skryptami PowerShell (na piątkę)

## Warunki zadania

Użytkownicy w ActiveDirectory powinni:

- mieć wypełnione wszystkie atrybuty AD opisowe (zaznaczone na zielono)
- mieć wypełniony atrybut AD o nazwie Street połączonym opisem pól z csv ulica + numer budynku + numer pomieszczenia
- być rozlokowani po przyporządkowanych Organization Units (pole csv Obszar, atrybut AD DistinguishedName)
- mieć ustawionego przełożonego atrybut AD Manager
- mieć ustawione hasło: `!1Olsztyn`
- mieć aktywne konto AD
- mieć ustawione `hasło nigdy nie wygasa`
- mieć ustawione `użytkownik nie może zmienić sobie hasła`
- mieć członkostwo w przypisanych grupach pola csv : `Grupa1`, `Grupa2`, `Grupa3`.

Miejsce składowania csv – LINK do SCV

**UWAGA:** przed zasileniem ActiveDirectory należy pobrać csv i poprawnie sformatować separatory i stronę kodowania (utf8)

## Przydatne linki

- [How to Create New Active Directory Users with PowerShell](https://blog.netwrix.com/2018/06/07/how-to-create-new-active-directory-users-with-powershell/)
- [Using the Set-ADUser Cmdlet to Modify Properties of Active Directory Users](https://blog.netwrix.com/2023/06/21/set-aduser-cmdlet-for-managing-active-directory-user-properties/)
- [How to Create New Active Directory Users with PowerShell](https://blog.netwrix.com/2018/06/07/how-to-create-new-active-directory-users-with-powershell/)
- [Using the Set-ADUser Cmdlet to Modify Properties of Active Directory Users](https://blog.netwrix.com/2023/06/21/set-aduser-cmdlet-for-managing-active-directory-user-properties/)
- [How to Use Get-ADGroup in PowerShell](https://blog.netwrix.com/2023/05/24/get-ad-group-powershell-cmdlet/)

- Pomocne frazy w Google: „powershell bulk create ad users from csv file”

## Terminy

- Czas realizacji: sobota 2024-05-11 godz. 12:00.
- Przekroczenie terminu: 1 ocena w dół (maksymalnej oceny) za każde 2 tyg. przekroczenie.

## Rozliczenie zadania

1. Opisz w tym dokumencie w krokach sposób realizacji zadania dodając screanshooty.
2. Dołącz w dokumencie listę users.csv wygenerowaną komendą:

```powershell
Get-ADUser –Filter {employeeid –like ‘\*’} –Properties employeeid | Export-csv –Path C:\tmp\users.csv –NoTypeInformation –Encoding utf8
```

1. Zapisz dokument w folderze grupowym na GitHub.
2. Kierownik grupy odpowiedzialny za całość, recenzja wykonania ze wskazania kierownika grupy.
