# Comparing XML (application/xml) and JSON (application/json)

As the internet has continued to grow and be refined, we find that some technologies have been replaced by newer ones and this trend will likely continue. In the early days of the web, building APIs was a little different. Even if an API was following a RESTful convention, the data exchange format was likely different from what we see today. Particularly, the once common data exchange format, XML, has been replaced with JSON except in cases where an existing architecture simply demands XML (Eg: SOAP api). Below, we will outline some of the differences between these 2 formats and why JSON was an obvious choice moving forward.

## Formatting Payload as XML:
Here we will see the ways that developers can format a payload as XML. Note that BOTH of the methods below are more tedious than simply creating an object and calling a method on that object. The string concatenation method is VERY tedious and error prone, and while a library can be used for this purpose, it's use is very similar to using the FormData class in Javascript, which while convenient for specific tasks, requires more code to implement than JSON does.

### String Concatenating Method:
<img width="543" alt="xml_payload_string_cat" src="https://github.com/bkieselEducational/Computer-Science-Episode-Two-Comparing-XML-and-JSON/assets/131717897/4b8487da-266e-440c-b850-e52d1a01269e">

### Library Method:
<img width="544" alt="xml_payload_lib" src="https://github.com/bkieselEducational/Computer-Science-Episode-Two-Comparing-XML-and-JSON/assets/131717897/f78f320c-d5d6-42e2-91d2-52279d8b078e">


## Request / Response Payload comparison between XML and JSON:
In consideration of the 2 payloads below, we can immediately observe 2 things. 1) The XML payload is a little more difficult to read than the JSON payload and  2) The XML payload appears to be comprised of a lot more characters, meaning a lot more bytes, and a lot more data... This topic will be broached in the following section.

XML Response:</br>
<img width="545" alt="xml_payload" src="https://github.com/bkieselEducational/Computer-Science-Episode-Two-Comparing-XML-and-JSON/assets/131717897/e918b9b5-0f92-459b-8562-3f06db44ff19">

JSON Response:</br>
<img width="546" alt="json_response" src="https://github.com/bkieselEducational/Computer-Science-Episode-Two-Comparing-XML-and-JSON/assets/131717897/9ad50025-3a74-462c-89cb-a0f1c031fed6">

## Practical and Technical Comparison of XML and JSON formats for Web Development:

### Practical Considerations:
By simply looking at the 2 formats, it is obvious that JSON is not only MORE human-readable but it is also almost identical to the way that write code in an Object Oriented Way. XML does not resemble our application code at all (aside from looking similar to HTML) and will always require extra parsing steps to change it into an object representation of the data.

### Technical / Performance Comparison:

1. Parsing Performance: JSON is generally faster to parse than XML!!
2. Serialization Performance: Serializing an object into a JSON string is also faster than producing an XML Document.
3. Payload Size: JSON format also results in a smaller payload size (sometimes significant) than XML, further making data transmission quicker and less costly than XML.
4. Server Load: The strain on the server is actually noticable when comparing the memory footprints for serialization / deserialization processes and also in the simple fact that with JSON, there is less data to even process in the first place!
5. Human Aspect: A JSON serialized object is VERY close to a python dictionary or javascript object when we recieve it!! As an engineer, we want to work with more straightforward data types.
