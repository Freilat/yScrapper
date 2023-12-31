# yScrapper

## Laravel / Vue.js task

### Create a scraper that reads data from https://news.ycombinator.com/ (title, link, points, date created)
* Store data to a local database (Postgres or MySQL)
* Scraper also must update points for each article
* It must be run from the console
 
### Create frontend part:
* Accessible only by username/password (user data must be in DB)
* Display all scraped information using DataTables, 10 entries per package
* Add the possibility to delete an item - if it’s deleted, then do not update it from Hacker News.
 
Create a readme file on how to set up the site
Put all code in github/gitlab repository.
 
Bonus points: Docker usage, Unit tests.


## Setup


To set up this project You should install [Docker](https://www.docker.com/products/docker-desktop/) and then clone [this](https://github.com/Freilat/yScrapper) project. After that You cd into project and continue with comands below. 

```
cp .env.example .env

```
```
docker run --rm -u "$(id -u):$(id -g)" -v "$(pwd):/var/www/html" -w /var/www/html laravelsail/php82-composer:latest composer install --ignore-platform-reqs

```
```

sail down -v && sail build --no-cache && sail up

```
```
sail npm install

```
```
sail php artisan migrate
```
```
sail php artisan db:seed

```
```
sail npm run dev
```



### To run scraper:
```
sail php artisan scrapper:run
```
### To log in You can use
user: 
```
test@example.com
```
password:

```
password
```
