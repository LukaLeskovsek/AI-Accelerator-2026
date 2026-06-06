# processed/

Sortirane datoteke. Agent jih premakne sem iz `inbox/`, razdeljene
po podmapah, ki si jih dogovorita.

Tipične podmape (jih agent ustvari sproti):
- `processed/racuni/` — prejeti računi (DDV, podjetje plača)
- `processed/racuni-izdani/` — izdani računi (podjetje izstavlja)
- `processed/sporocila-strank/` — vse, kar pošljejo stranke
- `processed/zapisniki/` — zapisniki sestankov
- `processed/marketing/` — IG, kampanje, vsebina
- `processed/drugo/` — še nedoločeno

Pravilo iz lekcije 4: če nekaj ne sodi v obstoječo podmapo, naj
agent **predlaga** novo, ne ustvari je tiho. Sicer se v treh mesecih
nabere devetnajst kategorij.
