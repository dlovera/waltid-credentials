# DataConnectorServiceOffering

```json
{
  "@context": [
    "https://www.w3.org/2018/credentials/v1",
    "https://w3id.org/security/suites/jws-2020/v1",
    "https://w3id.org/gaia-x/development#service-offering"
  ],
  "type": [
    "VerifiableCredential",
    "GaiaXCredential",
    "DataConnectorServiceOffering"
  ],
  "id": "THIS WILL BE REPLACED WITH DYNAMIC DATA FUNCTION",
  "issuer": "THIS WILL BE REPLACED WITH DYNAMIC DATA FUNCTION",
  "issuanceDate": "THIS WILL BE REPLACED WITH DYNAMIC DATA FUNCTION",
  "expirationDate": "THIS WILL BE REPLACED WITH DYNAMIC DATA FUNCTION",
  "credentialSubject": {
    "id": "THIS WILL BE REPLACED WITH DYNAMIC DATA FUNCTION",
    "type": "DataConnectorServiceOffering",
    "name": "Data connector EU",
    "description": "The data connector service offering handles data exchange and processing within the data space.",
    "providedBy": {
      "id": "urn:uuid:7863e97d-95b0-4286-b9c5-ebd1eaee55d6",
      "type": "gx:LegalPerson",
      "gx:legalName": "Data Provider",
      "gx:legalRegistrationNumber": {
        "local": "810307207"
      },
      "gx:headquarterAddress": {
        "gx:countrySubdivisionCode": "FR-69"
      },
      "gx:legalAddress": {
        "gx:countrySubdivisionCode": "FR-69"
      }
    },
    "serviceOfferingTermsAndConditions": [
      {
        "id": "did:web:www.data4industry-x.com:terms-and-conditions",
        "type": "TermsAndConditions",
        "title": "Terms and Conditions",
        "url": "https://www.data4industry-x.com"
      }
    ],
    "servicePolicy": [
      {
        "id": "did:web:www.data4industry-x.com:access-usage-policy",
        "type": "AccessUsagePolicy",
        "title": "Access Usage Policy",
        "policyDocument": "https://www.data4industry-x.com"
      }
    ],
    "dataProtectionRegime": [
      {
        "id": "did:web:www.data4industry-x.com:privacy-policy",
        "type": "PersonalDataProtectionRegime",
        "title": "European General Data Protection Regulation",
        "jurisdiction": "EU"
      }
    ],
    "keyword": ["data connector", "d4ix", "EU", "infrastructure", "sovereign", "data space"],
    "provisionType": "on-demand",
    "endpoint": {
      "id": "did:web:www.data4industry-x.com:data-connector",
      "type": "Endpoint",
      "url": "https://www.data4industry-x.com",
      "protocol": "HTTPS"
    },
    "hostedOn": [
      "eu-west-1-datacenter",
      "eu-central-1-datacenter"
    ],
    "cryptographicSecurityStandards": [
      {
        "id": "did:web:datatracker.ietf.org:doc:html:rfc8446",
        "type": "CryptographicSecurityStandards",
        "name": "TLS1.3",
        "version": "1.3"
      }
    ],
    "requiredMeasures": [
      {
        "id": "did:web:www.iso.org:standard:27001",
        "type": "Measure",
        "name": "ISO 27001 Compliance",
        "description": "ISO 27001."
      }
    ],
    "providerContactInformation": {
      "id": "did:web:www.data4industry-x.com:contact",
      "type": "ContactInformation",
      "contactName": "D4IX DPO",
      "email": "dpo@data4industry-x.com"
    }
  }
}

```

## Manifest

```json
{
    "claims": {
        "Provided By": "$.credentialSubject['providedBy']"
    }
}
```

## Mapping example

```json
{
  "id": "<uuid>",
  "issuer": "<issuerDid>",
  "credentialSubject": {
    "id": "<subjectDid>"
  },
  "issuanceDate": "<timestamp>",
  "expirationDate": "<timestamp-in:365d>"
}
```