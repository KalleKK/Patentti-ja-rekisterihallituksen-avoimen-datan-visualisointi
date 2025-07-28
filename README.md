** Datan tuominen ja käsittely **

Tämän projektin tarkoituksena oli visualisoida Patentti - ja Rekisterihallituksen (PRH) suomalaisiin yrityksiin liittyvä data Power BI:n avulla. Datalähteenä toimii PRH:n rajapinta (https://avoindata.prh.fi/fi/ytj/swagger-ui) sekä tilastokeskuksen avoin data, mistä esimerkiksi toin yritysmuodot. 

Datan saa datalähteestä JSON-muodossa, joten päätin hyödyntää Fabricin eri ominaisuuksia datan tuomista varten. Lopullinen ratkaisu oli Fabric dataputki, Lakehouse sekä Notebookit. Tuon kaiken datan batcheina dataputkella Lakehousiin rajapinnasta ja sitten räjäytän auki sekä muokkaan tauluiksi JSON-datan eri hierarkian osiot Notebookeilla. 

Kuva 1, ETL Data-arkkitehtuuri 
<img width="1525" height="983" alt="image" src="https://github.com/user-attachments/assets/efc4c576-aab0-4730-85b9-f61b7ef19a42" />

Kuva 2, JSON-datan tuominen Lakehousista Spark-dataframeksi ja datan muokkaus rakenteelliseksi dataksi 
<img width="2212" height="1080" alt="image" src="https://github.com/user-attachments/assets/c2575d71-77da-4cb0-a96b-2080f62aea77" />

**Raportointi**

Tarkoituksena oli luoda PBI raportti avoimesta datasta. Tein tämän tunnistamalla pari yksinkertaista faktaa, kuten yritysten määrä ja yritysten määrän muutos sekä tunnitamalla, että mitkä ovat mielenkiintoiset dimensiot datassa. Toteutin tietojoukon, raportille oman teeman sekä 3 erilaista sivua datasta. Lopuksi toteutin raportin verkkoon jaettavaksi

Kuva 3, Tietojoukko
<img width="1572" height="921" alt="image" src="https://github.com/user-attachments/assets/95fb3d8e-7d77-48aa-8172-23bbd4805f0c" />

Kuva 4, Raportin etusivu
<img width="2195" height="1134" alt="image" src="https://github.com/user-attachments/assets/038c3643-dce2-4c9d-9166-90f41b680e20" />


Linkki raporttiin
https://app.powerbi.com/view?r=eyJrIjoiMTNkOTNjZTMtNDI2ZC00YmU0LWE2NTQtOWEwNzljOGExMTEzIiwidCI6ImM4NTBmZTljLWI0NmMtNGIyZC1iODYzLTAxZmEyYTg5ODA2OCIsImMiOjh9
