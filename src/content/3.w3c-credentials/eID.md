# eID

```json
{
    "@context": ["https://www.w3.org/2018/credentials/v1"],
    "type": ["VerifiableCredential", "VerifiableAttestation", "eID"],
    "id": "THIS WILL BE REPLACED WITH DYNAMIC DATA FUNCTION",
    "credentialSubject": {
        "id": "THIS WILL BE REPLACED WITH DYNAMIC DATA FUNCTION",
        "firstName": "John",
        "lastName": "Doe",
        "dateOfBirth": "1980-01-01",
        "gender": "Male",
        "nationality": "US",
        "address": "123 Main St, Anytown, USA",
        "documentId": "G7F2A04F7O"
    },
    "issuer": {
        "id": "THIS WILL BE REPLACED WITH DYNAMIC DATA FUNCTION",
        "name": "Government of Anytown"
    },
    "issuanceDate": "THIS WILL BE REPLACED WITH DYNAMIC DATA FUNCTION",
    "expirationDate": "THIS WILL BE REPLACED WITH DYNAMIC DATA FUNCTION"
}
```

## Manifest

```json
{
    "claims": {
        "Document ID": "$.credentialSubject.documentId",
        "Name": "$.credentialSubject.firstName",
        "Last Name": "$.credentialSubject.lastName",
        "Date of Birth": "$.credentialSubject.dateOfBirth",
        "Gender": "$.credentialSubject.gender",
        "Nationality": "$.credentialSubject.nationality",
        "Address": "$.credentialSubject.address"
    }
}
```

## Mapping example

```json
{
    "id": "<uuid>",
    "issuer": {
        "id": "<issuerDid>"
    },
    "credentialSubject": {
        "id": "<subjectDid>"
    },
    "issuanceDate": "<timestamp>",
    "expirationDate": "<timestamp-in:365d>"
}
```