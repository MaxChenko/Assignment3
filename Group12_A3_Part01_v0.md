
## Description

Our API is for finding Institutes in Manitoba. We can filter the return objects by passing parameters for whether the institute is public or private, by its name, or by the city its in.

## Endpoints

**Get By Name** 
   
    /institutes/json?name=string
    
**Get By Public or Private**
  
    /institutes/json?public=bool
    
 **Get By City**
 
    /institutes/json?city=string
  

## Resources
[Designated learning institutions list](https://www.canada.ca/en/immigration-refugees-citizenship/services/study-canada/study-permit/prepare/designated-learning-institutions-list.html#wb-auto-24)

## Examples

**Endpoint **

    /institutes/json?name=University_of_Manitoba
    
**Return **

    {
      "name":"University of Manitoba",
      "date_of_establishment": 1877,
      "number_of_attendees": 30370
    }
