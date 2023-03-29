## Description

The ManitobaInstitutes API allows users to getting university and colleges infomation within Manitoba, including the name of the university, the date of establish and the number of students in the university.

## Endpoints

### 1. Get By Name

This endpoint returns the name of the institution, date of establishment and number of attendees. 

**Parameters**

 - **Name**(String) : the name of the institution for which the user wants the information .
 
 **Query**
 
    /institutes/json?name=string
    
### 2. Get By Public or Private

This endpoint returns the name of the institution , date of establishment and number of attendees. 

**Parameters**

- **Public**(true/false) : The user passes true if they want list of all public instutions in Manitoba. The user passes false in the query if they want the list of private instutions in Manitoba.

**Query**

    /institutes/json?public=bool
    
### 3. Get By City

**Parameters**
- **City**(String) : the name of the city for which user wants the list of institutions. 

**Query**

    /institutes/json?city=string

## Resources Description
Response from getting by name:
```json
{
    "name": "String",
    "date_of_establishment": "number",
    "number_of_attendees": "number"
}
```
Response from getting by the type of the institutes:
```json
[{
    "name": "String",
    "date_of_establishment": "number",
    "number_of_attendees": "number"
},
{
    "name": "String",
    "date_of_establishment": "number",
    "number_of_attendees": "number"
}]
```
Response from getting by the city:
```json
[{
    "name": "String",
    "date_of_establishment": "number",
    "number_of_attendees": "number"
}]
```
## Examples
**Request: 1**

    /institutes/json?name=University_of_Manitoba
    
**Response: 1**
```json
{
    "institute":
    {
        "name":"University of Manitoba",
        "date_of_establishment": 1877,
        "number_of_attendees": 30370
    },
    "status": "OK"
}
```
**Request: 2**

    /institutes/json?public=false

**Response: 2**
```json
{
    "result":
    {
        [{
            "name": "Booth University College",
            "date_of_establishment": 1982,
            "number_of_attendees": 700
        },
        {
            "name": "Canadian Mennonite University",
            "date_of_establishment": 1999,
            "number_of_attendees": 1750
        },
        {
            "name": "Providence University College and Theological Seminary",
            "date_of_establishment": 1925,
            "number_of_attendees": 4735
        },
        {
            "name": "Steinbach Bible College",
            "date_of_establishment": 1936,
            "number_of_attendees": 500
        }]
    },
    "status": "OK"
}
```
**Request: 3**

    /institutes/json?city=brandon

**Response: 3**
```json
{
    "result":
    {
        [{
            "name": "Brandon University",
            "date_of_establishment": 1890,
            "number_of_attendees": 3073
        }]
    },
    "status": "OK"
}
```
