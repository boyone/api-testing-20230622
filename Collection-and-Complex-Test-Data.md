# Collection and Complex Test Data

## Collection Structure

![postman.png](/.attachments/postman-c313a3ab-fbbd-46f3-b426-b82cfebe5d56.png)

## Run newman

```sh
newman run ComplexStructure.postman_collection.json
```

```sh
newman -h
```

```sh
newman run -h
```

## Run newman with Top Level Collection

```sh
newman run ComplexStructure.postman_collection.json --folder Feature01
```

```sh
newman run ComplexStructure.postman_collection.json --folder 'Feature 02'
```

## Run newman with Multiple Top Level Collection

```sh
newman run ComplexStructure.postman_collection.json --folder Feature01 --folder 'Feature 02'
```

## Run newman with Specific Request

```sh
newman run ComplexStructure.postman_collection.json --folder list-users
```

```sh
newman run ComplexStructure.postman_collection.json --folder get-user
```

## Run newman with data file

```sh
newman run ComplexStructure.postman_collection2.json -d newuser.json
```

## Use data file in Request Body

- newuser.json

  ```json
  [
    {
      "name": "J Newman04",
      "username": "j4.newman",
      "email": "j.newman@karina.biz",
      "address": {
        "street": "Kattie Turnpike",
        "suite": "Suite 198",
        "city": "Lebsackbury",
        "zipcode": "31428-2261",
        "geo": {
          "lat": "-38.2386",
          "lng": "57.2232"
        }
      },
      "phone": "024-648-3804",
      "website": "ambrose.net",
      "company": {
        "name": "Hoeger LLC",
        "catchPhrase": "Centralized empowering task-force",
        "bs": "target end-to-end models"
      }
    }
  ]
  ```

1. Inline data with data file

   - Body
     ![inline-data.png](/.attachments/inline-data-c5a53b41-41c9-4ed5-850e-b4642e5104af.png)

2. Inline data object

   - Pre-request Script
     ![pre-request-data.png](/.attachments/pre-request-data-1ab30b95-01bc-492f-b214-339f84c9c7e4.png)

   - Body
     ![inline-with-object.png](/.attachments/inline-with-object-ec372beb-2457-4d47-940e-f591ba871799.png)

3. Use data file in Test

   - Test
     ![test-with-data-file.png](/.attachments/test-with-data-file-5696bf81-c474-41c9-b234-182389d9024d.png)
