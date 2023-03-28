
## Description

Our API is for finding Institutes in Manitoba. We can filter the return objects by passing parameters for whether the institute is public or private, by its name, or by the city its in.

## Endpoints

### Get By Name

This endpoint returns the name of the institution , date of establishment and number of attendees . 

**Parameters**

 - name : the name of the institution for which the user wants the information .
 
 **Query**
 
    /institutes/json?name=string
    
### Get By Public or Private

This endpoint returns the name of the institution , date of establishment and number of attendees . 

**Parameters**

- public (true/false) : The user passes true if they want list of all public instutions in Manitoba .The user passes false in the query if they want the list of private instutions in Manitoba.
**Query**
    /institutes/json?public=bool
    
### Get By City

**Parameters**
- city : the name of the city for which user wants the list of institutions. 

**Query**
    /institutes/json?city=string
  

## Resources
* [Designated learning institutions list](https://www.canada.ca/en/immigration-refugees-citizenship/services/study-canada/study-permit/prepare/designated-learning-institutions-list.html#wb-auto-24)
* [Higher education in Manitoba](https://en.wikipedia.org/wiki/Higher_education_in_Manitoba)

## Examples

**Endpoint**

    /institutes/json?name=University_of_Manitoba
    
**Return**

    {
      "name":"University of Manitoba",
      "date_of_establishment": 1877,
      "number_of_attendees": 30370
    }
**Endpoint**

    /institutes/json?public=false

**Return**

    [{
       "name": "Booth University College",
       "date_of_establishment": 1982,
       "number_of_attendees": 282
    },
    {
       "name": "Canadian Mennonite University",
       "date_of_establishment": 1999,
       "number_of_attendees": 1607
    },
    {
       "name": "Providence University College and Theological Seminary",
       "date_of_establishment": 1925,
       "number_of_attendees": 325
    },
    {
       "name": "Steinbach Bible College",
       "date_of_establishment": 1936,
       "number_of_attendees": 118
    }]
**Endpoint**

    /institutes/json?city=brandon

**Return**

    [{
       "name": "Brandon University",
       "date_of_establishment": 1890,
       "number_of attendees": 2980
    }]
