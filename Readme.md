![image](https://github.com/Meusz/API-FOOTBALL/assets/61017010/6de26b5a-7382-4631-a79f-68c66d1b1fde)
# API_FOOTBALL para lesiones<a href="#API_FOOTBALL-para-lesiones" class="anchor-link">¶</a>

Con el codigo aportado, se obtienen datos de lesiones de jugadores en la Premier League y La Liga durante las temporadas 2020-2023


|     | player_id | player_name     | player_photo                                          | player_type       | player_injury_reason     | team_id | team_name        | team_logo                                             | fixture_id | fixture_timezone | fixture_date                | fixture_timestamp | league_id | league_season | league_name | league_country | league_logo                                           | league_flag                                           |
|-----|-----------|-----------------|-------------------------------------------------------|-------------------|--------------------------|---------|------------------|-------------------------------------------------------|------------|------------------|-----------------------------|-------------------|-----------|---------------|-------------|----------------|-------------------------------------------------------|-------------------------------------------------------|
| 0   | 13062     | "Leo Baptistao" | "https:\\/\\/media-4.api-sports.io\\/football\\/pl... | "Missing Fixture" | "Achilles Tendon Injury" | 723     | "Almeria"        | "https:\\/\\/media-4.api-sports.io\\/football\\/te... | 1037952    | "UTC"            | "2023-08-11T17:30:00+00:00" | 1691775000        | 140       | 2023          | "La Liga"   | "Spain"        | "https:\\/\\/media-4.api-sports.io\\/football\\/le... | "https:\\/\\/media-4.api-sports.io\\/flags\\/es.svg"} |
| 1   | 282131    | "M. Svidersky"  | "https:\\/\\/media-4.api-sports.io\\/football\\/pl... | "Missing Fixture" | "Knee Injury"            | 723     | "Almeria"        | "https:\\/\\/media-4.api-sports.io\\/football\\/te... | 1037952    | "UTC"            | "2023-08-11T17:30:00+00:00" | 1691775000        | 140       | 2023          | "La Liga"   | "Spain"        | "https:\\/\\/media-4.api-sports.io\\/football\\/le... | "https:\\/\\/media-4.api-sports.io\\/flags\\/es.svg"} |
| 2   | 47551     | "R. de Tomas"   | "https:\\/\\/media-4.api-sports.io\\/football\\/pl... | "Missing Fixture" | "Injury"                 | 728     | "Rayo Vallecano" | "https:\\/\\/media-4.api-sports.io\\/football\\/te... | 1037952    | "UTC"            | "2023-08-11T17:30:00+00:00" | 1691775000        | 140       | 2023          | "La Liga"   | "Spain"        | "https:\\/\\/media-4.api-sports.io\\/football\\/le... | "https:\\/\\/media-4.api-sports.io\\/flags\\/es.svg"} |
| 3   | 47209     | "A. Martin"     | "https:\\/\\/media-4.api-sports.io\\/football\\/pl... | "Questionable"    | "Injury"                 | 728     | "Rayo Vallecano" | "https:\\/\\/media-4.api-sports.io\\/football\\/te... | 1037952    | "UTC"            | "2023-08-11T17:30:00+00:00" | 1691775000        | 140       | 2023          | "La Liga"   | "Spain"        | "https:\\/\\/media-4.api-sports.io\\/football\\/le... | "https:\\/\\/media-4.api-sports.io\\/flags\\/es.svg"} |
| 4   | 433       | "Marcao"        | "https:\\/\\/media-4.api-sports.io\\/football\\/pl... | "Missing Fixture" | "Muscle Injury"          | 536     | "Sevilla"        | "https:\\/\\/media-4.api-sports.io\\/football\\/te... | 1037956    | "UTC"            | "2023-08-11T20:00:00+00:00" | 1691784000        | 140       | 2023          | "La Liga"   | "Spain"        | "https:\\/\\/media-4.api-sports.io\\/football\\/le... | "https:\\/\\/media-4.api-sports.io\\/flags\\/es.svg"} |

Podemos ver el numero de lesiones por equipo de La Liga a lo largo de las temporadas como en el siguiente ejemplo:

| league_season     | 2020 | 2021  | 2022  | 2023  |
|-------------------|------|-------|-------|-------|
| team_name         |      |       |       |       |
| "Alaves"          | 38.0 | 66.0  | NaN   | 34.0  |
| "Almeria"         | NaN  | NaN   | 117.0 | 73.0  |
| "Athletic Club"   | 54.0 | 142.0 | 115.0 | 58.0  |
| "Atletico Madrid" | 15.0 | 124.0 | 126.0 | 94.0  |
| "Barcelona"       | 35.0 | 243.0 | 103.0 | 53.0  |
| "Cadiz"           | 31.0 | 117.0 | 226.0 | 80.0  |
| "Celta Vigo"      | 45.0 | 54.0  | 79.0  | 31.0  |
| "Eibar"           | 24.0 | NaN   | NaN   | NaN   |
| "Elche"           | 15.0 | 72.0  | 168.0 | NaN   |
| "Espanyol"        | NaN  | 90.0  | 141.0 | NaN   |
| "Getafe"          | 27.0 | 83.0  | 79.0  | 56.0  |
| "Girona"          | NaN  | NaN   | 196.0 | 116.0 |
| "Granada CF"      | 54.0 | 168.0 | NaN   | 37.0  |
| "Huesca"          | 34.0 | NaN   | NaN   | NaN   |
| "Las Palmas"      | NaN  | NaN   | NaN   | 63.0  |
| "Levante"         | 31.0 | 155.0 | NaN   | NaN   |
| "Mallorca"        | NaN  | 140.0 | 121.0 | 28.0  |
| "Osasuna"         | 22.0 | 72.0  | 97.0  | 37.0  |
| "Rayo Vallecano"  | NaN  | 83.0  | 67.0  | 20.0  |
| "Real Betis"      | 31.0 | 158.0 | 140.0 | 82.0  |
| "Real Madrid"     | 55.0 | 166.0 | 115.0 | 99.0  |
| "Real Sociedad"   | 64.0 | 188.0 | 196.0 | 60.0  |
| "Sevilla"         | 5.0  | 142.0 | 164.0 | 104.0 |
| "Valencia"        | 11.0 | 125.0 | 126.0 | 65.0  |
| "Valladolid"      | 29.0 | NaN   | 128.0 | NaN   |
| "Villarreal"      | 27.0 | 103.0 | 148.0 | 75.0  |

O podemos ver los datos segun el tipo de lesion

| league_season            | 2020  | 2021  | 2022  | 2023  |
|--------------------------|-------|-------|-------|-------|
| player_injury_reason     |       |       |       |       |
| "Abdominal strain"       | 7.0   | 20.0  | 2.0   | NaN   |
| "Achilles Tendon Injury" | 2.0   | 39.0  | 66.0  | 9.0   |
| "Ankle Injury"           | 32.0  | 239.0 | 245.0 | 185.0 |
| "Arm Injury"             | 1.0   | 1.0   | 5.0   | NaN   |
| "Back Injury"            | 5.0   | 11.0  | 35.0  | 19.0  |
| "Broken Leg"             | 11.0  | 34.0  | 38.0  | NaN   |
| "Broken ankle"           | 7.0   | NaN   | NaN   | NaN   |
| "Buttock Injury"         | 1.0   | NaN   | NaN   | NaN   |
| "Calf Injury"            | 44.0  | 142.0 | 225.0 | 101.0 |
| "Coach's decision"       | 2.0   | 9.0   | 13.0  | 3.0   |
| "Concussion"             | 8.0   | 1.0   | 7.0   | 1.0   |
| "Convalescence"          | NaN   | NaN   | 1.0   | NaN   |
| "Elbow Injury"           | NaN   | 2.0   | NaN   | NaN   |
| "Eye injury"             | 2.0   | 6.0   | 2.0   | NaN   |
| "Face Injury"            | NaN   | NaN   | 3.0   | NaN   |
| "Finger Injury"          | 2.0   | NaN   | 13.0  | NaN   |
| "Foot Injury"            | 5.0   | 43.0  | 36.0  | 25.0  |
| "Groin Injury"           | 32.0  | 127.0 | 58.0  | 42.0  |
| "Hamstring Injury"       | NaN   | NaN   | 37.0  | 19.0  |
| "Hand Injury"            | NaN   | NaN   | 1.0   | NaN   |
| "Head Injury"            | 3.0   | 12.0  | 21.0  | 3.0   |
| "Health problems"        | NaN   | NaN   | 10.0  | NaN   |
| "Heel Injury"            | NaN   | 4.0   | 7.0   | NaN   |
| "Hernia"                 | 3.0   | 8.0   | NaN   | NaN   |
| "Hip Injury"             | 15.0  | 39.0  | 7.0   | 29.0  |
| "Illness"                | 12.0  | 204.0 | 47.0  | 24.0  |
| "Inactive"               | NaN   | 16.0  | 41.0  | 6.0   |
| "Injury"                 | 14.0  | 61.0  | 210.0 | 181.0 |
| "Knee Injury"            | 165.0 | 489.0 | 690.0 | 331.0 |
| "Knock"                  | 26.0  | 79.0  | 98.0  | 44.0  |
| "Lacking Match Fitness"  | NaN   | 22.0  | 82.0  | 7.0   |
| "Leg Injury"             | 15.0  | 14.0  | 25.0  | 8.0   |
| "Loan agreement"         | 7.0   | 7.0   | 15.0  | 5.0   |
| "Lower Back Injury"      | 4.0   | 31.0  | 2.0   | 4.0   |
| "Muscle Injury"          | 62.0  | 271.0 | 346.0 | 208.0 |
| "National selection"     | NaN   | 53.0  | NaN   | NaN   |
| "Pelvis Injury"          | NaN   | NaN   | 7.0   | 2.0   |
| "Personal Reasons"       | 3.0   | 11.0  | 5.0   | NaN   |
| "Quarantine"             | NaN   | 8.0   | NaN   | NaN   |
| "Red Card"               | NaN   | 58.0  | 63.0  | 40.0  |
| "Rest"                   | NaN   | 1.0   | 9.0   | 1.0   |
| "Ribs Injury"            | 1.0   | NaN   | NaN   | NaN   |
| "Shin Injury"            | 6.0   | 6.0   | NaN   | NaN   |
| "Shoulder Injury"        | 4.0   | 25.0  | 33.0  | 36.0  |
| "Stomach Disorder"       | NaN   | 1.0   | NaN   | NaN   |
| "Surgery"                | NaN   | NaN   | NaN   | 8.0   |
| "Suspended"              | 19.0  | 35.0  | 43.0  | 38.0  |
| "Tendon Injury"          | 2.0   | 5.0   | NaN   | 3.0   |
| "Thigh Injury"           | 75.0  | 392.0 | 461.0 | 255.0 |
| "Toe Injury"             | NaN   | 5.0   | 2.0   | 1.0   |
| "Wrist Injury"           | NaN   | NaN   | 16.0  | 1.0   |
| "Yellow Cards"           | NaN   | 31.0  | 28.0  | 29.0  |


Aunque, vamos solo a destacar aquellas lesiones que importan pues, tarjetas
amarillas etc no nos interesan



| league_season            | 2020.0 | 2021.0 | 2022.0 | 2023.0 |
|--------------------------|--------|--------|--------|--------|
| player_injury_reason     |        |        |        |        |
| "Abdominal strain"       | 7.0    | 20.0   | 2.0    | NaN    |
| "Achilles Tendon Injury" | 2.0    | 50.0   | 125.0  | 44.0   |
| "Ankle Injury"           | 89.0   | 385.0  | 425.0  | 287.0  |
| "Arm Injury"             | 1.0    | 1.0    | 6.0    | NaN    |
| "Back Injury"            | 9.0    | 39.0   | 46.0   | 28.0   |
| "Broken Hand"            | NaN    | 1.0    | NaN    | 2.0    |
| "Broken Leg"             | 11.0   | 41.0   | 38.0   | 16.0   |
| "Broken ankle"           | 7.0    | 2.0    | NaN    | NaN    |
| "Broken calfbone"        | NaN    | NaN    | NaN    | 10.0   |
| "Broken collarbone"      | NaN    | NaN    | 15.0   | NaN    |
| "Broken nose"            | NaN    | 1.0    | 2.0    | NaN    |
| "Broken rib"             | NaN    | NaN    | 1.0    | NaN    |
| "Buttock Injury"         | 1.0    | NaN    | NaN    | NaN    |
| "Calf Injury"            | 61.0   | 188.0  | 265.0  | 135.0  |
| "Collarbone injury"      | NaN    | NaN    | 8.0    | NaN    |
| "Concussion"             | 8.0    | 1.0    | 7.0    | 1.0    |
| "Contusion"              | NaN    | NaN    | 5.0    | 7.0    |
| "Convalescence"          | NaN    | 4.0    | 1.0    | NaN    |
| "Elbow Injury"           | NaN    | 2.0    | NaN    | NaN    |
| "Eye injury"             | 2.0    | 6.0    | 2.0    | NaN    |
| "Face Injury"            | NaN    | NaN    | 4.0    | 6.0    |
| "Finger Injury"          | 11.0   | 11.0   | 24.0   | NaN    |
| "Foot Injury"            | 14.0   | 53.0   | 78.0   | 37.0   |
| "Groin Injury"           | 54.0   | 151.0  | 93.0   | 62.0   |
| "Hamstring Injury"       | NaN    | NaN    | 46.0   | 31.0   |
| "Hand Injury"            | NaN    | 1.0    | 3.0    | NaN    |
| "Head Injury"            | 3.0    | 16.0   | 21.0   | 7.0    |
| "Health problems"        | NaN    | NaN    | 19.0   | NaN    |
| "Heart Problems"         | NaN    | 5.0    | 3.0    | NaN    |
| "Heel Injury"            | NaN    | 4.0    | 7.0    | NaN    |
| "Hernia"                 | 12.0   | 9.0    | NaN    | NaN    |
| "Hip Injury"             | 19.0   | 48.0   | 25.0   | 38.0   |
| "Illness"                | 38.0   | 346.0  | 68.0   | 29.0   |
| "Inactive"               | NaN    | 36.0   | 80.0   | 11.0   |
| "Knee Injury"            | 334.0  | 796.0  | 1215.0 | 695.0  |
| "Knock"                  | 26.0   | 82.0   | 98.0   | 44.0   |
| "Lacking Match Fitness"  | NaN    | 39.0   | 85.0   | 9.0    |
| "Leg Injury"             | 24.0   | 77.0   | 91.0   | 8.0    |
| "Lower Back Injury"      | 4.0    | 31.0   | 2.0    | 4.0    |
| "Muscle Injury"          | 237.0  | 886.0  | 921.0  | 463.0  |
| "Neck Injury"            | NaN    | NaN    | 9.0    | NaN    |
| "Pelvis Injury"          | NaN    | NaN    | 7.0    | 2.0    |
| "Quarantine"             | 1.0    | 11.0   | NaN    | NaN    |
| "Rest"                   | 2.0    | 5.0    | 12.0   | 1.0    |
| "Ribs Injury"            | 1.0    | NaN    | NaN    | NaN    |
| "Shin Injury"            | 6.0    | 6.0    | NaN    | 2.0    |
| "Shoulder Injury"        | 21.0   | 78.0   | 71.0   | 40.0   |
| "Stomach Disorder"       | NaN    | 12.0   | 5.0    | NaN    |
| "Surgery"                | NaN    | 15.0   | NaN    | 10.0   |
| "Tendon Injury"          | 2.0    | 44.0   | 1.0    | 3.0    |
| "Thigh Injury"           | 92.0   | 519.0  | 586.0  | 297.0  |
| "Toe Injury"             | NaN    | 5.0    | 2.0    | 1.0    |
| "Wrist Injury"           | NaN    | 17.0   | 21.0   | 1.0    |


Esto nos puede dar una idea de las lesiones fisicas que sufren los
jugadores, pero vamos a tratar de ver estos datos de manera grafica


# Gafico lineal<a href="#Gafico-lineal" class="anchor-link">¶</a>
![https://github.com/Meusz/API-FOOTBALL/blob/main/Images/Grafico_lineal_tipo_lesiones.png](https://github.com/Meusz/API-FOOTBALL/blob/main/Images/Grafico_lineal_tipo_lesiones.png?raw=true)


Con la grafica anterior, podemos ver datos, que la verdad no son
impactantes. Pues las lesiones mas comunes son las que son mas
llamativas, como la lesion de rodilla, u otros musculos.

Ademas, la grafica no es muy visual. Y ningun dato destaca.

Por ello vamos a buscar otra clase de datos, por ejemplo, el numero de
lesiones por temporada

![Image](https://github.com/Meusz/API-FOOTBALL/blob/main/Images/Grafico_lineal_lesiones_season.png?raw=true)


Ahora, podemos ver datos mas que interesantes, pues como con los años, o
al menos la tendencia durante las ultimas temporadas, es que cada vez
haya mas lesiones. En la temporada 2023, como aun no hemos llegado al
ecuador de la temporada es normal que los datos sean bajos.

Aun asi, llama la atencion que la Premier League, posee mas lesiones.
Esto puede deberse a diversos factores. Entre los mas habituales, puede
ser la exigencia de la liga, pues la Premier es durante ya muchas
temporadas la liga mas competitiva y exigente del mundo. Esto puede
tener consecuencias en sus jugadores. Aunque tambien podria deberse a
los cuidados y seguimientos realizados sobre los jugadores.


# Gafico de Cajas y Bigotes<a href="#Gafico-de-Cajas-y-Bigotes" class="anchor-link">¶</a>

![Image](https://github.com/Meusz/API-FOOTBALL/blob/main/Images/Cajas_y_bigotes.png?raw=true)

Desde la anterior grafica, podemos confirmar la diferencia de lesionados
entre las dos ligas. Pero en esta grafica, podemos ver las medias de
lesionados en ambas ligas. Sobre todo, llama la atencion, como La liga
posee un limite superior de lesionados mas bajo, frente al alto limite
que posee la premier. Podriamos seguir estudiando, o incluso, llegar a
predecir que la Premier, va a tener una tendencia de jugadores
lesionados cada vez mas alta.



# Grafico de Barras<a href="#Grafico-de-Barras" class="anchor-link">¶</a>

![Image](https://github.com/Meusz/API-FOOTBALL/blob/main/Images/Columnas.png?raw=true)
