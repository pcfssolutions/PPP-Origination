# ThirdPartyDocUpload

Upload Files related to Third Party.

**URL** : ` LoanBoardingThirdParty/ThirdPartyDocUpload`

**Method** : `POST`

**Data Params**

| Parameter Name      | Data Type     | Sample Value     | Description     |
| :------------- | :----------: | -----------: | -----------: |
| FileName  | string   | “PPPLenderApplicationForm_SDTest1.pd”    |     |
| FileType   | string   | “application/pdf” |   |  |
| IsSigned   | boolean   |  |   |
| IsDocSign   | boolean   |  |   |
| LoanInfoId   | guid   | 7285B288-5824-45C3-A920-08D8E50457FA  |   |
| ClientId   | guid   | 04EE8181-91AE-4F94-B741-08D7E239BBC1  |   |
| docData   | byte   |   | Document as byte data    |

## Response

**Response** : Boolean

## Content

**True** : Successfully inserted
**False** : Insertion not successful

## Screenshot

![Screenshot](/ThirdPartyDocUpload.png?raw=true)