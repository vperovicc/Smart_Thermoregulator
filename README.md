 SmartThermoregulator

 Zadatak projekta je napraviti dizajn sistema, arhitekturu sistema, implementirati i istestirati rešenje koje simulira rad pametnog uređaja za kontrolu temperature. Sistem sadrži jednu centralnu peć čiji se rad kontroliše, regulator temperature i više uređaja za očitavanje temperature prostorija.

#Device

• Poseduje jedinstveni ID

• Proverava temperaturu na svake 3 minute i šalje vrednost temperature regulatoru

• Potrebno je da postoji minimum 4 registrovanih uređaja

#Regulator

• Nudi korisniku UI za podešavanja režima rada regulatora kao i temperature za svaki režim. Regulator poseduje dva različita režima rada: dnevni i noćni. Korisnik mora prvo da unese koji opseg sati u danu predstavlja dnevni režim a zatim preostale sate regulator smatra za noćni režim. Korisnik unosi koju temperaturu želi preko dana a zatim i preko noći. Na osnovu datog podešavanja regulator započinje svoj rad.

• Prima vrednost temperatura od uređaja, čuva ih i zatim na osnovu prosečne temperature i temperature zadate za trenutni režim rada, vrši regulaciju, odnosno izdaje komande centralnoj peći.

• Ukoliko je regulator izdao komandu za paljenje grejača, svim uređajima se šalje informacija da je peć uključena i tada svaki uređaj započinje proces zagrevanja gde se temperatura u okolini uređaja povećava za 0.01 na svaka 2 minuta.

• Regulator i dalje prima vrednosti temperatura od uređaja i određuje kada će se peć ugasiti

• Loguje sve događaje u txt fajl

• Potrebno je da postoji samo jedan regulator

#Heater

• Prima komande za paljenje i gašenje od regulatora i na taj način optimalno troši resurse za održavanje tražene temperature

• Svaki put kada dobije komandu za uključivanje i isključivanje pamti količinu vremena koju je bio uključen u bazi podataka. Pored infomacije o količini radnih sati peć u bazi čuva i informacije o vremenskom trenutku kada je počela da radi kao i količinu resursa koju je potrošila u periodu rada.

• Potrebno je da postoji jedna centralna peć

Sva vremena moraju biti konfigurabilna
