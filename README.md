# Konvoliuciniai-neuroniniai-tinklai

## Projekto tikslas

Darbe siekiama eksperimentuoti su konvoliuciniais neuroniniais tinklais (CNN) norint išanalizuoti ir optimizuoti modelio architektūras, aktyvacijos funkcijas ir kitus parametrus vaizdų klasifikavimo užduotyje.

## Duomenų apdorojimas

- Automatiškai atsisiunčiamas „Rock-Paper-Scissors“ paveikslėlių rinkinys iš GitHub, duomenys išpakuojami ir apdorojami.
- Vaizdai normalizuojami, išskiriamos spalvų klasės, paveikslėliai padidinami, transformuojami į tinkamą formatą tinklams apmokyti.
- Sukuriama žymių žemėlapis („rock“, „paper“, „scissors“) ir suskirstoma į mokymo, validavimo ir testavimo imtis.

## CNN modelio konstravimas ir eksperimentai

- Yra kelios CNN architektūrų variacijos: sekli, vidutinė ir giliausia.
- Pasirenkamos aktyvacijos funkcijos (ReLU, LeakyReLU, sigmoidinė).
- Į modelį integruojamas dropout (sluoksnių kiekis ir tikimybė kinta), galimas batch normalizavimas.
- Modelio apmokymas vyksta pasirenkant optimizatorių (Adam, SGD, RMSProp).

## Mokymo eiga ir optimizavimas

- Apmokomas modelis per kelias epochas, metrikos stebimos: tikslumas, nuostolis (loss) – tiek mokymo, tiek validavimo ir testavimo aibėse.
- Funkcija `train_and_validate` apdoroja visą mokymo ciklą, skaičiuoja tikslumą/nuostolį, grąžina prognozes ir realias žymes.
- Modelių veikimas lyginamas pagal architektūrą, aktyvacijos funkciją, dropout ir batch normalizavimą, galutiniai rezultatai pateikiami lentelėse su pandas DataFrame.

## Hyperparametrų paieška

- Naudojamas Optuna Bayes optimizacijos įrankis, kuris automatiškai ieško optimalių modelio parametrų (architektūra, aktyvacija, dropout, sluoksnių kiekis, optimizatorius, norminimas).
- Geriausi parametrai parenkami pagal validavimo tikslumą.

## Rezultatų vizualizacija ir analizė

- Skirtingų modelio architektūrų, aktyvacijų, dropout, batch normalizavimo ir optimizatorių palyginimai vizualizuojami grafikuose.
- Vaizduojama klasifikavimo matrica ir rezultatai.
- Atsitiktinai parenkama testinių įrašų imtis, kurioje spėjama ir tikra klasė lyginama tekstu.
- Išsamiai analizuojami eksperimento rezultatai.

## Apibendrinimas

Darbas leidžia išbandyti įvairias CNN architektūras, optimizacijos metodikas ir parametrų rinkinius su realiais vaizdų duomenimis.
