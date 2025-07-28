**Datan tuominen ja käsittely**

Tämän projektin tarkoituksena oli visualisoida Patentti - ja Rekisterihallituksen (PRH) data Power BI:n avulla. Data liittyy suomalaisiin yrityksiin sekä yritysten tekemiin julkaisuihin. Datalähteenä toimii PRH:n rajapinta (https://avoindata.prh.fi/fi/ytj/swagger-ui) sekä tilastokeskuksen avoin data, mistä esimerkiksi toin yritysmuodot.

Datan saa datalähteestä JSON-muodossa, joten päätin hyödyntää Fabricin eri ominaisuuksia datan tuomista varten. Lopullinen ratkaisu oli Fabric dataputki, Lakehouse sekä Notebookit. Tuon kaiken saatavilla olevan datan dataputkella Lakehousiin PRH:n rajapinnasta ja sitten räjäytän auki sekä muokkaan JSON-datan eri hierarkian osiot notebookeilla rakenteelliseksi dataksi. 

Kuva 1, ETL Data-arkkitehtuuri 
<img width="1525" height="983" alt="image" src="https://github.com/user-attachments/assets/efc4c576-aab0-4730-85b9-f61b7ef19a42" />

Kuva 2, JSON-datan tuominen Lakehousista Spark-dataframeksi ja datan muokkaus rakenteelliseksi dataksi 
<img width="2212" height="1080" alt="image" src="https://github.com/user-attachments/assets/c2575d71-77da-4cb0-a96b-2080f62aea77" />

**Raportointi**

Raportoinnin tarkoituksena oli luoda yleiskatsaus PRH:n dataan ja tuoda esille mielestäni mielenkiintoisia trendejä/havaintoja. Toteutuksen aloitin tunnistamalla mielenkiintoiset faktat - ja dimensiot ja luomalla mittarit sekä semanttisen tietomallin. Pidin myös tärkeänä, että raportin visualisointeja pystyi suodattamaan maantieteellisesti, joten toin raportille mukaan maakunta - ja kunta suodatuksen hyödyntämällä PRH_n datassa olevaa yrityksen osoitetta. Mielenkiintoisiksi asioiksi nousi itselläni taloudelliset vaikeudet, mitkä sain laskemalla yritysten tekemistä julkaisuista (Konkurssi, saaneeraus yms) sekä yritysten määrä toimialan mukaan historiallisesti. Toteutin myös raportille oman teeman. 

Kuva 3, Tietojoukko
<img width="1572" height="921" alt="image" src="https://github.com/user-attachments/assets/95fb3d8e-7d77-48aa-8172-23bbd4805f0c" />

Kuva 4, Raportin etusivu
<img width="2195" height="1134" alt="image" src="https://github.com/user-attachments/assets/038c3643-dce2-4c9d-9166-90f41b680e20" />


Linkki raporttiin
https://app.powerbi.com/view?r=eyJrIjoiMTNkOTNjZTMtNDI2ZC00YmU0LWE2NTQtOWEwNzljOGExMTEzIiwidCI6ImM4NTBmZTljLWI0NmMtNGIyZC1iODYzLTAxZmEyYTg5ODA2OCIsImMiOjh9
