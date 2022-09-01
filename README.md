# <a href="https://bookseft-api.herokuapp.com/books" target="_BLANK"> Bookhelf-API </a>

<a href="https://bookseft-api.herokuapp.com/books" target="_BLANK"> Bookhelf-API </a>

### API dapat menyimpan buku
> Method : POST <br>
> URL : /books <br>
> Body Request: <br>
 ```
   {
      "name": string,
      "year": number,
      "author": string,
      "summary": string,
      "publisher": string,
      "pageCount": number,
      "readPage": number,
      "reading": boolean
  }
 ```
 
 ### API dapat menampilkan seluruh buku
> Method : GET <br>
> URL: /books <br>
> Response Body : <br>
```
  {
      "status": "success",
      "data": {
          "books": []
      }
  }
```

### API dapat menampilkan detail buku
> Method : GET <br>
> URL: /books/{bookId} <br>
> response Body:
  >> #### Status Code 404
  ```
  {
    "status": "fail",
    "message": "Buku tidak ditemukan"
  }
  ```
 >> #### status code 200
 ```
  {
    "status": "success",
    "data": {
        "book": {
            "id": "aWZBUW3JN_VBE-9I",
            "name": "Judul Buku",
            "year": 2011,
            "author": "Romando",
            "summary": "Lorem Dolor sit Amet",
            "publisher": "Romando",
            "pageCount": 200,
            "readPage": 26,
            "finished": false,
            "reading": false,
            "insertedAt": "2021-03-05T06:14:28.930Z",
            "updatedAt": "2021-03-05T06:14:30.718Z"
          }
        }
    }
   ```
### API dapat mengubah data buku
> Method : PUT
> URL : /books/{bookId}
> Body Request:
  ```
  {
    "name": string,
    "year": number,
    "author": string,
    "summary": string,
    "publisher": string,
    "pageCount": number,
    "readPage": number,
    "reading": boolean
  }
  ```
  
### API dapat menghapus buku
> Method : DELETE
> URL: /books/{bookId}
> Response Body :
  ```
  {
    "status": "success",
    "message": "Buku berhasil dihapus"
  }
  ```

### Tambahan
> Method: GET<br>
> Path: /books?{query_parameter}
>> ?name : `Tampilkan seluruh buku yang mengandung nama berdasarkan nilai yang diberikan pada query ini.` <br>
>> ?reading : `Bernilai 0 atau 1. Bila 0, maka tampilkan buku yang sedang tidak dibaca (reading: false). Bila 1, maka tampilkan buku yang sedang dibaca (reading: true). Selain itu, tampilkan buku baik sedang dibaca atau tidak.` <br>
>> ?finished : `Bernilai 0 atau 1. Bila 0, maka tampilkan buku yang sudah belum selesai dibaca (finished: false). Bila 1, maka tampilkan buku yang sudah selesai dibaca (finished: true). Selain itu, tampilkan buku baik yang sudah selesai atau belum dibaca.` <br>


## View App
<a href="https://bookseft-api.herokuapp.com/books" target="_BLANK"> Bookhelf-API </a>
