


# FastAPI Book Project

A containerized FastAPI application for managing books, set up with Docker Compose and Nginx as a reverse proxy.




## Project Structure


````
fastapi-book-project/
├── api/                # FastAPI logic: routes, schemas, db
│   ├── db/
│   ├── routes/
│   └── router.py
├── core/               # App settings and configuration
├── deployment/         # Nginx reverse proxy configuration
│   └── nginx.conf
├── tests/              # Unit tests for the API
├── main.py             # App entry point
├── Dockerfile          # Docker image build instructions
├── docker-compose.yml  # Multi-container setup
├── requirements.txt    # Python dependencies
└── README.md           # Project documentation

````

</br>


# Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/ntando-mv15/fastapi-book-project.git
cd fastapi-book-project
```

### 2. Start the App with Docker Compose

```bash
docker compose up
```

### 3. Open in Browser

```
http://localhost/8080
```

>  Make sure port `8080` is not in use on your system.



## Services                            

`fastapi` - The FastAPI application (on port 8000) 

 `nginx`  - Reverse proxy, exposed on port 8080    

Nginx receives all traffic and forwards it to the FastAPI app.


## Nginx Configuration

Nginx is configured to:

* Listen on port 80 (mapped to 8080 on your host)
* Forward requests to the FastAPI container on port 8000


Config file: [`deployment/nginx.conf`](./deployment/nginx.conf)


## Clean Up

To stop and remove all containers, networks, and volumes:

```bash
docker compose down -v
```

</br>

## Notes

- This project was cloned and updated to support Docker for development and production, using Nginx.

- If you'd like to contribute or report issues, feel free to open a PR or issue on GitHub.




