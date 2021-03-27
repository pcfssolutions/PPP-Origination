# SaveThirdPartySystem

Save Loan Boarding ThirdParty to the Origination Database. 

**URL** : `LoanBoardingThirdParty/SaveThirdPartySystem`

**Method** : `POST`

**Data Params**

```json
{
  "business": {
    "owners": [
      {
        "business_name": "Test",
        "owner_type": 1,
        "first_name": "Test",
        "last_name": "Test",
        "title": "Test",
        "business_type": 1,
        "ownership_percentage": 1,
        "tin": "Test",
        "tin_type": 0,
        "address_line_1": "Test",
        "address_line_2": "Test",
        "city": "Test",
        "state": "Ty",
        "zip_code": "Test",
        "zip_code_plus4": "Test",
        "position": "Test",
        "veteran_status": "Test",
        "gender": "Test",
        "ethnicity": "Test",
        "race": [
          "11",
          "22"
        ]
      }
    ],
    "naics_code": "Test",
    "business_type": 2,
    "dba_tradename": "Test",
    "legal_name": "Test",
    "first_name": "Test",
    "last_name": "Test",
    "address_line_1": "Test",
    "address_line_2": "Test",
    "city": "Test",
    "state": "Ty",
    "zip_code": "Test",
    "zip_code_plus4": "Test",
    "tin": "Test",
    "tin_type": 0,
    "phone_number": "Test",
    "primary_contact": "Test",
    "primary_contact_email": "Test@example.com",
    "is_franchise": true,
    "is_sba_listed_franchise": true,
    "franchise_code": "Test",
    "date_of_establishment": "2019-01-01"
  },
  "average_monthly_payroll": 1000,
  "loan_amount": 2500,
  "refinance_of_eidl_amount": 0,
  "refinance_of_eidl_loan_number": "Test",
  "number_of_employees": 1,
  "period_1_quarter": "1",
  "period_1_revenue": 0,
  "period_2_quarter": "1",
  "period_2_revenue": 0,
  "purpose_of_loan_payroll": true,
  "purpose_of_loan_mortgage": false,
  "purpose_of_loan_utilities": false,
  "purpose_of_loan_covered_operations_expenditures": false,
  "purpose_of_loan_covered_property_damage": false,
  "purpose_of_loan_covered_supplier_costs": false,
  "purpose_of_loan_covered_worker_protection_expenditure": false,
  "purpose_of_loan_other": false,
  "purpose_of_loan_other_info": "",
  "ineligible_general": true,
  "ineligible_bad_loan": true,
  "ineligible_criminal_charges": true,
  "ineligible_felony": true,
  "applicant_is_eligible": true,
  "applicant_meets_revenue_test_and_size_standard": true,
  "applicant_no_shuttered_venue_grant": true,
  "applicant_has_reduction_in_gross_receipts": true,
  "applicant_wont_receive_another_second_draw": true,
  "applicant_meets_size_standard": 1,
  "lender_contracted_third_party": true,
  "loan_request_is_necessary": true,
  "has_other_businesses": true,
  "received_eidl": false,
  "all_employees_residency": true,
  "second_draw_ppp_loan": false,
  "ppp_first_draw_sba_loan_number": 0,
  "ppp_first_draw_loan_amount": 0,
  "lender_application_number": "12345",
  "bank":10,
  "branch":1
}
```

## Response

**Response** : Boolean

## Content

**True** : Successfully inserted
**False** : Insertion not successful

## Screenshot

![Screenshot](/SaveThirdPartySystem.png?raw=true)
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
# ThirdPartySystemClarifications

API to refer from origination system

**Data Params**

| JSON                                                                  | Column Name                      | Table Name                    | Comments                                  |
|-----------------------------------------------------------------------|----------------------------------|-------------------------------|-------------------------------------------|
| {                                                                     |                                  |                               |                                           |
|       "business": {                                                   |                                  |                               |                                           |
|           "owners": [                                                 |                                  |                               |                                           |
|               {                                                       |                                  |                               |                                           |
|                   "business_name": "ABC Corp",                        | Business_Name                    | AP_PPPOrgination_BusinessInfo |                                           |
|                   "owner_type": 2,                                    | isTax                            | AP_Borrower/AP_Principal      |                                           |
|                   "first_name": "James",                              | FirstName                        | AP_Principal                  |                                           |
|                   "last_name": "Marshall",                            | LastName                         | AP_Principal                  |                                           |
|                   "title": "Director",                                | Title                            | AP_Borrower                   |                                           |
|                   "business_type": 2,                                 | BusinessType                     | AP_Principal                  |                                           |
|                   "ownership_percentage": 25,                         | N/A                              | N/A                           |                                           |
|                   "tin": "252751625",                                 | Tax_ID or SSN based onIsusetaxID | AP_Borrower                   |                                           |
|                   "tin_type": 0,                                      | IsusetaxID                       | AP_Borrower                   |                                           |
|                   "address_line_1": "123 Second St",                  | Address1                         | AP_Borrower                   |                                           |
|                   "address_line_2": "",                               | Address2                         | AP_Borrower                   |                                           |
|                   "city": "Manhattan",                                | City                             | AP_Borrower                   |                                           |
|                   "state": "NY",                                      | State                            | AP_Borrower                   |                                           |
|                   "zip_code": "10004",                                | ZipCode                          | AP_Borrower                   |                                           |
|                   "zip_code_plus4": "1234",                           | Zip_Code_Plus4                   | AP_Principal                  |                                           |
|                   "position": "Director",                             | Position                         | AP_Principal                  |                                           |
|                   "veteran_status": "1",                              | veteranStatus                    | AP_Principal                  |                                           |
|                   "gender": "M",                                      | Gender                           | AP_Principal                  |                                           |
|                   "ethnicity": "N",                                   | Ethnicity                        | AP_Principal                  |                                           |
|                   "race": [                                           | Race                             | AP_Principal                  |                                           |
|                       "1",                                            |                                  |                               |                                           |
|                       "2"                                             |                                  |                               |                                           |
|                   ]                                                   |                                  |                               |                                           |
|               }                                                       |                                  |                               |                                           |
|         ],                                                            |                                  |                               |                                           |
|           "naics_code": "722513",                                     | NAICS_CODE                       | Borrower                      |                                           |
|           "business_type": 2,                                         | BusinessType                     | AP_Principal                  |                                           |
|           "dba_tradename": "ABC Corp",                                | TRADENAME_DBA                    | Borrower                      |                                           |
|           "legal_name": "ABC Corp",                                   | BorrowerName                     | Ap_Borrower                   |                                           |
|           "first_name": "James",                                      | FirstName                        | AP_Principal                  |                                           |
|           "last_name": "Marshall",                                    | LastName                         | AP_Principal                  |                                           |
|           "address_line_1": "5050 Ritter Rd",                         | Address1                         | AP_Borrower                   |                                           |
|           "address_line_2": "Suite B",                                | Address2                         | AP_Borrower                   |                                           |
|           "city": "Mechanicsburg",                                    | City                             | AP_Borrower                   |                                           |
|           "state": "PA",                                              | State                            | AP_Borrower                   |                                           |
|           "zip_code": "17055",                                        | ZipCode                          | AP_Borrower                   |                                           |
|           "zip_code_plus4": "1234",                                   | Zip_Code_Plus4                   | AP_Principal                  |                                           |
|           "tin": "835881068",                                         | Tax_ID or SSN based onIsusetaxID | AP_Borrower                   |                                           |
|           "tin_type": 0,                                              | IsusetaxID                       | AP_Borrower                   |                                           |
|           "phone_number": "5482562187",                               | Phone                            | AP_Borrower                   |                                           |
|           "primary_contact": "James",                                 | IsPrimaryContact                 | AP_Principal                  |                                           |
|           "primary_contact_email": "user@example.com",                | Email                            | AP_Principal                  |                                           |
|           "is_franchise": true,                                       | Isfranchise                      | AP_LoanInfo                   |                                           |
|           "is_sba_listed_franchise": true,                            | PPPSBAFranchiseFlag              | Ap_LoanBorrower               |                                           |
|           "franchise_code": "S2956",                                  | FranchiseCode                    | AP_LoanInfo                   |                                           |
|           "date_of_establishment": "2019-01-01"                       | EstablishmentDate                | AP_PPPOrgination_BusinessInfo |                                           |
|     },                                                                |                                  |                               |                                           |
|       "average_monthly_payroll": 1000,                                | PPPPayrollMnthlyAvgAmt           | AP_LoanInfo                   |                                           |
|       "loan_amount": 2500,                                            | LoanAmount                       | AP_LoanInfo                   |                                           |
|       "refinance_of_eidl_amount": 0,                                  | PPPRefiEIDLAmt                   | AP_LoanInfo                   |                                           |
|       "refinance_of_eidl_loan_number": "string",                      | EIDL_LoanNumber                  | AP_LoanInfo                   |                                           |
|       "number_of_employees": 1,                                       | NoOfEmployees                    | AP_LoanInfo                   |                                           |
|       "period_1_quarter": "1",                                        | Period_1_Quarter                 | AP_LoanInfo                   |                                           |
|       "period_1_revenue": 0,                                          | Period_1_Revenue                 | AP_LoanInfo                   |                                           |
|       "period_2_quarter": "1",                                        | Period_2_Quarter                 | AP_LoanInfo                   |                                           |
|       "period_2_revenue": 0,                                          | Period_2_Revenue                 | AP_LoanInfo                   |                                           |
|       "purpose_of_loan_payroll": true,                                | Purpose_Payroll                  | AP_LoanInfo                   |                                           |
|       "purpose_of_loan_mortgage": false,                              | Purpose_Lease                    | AP_LoanInfo                   |                                           |
|       "purpose_of_loan_utilities": false,                             | Purpose_Utilities                | AP_LoanInfo                   |                                           |
|       "purpose_of_loan_covered_operations_expenditures": false,       | Purpose_Operations               | AP_LoanInfo                   |                                           |
|       "purpose_of_loan_covered_property_damage": false,               | Purpose_Property                 | AP_LoanInfo                   |                                           |
|       "purpose_of_loan_covered_supplier_costs": false,                | Purpose_Supplier                 | AP_LoanInfo                   |                                           |
|       "purpose_of_loan_covered_worker_protection_expenditure": false, | Purpose_Worker                   | AP_LoanInfo                   |                                           |
|       "purpose_of_loan_other": false,                                 | Purpose_Other                    | AP_LoanInfo                   |                                           |
|       "purpose_of_loan_other_info": "",                               | OtherPurpose                     | AP_LoanInfo                   |                                           |
|       "ineligible_general": true,                                     | Q1                               | ap_ppporiginationquest        |                                           |
|       "ineligible_bad_loan": true,                                    | Q2                               | ap_ppporiginationquest        |                                           |
|       "ineligible_criminal_charges": true,                            | Q5                               | ap_ppporiginationquest        |                                           |
|       "ineligible_felony": true,                                      | Q6                               | ap_ppporiginationquest        |                                           |
|       "applicant_is_eligible": true,                                  | LQ1                              | ap_ppporiginationquest        |                                           |
|       "applicant_meets_revenue_test_and_size_standard": true,         | LQ2                              | ap_ppporiginationquest        |                                           |
|       "applicant_no_shuttered_venue_grant": true,                     | LQ3                              | ap_ppporiginationquest        |                                           |
|       "applicant_has_reduction_in_gross_receipts": true,              | N/A                              | N/A                           |                                           |
|       "applicant_wont_receive_another_second_draw": true,             | Cert4                            | ap_ppporiginationquest        |                                           |
|       "applicant_meets_size_standard": 1,                             | ap_ppporiginationquest           | LQ2                           |                                           |
|       "lender_contracted_third_party": true,                          | N/A                              | N/A                           |                                           |
|       "loan_request_is_necessary": true,                              | N/A                              | N/A                           |                                           |
|       "has_other_businesses": true,                                   | LQ10                             | ap_ppporiginationquest        |                                           |
|       "received_eidl": false,                                         | eidl                             | AP_Loaninfo                   |  Eidl is float in AP_LoanInfo             |
|       "all_employees_residency": true,                                | LQ11                             | ap_ppporiginationquest        |                                           |
|       "second_draw_ppp_loan": false,                                  | seconddraw                       | AP_LoanInfo                   |                                           |
|       "ppp_first_draw_sba_loan_number": 0,                            | AP_LoanInfo                      | FirstDraw_SBALoanNumber       |                                           |
|       "ppp_first_draw_loan_amount": 0,                                | AP_LoanInfo                      | FirstDraw_LoanAmount          |                                           |
|       "branch":1                                                      | AP_LoanInfo                      | Branch                        | Branch Column is mandatory in AP_LoanInfo |
|         "bank":10                                                     | AP_LoanInfo                      | Bank                          | Bank Column is mandatory in AP_LoanInfo   |
|       "lender_application_number": "12345"                            | LoanNumber                       | AP_LoanInfo                   |                                           |
| }                                                                     |                                  |                               |                                           |
