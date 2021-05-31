# Simple Bookshelf API

To run, type on your terminal:

```
npm install
npm run start
```

### How to use

This API can receive all four method requests:

1. Method: POST

   URL: `/books`

   Body Request:

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

2. Method: GET

   URL: `/books`

   Response Body:

   ```
   {
       "status": "success",
       "data": {
           "books": [
               {
                   "id": "Qbax5Oy7L8WKf74l",
                   "name": "Buku A",
                   "publisher": "A"
               },
               {
                   "id": "1L7ZtDUFeGs7VlEt",
                   "name": "Buku B",
                   "publisher": "B"
               },
               {
                   "id": "K8DZbfI-t3LrY7lD",
                   "name": "Buku C",
                   "publisher": "C"
               }
           ]
       }
   }
   ```

3. Method: GET

   URL: `/books/{bookId}`

   Response Body:

   ```
   {
       "status": "success",
       "data": {
           "book": {
               "id": "aWZBUW3JN_VBE-9I",
               "name": "Buku A Revisi",
               "year": 2011,
               "author": "Jane Doe",
               "summary": "Lorem Dolor sit Amet",
               "publisher": "A",
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

4. Method: PUT

   URL: `/books/{bookId}`

   Body Request:

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

5. Method: DELETE

   URL: `/books/{bookId}`