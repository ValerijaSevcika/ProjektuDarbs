# Vārda tulkojums tekstā

## Projekta uzdevums - atvieglot teksta lasīšanu angļu valodā ar nepazīstamām vārdiem

Šīs projekts tika domāts cilvēiem, kam gribas lasīt informāciju(zinātniskus rakstus,pētījumus, svarīgus dokumentus un t.t.) angļu valodā, bet ir daži nezināmi termini. Lasot informāciju, paliek garlaicīgi tulkojot vienu un to pašu vārdu vairākas reizēs, kamēr nebūs iemācīts vārds no galvas. Tāpēc tika izdomāta programma, kur vienu reizu ievietojot nezināmu vārdu, tekstā pēc katra šī termina tika ievetots tulkojums iekavās un uzreiz būs redzams tulkojums, kas samazinās ne tikai laiku, bet arīvar palīdzēt vārdu iegaumēšaana.

## Izmantotas bibliotēkas
1. seleium
    Šī bibliotēka ir domāta lai strādāt ar tīmekļiem un kodā tika izmantoti:
        1. from selenium import webdriver - kas dod iespēju veikt dabības tīmekļa lapā un vadīt pārlūkprogrammu
        2. from selenium.webdriver.chrome.service import Service - ar to atvēras Chrome lapa, kur jau parādas iespēja veikt darbības
        3. from selenium.webdriver.common.by import By - šī apakšbibliotēka palīdz indificēt HTML elementus tīmekļa lapā. Šeit izmantojas 
           indifikatori kuri parāda tīmekļa lapas konkrētu vietu un/vai darbību

2. openpyxl
    Openpyxl bibliotēka palīdz strādāt ar Excel failiem - lasīt un veikt tur izmaiņas
3. time
    Bibliotēka time dod iespēju ielikt laiku pa kuru izvēlētai darbībai ir jābūt izpildītai
4. csv
    Pēdēja izmantotta bibliotēka CSV ir domāta, lai strādāt ar csv failiem - lasīt un veikt tur izmaiņas

## Izmantosanas metodes

Pirmkārt, lai strādāt ar tekstu, ir jāsāk ar jaunju vārdu ievietošanai. Tālāk Excel failu ver iezmantot kā arī tulkotāju. Priekš vieglākai izmantošanaj šajā gadījumā vārdi tiek sakārtoti alfabētiskā secībā. Bet ir jāņēm vērā, ka vārdu kombinācijas nebūs iespējas pārtulkot tekstā, tāpēc labāk ievietot vārdus pa vienam, lai tālāk izmantotu teksta tulkojumā. Ja vards jau būs ievietots failā, tas automātiski nepievienojas.

Otrkart, ir iespēja atrast konkrētu vārdu no Excel failā. Lietotājam tiek dota iespēja izvēlēties valodu, kurā viņi vēlās meklēt vārdu - angļu vai latviešu valodā. Jā ievadīta vārda nav sarakstā, programma paziņos to, bet ja vārds tika ievietots angļu valodā, lietotājam piedāvā pievienot to failā.

Un vissvarigākais, nezināmu valodu tulkošana. Programma prasa ievietot vēlamu tekstu. Programma salīdzina vārdus terminālā un Excel failā un ja paradās, ka ir vienādi vārdi, tad csv failā aiz nezināmam un ievietotam Excel faila vārdiem iekavās parādas tulkojums latviešu valodā. Jābūt uzmanīgam, ka ievadot jaunu tekstu, vecais tika dzēsts.