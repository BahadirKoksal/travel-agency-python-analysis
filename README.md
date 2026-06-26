# 🧳 Travel Agency Database Challenge

Python project building a functional city database and geolocation-based search engine for a travel agency.

---

## Objective

A travel agency stores information about the cities it operates in as a Python dictionary database. The goal of this project is to build a set of reusable functions that allow the agency to retrieve, update, and search city data — culminating in a proximity-based search engine that recommends nearby destinations to customers.

---

## Dataset

A manually defined list of city dictionaries, each containing:

| Field | Description |
|---|---|
| `name` | City name |
| `total_population` | Total population |
| `continent` | Continent |
| `location` | `[latitude, longitude]` coordinates |
| `area` | Nested dictionary with `prefecture_level` (km²) |

Cities included: Paris, Xi'an, Chengdu, Los Angeles, Brooklyn

---

## Project Steps

### 1. Data Exploration
Explored the structure of a single city dictionary — accessing nested values, identifying data types (`list`, `dict`), and extracting fields like `prefecture_level` and `longitude`.

### 2. Single-City Lookup Function
Built `get_key_value_from_city(city, key)` — a reusable function that returns the value for any key in a city dictionary, with a fallback message if the key doesn't exist.

### 3. Database Retrieval Function
Extended the logic to `retrieve_city_key_value_database(city_name, key)` — loops through the full cities list, matches by name, and returns the requested value. Returns `"city not available or not covered"` for unknown cities.

### 4. Database Update Function
Built `modify_city_key_value(city_name, key, value)` — updates an existing key for a given city and returns a confirmation message. Handles three scenarios:
- City not found
- Key not found
- Successful update

### 5. Geolocation Search Engine
Used the `geopy` library to calculate geodesic distances between coordinates. Built `get_cities_nearby(customer_location, radius)` — takes a `[lat, lon]` coordinate and a radius in km, and returns all cities within range.

**Example:** A customer near Guangyan, China (32.4355, 105.8436) with a 500 km radius → returns Xi'an and Chengdu.

---

## Key Skills Demonstrated

| Skill | Application |
|---|---|
| Python dictionaries | Storing and accessing nested city data |
| Functions & arguments | Reusable, parameterised logic |
| Loops & conditionals | Iterating city lists, key-existence checks |
| f-strings | Dynamic return messages |
| Geopy library | Geodesic distance calculation |
| Pseudocode planning | Structuring logic before coding |

---

## Technology

Python · Geopy

---

## Notebook

[Travel_agency_database_challenge.ipynb](./Travel_agency_database_challenge.ipynb)
