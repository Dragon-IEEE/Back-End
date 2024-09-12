# Back-End
for Back-End App


How to use the app 

1:download the app from github
2:create .env file  beside  .env.example file 
3:copy what inside  .env.example file  in the .env file
4: add 

this code

    DB_CONNECTION=mysql

    DB_HOST=127.0.0.1

    DB_PORT=3306

    DB_DATABASE=Dragon_IEEE

    DB_USERNAME=root

    DB_PASSWORD=

    to .env file     to create the DB

5: open terminal  and use php artisan serve 

6:open the server and start using api like the Restaurants example

(maybe you need add some data to db to use it )






Restaurants:-

    Get all  Restaurants

        (1) Request :

            [GET]  http://127.0.0.1:8000/api/restaurants


        (2) Response:

            [
                {
                    "id": 3,
                    "name": "res kok",
                    "address": "five's street",
                    "latitude": "7.00000000",
                    "longitude": "6.70000000",
                    "user_ratings": "3.70",
                    "created_at": "2024-09-12T12:53:19.000000Z",
                    "updated_at": "2024-09-12T16:42:40.000000Z"
                },
                {
                    "id": 4,
                    "name": "res you",
                    "address": "oop 999",
                    "latitude": "7.00000000",
                    "longitude": "6.70000000",
                    "user_ratings": "3.70",
                    "created_at": "2024-09-12T16:41:24.000000Z",
                    "updated_at": "2024-09-12T16:41:24.000000Z"
                },
                {
                    "id": 5,
                    "name": "res fried",
                    "address": "99's street",
                    "latitude": "7.40000000",
                    "longitude": "6.70000000",
                    "user_ratings": "3.20",
                    "created_at": "2024-09-12T16:44:45.000000Z",
                    "updated_at": "2024-09-12T16:44:45.000000Z"
                }
            ]




    Get a single  Restaurant

        (1) Request : 
            [GET] http://127.0.0.1:8000/api/restaurants/3

        (2) Response:

            {
                "id": 3,
                "name": "res kok",
                "address": "five's street",
                "latitude": "7.00000000",
                "longitude": "6.70000000",
                "user_ratings": "3.70",
                "created_at": "2024-09-12T12:53:19.000000Z",
                "updated_at": "2024-09-12T16:42:40.000000Z"
            }




        Create A Restaurant

        (1) Request : 
            [POST] http://127.0.0.1:8000/api/restaurants

            {
                "name": "res pop ",
                "address": " 66's street ",
                "latitude": "4.4",
                "longitude": "5.7",
                "user_ratings": "3.2"
            }
        
        (2) Response:
            {
                "id": 6,
                "name": "res pop",
                "address": "66's street",
                "latitude": "4.40000000",
                "longitude": "5.70000000",
                "user_ratings": "3.20",
                "created_at": "2024-09-12T16:54:19.000000Z",
                "updated_at": "2024-09-12T16:54:19.000000Z"
            }


        Update A Restaurant 
            (1) Request: 

            [PUT]  http://127.0.0.1:8000/api/restaurants/5

            {
                "name": "res JIN ",
                "address": " 505's street ",
                "latitude": "9.4",
                "longitude": "8.7",
                "user_ratings": "3.2"
            }

                (2) Response:
                     {
                        "id": 5,
                        "name": "res JIN",
                        "address": "505's street",
                        "latitude": "9.40000000",
                        "longitude": "8.70000000",
                        "user_ratings": "3.20",
                        "created_at": "2024-09-12T16:44:45.000000Z",
                        "updated_at": "2024-09-12T16:59:44.000000Z"
                    }


    Delete a Restaurant

        (1) Request: 

        [DELETE] http://127.0.0.1:8000/api/restaurants/3

        (2) Response:

        TRUE (IN MY APP RETURN )
        {
                "message": " Restaurant deleted correctly"
        }

