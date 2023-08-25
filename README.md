# Greenlight

## Tech used here
| item            | tech                                                                        |
|:-----------------:|:-----------------------------------------------------------------------------:|
| router          | [julienschmidt/httprouter](https://github.com/julienschmidt/httprouter)     |

## PostgreSQL setup
Create database and dedicated user

```sql
-- create database
CREATE DATABASE greenlight;

-- enter database
\c greenlight

-- create a role with password
CREATE ROLE greenlight WITH LOGIN PASSWORD 'greenlight'

-- add extension `citext`
CREATE EXTENSION IF NOT EXISTS citext;

exit
```

Connect it as dedicated user we just created

```bash
$ psql --host=localhost --dbname=greenlight --username=greenlight
```




## Acknowledgment
Take a look [Let's GO further 💞](https://lets-go-further.alexedwards.net/)

