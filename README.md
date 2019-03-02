# Cactus app
Cactus app is an open source service to stream your favorite anime.

## Services
|  [Client Repo](https://github.com/Krystian19/cactus-app-client-service) | [Backend Repo](https://github.com/Krystian19/cactus-app-backend-service/tree/master) | [Admin Repo](https://github.com/Krystian19/cactus-app-backend-admin-service/tree/master) |
|:---------------------:|:---------------------:|:---------------------:|
| [![Build Status](https://travis-ci.org/Krystian19/cactus-app-client-service.svg?branch=master)](https://travis-ci.org/Krystian19/cactus-app-client-service) [![Code Climate](https://codeclimate.com/github/Krystian19/cactus-app-client-service/badges/gpa.svg)](https://codeclimate.com/github/Krystian19/cactus-app-client-service) [![Test Coverage](https://codecov.io/gh/Krystian19/cactus-app-client-service/branch/master/graph/badge.svg)](https://codecov.io/gh/Krystian19/cactus-app-client-service) | [![Build Status](https://travis-ci.org/Krystian19/cactus-app-backend-service.svg?branch=master)](https://travis-ci.org/Krystian19/cactus-app-backend-service) [![Code Climate](https://codeclimate.com/github/Krystian19/cactus-app-backend-service/badges/gpa.svg)](https://codeclimate.com/github/Krystian19/cactus-app-backend-service) [![Test Coverage](https://codecov.io/gh/Krystian19/cactus-app-backend-service/branch/master/graph/badge.svg)](https://codecov.io/gh/Krystian19/cactus-app-backend-service) | [![Build Status](https://travis-ci.org/Krystian19/cactus-app-backend-admin-service.svg?branch=master)](https://travis-ci.org/Krystian19/cactus-app-backend-admin-service) [![Code Climate](https://codeclimate.com/github/Krystian19/cactus-app-backend-admin-service/badges/gpa.svg)](https://codeclimate.com/github/Krystian19/cactus-app-backend-admin-service) [![Test Coverage](https://codecov.io/gh/Krystian19/cactus-app-backend-admin-service/branch/master/graph/badge.svg)](https://codecov.io/gh/Krystian19/cactus-app-backend-admin-service) |

|  [Image CDN Repo](https://github.com/Krystian19/cactus-fake-image-cdn-service/tree/master) | [Video CDN Repo](https://github.com/Krystian19/cactus-fake-video-cdn-service/tree/master) |
|:---------------------:|:---------------------:|
| [![Build Status](https://travis-ci.org/Krystian19/cactus-fake-image-cdn-service.svg?branch=master)](https://travis-ci.org/Krystian19/cactus-fake-image-cdn-service) [![Code Climate](https://codeclimate.com/github/Krystian19/cactus-fake-image-cdn-service/badges/gpa.svg)](https://codeclimate.com/github/Krystian19/cactus-fake-image-cdn-service)  [![Test Coverage](https://codecov.io/gh/Krystian19/cactus-fake-image-cdn-service/branch/master/graph/badge.svg)](https://codecov.io/gh/Krystian19/cactus-fake-image-cdn-service) | [![Build Status](https://travis-ci.org/Krystian19/cactus-fake-video-cdn-service.svg?branch=master)](https://travis-ci.org/Krystian19/cactus-fake-video-cdn-service) [![Code Climate](https://codeclimate.com/github/Krystian19/cactus-fake-video-cdn-service/badges/gpa.svg)](https://codeclimate.com/github/Krystian19/cactus-fake-video-cdn-service) [![Test Coverage](https://codecov.io/gh/Krystian19/cactus-fake-video-cdn-service/branch/master/graph/badge.svg)](https://codecov.io/gh/Krystian19/cactus-fake-video-cdn-service) |

## Modules
|  [GraphQL Schema](https://github.com/Krystian19/cactus-app-schema-module/tree/master) | [JS DB module](https://github.com/Krystian19/cactus-app-db-module/tree/master)|
|:---------------------:|:---------------------:|
| [![Build Status](https://travis-ci.org/Krystian19/cactus-app-schema-module.svg?branch=master)](https://travis-ci.org/Krystian19/cactus-app-schema-module) [![Code Climate](https://codeclimate.com/github/Krystian19/cactus-app-schema-module/badges/gpa.svg)](https://codeclimate.com/github/Krystian19/cactus-app-schema-module) [![Test Coverage](https://codecov.io/gh/Krystian19/cactus-app-schema-module/branch/master/graph/badge.svg)](https://codecov.io/gh/Krystian19/cactus-app-schema-module)      | [![Build Status](https://travis-ci.org/Krystian19/cactus-app-db-module.svg?branch=master)](https://travis-ci.org/Krystian19/cactus-app-db-module) [![Code Climate](https://codeclimate.com/github/Krystian19/cactus-app-db-module/badges/gpa.svg)](https://codeclimate.com/github/Krystian19/cactus-app-db-module) [![Test Coverage](https://codecov.io/gh/Krystian19/cactus-app-db-module/branch/master/graph/badge.svg)](https://codecov.io/gh/Krystian19/cactus-app-db-module)

## Screenshots
![Alt text](screenshots/view1.png?raw=true "Anime Description view")

# How to Setup

## IMPORTANT!!! - Make sure you have these installed, before doing anything ...
```sh
docker -v
  Docker version 18.03.0-ce # Or later

git-lfs --version
  git-lfs/2.5.2 (GitHub; darwin amd64; go 1.11) # Or later
```

Clone this project with all of it's modules recursively (it's a little heavy, so it'll take a bit):

```sh
git clone --recurse-submodules git@github.com:Krystian19/cactus-app.git
```

And start the project with:
```sh
docker-compose up -d
```

Then run the seeders to have some basic data ...
```sh
# Run the seeders
docker exec -ti cactus_app_backend_admin /code/seeds.sh
```

And voilà, the web client should be running @ http://localhost:5000/

## Todo list
+ - [ ] Release dates in Anime thumbnails should show the realease year accurately
+ - [x] Backend admin's service API should have a limit for the maximum of records to retrieve at a time
+ - [ ] Setup a way in the anime info view to connect with the next season
+ - [ ] Find and implement a better design for the current video player component
+ - [x] Move error image placeholder and missing images placeholders to the client's server
+ - [ ] Setup pagination for the Genre schemas and the client's Genre view
+ - [ ] Setup name search for the Genre schemas and the client's Genre view
+ - [ ] Implement a not found page for for requests outside of client or content that is not found
+ - [ ] Add more series to the backend-admin's seeding script data
+ - [ ] Create an error component to show if the client's requests fails
+ - [x] Create a server-side error page to show if the initial ApolloClient SSR request fails
+ - [ ] Setup Category filters for the search view
  + - [ ] Implement Category filtering Component for the search view
+ - [ ] Setup multi-language support for the client
  + - [ ] Setup English language support for the client
  + - [ ] Setup Spanish language support for the client
+ - [ ] Complete missing tests of backend admin's models
+ - [ ] Complete model tests for the db module
+ - [ ] Study how to convert the Frontend app in a Desktop native app

## License
MIT © [Jan Guzman](https://github.com/Krystian19)
