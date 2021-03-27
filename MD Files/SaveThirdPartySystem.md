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