Thank you for using the Philly Tenant Assistance Screener.
[BR]
Based on the answers you provided to our questions, we think you may be able to seek rental assistance from the following organizations. Please note that you will still need to visit and apply separately for assistance from the following organizations.

% for source in sources:
- **${ source['name'] }:** To apply for assistance, you can ${ source['availability'] }
% endfor

% if housing_type == "Public":
Please consider talking with your manager about a rent reduction.
% endif

% for source in sources:
[PAGEBREAK]

[BOLDCENTER] Required Documentation for ${ source['name'] }

% if is_dhs_involved and source['name'] == 'DHS Prevention Assistance Fund':
[FLUSHLEFT] Before applying for the DHS Prevention Assistance fund, please talk with your social worker
% endif

[FLUSHLEFT] What should I bring when applying for the resources above?

- Photo ID for all household members age 18 and over
- Social Security cards and Birth Certificates for all household members
% if monthly_income > 0:
- Proof of Income dated within last 30 days
    - Pay stubs (for last thirty days)
    - Employment letter (hours, pay date(s), wages/salary)
    - Award Letter from Social Security office
    - Any other documentation of income
% endif
- Proof of Assets, such as bank statements or inheritance award letters
- Lease Agreement
% if assistance_category == "Rental Arrears":
- Eviction Notice and/or Court Documents (if seeking assistance for back rent)
% endif
% if previous_ohs_assistance == False and source['name'] == 'Office of Homeless Services':
- Documentation from L&I – link to phila.gov/li website where they can look up violations
- Medical and/or mental health documentation
- Unit must pass OHS inspection for private rentals
- If subsidized housing, will need HAP contract, lease, or some other proof
- Statement of current balance dated within last 10 days by landlord or property manager
- Verification of assistance from other agencies if applicable
- For security deposit: letter of approval, inspection request, or other proof of move-in
- Landlord’s contact information
- All clients are expected to pay a portion of the move in cost or rental balance
- Documented income must be sufficient to maintain rent and living expenses
- Funds will be issued based on complete application and availability of funds
- Other requirements may be imposed by intake worker
- Final determination made by OHS administrator – not all applications accepted/funded
% endif
% if is_veteran:
- Completed DD-214 Form
- State Identification or VA medical card with picture (Identification is required for all individuals in the home)
- Housing Crisis Documentation. For example, a 10-day Eviction Notice or Court Ordered Eviction Notice
% endif
[BR]

[FLUSHLEFT] What should I get from my landlord?

- Rental License, also called a Housing Inspection License. You can lookup your current rental license on the City of Philadelphia's website.
- W-9 signed by landlord. You can find a blank copy of the W9 for your landlord to sign here.
    % if assistance_category == "Rental Arrears":
- Letter with current balance owed signed and dated by landlord (if seeking assistance for back rent)
% endif

% endfor
