

-------------------------

**Clients**

-  A client has connected to a server and fetched a patient's medications using `GET /MedicationOrder?patient=[id]`.


**Servers**

- A server is capable of returning a patient's medications `GET /MedicationOrder?patient=[id]`.


- A server has ensured that every API request includes a valid Authorization token, supplied via:Authorization: Bearer {server-specific-token-here}
- A server has rejected any unauthorized requests by returning an HTTP 401 Unauthorized response code.

-----------

`GET /MedicationOrder?patient={id}[edit]`

*Support:* Mandatory to support search by patient.

*Implementation Notes:*  Search for all MedicationOrder resources for a patient. Fetches a bundle of all MedicationOrder resources for the specified patient  [(how to search by reference)].



*Response Class:*

-   (Status 200): successful operation
-   (Status 400): invalid parameter
-   (Status 401/4xx): unauthorized request
-   (Status 403): insufficient scope

**Example:**

GET https://fhir-open-api-dstu2.smarthealthit.org/MedicationOrder?patient=1137192

-----------

  [(how to search by reference)]: http://hl7.org/fhir/DSTU2/search.html#reference
  [(how to search by token)]: http://hl7.org/fhir/DSTU2/search.html#token
  [Composite Search Parameters]: http://hl7-fhir.github.io/search.html#combining
  [(how to search by date)]: http://hl7.org/fhir/DSTU2/search.html#date