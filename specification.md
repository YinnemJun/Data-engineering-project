# Házi Feladat Specifikáció
**Data Engineering** - Opcionális házi feladat

---

## 1. Hallgató adatai

| | |
|---|---|
| **Yin Jun** | |
| **TN1KZI** | |
| **1171276297yin@gmail.com** | |

---

## 2. Témaválasztás

| | |
|---|---|
| **steam-tracker** | |


> Ez a pipeline egy automatizált adatfolyamba integrálja a Steam legnépszerűbb játékainak valós idejű játékosszámát a Steam REST API ([link](https://partner.steamgames.com/doc/webapi/ISteamUserStats)) és egy Kaggle CSV fájl ([link](https://www.kaggle.com/datasets/nikdavis/steam-store-games)) felhasználásával. A folyamat eredménye egy dashboard, amely bemutatja a különböző játékok játékosbázisának alakulását a nap folyamán és egyéb játék adataik.

---

## 3. Tervezett pipeline elemei

| Elem | Tervezett megoldás / eszköz |
|---|---|
| **Adatforrások**  | REST API + CSV fájl |
| **Feldolgozási mód** | Batch  |
| **Landing zone**  | MinIO|
| **Adatmodell típusa** |Csillag séma – 1 ténytábla(fact_player_activity) + 2 dimenziótábla(dim_games + dim_time) |
| **Adattárház / adatplatform** |PostgreSQL|
| **Transzformáció** | dbt, Spark SQL |
| **Orchestration eszköz** |Apache Airflow |
| **Infrastruktúra** |Docker Compose |
| **Adatkiszolgálás** |Metabase dashboard |

---