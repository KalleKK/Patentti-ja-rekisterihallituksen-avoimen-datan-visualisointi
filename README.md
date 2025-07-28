<img width="1525" height="983" alt="image" src="https://github.com/user-attachments/assets/97b9dcda-f88a-4af4-87cd-81fd321f1aee" /># Patentti-ja-rekisterihallituksen-avoimen-datan-visualisointi

Tämän projektin tarkoituksena oli visualisoida Patentti - ja Rekisterihallituksen (PRH) suomalaisiin yrityksiin liittyvä data. Datalähteenä toimii PRH:n rajapinta (https://avoindata.prh.fi/fi/ytj/swagger-ui) sekä tilastokeskuksen avoin data, mistä esimerkiksi toin yritysmuodot. 

Datan saa datalähteestä JSON-muodossa, joten päätin hyödyntää Fabricin eri ominaisuuksia datan tuomista varten. Lopullinen ratkaisu oli Fabric dataputki, Lakehouse sekä Notebookit. Tuon kaiken datan batcheina dataputkella Lakehousiin rajapinnasta ja sitten räjäytän auki sekä muokkaan tauluiksi JSON-datan eri hierarkian osiot Notebookeilla. 

Kuva 1, ETL Data-arkkitehtuuri 
<img width="1525" height="983" alt="image" src="https://github.com/user-attachments/assets/efc4c576-aab0-4730-85b9-f61b7ef19a42" />

Kuva 2, JSON-datan tuominen Lakehousista Spark-dataframeksi ja datan muokkaus rakenteelliseksi dataksi 

<img width="2212" height="1080" alt="image" src="https://github.com/user-attachments/assets/c2575d71-77da-4cb0-a96b-2080f62aea77" />

